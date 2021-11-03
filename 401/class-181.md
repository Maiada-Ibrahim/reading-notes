
# Web App Security
# Many to Many
- A many-to-many relationship we use when multiple records in a table are associated with multiple records in another table

- use for that @ManyToMany annotation

- example for this relation relationship is the employee and project the employee can be assigned to multiple projects and a project may have multiple employees working at it, so here use many to many

- using our example we will write this code in the employ Entity

       @ManyToMany(cascade = { CascadeType.ALL })
       @JoinTable(
        name = "Employee_Project", 
        joinColumns = { @JoinColumn(name = "employee_id") }, 
        inverseJoinColumns = { @JoinColumn(name = "project_id") }
       )
           Set<Project> projects = new HashSet<>();
   
       // standard constructor/getters/setters
      }



and write that in project Entity


       @ManyToMany(mappedBy = "projects")
       private Set<Employee> employees = new HashSet<>();
    
    // standard constructors/getters/setters   
       }




--------------------------------------------------------
# Security: a humorous overview
at first page he tell us it is better to take care before have aproblem 

websites are amazing BUT DON'T
CLICK ON THAT LINK, and your phone can run all of these amazing apps BUT MANY
OF YOUR APPS ARE EVIL, and if you order a Russian bride on Craigslist YOU MAY GET
A CONFUSED FILIPINO MAN WHO DOES NOT LIKE BEING SHIPPED IN A BOX.

he said that two tell us we have always two side good and bad side

so in page two he said we must foucse to put strong password at the same time easy to remmber for us instead of thinking about what I do after my account My account is hacke 
and he think we must know what the reason and Actions if I do it then My account can hacke and ignore it this solve any problem from the root

in page three he said the a definitely
a problem, but problem identification is what makes every thing
clear, and now we know what we need