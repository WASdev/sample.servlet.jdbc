JDBC Servlet Sample
==============

The ServletJDBCEngine sample contains a server definition for basic servlet support, and illustrates a simple datasource definition using an included configuration file. It uses Apache Derby (an open source relational database). Also included is a servlet which gets a connection to the database using the defined datasource, creates a table, inserts some data, retrieves the data, and prints the data out to the browser.

Once the server is running, the application will be available under [http://localhost:9080/JDBCApp](http://localhost:9080/JDBCApp).

## Running in Eclipse with Maven

1. Clone this project and import into Eclipse as an 'Existing Maven Project'.
2. Right click the project and select `Run As` -> `Maven Clean`.
3. Right click the project and select `Run As` -> `Maven Install`.
4. Right click the project and select `Run As` -> `Maven Build...` then run the goal `liberty:install-server`.
5. You should see the following in the console:
   `CWWKZ0001I: Application JDBCApp started in XX.XX seconds.`
    In your browser, enter the URL for the application: [http://localhost:9080/JDBCApp](http://localhost:9080/JDBCApp).
    In your browser, you should see the message:
    `Text retrieved from database is: myHomeCounty`

## Running in Eclipse with WDT

1. WIP

## Running with Maven

This project can be built with [Apache Maven](http://maven.apache.org/). The project uses [Liberty Maven Plug-in][] to automatically download and install Liberty profile runtime from the [Liberty repository](https://developer.ibm.com/wasdev/downloads/). Liberty Maven Plug-in is also used to create, configure, and run the application on the Liberty server. 

Use the following steps to run the application with Maven:

1. Execute full Maven build. This will cause Liberty Maven Plug-in to download and install Liberty profile server.
    ```bash
    $ mvn clean install
    ```

2. To run the server with the Servlet sample execute:
    ```bash
    $ mvn liberty:run-server
    ```

## Deploying to Bluemix

Click the button below to deploy your own copy of this application to [Bluemix](https://bluemix.net).

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.com/WASdev/sample.servlet.jdbc.git)

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

