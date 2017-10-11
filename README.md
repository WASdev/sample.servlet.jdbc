JDBC Servlet Sample [![Build Status](https://travis-ci.org/WASdev/sample.servlet.jdbc.svg?branch=master)](https://travis-ci.org/WASdev/sample.servlet.jdbc)
==============

The ServletJDBCEngine sample contains a server definition for basic servlet support, and illustrates a simple datasource definition using an included configuration file. It uses Apache Derby (an open source relational database). Also included is a servlet which gets a connection to the database using the defined datasource, creates a table, inserts some data, retrieves the data, and prints the data out to the browser.

Once the server is running, the application will be available under [http://localhost:9080/JDBCApp](http://localhost:9080/JDBCApp).

## Running with Maven

### Running in Eclipse with Maven

1. Clone this project and import into Eclipse as an 'Existing Maven Project'.
2. Right-click the project and select **Run As > Maven Clean**.
3. Right-click the project and select **Run As > Maven Install**.
4. Right-click the project and select Run As -> Run on Server.
5. You should see the following in the console:
   `CWWKZ0001I: Application JDBCApp started in XX.XX seconds.`
    In your browser, enter the URL for the application: [http://localhost:9080/JDBCApp](http://localhost:9080/JDBCApp).
    In your browser, you should see the message:
    `Text retrieved from database is: myHomeCounty`

### Running from the command-line with Maven

This project can be built with [Apache Maven](http://maven.apache.org/). The project uses the [Liberty Maven Plug-in] to automatically download and install the Liberty 
Java EE Web Profile 7 from [Maven Central]. The Liberty Maven Plug-in is also used to create, configure, and run the application on the Liberty server. 

Use the following steps to run the application with Maven:

1. Execute full Maven build. The Liberty Maven Plug-in will download and install the Liberty server.
    ```bash
    $ mvn clean install
    ```

2. To run the server with the Servlet sample execute:
    ```bash
    $ mvn liberty:run-server
    ```

## Running with Gradle

This project can also be built and run using [Gradle](http://gradle.org/). The provided `build.gradle` file applies the Liberty Gradle Plug-in and is configured to automatically download and install the Liberty Java EE Web Profile 7 runtime from [Maven Central]. The Liberty Gradle Plug-in also has tasks that create, configure, and run applications on a Liberty server.

Use the following steps to run the application with the Gradle wrapper. (Windows machines use `gradlew.bat`):

1. Execute the full Gradle build. The Liberty Gradle Plug-in will download and install the Liberty server.
    ```bash
    $ ./gradlew clean build
    ```

2. To start the server with the JDBCApp sample run:
    ```bash
    $ ./gradlew libertyStart
    ```

    Alternatively, execute the run command:
    ```bash
    $ ./gradlew libertyRun --no-daemon
    ```

3. To stop the server, execute:
    ```bash
    $ ./gradlew libertyStop
    ```  

Please refer to the [Liberty Gradle Plug-in] repository for documentation and configuration examples for the plug-in.


# Notice

© Copyright IBM Corporation 2017.

# License

```text
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
````

[Liberty Maven Plug-in]: https://github.com/WASdev/ci.maven
[Liberty Gradle Plug-in]: https://github.com/WASdev/ci.gradle
[Maven Central]: https://search.maven.org/

