# SpringNotes
Tiers of MVC are the presentation Layer, the Business Logic and the Data layer
The Controller Tier Handles Request/Response, exceptions and view routing, has No business logic, coordinates with service and repository class, annotated with @Controller.
Service Tier is annotated with @Service, Describes verbs/actions of system. Business Logic belongs here. Transactional. Often same methods as repository.
Repository Tier is annotated with @Repository. Nouns(Data) of the system. Database Interaction. One to one object mapping. Often one to one table Mappinh.
Injection allows you to turn regular classes into managed objects and to inject them into any other managed object. 
Transactional uses @Transactional annotation refers to a series of actions that must all complete successfully. If one or more actions fail, all other actions must backout leaving the state of the application unchanged. If the method doesn't just read only it should be wrapped with transactional annotation. Always start transactions at the service Teir.
@RestController Vs @Controller - Restcontroller annotates every Return type as a @ResponseBody. Controller does not do this and responseBody annotation will need to be added manually.
Join type annotations -
* @OneToOne - One to one represents that a single entity is associated with a single instance of the other entity. An instance of a source entity can be at most mapped to one instance of the target entity.
* @OneToMany - used to define a one to many relationship between an object and a list of objects. This is paired with @manyToOne. Mapped by property ties the @ManyToOne object to this list. Mapped by property is set to the name of the variable with the @ManyToOne annotation. The list on the @OneToMany side will be updated by this relationship. one-to-many mapping means that one row in a table is mapped to multiple rows in another table.
* @ManyToOne - where one entity contains values that refer to another entity (a column or set of columns) that has unique values.
* @ManyToMany - when multiple records in a table are associated with multiple records in another table. For example, a many-to-many relationship exists between customers and products: customers can purchase various products, and products can be purchased by many customers.
Fetch Types - used with join types to choose when we want to fetch there are 2 types... Lazy and Eager. Lazy queries the database when the getter for that property is called. Eager queries the database when the object is created.
```
-----------------------------------------------------------------------------------------------------------------------------------------------------------
```
Spring boot works with spring applications by
Using build and dependency managment. Maven and Gradle are build tools ised to specify what dependencies or libraries the application will use for compilation and packaging for deployment. 
Project Layout and structure is partly tied to a maven project layout mixed with spring annotations to help identify different architectural pieces of the application.
Spring boot Starters are packages or wrappers onto spring popular frameworks like spring MVC, Spring data, Spring Batch etc.. When adding a dependency like spring boot MVC the spring boot MVC starter will integrate and setup that library so it is fully configured and ready to use.
Embeded Servers Apache Tomcat, Jetty-Undertow


Spring framework boot provides the parent spring boot definition. This specifies the spring boot version you are using. The dependencies do not have to specify the version because of the parent. 
@SpringBootApplication annotation enables auto configuration, this sets up tomcat, a port number and adjusts any other needed configuration to get that library up and running. Also sets uo auto scanning for repos, entity beans and mvc controllers.
Spring-Boot-Starter-Actuator can give you a health check on your application. identifying if services are up running or not. can get JVM statistics like memory, heap and thread dump, and process info.


Testing With Spring boot starts with adding the spring test starter to the dependency list. This gives you the appropriate testing annotations and testing frameworks.
