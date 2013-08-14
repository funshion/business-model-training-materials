

## Example Spring-petclinic

- code <https://github.com/SpringSource/spring-petclinic>
- presentation <https://speakerdeck.com/michaelisvy/spring-petclinic-sample-application>

overview  

![](packages.PNG)

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
