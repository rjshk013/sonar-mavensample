# SonarQube Basic Maven Example

This simple Maven project is importing JaCoCo's coverage report.
<br /><br />

## Usage

* Download SonarQube which matches with your Java version from [here](https://www.sonarqube.org/downloads/)

* Start the SonarQube server\
**For Windows**\
`YOUR_DIR_PATH\sonarqube\bin\windows-x86-xx\StartSonar.bat`\
**For other operating systems like Linux/Ubuntu**\
`YOUR_DIR_PATH/sonarqube/bin/[OS]/sonar.sh console`

* Once the SonarQube Server is up and running then you can visit the SonarQube Dashboard at http://localhost:9000/dashboard/ \
Default System administrator credentials are **admin/admin**

* Build the project, execute all the tests and analyze the project with SonarQube Scanner for Maven\
**`mvn clean verify sonar:sonar`**\
or\
**`mvn clean install sonar:sonar`**
        
* Click on the project name to see the code quality inspection
<br />

## Documentation

[SonarScanner for Maven](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-maven/)

change sonarcube url accordingly

Integrate maven project with sonarcube
--------------------------------------

1.Run sonarcube server in docker using the given docker-compose file
2.change sonarcube host url as per requirement is pom.xml
3.Install sonarcube plugin to Jenkins
4.On build step add below commands 

clean install

mvn sonar:sonar

Reference: https://blog.knoldus.com/integrate-maven-project-sonarqube/
