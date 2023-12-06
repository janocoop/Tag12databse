# 4-Spring/4-Spring-Data

## Unklarheiten beseitigen

Welche Fragen sind aus dem Vortrag oder dem bisherigen Unterricht offen geblieben?
Bitte klärt diese Fragen als Gruppe.
Nutzt zur Klärung alle verfügbaren Quellen.

## Recherche

Findet gemeinsam Antworten auf die folgenden Fragen und tragt sie hier ein.
Nutzt zur Recherche verschiedene Quellen, wie Google, offizielle Dokumentationen und Fachliteratur.

* Stellt Euch vor, Ihr habt einen Record, in dem der Primärschlüssel nicht in der Eigenschaft "id" sondern in der Eigenschaft "isbn" gespeichert wird. Ihr wollt aber "isbn" in der MongoDB als Primärschlüssel ("_id") nutzen. Recherchiert wie man ein anderes Feld statt "ID" als den Primärschlüssel verwenden kann.
  `inputfield`
* Welche grundlegenden Operationen werden durch die Standardmethoden im Spring Data Repository-Interface bereitgestellt?
  Nenne 3 bis 5 Methoden.
  `inputfield`
* Was ist BSON und wie unterscheidet es sich von JSON?
  `inputfield`
* In Spring Data-Repositories nutzen wir die Namenskonventionen um Methoden zu generieren zu lassen. Nehmen wir an, wir haben zum Beispiel eine "Car"-Entity, die ein Attribut "color" hat. Wie muss die Methodensignatur (Rückgabetyp, Name, Parameter) im Repo-Interface aussehen, damit Spring Data eine Methode generiert, die alle Cars von einer bestimmten Farbe zurückgibt?
  `inputfield`

* Das hier ist das Logfile Eurer Spring-Boot-Anwendung beim Starten der Anwendung. Was könnte das Problem sein?

