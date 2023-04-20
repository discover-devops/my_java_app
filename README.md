##### build the project

    ./gradlew build

##### build Docker image called java-app. Execute from root

    docker build -t java-app .
    
##### push image to repo 

    docker tag my_java_app discoverdevops/myprodapp:my_java_app-1.0
    

##############################


Gradle wrapper version upgraded from version 6.x to 7.0 
        
###### This will change the version in wrapper.settings

     ./gradlew wrapper --gradle-version 7.0

###### This will update the complete wrapper and download version 7.0 jar

     ./gradlew wrapper --gradle-version 7.0

In build.gradle file, replace:
- compile with implementation 
- testCompile with testImplementation

Because, version 7.0 removed compile and testCompile configurations.
Source: https://docs.gradle.org/current/userguide/upgrading_version_6.html#sec:configuration_removal

##############################

Upgrade Gradle wrapper version from version 7.0 to 7.5(latest version)

###### Change version in the gradle wrapper file
    
    vim gradle/wrapper/gradle-wrapper.properties

Set the new version in the following line 

    distributionUrl=https\://services.gradle.org/distributions/gradle-7.5-bin.zip    
