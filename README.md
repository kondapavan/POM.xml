# POM.xml
<properties>
		<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
		<selenium.version>2.48.2</selenium.version>
		<junit.version>4.12</junit.version>
	</properties>

	<dependencies>
		<dependency>
			<groupId>org.seleniumhq.selenium</groupId>
			<artifactId>selenium-server</artifactId>
			<version>${selenium.version}</version>
			<scope>main</scope>
		</dependency>

		<dependency>
			<groupId>org.seleniumhq.selenium</groupId>
			<artifactId>selenium-java</artifactId>
			<version>${selenium.version}</version>
		</dependency>


		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<version>${junit.version}</version>
		</dependency>

	</dependencies>
	<build>
		<plugins>
			<plugin>
				<groupId>org.eclipse.m2e</groupId>
				<artifactId>lifecycle-mapping</artifactId>
				<version>1.0.0</version>
				<configuration>
					<lifecycleMappingMetadata>
						<pluginExecutions>
							<pluginExecution>
								<pluginExecutionFilter>
									<groupId>org.codehaus.mojo</groupId>
									<artifactId>aspectj-maven-plugin</artifactId>
									<versionRange>[1.0,)</versionRange>
									<goals>
										<goal>test-compile</goal>
										<goal>compile</goal>
									</goals>
								</pluginExecutionFilter>
								<action>
									<execute />
								</action>
							</pluginExecution>
						</pluginExecutions>
					</lifecycleMappingMetadata>
				</configuration>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>2.3.2</version>

				<configuration>
					<source>1.7</source>
					<target>1.7</target>
				</configuration>
			</plugin>

		</plugins>
	</build>
</project>
