# Campus Course & Records Manager (CCRM)

## Project Overview
The Campus Course & Records Manager (CCRM) is a **Java SE console-based application** for managing students, courses, enrollments, grades, transcripts, and file operations (import/export, backups).  
It demonstrates **OOP principles, Java NIO.2, Streams, Date/Time API, lambdas, recursion, enums, nested classes, and design patterns (Singleton & Builder).**

---

## Features
- **Student Management**: add, list, update, deactivate, print profiles and transcripts  
- **Course Management**: add, list, search/filter by instructor/department/semester  
- **Enrollment & Grading**: enroll/unenroll students, assign marks, compute GPA, generate transcript view  
- **File Utilities**: import/export CSV, recursive backup with timestamped folders  
- **Console CLI**: menu-driven workflow with loops, switch/case, and jump statements  

---

## How to Run
1. Install **JDK 17** (or newer).  
2. Compile:
   ```bash
   javac -d out $(find src/main/java -name "*.java")
   ```
3. Run:
   ```bash
   java -cp out edu.ccrm.cli.Main
   ```

---

## Evolution of Java (highlights)
- 1995 – Java 1.0 released  
- 1998 – J2SE, J2EE, J2ME split  
- 2004 – Java 5: Generics, Annotations  
- 2011 – Java 7: NIO.2 API  
- 2014 – Java 8: Lambdas, Streams  
- 2017 – Java 9: Modules  
- 2021 – Java 17 (LTS): pattern matching, sealed classes  

---

## Java Editions
- **Java ME**: for embedded/mobile devices  
- **Java SE**: core libraries for standard desktop/server apps  
- **Java EE (Jakarta EE)**: enterprise APIs (servlets, JPA, EJB)  

---

## JDK, JRE, JVM
- **JVM**: runtime engine executing bytecode  
- **JRE**: JVM + standard libraries (for running)  
- **JDK**: JRE + compilers & tools (for development)  

---

## Package Structure
```
edu.ccrm
 ├─ cli/       → Menu & console loop
 ├─ config/    → Singleton AppConfig
 ├─ domain/    → Person, Student, Course, Enrollment, Enums
 ├─ service/   → Interfaces for Student/Course/Enrollment services
 ├─ io/        → ImportExport, Backup
 └─ util/      → Validators, recursion utilities
```

---

## Technical Highlights
- **OOP**: Encapsulation, Inheritance, Abstraction, Polymorphism  
- **Design Patterns**: Singleton (AppConfig), Builder (Course)  
- **Enums**: Semester, Grade with grade points  
- **Lambdas & Streams**: sorting, filtering, GPA distribution  
- **NIO.2**: file import/export, recursive backups  
- **Custom Exceptions**: e.g., `DuplicateEnrollmentException`  
- **Assertions**: used for data invariants (run with `-ea`)  

---

## Sample CSV Data
`test-data/students.csv`
```
id,regNo,fullName,email,dob
s001,REG2025-001,Alice Kumar,alice@example.com,2002-05-12
```

`test-data/courses.csv`
```
code,title,credits,department,semester
CS101,Intro to CS,4,CS,FALL
```

---

## Usage
- Run program → choose from menu: manage students/courses/enrollments, import/export, backup, reports.  
- Backup folders are created with timestamp names.  
- Transcripts show GPA and grades using overridden `toString()`.  

---

## Screenshots
*(to be added: JDK installation, Eclipse setup, program menus, exports/backups)*  

---

## Acknowledgements
This project is built as per the academic requirements for demonstrating Java fundamentals and advanced concepts.
