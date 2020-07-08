# maven-ci-friendly
Maven CI friendly version

Usage examples:

mvn clean package -Drevision=1.5

mvn clean install -Drevision=1.5

# start docker container for nexxus to simulate the maven push
docker run -d -p 8081:8081 --name nexus sonatype/nexus3

http://localhost:8081
sign in with : 
user:admin
passwrod:a63b5d11-aae4-4a41-bc27-1a4d7c1863d1
Note: you would need to change the password upon first login, i changed it to admin. 
Now set this user pass in the settings.xml

mvn clean deploy -Drevision=1.5

mvn clean deploy -Drevision=1.5-SNAPSHOT


