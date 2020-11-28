

**Notes:**
---
- This project prints all the envt properties using Java and shows how to pass custom System and Envt properties to a java executable.
- This project creates a jar which is executable with - `java -jar target/java-envt-mvn-1.0-SNAPSHOT.jar`

- You can pass custom ENVT variable while running to the jar, which won't get persisted to envt as follows 

`zAA="custom" zBB="custom2" java -jar target/java-envt-mvn-1.0-SNAPSHOT.jar`

<br>
this can be used to set envt, and configs.

- To set system variables while running from maven we can use `-D` construct like - `mvn compile; mvn exec:java -Dexec.mainClass="com.java.app.App" -DzAA="Custum_Value"`

- To set system variable while running jar we can also use `-D` like
`java -DzEnvt="STAGE" -DzVendor="Vendor1"  -jar target/java-envt-mvn-1.0-SNAPSHOT.jar`

**System & Envt Variable Set**
---
- `zAA="custom" zBB="custom2" java -DzEnvt="STAGE" -DzVendor="Vendor1"  -jar target/java-envt-mvn-1.0-SNAPSHOT.jar`


**Execute:-**
---
- `mvn compile; mvn exec:java -Dexec.mainClass="com.java.app.App"`

- `mvn package` - will generate jar file.


**References:**
---
- https://stackoverflow.com/questions/55440726/how-to-make-environment-variables-work-in-a-jar-file