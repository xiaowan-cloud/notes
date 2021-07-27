##Lombok

>实体常用注解
> + @Data 包含getter、setter、toSting || 没有构造器哦
> - @Setter @Getter 就是各个属性的get、set
> * @SneakyThrows 抛异常的,底层是将异常假装成RunTimeException抛出(好用的一比)
``` java
  /**
     * 连接demo数据库
     */
    @SneakyThrows
    public static Statement getConn(){
        Class.forName("com.mysql.cj.jdbc.Driver");
        conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/demo?serverTimezone=GMT%2B8", "root", "123123");
        statement = conn.createStatement();
        return statement;
    }
···