


培训分享
Training Share "Business model, code first & persistence"
业务模型，首先代码，保存

contents

- DDD, business domain model，UML or not
- code first and layered architecture
- Java persistence options (iBatis, Hibernate, JPA2, Spring Data)

JPA2/Hibernate database generation or read-oly mode

`persistence.xml`

	<?xml version="1.0" encoding="UTF-8" standalone="no"?>
	<persistence xmlns="http://java.sun.com/xml/ns/persistence" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" version="2.0" xsi:schemaLocation="http://java.sun.com/xml/ns/persistence http://java.sun.com/xml/ns/persistence/persistence_2_0.xsd">
	<persistence-unit name="persistenceUnit" transaction-type="RESOURCE_LOCAL">
	        <provider>org.hibernate.ejb.HibernatePersistence</provider>
	        <properties>
	            <property name="hibernate.dialect" value="org.hibernate.dialect.H2Dialect"/>
	            <!-- value="create" to build a new database on each run; value="update" to modify an existing database; value="create-drop" means the same as "create" but also drops tables when Hibernate closes; value="validate" makes no changes to the database -->
	            <property name="hibernate.hbm2ddl.auto" value="create"/>
	            <property name="hibernate.ejb.naming_strategy" value="org.hibernate.cfg.ImprovedNamingStrategy"/>
	            <property name="hibernate.connection.charSet" value="UTF-8"/>
	            <!-- Uncomment the following two properties for JBoss only -->
	            <!-- property name="hibernate.validator.apply_to_ddl" value="false" /-->
	            <!-- property name="hibernate.validator.autoregister_listeners" value="false" /-->
	        </properties>
	    </persistence-unit>
	</persistence>

value="create" to build a new database on each run; 
value="update" to modify an existing database; 
value="create-drop" means the same as "create" but also drops tables when Hibernate closes; 
value="validate" makes no changes to the database
 

-- 

The Principles of OOD (SOLID)
http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod

