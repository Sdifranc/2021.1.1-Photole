# Application

An **Application** is the means to create a specific IIoT solution. Using the DevBox it is possible to create one or more applications; each of these applications can pertain to a different scope, department, project, etc.

For example, if a manufacturing company wants to optimize asset management using DAC, it can create an application that gets data from the asset, obtaining real-time analysis and predicting failures or maintenance. Each application can be built using one or more pages and functionality that can be configured and arranged to deliver data and tools according to the business users’ requirements.

DAC contains an existing demo application that you can use to understand how a simple application is built. Please refer to the Starter Kit to find out more about the Decisyon Reference App.

All the objects of the DAC-DS environment -- dimensions, cubes, metrics, and reports -- are created within an application. The objects of an application cannot be used by another application.

In addition to defining descriptive parameters during the application creation phase, users must associate the data warehouse to which dimensions and cubes will be mapped.

The data warehouse may reside both on the same instance of the Data Model to which it is connected, and on a remote data source.

A DAC application cannot share the objects contained within it: access to those objects is only permitted to users associated with the applications.

Functions are also available to deploy applications, which lets you:

* manage an application on different environments, for example, to manage a production or test application, rather than a development applicationcopy and then synchronize objects belonging to different applications \(however, objects created within applications belong exclusively to the applications\)

### Create Application

DAC applications are created from the **Manage Application** window, opened from the menu item:

**File &gt;&gt; Manage Application**

A wizard, will show you all the existing applications on the left. The wizard will also allow you to create a new app from scratch. As shown in the figure below, you create an application by defining the descriptive parameters and the data warehouse association parameters.

![](../.gitbook/assets/image%20%2810%29.png)

You create an application by defining the fields indicated in the figure above:

* **Application name:** name of the application, used by DAC and by DAC to identify the application
* **Description**: a description associated with the application \(optional\)
* **Default DB Schema**: select the database schema that contains the data used for the analysis
* **Open this application at login:** if selected, the application is opened at the next login

### Opening Decisyon App Composer

A DAC application is a set of different objects and functions that you bring together to create the functionality you need. For example, an application contains pages and a rules schedule which are configurable.

The Welcome Screen is the first and central part of DAC-DS where the developer has instantaneous access to the main and most frequent functions used to create an application.

![](../.gitbook/assets/image%20%2841%29.png)

The **Recently used** table shows the latest edited objects, in chronological order. Select one of these to directly open its edit window. The detailed information below is available for each object.

* **Name:** component name.
* **Type:** Component type \(e.g. Report, Metric, Page…\).
* **Last Edit:** date and time of the last edit.
* **User:** User that made the last edit.

The **Shortcuts** section contains direct links for access to:

* **Page designer:** for the creation of a new Page.
*  Rule Setup: for the creation of new rules.
* User management: for the creation and management of the users.
* Group management: for the creation and management of the groups.
* Deploy Application: access to the wizard to execute the deployment.

In the **Help Quick Links** section links are available to access DAC documentation:

·        **Getting Started:** tutorials that explain how to create a new application.

·        **Design Studio User Manual:** access to the Developer manual \(this one\)

·        **DAC User Manual:** access to the end user manual.

When DAC is opened, information about the connection is shown at the bottom:

* **User:** Connected User.
*  **Connection:** Data Model, in terms of Hostname and Database.
* **Application:** Application loaded.

\*\*\*\*

![](../.gitbook/assets/image%20%2824%29.png)



### The Toolbar

The DAC-DS toolbar is shown in the following figure:

![](../.gitbook/assets/image%20%2811%29.png)

Once the application is loaded, a first line toolbar is enabled. Once a report is opened, two more toolbar lines are enabled, which show the functions that can be applied to the report.

As the mouse moves over a button, the tooltip is enabled, providing a short description of the associated function as described below:

|  |  |  |
| :--- | :--- | :--- |
| **1** | Reports Catalog |  |
| 2 | Report Editor  |  |
| 3 | Dimension management \(see Dimensions\) |  |
| 4 | Cube management \(see Cubes and measures section\) |  |
| 5 | Metric Management \(see Metrics\) |  |
| 6 | Direct filters management \(see Direct Filters\) |  |
| 7 | Range filters management \(see Range filters\) |  |
| 8 | User filters \(see User filters\) |  |
| 9 | Indicator Designer \(see Indicator Designer\) |  |
| 10 | Page Designer \(see DAC Design page\) |  |
| 11 | Opens widget designer on DAC \(see DAC Design Page\) |  |
| 12 | Scheduler,  \(see Scheduler\) |  |
| 13 | Rule setup \(see Ruke\) |  |
| 14 | Data Load via Report \(Data load via Repor**t** \(DLR\)\) |  |
| 15 | Object Explorer \(see Managing Application Objects\) |  |
| 16 | Online Help Search Box **\(**see Online Help\) |  |

### Object Dependencies

You can see the dependencies of DAC\_DS objects through the **Dependencies** menu item, enabled by right-clicking the mouse in the management windows.

![](../.gitbook/assets/image%20%2812%29.png)

Selecting the **Dependencies** item enables the window displayed at the bottom.

You can request two types of dependency:

* **Object That use ‘…’:** list of objects that use the selected object \(in the figure above, where, for the "Act Vs Bdg" indicator, all the Pages that use it are listed\)

![](../.gitbook/assets/image%20%2836%29.png)

* **Object used by ‘…’:** list of objects used by the selected object \(see figure below\). For each selected object, the right side of the dependencies window shows summary information for the selected object.

![](../.gitbook/assets/image%20%2815%29.png)

