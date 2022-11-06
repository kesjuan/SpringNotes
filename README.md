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
* @OneToMany - used to define a one to many relationship between an object and a list of objects. This is paired with @manyToOne. Mapped by property ties the @ManyToOne object to this list. Mapped by property is set to the name of the variable with the @ManyToOne annotation. The list on the @OneToMany side will be updated by this relationship. 
* @ManyToOne
* @ManyToMany
