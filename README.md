# Basic Maven Example

This simple Maven project is importing JaCoCo's coverage report. For multi-module project example 
see [multi-module Maven project](../maven-multimodule/README.md)

## Usage

* Build the project, execute all the tests and analyze the project with SonarQube Scanner for Maven(from root  of the project):

```shell
        mvn clean verify sonar:sonar
```

## Documentation

[SonarScanner for Maven](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-maven/)


Steps to run SonarQube:

1. Pull the docker image and run the command -> docker pull sonarqube:8.7.1-community
2. Once the process starts running, navigate to http://localhost:9000 to see the UI
3. Generate a token through the UI. You can generate new tokens at User > My Account > Security.
4. Run the command to generate report

```shell
mvn clean verify sonar:sonar -Dsonar.login=<Token generated in Step 3.>
```

5. Navigate to http://localhost:9000/projects



Refer Below links for more details:

1. https://medium.com/knoldus/how-to-integrate-your-maven-project-with-sonarqube-79f7368f8c7a
2. https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-maven/
3. https://docs.sonarqube.org/latest/user-guide/user-token/
4. https://medium.com/@HoussemDellai/setup-sonarqube-in-a-docker-container-3c3908b624df