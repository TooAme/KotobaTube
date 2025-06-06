# KotobaTube开发日志

## 2025/5/31

**从jhipster搭建的框架开始**

**jhipster选项：**

```cmd
√ What is the base name of your application? kotobaTube
√ Which *type* of application would you like to create? Monolithic application (recommended for simple projects)
√ What is your default Java package name? com.chenhy
√ Would you like to use Maven or Gradle for building the backend? Maven
√ Do you want to make it reactive with Spring WebFlux? No
√ Which *type* of authentication would you like to use? JWT authentication (stateless, with a token)
√ Besides JUnit, which testing frameworks would you like to use?
√ Which *type* of database would you like to use? SQL (H2, PostgreSQL, MySQL, MariaDB, Oracle, MSSQL)
√ Which *production* database would you like to use? MySQL
√ Which *development* database would you like to use? MySQL (requires Docker or manually configured database)
√ Which cache do you want to use? (Spring cache abstraction) Redis (distributed cache)
√ Do you want to use Hibernate 2nd level cache? Yes
√ Which other technologies would you like to use? WebSockets using Spring Websocket, API first development using
OpenAPI-generator
√ Which *framework* would you like to use for the client? Vue
√ Besides Jest/Vitest, which testing frameworks would you like to use?
√ Do you want to generate the admin UI? Yes
√ Would you like to use a Bootswatch theme (https://bootswatch.com/)? Darkly
√ Choose a Bootswatch variant navbar theme (https://bootswatch.com/)? Dark
√ Would you like to enable internationalization support? Yes
√ Please choose the native language of the application Chinese (Simplified)
√ Please choose additional languages to install Japanese
```

**因为设置了认证，所以前端需要访问从日志里看到的公网ip：http://192.168.xxx.xxx:9000/**

**也要切换vite.config.mts中第64行的代理ip。**

**启动前开启redis：**

```cmd
cd C:\Program Files\Redis
redis-server.exe redis.windows.conf
```

**报错没有docker就重启ide。**

**启动ngrok：**

```cmd
ngrok config add-authtoken 2y93YqqyzJ2zQi6YhjtlAI9XmsF_7Fw74J7yqdYuNx248Dmcc
ngrok http http://192.168.xxx.xxx:9000
```

**随后修改vite.config,mts的第56行为ngrok提供的公网链接。**
