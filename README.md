Run

    $ mvn clean verify -T4

to see the failure.  This fails 100% of the time for me, but as with any race condition, YMMV.

The error should look like

> [ERROR] Failed to execute goal org.apache.maven.plugins:maven-invoker-plugin:1.10:install (integration-test) on project project-3: Failed to install project dependencies: MavenProject: com.tavianator.minvoker191:project-3:1.0-SNAPSHOT @ /home/tavianator/code/MINVOKER-191/project-3/pom.xml: Failed to install project artifacts: MavenProject: com.tavianator.minvoker191:project-2:1.0-SNAPSHOT @ /home/tavianator/code/MINVOKER-191/project-2/pom.xml: Failed to install artifact: com.tavianator.minvoker191:project-2:jar:1.0-SNAPSHOT: Artifact is not fully assembled: /home/tavianator/code/MINVOKER-191/project-2/target/classes -> [Help 1]
