# spring-rest
An example Spring project that will include different parts of Spring Framework, Spring Boot and other commonly used parts.

## Database
### H2
This example uses a H2 In-Memory DB as configured in ```application.properties```.

You can access the Web Console using http://localhost:9090/h2-console/  
(Ensure you use the URL, e.g. jdbc:h2:mem:testdb, user and password from the properties file - default values differ)

## REST and Links

A simple REST repository is implemented in the interface ```PersonRepository```.  
Extending the Spring Data ```PagingAndSortingRepository``` annotated with ```RepositoryRestResource``` it allows you to do basic CRUD operations mapped to the appropriate HTTP verbs.  
A easy way to explore and add new elements is to use the HAL explorer included in the pom.xml.  
You can access it using <http://localhost:9090> and add some elements and afterwards test the paging and sorting using, e.g.
<http://localhost:9090/explorer/index.html#uri=/persons?page=1&size=1&sort=lastName,asc>
