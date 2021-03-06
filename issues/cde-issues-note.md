#问题跟踪表

| 序号 | 问题发现时间 | 功能模块       | 负责人  | 问题描述                        | 处理人  | 处理情况    | 处理时间   | 处理状态 |
|-----|------------|---------------|--------|--------------------------------|--------|-----------|------------|--------|
| 1   | 2016.11.22 | 整体           | 全员   | 代码缩进问题，java 4个空格，js 2个 | 
| 2   | 2016.11.22 | 后端pom.xml文件 | 廖芳才  | 使用parent以后指定的依赖，不用写版本信息| 廖芳才 | 根据要求处理 |       | 已处理
| 3   | 2016.11.22 | 后端pom.xml文件 | 后端  | 1. import 的内容放在 dependency management 的最前面 2.另外，不是所有定义的 properties 都有用到，没用到的 properties 不要定义 |廖芳才|||已处理
| 4   | 2016.11.23 | 后端代码        | 后端   | 配置文件中的自定义key需要加上命名空间，使用驼峰命名规则 |廖芳才|||已处理
| 5   | 2016.11.23 | 后端代码        | 后端   | 除了命名规则按照相关规则命名外，名称还需要能表达具体意义||||处理完
| 6   | 2016.11.23 | 后端服务配置文件 | 后端   | 在不清楚相关配置参数的使用的时候需要进行查询 |廖芳才|||已处理
| 7   | 2016.11.23 | 后端代码        | 后端   | 对于@Bean注入，只能在两个相同类型的Bean同时被注入时使用name属性|廖芳才|||已处理
| 8   | 2016.11.24 | 后端代码        | 后端   | exception 不要直接 printStackTrace 要用 log 组件 | 廖芳才|||已处理
| 9   | 2016.11.24 | 后端代码        | 后端   | 注意下包引用的顺序，java > javax > apache > spring > 我们自己的 |廖芳才|||已处理
| 10  | 2016.11.24 | 后端           | 后端   |  现在需要的就是把 config service 引进来，来管理所有系统的配置 ||||延后处理，需要启动单独的配置服务
| 11  | 2016.11.25 | 整体           | 全员   | 在提交代码的时候不要把不想管的代码同时提交，便于以后的管理 |廖芳才|||已处理
| 12  | 2016.11.25 | cde-account-service| 李昌林| pom.xml文件中的项目名为大写的CDE，注意依赖关系的嵌套，pring-boot-starter-data-monogodb 已经包含了 spring-data-commons 这个库了，不需要再额外引用 | 李昌林 | 根据问题描述进行处理 | 2016.11.25 | 已处理 |
| 13  | 2016.11.25 | 后端cde-account-service配置文件     | 李昌林  | 如果是spring自带的配置项，不需要再配置类中引入 | 李昌林 | 修改为自定义属性 | 2016.11.25 | 已处理 |
| 14  | 2016.11.25 |  后端cde-account-service配置文件  | 李昌林 | 日志不写文件，直接输出到 console 就行了 | 李昌林 | 已经加了日志打印   |     |  未处理  |
| 15  | 2016.11.25 |  后端配置文件  | 后端 | 配置数据库的时候，都要考虑一下数据库集群部署时的情况 ||||问题跟进中
| 16  | 2016.11.25 | 后端代码 | 后端 | 对于程序中的异常的处理。第一，一般不会出现运行时异常的异常定义情况；第二，异常应该使用日志记录下来。这里的日志指的是日志服务。||||异常已经按照要求处理，日志服务没启动，目前直接终端输出
| 17  | 2016.11.25 | 后端代码 | 后端 | 成员变量不需要初始化。除了一些特殊的情况，比如说永远不返回null的list、map等。其次就是为了区分成员变量，在使用的时候应该加上this关键字。 |廖芳才|||已处理
| 18  | 2016.11.25 | 后端代码 | 后端 | 代码中不应该出现用来测试的方法，其中可以通过两种途径来进行解决：第一，使用日志记录；第二，写测试用例。 |廖芳才|||已处理
| 19  | 2016.11.25 | 后端代码 | 后端 | 对于一些特殊的不可变的类型，应该定义为没有set方法。创建对象可以通过构造函数和Builder的方式实现，其中构造函数的方式不适用于属性较多的方式。 | 廖芳才|||已处理
| 20  | 2016.11.25 | 后端代码 | 后端 | 在程序中对于map的使用，应该当成一种数据类型来使用，一般就在本类中或是本方法中使用，不暴露给外界。 | 廖芳才|||已处理
| 21  | 2016.11.25 | 后端代码 | 后端 | 在注入Bean的情况下，Spring一般默认是单例的情况，对于可变的对象，应该采用工厂的方式来创建对象。||||已处理
| 22  | 2016.11.25 | 后端代码 | 后端 | 所有的URL不应该出现大写形式（除了是变量的情况），使用“-”符号进行分割。|廖芳才|||已处理
| 23  | 2016.11.25 | 后端代码 | 后端 | 对前端数据应该采用完全不信任的情况，这是作为一个后台服务必须要遵守的规则，为了自身安全做保障。| 李昌林| 已按要求处理 | | 已处理 |
| 24  | 2016.11.25 | 后端代码 | 后端 | 对cde-account-service系统的设计进行讲评。mobile和email不应该存到数据库表中，应该属于account的属性作为存储。| 李昌林 | 已使用内嵌文档的形式存入用户信息中| | 已处理|
| 25  | 2016.11.25 | 后端代码 | 后端 | 对于错误码的设计，为了以后更方便扩展，错误码应该分为服务码和具体的错误码，进行组合。| 李昌林 | 按要求处理| | 已处理|
| 26  | 2016.11.25 | 后端代码 | 后端 | 接口与model应该独立出来（还没有理解其中的意思）。 ||||暂未处理
| 27  | 2016.11.25 | 后端代码 | 后端 | application.yml,mongdb:url 支持集群写法。 ||||暂未处理
| 28  | 2016.11.25 | 后端代码 | 后端 | 开发工具尽量使用IntelliJ。并且需要加入代码检查。||||已处理
| 29  | 2016.11.25 | 后端代码 | 后端 | cde-oauth2-client，RequestConfiguration中两个@Bean问题 |廖芳才|||已处理
| 30  | 2016.11.25 | 后端代码 | 后端 | 对于Java8 新语法，应该多进行关注，节省代码量。||||已处理
| 31  | 2016.11.25 | 后端代码 | 后端 | controller endpoint 名称应该统一。||||已处理
| 32  | 2016.11.25 | 后端代码 | 后端 | 成员变量message问题，由于该变量在并发的时候后造成严重的影响，一定要避免。|李昌林 | | |已处理| 
| 33  | 2016.11.25 | 后端代码 | 后端 | 返回值全部Object，Service层要处理异常，只有当正常的时候返回结果，其他的时候必须对异常进行处理。|李昌林|||已处理|
| 34  | 2016.11.25 | 后端代码 | 后端 | 代码缩进问题，不能使用tab建。||||问题跟进中|
| 35  | 2016.11.25 | 后端代码 | 后端 | 没有resultmodel，domain拼写错误 |李昌林|按要求修改| |已处理|
| 36  | 2016.11.25 | 后端代码 | 后端 | 方法名称不应该与业务存在联系，如checkEmailbyEmailName方法名称就是不规范的。 |李昌林| ||已处理|
