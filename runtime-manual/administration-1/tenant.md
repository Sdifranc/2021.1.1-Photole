# Tenant

## What is a Tenant?​

The segregation of users by Tenant, unlike that by groups, allows to create a more hierarchically structured group.

Users, Administrators and Users Administration can be defined in a tenant.  
Users created in the DAC are automatically associated with a default Tenant. Then they are associated with specific Tenants.

Any users could be associated to no Tenant or to one or more Tenants. If no Tenant is selected during user creation or modification then the user created or modified will be assigned to no Tenant.

In the discussion widget it’s possible to mention users belonging to, at least, one of the tenant the writer belongs to. The user that are not listed in any tenant are visible only if the discussion author does not belong to any tenant too.  


Watch the video for a brief overview of the tenants:

{% embed url="https://dac-docs.s3-us-west-1.amazonaws.com/3.Ludwig/Tenant/TenantOverview.mp4" %}

\*\*\*\*

Administrator and Business User grants :

* **Administrator Grants:**
  * An Administrator manages all existing Tenants and all existing users.
  * An Administrator manages all Users’ Attribute. A User Attribute is defined for any users, regardless of the Tenant he is associated to.
  * An Administrator is able to create new Users and Administrators and can associate them to any Tenants he wants or no Tenants.
  * An Administrator can move Users and Administrators to any Tenants he wants or can remove them from all Tenants they are associated to.
* **Business User Grants:**

  * Any user have all Users’ Attribute defined in the Users’ Attribute section, regardless of the Tenant he is associated to
  * A User can belong to one or more Tenant.
  * A User can set a default tenant and change it during the session.

## Who manages the tenants​

### Tenant Management by scoop

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Scope</b>
      </th>
      <th style="text-align:left"><b>Create Tenant</b>
      </th>
      <th style="text-align:left"><b>Modify Tenant</b>
      </th>
      <th style="text-align:left"><b>Delete Tenant</b>
      </th>
      <th style="text-align:left">
        <p><b>Create</b>
        </p>
        <p><b>User</b>
        </p>
      </th>
      <th style="text-align:left"><b>Assign Scope to New User</b>
      </th>
      <th style="text-align:left"><b>Assign Tenant to new User</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">All Tenant Administration</td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>All Tenant</p>
      </td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>All Tenant</p>
      </td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>All Scope</p>
      </td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>All Tenant</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Tenant Administration</td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>Only the tenants he is associate to</p>
      </td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>Only the tenants he is associate to</p>
      </td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>Only:</p>
        <ul>
          <li>None</li>
          <li>Users Administration</li>
          <li>Tenants Administration</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>(Only the tenants he is associate to)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Users Administration</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>Only:</p>
        <ul>
          <li>None</li>
          <li>Users Administration</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>Yes</p>
        <p>(Only the tenants he is associated to)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>None</b>
      </td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
    </tr>
  </tbody>
</table>

### Tenants users’ management by scope

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Scope</b>
      </th>
      <th style="text-align:left">
        <p><b>Create</b>
        </p>
        <p><b>User</b>
        </p>
      </th>
      <th style="text-align:left">
        <p><b>Modify</b>
        </p>
        <p><b>User</b>
        </p>
      </th>
      <th style="text-align:left">
        <p><b>Delete</b>
        </p>
        <p><b>User</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Scope</b>
      </th>
      <th style="text-align:left">
        <p><b>Create</b>
        </p>
        <p><b>User</b>
        </p>
      </th>
      <th style="text-align:left">
        <p><b>Modify</b>
        </p>
        <p><b>User</b>
        </p>
      </th>
      <th style="text-align:left">
        <p><b>Delete</b>
        </p>
        <p><b>User</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>All Tenant Administration</b>
      </td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Tenant Administration</b>
      </td>
      <td style="text-align:left">Yes (but he can only associate him to the tenants he is associate to or
        no Tenant)</td>
      <td style="text-align:left">Yes (in the Tenants he is associate to or no Tenant)</td>
      <td style="text-align:left">Yes (in the Tenants he is associate to or no Tenant)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Users Administration</b>
      </td>
      <td style="text-align:left">Yes (but he can only associate him to the tenants he is associate to or
        no Tenant)</td>
      <td style="text-align:left">Yes (in the Tenants he is associate to or no Tenant)</td>
      <td style="text-align:left">Yes (in the Tenants he is associate to or no Tenant)</td>
    </tr>
  </tbody>
</table>

## How to create a new Tenant

To create a new tenant, access the Users Administration section.

Tenants can only be created by users who have an “All tenants administration” or “Tenants administration” scope. All the users belonging to the Tenant are shown in the tenant management panel. After creating the tenant the users can be associated to it.

## How to delete a Tenant

Tenants can only be removed by users who have a scope of type:

* **“All tenants administration”:** is able to delete all Tenant regardless of whether they belong to them or not.
* **“Users Administration” and “Tenants administration”:** is able to delete Business User belonging to Tenants he manages, Business Users belonging to other Tenants \(no Tenant excluded\) won’t be delete.

When the tenant is deleted, the users associated with it are automatically assigned to “No Tenant” if not assigned to other tenants.

### 

