
POC for https://issues.apache.org/jira/browse/MENFORCER-407

working with 3.0.0-M3
```
mvn validate
[INFO] Scanning for projects...
[INFO]
[INFO] ---------------------< io.mattnelson:menforcer394 >---------------------
[INFO] Building menforcer394 1.0-SNAPSHOT
[INFO] --------------------------------[ pom ]---------------------------------
[INFO]
[INFO] --- maven-enforcer-plugin:3.0.0-M3:enforce (default) @ menforcer394 ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.521 s
[INFO] Finished at: 2022-06-07T18:08:45-05:00
[INFO] -------------------------------------------------------------------------
```

broken with 3.1.0
```
mvn validate -P broken
[INFO] Scanning for projects...
[INFO]
[INFO] ---------------------< io.mattnelson:menforcer394 >---------------------
[INFO] Building menforcer394 1.0-SNAPSHOT
[INFO] --------------------------------[ pom ]---------------------------------
[INFO]
[INFO] --- maven-enforcer-plugin:3.1.0:enforce (default) @ menforcer394 ---
[WARNING]
Dependency convergence error for org.projectlombok:lombok:jar:1.18.24:runtime paths to dependency are:
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-dnsjava:dnsjava:jar:3.5.1:runtime
    +-org.projectlombok:lombok:jar:1.18.24:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-core:jar:5.12.2:runtime
      +-io.fabric8:kubernetes-model-common:jar:5.12.2:runtime
        +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-core:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-rbac:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-admissionregistration:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-apps:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-autoscaling:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-apiextensions:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-batch:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-certificates:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-coordination:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-discovery:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-events:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-extensions:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-flowcontrol:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-networking:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-metrics:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-policy:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-scheduling:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-storageclass:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-io.fabric8:kubernetes-model-node:jar:5.12.2:runtime
      +-org.projectlombok:lombok:jar:1.18.22:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-org.projectlombok:lombok:jar:1.18.22:runtime

[WARNING]
Dependency convergence error for org.robolectric:android-all:jar:12-robolectric-7732740:runtime paths to dependency are:
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-dnsjava:dnsjava:jar:3.5.1:runtime
    +-org.robolectric:android-all:jar:12-robolectric-7732740:runtime
and
+-io.mattnelson:menforcer394:pom:1.0-SNAPSHOT
  +-io.fabric8:kubernetes-client:jar:5.12.2:runtime
    +-com.squareup.okhttp3:okhttp:jar:3.12.12:runtime
      +-org.robolectric:android-all:jar:10-robolectric-5803371:runtime

[ERROR] Rule 0: org.apache.maven.plugins.enforcer.DependencyConvergence failed with message:
Failed while enforcing releasability. See above detailed error message.
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.479 s
[INFO] Finished at: 2022-06-07T18:11:57-05:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-enforcer-plugin:3.1.0:enforce (default) on project menforcer394: Some Enforcer rules have failed. Look above for specific messages explaining why the rule failed. -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoExecutionException
```
