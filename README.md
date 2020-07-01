In m2/settings.xml
	<server>
      <id>github</id>
      <username>username</username>
      <password>abcd</password>
    </server>


	<project.scm.id>github</project.scm.id>



	<scm>
		<developerConnection>scm:git:https://github.com/NagarajJB/work-with-maven-release-plugin.git</developerConnection>
		<url>https://github.com/NagarajJB/work-with-maven-release-plugin</url>
		<tag>HEAD</tag>
	</scm>


	<build>
		<extensions>
			<extension>
				<groupId>io.packagecloud.maven.wagon</groupId>
				<artifactId>maven-packagecloud-wagon</artifactId>
				<version>0.0.6</version>
			</extension>
		</extensions>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-release-plugin</artifactId>
				<configuration>
	
					<scmCommentPrefix>[maven-release-plugin] [skip ci]</scmCommentPrefix>
	
				</configuration>
			</plugin>
		</plugins>
	</build>
	
	
	<distributionManagement>
		<repository>
			<id>packagecloud.release</id>
			<url>packagecloud+https://packagecloud.io/NagarajaJB/release</url>
		</repository>
		<snapshotRepository>
			<id>packagecloud.snapshot</id>
			<url>packagecloud+https://packagecloud.io/NagarajaJB/snapshot</url>
		</snapshotRepository>
	</distributionManagement>