# MyProject
This is my private webapp to practice tools and techniques.

##Git
- ändere Message eines früheren Commits (vor push!):
    - zeige die letzten n commits: `git rebase -i HEAD~n` 
    - ersetze `pick` durch `reword`
    - gib neue message ein



##Maven
###Goals
###### `mvn compile`
   - erzeugt directory `/target` mit Subfolder `/classes`, in diesem befinden sich die kompilierten Files (.class) 
   - Problem 1:
    `[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!`
       - Lösung: Encoding muss in pom.xml festgelegt werden:
    `<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>`
   - Problem 2: 
    `[ERROR] Source option 5 is no longer supported. Use 6 or later.`
        - Lösung: Spezifiziere Java Version für source und target explizit in pom.xml: 
        `<maven.compiler.source>1.8</maven.compiler.source>
     <maven.compiler.target>1.8</maven.compiler.target>`
###### `mvn package`
   - erzeugt .jar in directory `/target`
   - Inhalt des jars ansehen: `jar -tf gardener-1.0-SNAPSHOT.jar`
    
###### `mvn install`
   - installiert .jar und pom.xml in `.m2/repository`
    
    
