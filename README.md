## beta4


```sh
asdf local maven 4.0.0-beta-4
mvn help:active-profiles -s setting.xml
```

```
[INFO] --- help:3.5.1:active-profiles (default-cli) @ profiles ---
[INFO]
Active Profiles for Project 'com.github.mattnelson:profiles:pom:1.0.0-SNAPSHOT':

The following profiles are active:

 - settings-xml-activeProfiles (source: external)
 - profile_active_from_mvn_config (source: /Users/Shared/DevBuild/code/maven-examples/pom.xml)



Active Profiles for Project 'com.github.mattnelson:module1:pom:1.0.0-SNAPSHOT':

The following profiles are active:

 - settings-xml-activeProfiles (source: external)
 - profile_active_from_mvn_config (source: /Users/Shared/DevBuild/code/maven-examples/pom.xml)
```

## beta5

```sh
asdf local maven 4.0.0-beta-5
mvn help:active-profiles -s setting.xml
```

```
[INFO] --- help:3.5.1:active-profiles (default-cli) @ profiles ---
[INFO]
Active Profiles for Project 'com.github.mattnelson:profiles:pom:1.0.0-SNAPSHOT':

The following profiles are active:

 - settings-xml-activeProfiles (source: external)
 - profile_active_from_mvn_config (source: com.github.mattnelson:profiles:pom:1.0.0-SNAPSHOT)
 - profile_active_from_condition (source: com.github.mattnelson:profiles:pom:1.0.0-SNAPSHOT)



Active Profiles for Project 'com.github.mattnelson:module1:pom:1.0.0-SNAPSHOT':

The following profiles are active:

 - settings-xml-activeProfiles (source: external)
```