```
  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::                (v3.1.3)

2023-09-15T17:33:18.159+02:00  INFO 36410 --- [           main] c.e.springdata.SpringDataApplication     : Starting SpringDataApplication using Java 19 with PID 36410 (/Users/danielschwarz/IdeaProjects/spring-data/target/classes started by danielschwarz in /Users/danielschwarz/IdeaProjects/spring-data)
2023-09-15T17:33:18.162+02:00  INFO 36410 --- [           main] c.e.springdata.SpringDataApplication     : No active profile set, falling back to 1 default profile: "default"
2023-09-15T17:33:18.414+02:00  INFO 36410 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data MongoDB repositories in DEFAULT mode.
2023-09-15T17:33:18.434+02:00  INFO 36410 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 18 ms. Found 1 MongoDB repository interfaces.
2023-09-15T17:33:18.638+02:00  INFO 36410 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8080 (http)
2023-09-15T17:33:18.644+02:00  INFO 36410 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2023-09-15T17:33:18.644+02:00  INFO 36410 --- [           main] o.apache.catalina.core.StandardEngine    : Starting Servlet engine: [Apache Tomcat/10.1.12]
2023-09-15T17:33:18.685+02:00  INFO 36410 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2023-09-15T17:33:18.686+02:00  INFO 36410 --- [           main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 493 ms
2023-09-15T17:33:18.740+02:00  WARN 36410 --- [           main] ConfigServletWebServerApplicationContext : Exception encountered during context initialization - cancelling refresh attempt: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'shopController' defined in file [/Users/danielschwarz/IdeaProjects/spring-data/target/classes/com/example/springdata/shop/ShopController.class]: Unsatisfied dependency expressed through constructor parameter 0: Error creating bean with name 'orderRepo' defined in com.example.springdata.shop.order.OrderRepo defined in @EnableMongoRepositories declared on MongoRepositoriesRegistrar.EnableMongoRepositoriesConfiguration: Cannot resolve reference to bean 'mongoTemplate' while setting bean property 'mongoOperations'
2023-09-15T17:33:18.741+02:00  INFO 36410 --- [           main] o.apache.catalina.core.StandardService   : Stopping service [Tomcat]
2023-09-15T17:33:18.748+02:00  INFO 36410 --- [           main] .s.b.a.l.ConditionEvaluationReportLogger : 

Error starting ApplicationContext. To display the condition evaluation report re-run your application with 'debug' enabled.
2023-09-15T17:33:18.756+02:00 ERROR 36410 --- [           main] o.s.boot.SpringApplication               : Application run failed

org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'shopController' defined in file [/Users/danielschwarz/IdeaProjects/spring-data/target/classes/com/example/springdata/shop/ShopController.class]: Unsatisfied dependency expressed through constructor parameter 0: Error creating bean with name 'orderRepo' defined in com.example.springdata.shop.order.OrderRepo defined in @EnableMongoRepositories declared on MongoRepositoriesRegistrar.EnableMongoRepositoriesConfiguration: Cannot resolve reference to bean 'mongoTemplate' while setting bean property 'mongoOperations'
	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:800) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.autowireConstructor(ConstructorResolver.java:245) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.autowireConstructor(AbstractAutowireCapableBeanFactory.java:1352) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1189) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:560) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:520) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:326) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:324) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.preInstantiateSingletons(DefaultListableBeanFactory.java:973) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.context.support.AbstractApplicationContext.finishBeanFactoryInitialization(AbstractApplicationContext.java:942) ~[spring-context-6.0.11.jar:6.0.11]
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:608) ~[spring-context-6.0.11.jar:6.0.11]
	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:146) ~[spring-boot-3.1.3.jar:3.1.3]
	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:734) ~[spring-boot-3.1.3.jar:3.1.3]
	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:436) ~[spring-boot-3.1.3.jar:3.1.3]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:312) ~[spring-boot-3.1.3.jar:3.1.3]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1306) ~[spring-boot-3.1.3.jar:3.1.3]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1295) ~[spring-boot-3.1.3.jar:3.1.3]
	at com.example.springdata.SpringDataApplication.main(SpringDataApplication.java:10) ~[classes/:na]
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'orderRepo' defined in com.example.springdata.shop.order.OrderRepo defined in @EnableMongoRepositories declared on MongoRepositoriesRegistrar.EnableMongoRepositoriesConfiguration: Cannot resolve reference to bean 'mongoTemplate' while setting bean property 'mongoOperations'
	at org.springframework.beans.factory.support.BeanDefinitionValueResolver.resolveReference(BeanDefinitionValueResolver.java:377) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.BeanDefinitionValueResolver.resolveValueIfNecessary(BeanDefinitionValueResolver.java:135) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.applyPropertyValues(AbstractAutowireCapableBeanFactory.java:1682) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.populateBean(AbstractAutowireCapableBeanFactory.java:1431) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:597) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:520) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:326) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:324) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1417) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1337) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:888) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:791) ~[spring-beans-6.0.11.jar:6.0.11]
	... 19 common frames omitted
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'mongoTemplate' defined in class path resource [org/springframework/boot/autoconfigure/data/mongo/MongoDatabaseFactoryDependentConfiguration.class]: Unsatisfied dependency expressed through method 'mongoTemplate' parameter 0: Error creating bean with name 'mongoDatabaseFactory' defined in class path resource [org/springframework/boot/autoconfigure/data/mongo/MongoDatabaseFactoryConfiguration.class]: Unsatisfied dependency expressed through method 'mongoDatabaseFactory' parameter 0: Error creating bean with name 'mongo' defined in class path resource [org/springframework/boot/autoconfigure/mongo/MongoAutoConfiguration.class]: Failed to instantiate [com.mongodb.client.MongoClient]: Factory method 'mongo' threw exception with message: Error creating bean with name 'standardMongoSettingsCustomizer' defined in class path resource [org/springframework/boot/autoconfigure/mongo/MongoAutoConfiguration$MongoClientSettingsConfiguration.class]: Failed to instantiate [org.springframework.boot.autoconfigure.mongo.StandardMongoClientSettingsBuilderCustomizer]: Factory method 'standardMongoSettingsCustomizer' threw exception with message: The connection string is invalid. Connection strings must start with either 'mongodb://' or 'mongodb+srv://
	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:800) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:550) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1332) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1162) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:560) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:520) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:326) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:324) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.BeanDefinitionValueResolver.resolveReference(BeanDefinitionValueResolver.java:365) ~[spring-beans-6.0.11.jar:6.0.11]
	... 33 common frames omitted
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'mongoDatabaseFactory' defined in class path resource [org/springframework/boot/autoconfigure/data/mongo/MongoDatabaseFactoryConfiguration.class]: Unsatisfied dependency expressed through method 'mongoDatabaseFactory' parameter 0: Error creating bean with name 'mongo' defined in class path resource [org/springframework/boot/autoconfigure/mongo/MongoAutoConfiguration.class]: Failed to instantiate [com.mongodb.client.MongoClient]: Factory method 'mongo' threw exception with message: Error creating bean with name 'standardMongoSettingsCustomizer' defined in class path resource [org/springframework/boot/autoconfigure/mongo/MongoAutoConfiguration$MongoClientSettingsConfiguration.class]: Failed to instantiate [org.springframework.boot.autoconfigure.mongo.StandardMongoClientSettingsBuilderCustomizer]: Factory method 'standardMongoSettingsCustomizer' threw exception with message: The connection string is invalid. Connection strings must start with either 'mongodb://' or 'mongodb+srv://
	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:800) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:550) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1332) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1162) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:560) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:520) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:326) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:324) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1417) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1337) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:888) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:791) ~[spring-beans-6.0.11.jar:6.0.11]
	... 43 common frames omitted
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'mongo' defined in class path resource [org/springframework/boot/autoconfigure/mongo/MongoAutoConfiguration.class]: Failed to instantiate [com.mongodb.client.MongoClient]: Factory method 'mongo' threw exception with message: Error creating bean with name 'standardMongoSettingsCustomizer' defined in class path resource [org/springframework/boot/autoconfigure/mongo/MongoAutoConfiguration$MongoClientSettingsConfiguration.class]: Failed to instantiate [org.springframework.boot.autoconfigure.mongo.StandardMongoClientSettingsBuilderCustomizer]: Factory method 'standardMongoSettingsCustomizer' threw exception with message: The connection string is invalid. Connection strings must start with either 'mongodb://' or 'mongodb+srv://
	at org.springframework.beans.factory.support.ConstructorResolver.instantiate(ConstructorResolver.java:659) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:647) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1332) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1162) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:560) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:520) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:326) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:324) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1417) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1337) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:888) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:791) ~[spring-beans-6.0.11.jar:6.0.11]
	... 57 common frames omitted
Caused by: org.springframework.beans.BeanInstantiationException: Failed to instantiate [com.mongodb.client.MongoClient]: Factory method 'mongo' threw exception with message: Error creating bean with name 'standardMongoSettingsCustomizer' defined in class path resource [org/springframework/boot/autoconfigure/mongo/MongoAutoConfiguration$MongoClientSettingsConfiguration.class]: Failed to instantiate [org.springframework.boot.autoconfigure.mongo.StandardMongoClientSettingsBuilderCustomizer]: Factory method 'standardMongoSettingsCustomizer' threw exception with message: The connection string is invalid. Connection strings must start with either 'mongodb://' or 'mongodb+srv://
	at org.springframework.beans.factory.support.SimpleInstantiationStrategy.instantiate(SimpleInstantiationStrategy.java:171) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.instantiate(ConstructorResolver.java:655) ~[spring-beans-6.0.11.jar:6.0.11]
	... 71 common frames omitted
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'standardMongoSettingsCustomizer' defined in class path resource [org/springframework/boot/autoconfigure/mongo/MongoAutoConfiguration$MongoClientSettingsConfiguration.class]: Failed to instantiate [org.springframework.boot.autoconfigure.mongo.StandardMongoClientSettingsBuilderCustomizer]: Factory method 'standardMongoSettingsCustomizer' threw exception with message: The connection string is invalid. Connection strings must start with either 'mongodb://' or 'mongodb+srv://
	at org.springframework.beans.factory.support.ConstructorResolver.instantiate(ConstructorResolver.java:659) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:647) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1332) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1162) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:560) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:520) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:326) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:324) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.addCandidateEntry(DefaultListableBeanFactory.java:1640) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.findAutowireCandidates(DefaultListableBeanFactory.java:1597) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveMultipleBeans(DefaultListableBeanFactory.java:1443) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1375) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory$DependencyObjectProvider.resolveStream(DefaultListableBeanFactory.java:2143) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory$DependencyObjectProvider.orderedStream(DefaultListableBeanFactory.java:2137) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.boot.autoconfigure.mongo.MongoAutoConfiguration.mongo(MongoAutoConfiguration.java:59) ~[spring-boot-autoconfigure-3.1.3.jar:3.1.3]
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:104) ~[na:na]
	at java.base/java.lang.reflect.Method.invoke(Method.java:578) ~[na:na]
	at org.springframework.beans.factory.support.SimpleInstantiationStrategy.instantiate(SimpleInstantiationStrategy.java:139) ~[spring-beans-6.0.11.jar:6.0.11]
	... 72 common frames omitted
Caused by: org.springframework.beans.BeanInstantiationException: Failed to instantiate [org.springframework.boot.autoconfigure.mongo.StandardMongoClientSettingsBuilderCustomizer]: Factory method 'standardMongoSettingsCustomizer' threw exception with message: The connection string is invalid. Connection strings must start with either 'mongodb://' or 'mongodb+srv://
	at org.springframework.beans.factory.support.SimpleInstantiationStrategy.instantiate(SimpleInstantiationStrategy.java:171) ~[spring-beans-6.0.11.jar:6.0.11]
	at org.springframework.beans.factory.support.ConstructorResolver.instantiate(ConstructorResolver.java:655) ~[spring-beans-6.0.11.jar:6.0.11]
	... 92 common frames omitted
Caused by: java.lang.IllegalArgumentException: The connection string is invalid. Connection strings must start with either 'mongodb://' or 'mongodb+srv://
	at com.mongodb.ConnectionString.<init>(ConnectionString.java:303) ~[mongodb-driver-core-4.9.1.jar:na]
	at org.springframework.boot.autoconfigure.mongo.PropertiesMongoConnectionDetails.getConnectionString(PropertiesMongoConnectionDetails.java:47) ~[spring-boot-autoconfigure-3.1.3.jar:3.1.3]
	at org.springframework.boot.autoconfigure.mongo.MongoAutoConfiguration$MongoClientSettingsConfiguration.standardMongoSettingsCustomizer(MongoAutoConfiguration.java:74) ~[spring-boot-autoconfigure-3.1.3.jar:3.1.3]
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:104) ~[na:na]
	at java.base/java.lang.reflect.Method.invoke(Method.java:578) ~[na:na]
	at org.springframework.beans.factory.support.SimpleInstantiationStrategy.instantiate(SimpleInstantiationStrategy.java:139) ~[spring-beans-6.0.11.jar:6.0.11]
	... 93 common frames omitted


Process finished with exit code 1

```
`inputfield`


