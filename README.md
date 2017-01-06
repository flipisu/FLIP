# FLIP_WEB
FLIP can simulate inheritance for diploid organisms with a variable
number of genes, chromosomes and traits. Traits are simulated by combining
genetic effects and random environmental effects. Genetic effects are simulated
from genes with known effects and linkages and the optional addition of unlinked
genes whose effects will generate desired means, variances and covariances. 

In addition to linkage effects, FLIP can simulate imprinting, dominance and epistasis. 
Trait performance of simulated animals can demonstrate response to selection as well
as inbreeding depression and heterosis.

Initially FLIP was developed by Robert Benson as a standalone application to be run in any
Desktop computer supporting JDK 1.2 or Higher. Later on, FLIP was modified in order that it 
can become a web-based software as today is available. 

SOFTWARE REQUIREMENTS

FLIP has been tested with the following software:

-JRE 1.5 or higher
-Apache Tomcat 6.0 and 7.0 (FLIP does not work with Tomcat 8)
-MySQL Server 5.5 or Higher

One of the installation steps of MySQL requires to set its root password. By Default, FLIP assumes this password is set as "FlipWeb".
If you want to change it (This is recommendable), you need to update a global variable, named "password", which is hard 
coded. You can find it at /FlipWeb/src/edu/iastate/ansci/flip/database/DatabaseFlip.java

Then, you need to download the following sql script: Flip_Database_2016_01_05_No_Examples.sql.
Example: %> mysql -u root -p < Flip_Database_2016_01_05_No_Examples.sql

This script will create automatically all needed tables to manage the flip data.Flip is configured  with a default admin account whose details are: username: "admin" and password: "edare1". You should be able to change it from FLIP_WEB

SOFTWARE INSTALLATION

Assuming you have installed Apache Tomcat, MYSQL Server and you have run the provided the sql script to create the FLIP tables, you just need to download FlipWeb_<creation_date>.war file.Choose the latest version and rename it simply as FlipWeb.war. In order that, Tomcat7 can recognize this war file, you need to move it to the webapps directory of your tomcat7 installation.

To test, if FlipWeb is running, from your browser (recommended firefox or chrome) open the url http://localhost:8080/FlipWeb
If this is working, you should able to see the FLIP's welcome page.




