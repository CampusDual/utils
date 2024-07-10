[![Last version](https://img.shields.io/maven-central/v/com.campusdual/utils?label=Latest%20version&style=flat-square)](https://maven-badges.herokuapp.com/maven-central/com.campusdual/utils)

# Utils

Class of utilities to generate a random number, express a double with 2 decimal places, list lists with System.out.println(), list and select elements of a list and help to facilitate the input of data by console in a Java project.

# FAQ
## I have an error for latest SNAPSHOT version.
This error occurs becase the command is trying to get the *latest* version (*99.9.9-SNAPSHOT*). This problem occurs because by default, ***SNAPSHOT versions cannot be accessed from Maven Central***. For it, it is necessary to activate, in the *settings.xml* file, the access to the SNAPSHOT versions of Maven Central. In case we do not have this file, we have to create it ***inside*** the .m2 folder (*by default, it is in the following path: ~/.m2*). [Here is an example](https://gist.github.com/supportcampusdual/fa55eb0fa7fd91f825abcc557a1f730d) of the *settings.xml* file content to enable SNAPSHOT versions:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" 
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd">
  <profiles>
	<profile>
		<id>ossrh</id>
		<repositories>
			<repository>
				<id>ossrh-snapshot</id>
				<url>https://s01.oss.sonatype.org/content/repositories/snapshots/</url>
				<snapshots>
					<enabled>true</enabled>
				</snapshots>
			</repository>
		</repositories>
	</profile>
  </profiles>
  <activeProfiles>
	<activeProfile>ossrh</activeProfile>
  </activeProfiles>
</settings>
```
In case you do not allow the use of SNAPSHOT versions, the latest available release is (without the v): [![Backend Archetype](https://img.shields.io/maven-central/v/com.campusdual/utils?label=&style=flat-square)](https://maven-badges.herokuapp.com/maven-central/com.campusdual/utils)

> **_NOTE:_**  The release version may not have the latest changes.
