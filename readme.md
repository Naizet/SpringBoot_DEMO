#CommandLineRunner

springboot有两个接口来实现---CommandLineRunner、ApplicationRunner。启动应用时的特殊处理，他们的执行时机为容器启动完成的时候(SpringApplication的run()方法运行完成之前被执行)

两者的区别在于：
ApplicationRunner中run方法的参数为ApplicationArguments，而CommandLineRunner接口中run方法的参数为String数组。
Spring Boot应用程序在启动后，会遍历CommandLineRunner或ApplicationRunner接口的实例并运行它们的run方法。
也可以利用@Order注解（或者实现Order接口）来规定所有CommandLineRunner或ApplicationRunner实例的运行顺序。

#springboot启动图案
可以修改springbbot的默认图案
banner+后缀

#Thymeleaf
--- 依赖添加
 <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-thymeleaf</artifactId>
        </dependency>

--- 配位文件添加热加载属性
spring.thymeleaf.cache=false

---  默认配置文件
默认从 src/main/resources/templates下加载
