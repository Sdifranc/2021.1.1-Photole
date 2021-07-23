# Users Administration

In this video you will learn how to control user creation their settings.

{% embed url="https://dac-docs.s3-us-west-1.amazonaws.com/3.Ludwig/10.Users/CreateUser.mp4" caption="" %}

## **Users Scope**

The users created within DAC can be associated at different scopes:

* **All Tenants Administration:** can create/modify/delete users associated to any Tenants or no tenant. He can assign to users he managed “All Tenants Administration” or “Tenants Administration” or “Users Administration” or “None” scope. He can’t create an Administrator user or promote as Administrator an existing user.
* **Tenants Administration:** he is able to modify only Tenants he is associated to. He can create/modify/delete users associated to tenants he is associated to. He can assign to users he managed only “Tenants Administration” or “Users Administration” or “None” scope. He can assign users to Tenants he is associated to. He can’t create an Administrator user or promote as Administrator an existing user.
* **Users Administration** \(NO Administrator\)**:** but he can create, modify, eliminate users associated to the Tenants he is associated to. He can assign to users he managed “Users Administration” or “None” scope. He can assign users to Tenants he is associated to. He can’t create an Administrator user or promote as Administrator an existing user.
* **None** This is the basic user that does not have administration capabilities.

Administrators act like they have “All Tenants Administration” scope assigned even though they do not have this scope assigned. Furthermore they can create an Administration user or promote to Administration an existing user.

