# Hibernate Many to Many Annotation 

A relationship is a connection between two types of entities. In the case of a many-to-many relationship, both sides can relate to multiple instances of the other side.

<img src="https://www.baeldung.com/wp-content/uploads/2017/09/New.png">

### The Model Classes
The model classes Employee and Project need to be created with JPA annotations:

```
@Entity
@Table(name = "Employee")
public class Employee { 
    // ...
 
    @ManyToMany(cascade = { CascadeType.ALL })
    @JoinTable(
        name = "Employee_Project", 
        joinColumns = { @JoinColumn(name = "employee_id") }, 
        inverseJoinColumns = { @JoinColumn(name = "project_id") }
    )
    Set<Project> projects = new HashSet<>();
   
    // standard constructor/getters/setters
}
@Entity
@Table(name = "Project")
public class Project {    
    // ...  
 
    @ManyToMany(mappedBy = "projects")
    private Set<Employee> employees = new HashSet<>();
    
    // standard constructors/getters/setters   
}
```
* The @ManyToMany annotation is used in both classes to create the many-to-many relationship between the entities.

* This association has two sides i.e. the owning side and the inverse side. In our example, the owning side is Employee so the join table is specified on the owning side by using the @JoinTable annotation in Employee class. The @JoinTable is used to define the join/link table. In this case, it is Employee_Project.

* The @JoinColumn annotation is used to specify the join/linking column with the main table. Here, the join column is employee_id and project_id is the inverse join column since Project is on the inverse side of the relationship.

* In the Project class, the mappedBy attribute is used in the @ManyToMany annotation to indicate that the employees collection is mapped by the projects collection of the owner side

## Security:
 a humorous overview It's almost as though security researchers have issues with public relations since they make it impossible to do everything you want on a website. Security experts are always working to address security vulnerabilities and improve people's ability to establish more secure passwords. Any password may be hacked. Using the same password for everything isn't a smart idea. Security researchers utilize the threat model to prevent security breaches by instructing individuals on how to create passwords and where security risks originate, although security breaches don't always come from apparent sources. There is no such thing as a flawless security system, and any security system, no matter how robust, will be breached at some point. To make things more safe, information flow control and security labels are employed. The majority of individuals do not want to pay a lot of money merely to make their system safer. As a result, security researchers should focus on what will happen when I properly construct my software, rather than what may happen.

