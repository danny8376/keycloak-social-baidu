# Baidu social identity providers for Keycloak.

This is Baidu social identity providers library for [Keycloak](https://www.keycloak.org/) server.
With this library you can log in into Keycloak via [Baidu](https://www.baidu.com)

## Keycloak versions

It was tested against Keycloak versions:
+ 5.0.0

## How to use it

To install this library manually, you could follow [instruction](https://www.keycloak.org/docs/latest/server_development/index.html#registering-provider-implementations) with a few extra steps.

Here's steps:

1. Build project from source or download release file.
2. Copy `keycloak-social-baidu-VERSION.jar` to `KEYCLOAK_HOME/standalone/deployments`.
3. Get `scribejava-core-6.5.1.jar` from [here](http://central.maven.org/maven2/com/github/scribejava/scribejava-core/6.5.1/scribejava-core-6.5.1.jar). Then install as module into keycloak:
  * Either manually:
```
mkdir -p modules/system/layers/keycloak/com/github/scribejava/core/main
```
Move `scribejava-core-6.5.1.jar` into `modules/system/layers/keycloak/com/github/scribejava/core/main`.
Then add file `modules/system/layers/keycloak/com/github/scribejava/core/main/module.xml` with contents.
```
<?xml version="1.0" encoding="UTF-8"?>
<module xmlns="urn:jboss:module:1.3" name="com.github.scribejava.core">
 <resources>
  <resource-root path="scribejava-core-6.5.1.jar" />
 </resources>
 <dependencies>
  <module name="javax.api"/>
 </dependencies>
</module>
```
  * Or: (theoretically, not tested :-P)
```
KEYCLOAK_HOME/bin/jboss-cli.sh --command="module add --name=com.github.scribejava.core --resources=PATH_TO_THE_JAR --dependencies=javax.api"
```
4. Copy files from `resources/keycloak/theme/base/admin/resources/partials` to `${keycloak.home.dir}/themes/base/admin/resources/partials`

