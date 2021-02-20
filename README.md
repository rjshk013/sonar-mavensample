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

3.Install SonarQube Scannerplugin to Jenkins

Login into sonarcube --my account --security--generate token & save 

Configure your SonarQube server:


    Log into Jenkins as an administrator and go to Manage Jenkins > Configure System.
    Scroll down to the SonarQube configuration section, click Add SonarQube, and add the values you're prompted for.
    The server authentication token should be created as a 'Secret Text' credential.

Job Configuration

    Configure the project, and go to the Build Environment section.
    Enable Prepare SonarScanner environment to allow the injection of SonarQube server values into this particular job. If multiple SonarQube instances are configured, you will be able to choose which one to use. Once the environment variables are available, use them in a standard Maven build step (Invoke top-level Maven targets) by setting the Goals to include, or a standard Gradle build step (Invoke Gradle script) by setting the Tasks to execute.

Maven goal:

$SONAR_MAVEN_GOAL


4.On build step add below commands 

clean install

mvn sonar:sonar

Reference: https://blog.knoldus.com/integrate-maven-project-sonarqube/

https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-jenkins/


sonar token : 9e38781d5d71d533a2655ea87f5c7364932b5e25
