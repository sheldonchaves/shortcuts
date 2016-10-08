#Maven

#### Build Lifecycle
goals:
- validate
- compile
- test
- package
- verify
- install
- deploy

####create simple project with class main

	mvn archetype:generate -DartifactId=Project -DgroupId=br.com.linkage.project -DinteractiveMode=false -DarchetypeArtifactId=maven-archetype-quickstart

	//compile class main:
	mvn compile

	//run test:
	mvn test
	//offline 
	mvn -o test

	//clean targer dir:
	mvn clean

	//create html test report
	mvn surefire-report:report

	//generate jar
	mvn package

#### verify exist new dependency version

	mvn versions:display-dependency-updates

#### update dependencies to last versions
	
	mvn versions:use-latest-versions

###Plugin PMD (code analysis)
	
	// Creates a PMD report
	pmd:pmd
 	
	// Fail the build if there were any PMD violations 
	pmd:check

config:

	...
	<build>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-pmd-plugin</artifactId>
				<version>3.6</version>
				<executions>
					<execution>
						<phase>verify</phase>
						<goals>
							<goal>check</goal>
						</goals>
					</execution>
				</executions>
			</plugin>
		</plugins>
	</build>
	...

###Plugin JaCoCo (code coverage test)

goals:
- help
- prepare-agent
- prepare-agent-integration
- merge
- report
- report-integration
- report-aggregate
- check
- dump
- instrument
- restore-instrumented-classes

Missed	
config:

	...
	<plugin>
		<groupId>org.jacoco</groupId>
		<artifactId>jacoco-maven-plugin</artifactId>
		<version>0.7.7.201606060606</version>
		<executions>
			<execution>
				<goals>
					<goal>prepare-agent</goal>
					<goal>report</goal>
				</goals>
			</execution>
		</executions>
	</plugin>
...

