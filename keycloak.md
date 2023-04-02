# Keycloak

#### How to remove resource_access from the token in keycloak clients:

1. Resource Access, Realme Access and Audience are related to scopes. So select the specific client which we need to remove the resource_access. Go to the _client-> scope_ and see what scopes are attached with the client. 
2. By Default _roles_ scope will be added or in most of the companies they will be having they own scopes.
3. From checking the Scope, goto left side _scopes->roles->mappers_ and we will be having three mappers by default:
   > audience resolve, realme roles, client roles
4. we need to focus on the client roles for removing the reource_access from token
5. Now Create a new scope and add click on the builts and select the audience resolves and realme roles.
6. Assign the this custom new scope to that client and remove the roles scope.
7. Now when we generate a token we will get the all fields except the resource_access.
8. If we want our custom resource_access in the token, we can use the script mappers.
