# Downloading and Building

## Jar Files

A complied jar file is available on Nexus (requires an Alfresco Nexus account). This can be found [here](https://artifacts.alfresco.com/nexus/content/repositories/alfresco-support-snapshots/org/alfresco/support/jmxdump-analyzer-fx/)

## To manually build from source:

**Pre-requisites:**

- Maven 3.3.9 or above
- Java 8

**Steps:**

1. Clone this repository:
`git clone https://github.com/Alfresco/jmxdump-analyzer.git`
2. Build using Maven:
`mvn clean install`
3. Run the application:
`java -jar target/jmxdump-analyzer-fx-x.x.x-jar-with-dependencies.jar`
(replacing x.x.x with the version you are running)
