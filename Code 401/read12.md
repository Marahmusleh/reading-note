# Spring RequestMapping

1. @RequestMapping — by Path
2. @RequestMapping — the HTTP Method
The HTTP method parameter has no default. So, if we don't specify a value, it's going to map to any HTTP request.

3. @RequestMapping With the headers Attribute

   The mapping can be narrowed even further by specifying a header for the request:
```
@RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)
@ResponseBody
public String getFoosWithHeader() {
    return "Get some Foos with Header";
}
``` 

4. RequestMapping With Path Variables
4.1. Single @PathVariable
```
@RequestMapping(value = "/ex/foos/{id}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariable(
  @PathVariable("id") long id) {
    return "Get a specific Foo with id=" + id;
}
```
4.2. Multiple @PathVariable
A more complex URI may need to map multiple parts of the URI to multiple values:
```
@RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariables
  (@PathVariable long fooid, @PathVariable long barid) {
    return "Get a specific Bar with id=" + barid + 
      " from a Foo with id=" + fooid;
}
```
4.3. @PathVariable With Regex

## CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data

### Spring Data Repositories
The JpaRepository – which extends PagingAndSortingRepository and, in turn, the CrudRepository.

Each of these defines its own functionality:

* CrudRepository provides CRUD functions
* PagingAndSortingRepository provides methods to do pagination and sort records
* JpaRepository provides JPA related methods such as flushing the persistence context and delete records in a batch.

And so, because of this inheritance relationship, the JpaRepository contains the full API of CrudRepository and PagingAndSortingRepository.

the typical CRUD functionality:

* save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch.
* findOne(…) – get a single entity based on passed primary key value.
* findAll() – get an Iterable of all available entities in database.
* count() – return the count of total entities in a table.
* delete(…) – delete an entity based on the passed object.
* exists(…) – verify if an entity exists based on the passed primary key  value.


