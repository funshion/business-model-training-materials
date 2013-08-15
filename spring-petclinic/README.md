
## Example Spring-petclinic

- code <https://github.com/SpringSource/spring-petclinic>
- presentation <https://speakerdeck.com/michaelisvy/spring-petclinic-sample-application>

overview  

![](packages.PNG)

Domain object - entity.  

![](ModelClasses-annotated.png)

Note: inclusion of ORM mapping into domain code (using annotations instead of XML binding) is violation of Layered Architecture principles (independence of layers).
However this is simpler (maintaining 1 file instead of 2; annotation don't affect code behavior, e.g. Unit test can run OK )

![](Owner.PNG)

Repository is interface that defines access methods:

-    `Collection<Owner> findByLastName(String lastName) throws DataAccessException;`
-    `Owner findById(int id) throws DataAccessException;`
-    `void save(Owner owner) throws DataAccessException;`


![](Repository.PNG)

JpaOwnerRepository

![](JpaOwnerRepository.PNG)

SpringDataOwnerRepository

![](SpringDataOwnerRepository.PNG)

`business-config.xml` defines possible configuration as `profiles`s.

![](business-config_xml.PNG)
