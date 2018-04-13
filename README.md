# MyProject
This is my private webapp to practice tools and techniques.

1. Maven
- maven compile
    - erzeugt target Folder, mit Subfolder classes, in diesem befinden sich die kompilierten .class Files 
    - Problem 1:
    `[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!`
        - Lösung: Encoding muss in pom.xml festgelegt werden:
    `<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>`
    - Problem 2: 
    `[ERROR] Source option 5 is no longer supported. Use 6 or later.`
        - Lösung: Spezifiziere Java Version für source und target explizit in pom.xml: 
    `<maven.compiler.source>1.8</maven.compiler.source>
     <maven.compiler.target>1.8</maven.compiler.target>`

