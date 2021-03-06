# Basic CodeCup Java project setup with Maven

### Introduction

[CodeCup](https://codecup.nl) contestants must submit their code in one single file. This repository contains
a basic project setup using Apache Maven. This setup is made for contestants who want to split up their implementation
into multiple files/classes. A source merger is included, which merges all source files into 1 single file. Import
statements are deduplicated and placed at the top of the generated source file.

### Rules

For this to work, the source files must follow a few simple rules:

* Only one public class may exist. Typically, this will be the class containing the `main` method (`Zuniq` in this case).
  All other classes must have default (package) visibility.
* All source files must reside in the default package. In this setup, this means that all source files
  reside in the `zuniq-player/src/main/java` directory.

### Generating the merged source file

The merge source file can be generated by simply executing the following command in the project root directory:

```shell script
mvn package
```

The merged source file will be saved in `zuniq-player/target`.