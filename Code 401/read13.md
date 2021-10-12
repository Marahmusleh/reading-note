# Working with Relationships in Spring Data REST

## Relationships in JPA 
1. One-to-One RelationShip 

* To define this relationship in Jpa we use the @OneToOne annotation.
* We can optionally use @RestResources to customize our end point.
* To expose each entity in Jpa we use a repository interface which will  be extending from CRUD Repository or any child of it.
* Sending get request to an endpoint would return an empty object if no post requests was sent.
* We use the PUT method to retrieve the JSON object or Delete to delete a record.
```
@OneToOne
@JoinColumn(name = "secondary_address_id")
@RestResource(path = "libraryAddress", rel="address")
private Address secondaryAddress;
```
2. One-to-Many RelationShip 
*One to many can be declared the same as one to one relationship in addition to many to one.*
* It can also have optional @RestResources to customize endpoints.
* to Expose it we need the same repository interface that extends CRUDRepository.
```
public interface BookRepository extends CrudRepository<Book, Long> { }
```
* Use the PUT request to associate the repository with the association.
3. Many-to-Many Relationship 
* Is the same as the previous realtionships.
* A many-to-many relationship is defined using @ManyToMany annotation, to which we can add @RestResource.

## Integration Testing
Some integration test we can write:

1. Verify View Name

2. Verify Response Body

3. Send GET Request With Path Variable

4. Send GET Request With Query Parameters