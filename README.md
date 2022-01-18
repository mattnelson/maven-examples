
POC for https://issues.apache.org/jira/browse/MENFORCER-407

working with 3.0.0-M3
```
mvn validate
[INFO] Scanning for projects...
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Build Order:
[INFO]
[INFO] menforcer407                                                       [pom]
[INFO] one                                                                [jar]
[INFO] two                                                                [jar]
[INFO]
[INFO] ---------------------< io.mattnelson:menforcer407 >---------------------
[INFO] Building menforcer407 1.0-SNAPSHOT                                 [1/3]
[INFO] --------------------------------[ pom ]---------------------------------
[INFO]
[INFO] --- maven-enforcer-plugin:3.0.0-M3:enforce (default) @ menforcer407 ---
[INFO]
[INFO] -------------------------< io.mattnelson:one >--------------------------
[INFO] Building one 1.0-SNAPSHOT                                          [2/3]
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-enforcer-plugin:3.0.0-M3:enforce (default) @ one ---
[INFO]
[INFO] -------------------------< io.mattnelson:two >--------------------------
[INFO] Building two 1.0-SNAPSHOT                                          [3/3]
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-enforcer-plugin:3.0.0-M3:enforce (default) @ two ---
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for menforcer407 1.0-SNAPSHOT:
[INFO]
[INFO] menforcer407 ....................................... SUCCESS [  0.264 s]
[INFO] one ................................................ SUCCESS [  0.009 s]
[INFO] two ................................................ SUCCESS [  0.454 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.878 s
[INFO] Finished at: 2022-01-18T16:44:09-06:00
[INFO] ------------------------------------------------------------------------
```

broken with 3.0.0
```
mvn validate -P broken
[INFO] Scanning for projects...
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Build Order:
[INFO]
[INFO] menforcer407                                                       [pom]
[INFO] one                                                                [jar]
[INFO] two                                                                [jar]
[INFO]
[INFO] ---------------------< io.mattnelson:menforcer407 >---------------------
[INFO] Building menforcer407 1.0-SNAPSHOT                                 [1/3]
[INFO] --------------------------------[ pom ]---------------------------------
[INFO]
[INFO] --- maven-enforcer-plugin:3.0.0:enforce (default) @ menforcer407 ---
[INFO]
[INFO] -------------------------< io.mattnelson:one >--------------------------
[INFO] Building one 1.0-SNAPSHOT                                          [2/3]
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-enforcer-plugin:3.0.0:enforce (default) @ one ---
[INFO]
[INFO] -------------------------< io.mattnelson:two >--------------------------
[INFO] Building two 1.0-SNAPSHOT                                          [3/3]
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-enforcer-plugin:3.0.0:enforce (default) @ two ---
[WARNING]
Dependency convergence error for junit:junit:jar:4.13.1:provided paths to dependency are:
+-io.mattnelson:two:jar:1.0-SNAPSHOT
  +-io.mattnelson:one:jar:1.0-SNAPSHOT:compile
    +-junit:junit:jar:4.13.1:provided
and
+-io.mattnelson:two:jar:1.0-SNAPSHOT
  +-junit:junit:jar:4.13.2:compile

[WARNING] Rule 0: org.apache.maven.plugins.enforcer.DependencyConvergence failed with message:
Failed while enforcing releasability. See above detailed error message.
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for menforcer407 1.0-SNAPSHOT:
[INFO]
[INFO] menforcer407 ....................................... SUCCESS [  0.270 s]
[INFO] one ................................................ SUCCESS [  0.462 s]
[INFO] two ................................................ FAILURE [  0.045 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.926 s
[INFO] Finished at: 2022-01-18T16:44:35-06:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-enforcer-plugin:3.0.0:enforce (default) on project two: Some Enforcer rules have failed. Look above for specific messages explaining why the rule failed. -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoExecutionException
[ERROR]
[ERROR] After correcting the problems, you can resume the build with the command
[ERROR]   mvn <args> -rf :two
```
