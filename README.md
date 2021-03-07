# Baidu social identity providers for Keycloak.

This is Baidu social identity providers library for [Keycloak](https://www.keycloak.org/) server.
With this library you can log in into Keycloak via [Baidu](https://www.baidu.com)

## Keycloak versions

It was tested against Keycloak versions:
+ 5.0.0
+ 12.0.4

## How to use it

To install this library manually, you could follow [instruction](https://www.keycloak.org/docs/latest/server_development/index.html#registering-provider-implementations) with a few extra steps.

Here's steps:

1. Build project from source or download release file.
2. Copy `keycloak-social-baidu-VERSION.jar` to `KEYCLOAK_HOME/standalone/deployments`.
3. Copy files from `resources/keycloak/theme/base/admin/resources/partials` to `${keycloak.home.dir}/themes/base/admin/resources/partials`

