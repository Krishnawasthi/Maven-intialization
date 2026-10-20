<img width="908" height="301" alt="image" src="https://github.com/user-attachments/assets/eaf086ee-987f-4454-a193-04f611cd5ae3" />
# Maven in Java

## 1. What is Maven?

Maven is a **build automation and dependency management tool** used in Java projects.

It helps us download required libraries, compile Java code, run tests, and package our application into a JAR file.

## 2. Why Do We Use Maven?

Without Maven, we may need to download JAR files manually, manage dependencies ourselves, and compile and package the project manually.

Maven automates these tasks and makes project management easier.

## 3. What Is Dependency Management?

A dependency is a library that our project needs to work.

For example, if we want to convert Java objects into JSON, we can use the Gson library.

Maven downloads the required library and manages its dependencies for us.

Example:

```xml
<dependency>
    <groupId>com.google.code.gson</groupId>
    <artifactId>gson</artifactId>
    <version>2.14.0</version>
</dependency>
```

Instead of manually downloading Gson, Maven can download it from a configured repository.

## 4. What Is `pom.xml`?

POM stands for **Project Object Model**.

`pom.xml` is the main configuration file of a Maven project. It tells Maven how the project is identified and which dependencies and build settings it needs.

It contains information such as:

- Project name and version
- `groupId` and `artifactId`
- Dependencies
- Build configuration

## 5. What Is `settings.xml`?

`settings.xml` is used to configure Maven for a particular user's environment or a Maven installation.

It can contain:

- Repository mirror settings
- Proxy settings
- Authentication configuration for private repositories
- Local repository location

Unlike `pom.xml`, it usually contains environment-specific settings rather than the project's main configuration.

Common location on Windows:

```text
C:\Users\<username>\.m2\settings.xml
```

This file is optional for many basic projects.

## 6. What Is `groupId`?

`groupId` identifies the organization, company, or group responsible for a project.

Example:

```xml
<groupId>com.example</groupId>
```

Think of it as identifying **who owns or maintains the project**.

## 7. What Is `artifactId`?

`artifactId` is the name of the particular project or module.

Example:

```xml
<artifactId>hdfc-finance</artifactId>
```

Think of it as identifying **which project it is**.

## 8. What Is `version`?

`version` identifies a particular release of a project.

Example:

```xml
<version>1.0-SNAPSHOT</version>
```

`SNAPSHOT` indicates a development version that may change before a final release.

## 9. What Is an Artifact?

An artifact is a file produced by a build or published for other projects to use.

For example:

```text
hdfc-finance-0.0.1-SNAPSHOT.jar
```

This JAR file is an artifact produced by your Maven project.

## 10. Important Maven Commands

| Command | Purpose |
|---|---|
| `mvn compile` | Compiles main Java code |
| `mvn test` | Compiles and runs tests |
| `mvn package` | Packages the project into a JAR or other configured format |
| `mvn clean` | Removes generated build files |
| `mvn install` | Installs the artifact in the local Maven repository |

## 11. Quick Revision

- **Maven:** Automates Java builds and manages dependencies.
- **Dependency:** A library required by a project.
- **`pom.xml`:** Main project configuration file.
- **`settings.xml`:** Environment-specific Maven configuration.
- **`groupId`:** Identifies the project group or organization.
- **`artifactId`:** Identifies the project or module.
- **`version`:** Identifies a particular version of the project.
- **Artifact:** A file produced or published by the build, such as a JAR.

**Remember:** Maven manages the build process and dependencies, while `pom.xml` tells Maven what your project needs.
