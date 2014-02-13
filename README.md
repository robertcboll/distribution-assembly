# Distribution Assembly

### About
A maven assembly plugin descriptor used to aggregate shaded jar, bin/* and conf/* into a compressed tar for distribution. The generated tar will follow the convention `${project.finalName}-dist.tar.gz`.

### Usage
```
<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-assembly-plugin</artifactId>
		<dependencies>
			<dependency>
				<groupId>com.robertcboll.assembly</groupId>
				<artifactId>dropwizard-distribution-assembler</artifactId>
				<version>${project.version}</version>
			</dependency>
		</dependencies>
		<configuration>
			<descriptorRefs>
				<descriptorRef>dist</descriptorRef>
			</descriptorRefs>
		</configuration>
</plugin>
```