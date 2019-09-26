# Enable Active Directory Authentication in DataGrip
The original instructions can be found [here](https://codejuicer.com/2018/08/29/datagrip-and-azure-sql-server-active-directory-howto/).

This repo already contains the POM file that you need to download all of the .jar files.

* Clone this repository.
* Run `mvn clean dependency:copy-dependencies` and they will show up in the `/lib` folder.
    * Do this if you have Maven installed or click the `M` int the Maven tab if using IntelliJ.
* In DataGrip in `File -> Data Sources And Drivers -> Drivers`, select the `Azure SQL Database` driver.
* Add the jars that were populated in the `lib` folder.

Now, when you go to configure a Azure SQL Database that uses Active Directory Authentication, in the *Advanced* tab you can set `authentication` to `ActiveDirectoryPassword`. 
