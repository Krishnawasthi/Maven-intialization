# JAR Files in Java

## 1. What is a JAR file?

JAR stands for **Java Archive**. It is a file that combines multiple Java class files and other resources into a single file.

Think of it like a ZIP file for a Java project.

## 2. Why do we use JAR files?

- **Easy to share:** Send many Java files as one file.
- **Code reuse:** Use existing Java code in other projects.
- **Easy distribution:** Package an application into a single archive.
- **Dependency management:** Add libraries to a Java project.

## 3. How does it work?

```text
Java Source Files (.java)
          |
          v
   Compile using javac
          |
          v
    Class Files (.class)
          |
          v
      JAR File (.jar)
```

## 4. Important JAR Commands

**Create a JAR:**
```bash
jar cf myapp.jar Main.class
```

**View JAR contents:**
```bash
jar tf myapp.jar
```

**Extract a JAR:**
```bash
jar xf myapp.jar
```

**Run an executable JAR:**
```bash
java -jar myapp.jar
```

Note: To run a JAR, it must be configured as an executable application, with its required dependencies available.

## 5. JAR File in Maven

Maven automatically creates a JAR when you run:

```bash
mvn package
```

The JAR is usually created inside the `target` folder.

For example:

```text
target/
└── hdfc-finance-0.0.1-SNAPSHOT.jar
```

## 6. Interview Question

**Q: Why do we use JAR files in Java?**

**Answer:** We use JAR files to package Java classes and resources into one file, making applications easier to share, distribute, and reuse.
