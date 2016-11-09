## Maven Repository for AgentWise

This repository contains dependencies needed in different projects from the AgentWise research group.

## Installing a new package
- Generate the needed jar files, including jar files for source and javadoc. How to generate such files is outside the scope of this README.
- Include the jar files using the following command (the command below uses  SwarmView as an example) :
    mvn install:install-file \\
    -DgroupId=io.github.agentwise \\
    -DartifactId=swarmview \\
    -Dversion=1.0-SNAPSHOT \\
    -Dpackaging=jar \\
    -Dfile=SwarmView-1.0-SNAPSHOT.jar \\ 
    -Dsources=SwarmView-1.0-SNAPSHOT-sources.jar \\
    -Djavadoc=SwarmView-1.0-SNAPSHOT-javadoc.jar \\
    -DlocalRepositoryPath=.

- Update the maven index
    ./update_index.sh

- Commit and push your changes to github
