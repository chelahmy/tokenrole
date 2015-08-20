# tokenrole
**Token-Role Access Control** is a Drupal 7 module that allows Drupal to extend its access control to external sub-systems. These sub-systems are usually not stand-alone. Implementing user management on sub-systems will trigger usability issues since they are integrated with other systems which already have their own user management. Users are not expecting to sign in into sub-systems while they are already signed in into the main system. Many web services are sub-systems which can entrust Drupal for their user management.

## How does it work?
![tokenrole-diagram](http://camar.xyz/sites/all/modules/tokenrole/tokenrole-diagram.png)
A user will sign in into Drupal and enter a sub-system from within Drupal. The sub-system is integrated seemlessly into Drupal where the user will barely notice. Drupal will send a user access token to the sub-system, which in turn will be used by the sub-system to query Drupal for the user's roles. The sub-system will refer to the assigned roles to limit the user access into itself. Usually the sub-system will implement access permission by roles.

The Token-Role Access Control module was initially implemented to allow Drupal integration with [Camar](http://camar.xyz) Maps and WMS.