## Pause

Nehmt euch eine 15-minütige Pause.

## Setup: Github-Project

Erstellt gemeinsam ein neues Spring Boot Projekt für eine "Asterix-API" in IntelliJ mit den Dependencies Spring Data Mongo und Spring Web.

Wie lautet die URL zum Github-Repository?
`inputfield`

## Coding: Wiederholung: REST-Controller "GET"

Definiert einen Character-Record mit den Feldern id, name, age, profession.

Baut einen AsterixController, der bei dem Endpunkt `GET /asterix/characters` diese Liste zurückgibt:

```java
return List.of(
        new Character("1", "Asterix", 35, "Krieger"),
        new Character("2", "Obelix", 35, "Lieferant"),
        new Character("3", "Miraculix", 60, "Druide"),
        new Character("4", "Majestix", 60, "Häuptling"),
        new Character("5", "Troubadix", 25, "Barden"),
        new Character("6", "Gutemine", 35, "Häuptlingsfrau"),
        new Character("7", "Idefix", 5, "Hund"),
        new Character("8", "Geriatrix", 70, "Rentner"),
        new Character("9", "Automatix", 35, "Schmied"),
        new Character("10", "Grockelix", 35, "Fischer")
);
```

Ruft den Endpunkt mit Postman auf. Ihr solltet die Liste der Charaktere sehen.

## Coding: MongoDB

Nun lasst den AsterixController die Charaktere aus einer MongoDB-Datenbank laden.

> ⚠️ Achtung: Achte darauf, Deine AtlasDB-URL als Environment Variable zu setzen, damit Dein Passwort nicht auf GitHub landet!

> ⚠️ Achtung: Der Name der Datenbankcollection MUSS dem Namen des Records entsprechen, aber mit einem Kleinbuchstaben anfangen! Wenn Eure Entity zum Beispiel ein Record "AsterixCharacter" ist, dann muss die MongoDB-Collection "asterixCharacter" heißen!

Schreibe die Charakter-Daten dafür davor manuell in die Datenbank (mit Compass). Tipp: Ihr könnt ChatGPT nutzen um die Daten zu JSON umzuwandeln.

Nutzt gerne den [Beispielcode aus dem Vortrag](https://github.com/bartfastiel/spring-data) als Vorlage. Denkt an die Dinge, die Ihr braucht:
* Die Maven-Dependency zu Spring Data MongoDB
* Ein Repository-Interface, dass `MongoRepository<Charakter-Record, String>` implementiert
* In der `application.properties` die MongoDB-URL (aus Umgebungsvariable) und den Datenbanknamen
* Die Umgebungsvariable `MONGODB_URI` mit der Launch-Configuration in IntelliJ


Wenn Du in der AtlasDB (via Compass) eine Änderung an einem Charakter vornimmst, solltet Ihr danach in Postman die geänderten Daten empfangen können.

## Bonus: Anlegen, Ändern und Löschen

Erweitere den AsterixController, sodass er auch POST, PUT und DELETE unterstützt.

## Bonus: Query-Parameter

Erweitere den GET-Controller, sodass er auch Query-Parameter unterstützt um die Charaktere nach ihren Eigenschaften zu filtern.

## Bonus: Swagger SpringDoc

Füge diese Dependency zu Deinem Projekt hinzu:

```xml
		<dependency>
			<groupId>org.springdoc</groupId>
			<artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
			<version>2.2.0</version>
		</dependency>
```

Nach dem Neustart der Spring-Boot-Anwendung, navigiere zu http://localhost:8080/swagger-ui/index.html

Du solltest nun eine Dokumentation Deiner API sehen.

## Bonus: Custom Queries

Ergänze einen weiteren Endpunkt, der mit einer Custom Query pro Profession das Durchschnittsalter der Charaktere dieser Profession zurückgibt.

## Bonus: Dörfer, Haustiere, Waffen

Überlegt Euch eine immer detailliertere API für das Asterix-Universum. 

Implementiert die API mit Spring Boot und Spring Data.

Achtet dabei auf die REST-Konventionen (RFC-Dokumentation!).
