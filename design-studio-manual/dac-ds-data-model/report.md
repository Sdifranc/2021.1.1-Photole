# Report

Reports are tools that allow users to carry out accurate data analysis: it is possible to use cubes and metrics of the application. It will be then possible to request analysis on dimensional levels and metrics for different application cubes, ensuring congruence among elements: dimensional levels and metrics must be linked by at least one cube.

After choosing the desired dimensional levels and metrics for analysis, you can apply filters to restrict the field of observation. Applicable filters are created with the _Direct_ _Filter_ and _Range_ _Filter_ modules, but it is also possible to create filters exclusively for the report.This section describes the functions to **develop reports**. The table lists the main subjects, with a short description and the link to the sub section where they are described.

| **Function/object** | **Description** | **Section** |
| :--- | :--- | :--- |
| Report | Presentation of the report and link to all the functions described in the manual. | Introducing the reports |
| Report creation | Creating a report: assigning metrics, filters and levels, creating exclusive filters. SQL execution and code and associated datamart. Display mode. | Editing reports |
| Report catalog | Saving and opening reports from the catalog. | Report catalog |
| Report publication | Publishing a report and assigning privileges. | Report publication |
| Drill operations | Setting the aggregation of the levels compared to the dimension of pertinence or the layout. _Hierarchy-drill_ setting for the graphs. | Aggregation of levels \(Drill-down /Roll-up\) |
| Query Report | Creating a report by entering a specific query, defined locally or on other data sources. | Report populated with data from SQL query |
| Graphs | Presenting the graph styles available in DAC and their customization. | Graphs |
| Table Layout | Customization of the table layout of the report. | Table Layout |
| Total functions | Applying total functions to reports. | Total functions |
| Excel like | Defining customized total functions in rows/columns/ cells of the report. | Customized totals \(Excel like\) |
| Page-by | Behavior and configuration of the page-bys in reports. | Page-by |
| Drill-through | Configuring and activating the drill-through in reports, to open other reports, Pages or generic URLs, depending on the data of the calling report. | Drill-through |
| Report with prompt | Defining and configuring a prompt on a report, with simple parameters or with a Page. | Report with prompt |
| Exporting reports | Configuration of exporting a report to PDF, Excel \(standard or using customized templates\) or CSV. | Exporting reports |
| Sorting data in a report | Setting the sorting of the data of a report, other than the standard one. | Data sorting |
| Discussions on reports | Enabling a Discussion on specific reports and Pages, used by the web users with the _Social User_ license. | Discussions |
| Additional functions | Customized functions which may be added to the toolbar of the reports in DAC. | Custom functions for reports |
| Other detailed properties | Configuring the other detailed properties, such as the aliases, join, debug, table write, activate-sorting, test parameters, etc. | Other detailed properties of reports |
| Accessing reports from external systems | Defining the URL link which lets you recall a report from other systems, making it also parametric. | Accessing reports from external systems |

## Introduction to Reports

Once the report has been defined, the system generates one or more queries to retrieve the data. Report execution produces a series of supporting tables for intermediate results until the final table is produced with the data requested by the report. This table represents the datamart for the requested analyses.

In DAC, you can define reports populated with data from a SQL query. These reports will define the cubes and dimensions valid exclusively for the current report, which will be integrated with data from BI cubes.

DAC offers a series of functions to increase the effectiveness and efficiency of report analysis, such as:

* mode of data visualization, such as tables and graphs
* customization of the graph or table section
* aggregation of dimensional levels \(so that _navigation_ can be enabled for drill-down and roll-up operations\) and the navigation mode
* definition of standard or Excel-like type totals
* customization of the behavior of levels used as filters \(Page-by\)
* using the report analysis as a filter for other reports, Pages, database queries or as parameters for web-type applications \(Drill-through\)
* inserting a Page as report prompt
* exporting the report, in PDF, Excel or CSV format
* customized sorting of data
* enabling custom functions on the toolbar of the report functions

There are other properties described in the Other detailed report properties section.

The creation of a report involves the selection of levels, metrics, and possibly filters; once the report has been created, it can be customized it in the ways described above, using the Editing Report window.

When a report is open, a second toolbar is enabled, with rapid commands for some of the functions described above \(see the figure below\).

![](../../.gitbook/assets/0%20%286%29.png)

The customization of report properties can take place, not only from the _Editing Report_ window, but also from the _Report Properties_ window which can be opened with the ![](../../.gitbook/assets/1%20%283%29.png) Button.

Reports are saved in a catalog, with a folder system identical to the standards and the logics found in Windows, so that users are working with a familiar interface.

The publication of reports for DAC users takes place through the allocation of privileges both on individual reports and on folders. Published reports can be changed by DAC users, but, when saved, a copy of the published report will be created and placed in the user’s Favorites folder. This ensures that reports published by DAC can never be changed by DAC.

The report display provides a pop-up menu with commands that allow you to directly access the elements that make up the report, such as metrics, levels, totals, etc.

![](../../.gitbook/assets/2%20%287%29.png)

Using the same pop-up menu, you can apply report functions, such as totals, or directly access the properties of the item under consideration.

The generic functions that apply are:

* _**Remove “\[level/metric name\]”**_: remove the level or the metric
* _**Edit “\[level/metric name\]”**_: The window opens of the dimensional \(Step 2 of the wizard\) or metric levels, to allow changes.

If the report is populated by queries, this item is disabled since the levels and the dimensions are not in the application, but exist only for the report.

* _**Enable/Disable span**_: enables/disables the grouping for the same row or column value
* _**Enable/Disable wrap**_: enables/disables the text wrapping, by row, column or header.
* _**Set alias/Remove alias**_ sets/removes the alias for the levels or metrics.

The _**Set alias**_ command is always active and lets you change the alias previously assigned

Example: **Edit Metric**

![](../../.gitbook/assets/3%20%282%29.png)

_The image above shows how you can open the editing window of a single object in the report._

_A right-click with the mouse opens the metrics window, already positioned on the \# of alerts: by clicking on the item: Edit metric "\# of alerts ", you can enter the metrics page to make changes._

## Editing Reports

Reports are created and changed in the _**Editing**_ _**Report**_ window, which is accessed:

As shown in the figure above, the folders in the top left section allow you to choose metrics and filters, both direct and range, that are available on the application. Filters and metrics to associate with the report must have been created earlier, using the corresponding modules for the management of metrics, direct filters and range filters .

You can also define filters for exclusive use by the report, both on the elements of the report itself and on those of the application.

Metrics and filters are selected simply by double-clicking and are then reported in the _**Elements**_ box \(top center\).

![](../../.gitbook/assets/7%20%282%29.png)

In _Type_ the type of metric is selected, whether first level, advanced or composite, then the \(_Name_\) is indicated, while in _Description_ the reference cube for the metric is indicated \(for composite metrics all the cubes of the metrics involved in the formula are specified\).

To change the order of display of the metrics, just click the up and down arrow buttons. To remove a metric from the report, double-click on the corresponding _Type_ field.

In the section at the bottom you’ll find the dimensional levels for the application grouped by cubes, dimensions and hierarchies. This helps users to choose dimensional levels consistent with the multicube analysis. The choice of a level, shared by two or more cubes, can be made on any cube even one that is different from that of the chosen metrics.![](../../.gitbook/assets/8.png)![](../../.gitbook/assets/9%20%285%29.png)

Dimensional levels are inserted directly in the desired layout position, chosen from Page-by, rows or columns. The selection is made by dragging the level onto the desired cell; the level can then be moved from one cell to the other by dragging it to the new location. To delete a level from the report just drag it to the central selection area.![](../../.gitbook/assets/10.png)

By right clicking the cells which represent the rows, columns or page-by, respectively, you can add 10-cell blocks.

Metrics must be grouped and connected to a single axis. For example, you cannot have one metric on a row and another one in a column.

The Metrics element ![](../../.gitbook/assets/11%20%287%29.png) groups the metrics. These are initially placed in columns. Later they can be moved through drag & drop operations like those for dimensional levels.

The folders in the top center section provide access to **properties** that can be customized by users:

* the _**Properties**_ _folder_ contains the generic properties, subdivided by groups
* the _**Page**_-_**By**_ folder contains the properties related to the levels/ metrics positioned at the top of the report
* in the _**Drill-Through**_ folder, you can access the properties that define the links associated with the levels/metrics of the report
* in the _**Prompt**_ folder, you can define the prompt associated with the report \(and displayed in DAC\)
* the folder _**Chart**_ groups all the properties related to the formatting of the graphs.

On the right- side, there are command buttons for:

* ![](../../.gitbook/assets/12%20%282%29.png)the execution of the report
* the SQL code generated by the report, with or without formatting of SQL commands
* **validation** of the report structure \(and not the query generated\), to verify the existence of the elements introduced in the report \(levels, metrics, and filters\)
* the opening of another report \(_**Open**_\)
* saving the report \(_**Save**_\)
* saving a copy with a different name \(_**Save**_ _**as**_\)
* closing the dialog without making any changes \(_**Cancel**_\)

You can open or save the reports on the catalog.

**Note:** If a Report is opened which is already being edited by another user, it will be possible to use it but in read only mode, and saved with another name.

When the user accesses a report in read only mode, for the entire duration of the usage session he can save the report as new, without overwriting the existing report. To be able to have the writing rights, he must access the report only when it is not being edited by another user.

### Execution

Clicking the Execute button starts the execution of the report, i.e. of the corresponding queries generated by the report.

During execution the system displays a window, where:

* in the _**Step View**_ folder the queries executed for the creation of the final report datamart are listed.
* in the _**Sql View**_ folder, the SQL code of the query being executed at that moment is displayed.
* the _**Statistics**_ folder, created at the end of the execution, shows a summary of information on the use of the automatic or absolute cache, on the date the report reference was created in the cache.

![](../../.gitbook/assets/13%20%282%29.png)

The first progress bar shows the report execution in real time, while the second bar shows the execution of any advanced metrics functions.

When execution is completed, the Close button is activated, which closes the window. If an error occurs, execution is stopped and the Edit button is activated, allowing the user to reopen the _Editing_ _report_ window_._

A specific property allows you to set the maximum execution time of the report:

* from the report property, in the Main _group_, we access the window of the **advanced** property
* _**maxExecTime**_ defines the minimum time \(in minutes\) for report execution, \(the default is -1, indicating the absence of controls on loading time\).

### SQL Code Generated

![](../../.gitbook/assets/14.png)The SQL code generated by DAC and executed in DataWarehouse is displayed in the _**Query Viewer**_ window, opened using one of the buttons of the _Editing Report_ window.

The SQL code is the same shown in the SQL View folder, during the execution.

The difference between the two buttons is that the first gives a colored formatting to the instructions, and the second one does not.

![](../../.gitbook/assets/15%20%283%29.png)

The generated code exists in the creation of temporary tables to hold advanced and composite metrics, until the final datamart containing all report data is created.

A specific property allows you to define a logical condition to be applied as a ‘HAVING’ clause to the query of final selection of the repository:

* from the report property, in the _Main_ group, we access the window of the **advanced** property
* _**having-clause**_ \(_SQL_ _-custom_ group\) opens a pop-up in which you type the ‘having_**’**_ condition_._

### Custom filters

The filters for exclusive use on the report can be defined:

* On the elements of the report \(_**View Filter**_\), therefore applied AFTER the execution of the report, directly on the datamart which is the result of the query to the data warehouse
* On the dimensional levels of the application \(_**Custom**_ _**Filter**_\), therefore applied DURING the query to the data warehouse

These filter categories are associated only with the report and cannot be reused or saved.

To define a custom filter, in the Custom Filters folder, place the cursor on _Filters_ and right click to open the menu. There will be two items on the menu: one creates a Custom filter and the other creates a View Filter.

![](../../.gitbook/assets/16%20%285%29.png)

Selecting either item opens a window to define the filter condition. This window has the same functions as the one for direct filters _\(\_see \_Presentation Administrator, Filters section\)._

Choosing _**Define Custom**_ _**Filter**_ allows you to choose any level in the application. If you choose levels found in the report, the condition will be applied during the query and not afterwards.

![](../../.gitbook/assets/17%20%287%29.png)

The option _**Define View Filter**_ opens the filter window, restricting level selection to those levels which are in the report. Note that in Define View Filter, you can also set conditions on the metrics of the report itself.

![](../../.gitbook/assets/18%20%284%29.png)

In defining a _View Filter_, you can apply the condition by selecting the property _**Apply as “Having” condition**_.

In this way the system will apply the filter on the aggregated values in drill, rather than on the datamart \(see the following example\). The property is enabled only if metrics, rather than levels, are selected.

Once created, the filter appears in the _Elements_ area: to change it, just select it and select _**Edit**_; to delete it, double-click on the row corresponding to the filter \(in _Type_\).

![](../../.gitbook/assets/19%20%287%29.png)

Parameters can be used in Custom Filters \(both Custom and View\):

* defined in a dashboard
* user parameters

For details, see _Presentation Administrator._

Example: View Filter in HAVING

![](../../.gitbook/assets/20%20%285%29.png)

_Report N°1 presents the Product Family level which aggregates the Product level, while the metric calculates sales quantities._

_A View Filter is applied on the Sales Qty metric to filter values greater than 9,000,000 and the HAVING flag is enabled._

_In report N°2 the filter has been applied; it can be seen that only product families meeting the filter condition are displayed._

_If the same condition is applied with HAVING disabled, the report would not show any result: no product \(detailed data from the datamart\) has values for Sales Qty greater than 9,000,000._

### Report Datamart

The report datamart is a temporary table where the information in the report is stored: all displays of the report take their data from this table.

The table is created on report execution and, if default enabling is left on, it is saved in cache.

This table is structured as follows:

* For each level found in the report two columns are created: one for the key and the other for the description
* For each first level metric and advanced metric a corresponding column is created
* For each composite metric, columns to contain the component metrics are created.

### Display Mode

DAC allows users to display reports in one of the following modes:

* Table
* Graph
* Document \(with both graph and table formats\)

The display can be defined both with the report function bar, found on the main screen, and from the specific properties of the report.

![](../../.gitbook/assets/21%20%282%29.png)

In the top section there are three buttons enabling the display of the report in the different modes \(Table, Graph, Document\).

You can browse the report pages using the page buttons, indicated by arrows. The arrow buttons, on the left, just above the report, allow two different types of shift: horizontal shift \(of columns\) and vertical shift \(of rows\) The single arrow allows you move one page forward or backward; the double arrow allows you to access the first or last page.

On the right of the Rows and Cols labels, respectively, the row total and the column total for the displayed report are indicated in round brackets. You can set the number of rows and columns displayed on the screen by selecting a value from the drop-down menu next to the two labels.

![](../../.gitbook/assets/22%20%284%29.png)

![](../../.gitbook/assets/23.png)The button at the top on the right side closes the main window from the layout of the last executed report.

On the bar, at the bottom of the report window, you’ll find information on:

* name of user connected in DAC \(_**User**_\)
* the server to which the user is connected \(_**Connection**_\)
* the application \(_**Application**_\)
* the report name \(_**Report**_\)

The display mode, chosen during editing, requires setting the **publish** **Type** property for the report \(**Main** group **Properties** section\), where the three available display formats are listed and can be selected.

The _Crosstab_ value, the system default, allows users to display the executed report with a table structure.

The _Graph_ value, set by the user, allows you to display the executed report with a graph structure.

The _Document_ value, set by the user, allows users to display the executed report with both structures, table and graph, on the same page.

#### Table Visualization

The _**Table**_ format allows you to display all dimensions, metrics, and any page-by set during the report editing phase in a table structure.

![](../../.gitbook/assets/24%20%283%29.png)

The headers indicated on the first row refer to the levels \(or metrics\) on the rows.

If the levels are grouped in drill, the header will only include the parent level.

![](../../.gitbook/assets/25%20%281%29.png)

The headers related to levels or metrics placed in columns are displayed only if more than one element is present: the most detailed element always remains without a header

![](../../.gitbook/assets/26%20%283%29.png)

In the report in the figure two elements have been placed in the column: YEAR level and the axis of the metrics. The detailed element \(in this case the axis of the metrics\) does not have a header, while the one for the YEAR level is visible.

These settings placed in rows and columns may be customized in DAC by using the formatting bar, which is described in the next paragraph.

#### Graphical Display

#### ![](../../.gitbook/assets/27%20%282%29.png)

* The _**Graph**_ format is of the type shown in the figure. Also the graph format allows users to display all dimensions, metrics and possibly page by set during report editing. _X axis_ is used for the row elements, the _Y-axis_ for metric values.

If a page-by has been placed in the report, you can also filter data from the display mode in graph format.

#### Document view

The _**Document**_ format allows you to display the report in both formats on the same page: graph \(at the top\), table \(at the bottom\). The separation line can be moved to make one area \(graph or table\) bigger or smaller with respect to the other.

The two arrows ![](../../.gitbook/assets/28%20%282%29.png) at the beginning of the separation line are used to hide the graph \(top arrow\) or the table \(bottom arrow\).![](../../.gitbook/assets/29%20%281%29.png)![](../../.gitbook/assets/30.png)![](../../.gitbook/assets/31%20%283%29.png)

The two selection boxes Rows and Cols, located on the right just above the report, allow you to choose and set the number of rows and of columns, per page, in which to divide the report in table format, which determines the number of pages needed to display the extracted data.

## Report Catalog

Reports are organized in a catalog where they are saved and from which it is possible to open them.

You can open a report from the catalog by clicking on File &gt;&gt; Open report or directly from the toolbar with the ![](../../.gitbook/assets/32.png) Button.

![](../../.gitbook/assets/33%20%282%29.png)

To save a report click on the File &gt;&gt; Save menu item or &gt;&gt; Save as or use the corresponding commands on the toolbar ![](../../.gitbook/assets/34%20%281%29.png).

Both operations open the catalog on the folder last accessed by the user:

* to open a report just double-click to select it or click on the _**Ok**_ button;

![](../../.gitbook/assets/35%20%281%29.png)

* to save a report just type its name in the bottom panel, after choosing the folder where it should be stored.

![](../../.gitbook/assets/36%20%281%29.png)

During the installation of DAC, the system creates two folders in Root:

LOCAL used as working folder \(reports in this folder cannot be published\)

Users\* which includes all the users’ favorite folders, in the DAC catalog. The folder name is just the _Username_ of the user himself.

![](../../.gitbook/assets/37%20%283%29.png)

The top right button allows you to create new main folders; these can then be published on DAC, defining the associated privileges.

![](../../.gitbook/assets/38%20%281%29.png)

_Buttons for the operations of cut, copy, paste and delete are especially useful to move reports from one folder to the other \(because drag & drop is not enabled\)._

The bottom panel contains the report search functions.

![](../../.gitbook/assets/39%20%283%29.png)

## Report Publication

To publish a report you must:

1. Create a main folder, in the catalog Root, where the reports to be published are placed
2. Open the pop-up menu, in the new folder, and click on Privileges
3. Choose the privilege to assign to all users \(_**Default**_ _**Privilege**_\):
   * no publication \(_Access_ _denied_\): folder and relative reports are not published on DAC
   * the folder and the reports are published on DAC \(_Read_\)

![](../../.gitbook/assets/40%20%283%29.png)

If the publication of a folder was denied \(_Access denied_ _as_ default privilege\), it is possible to give specific users, or user groups, full access to the folder:

* just select _Read_ for these users or user groups.
* If a user is part of more than one user group, with different authorization levels, the highest access privilege will be granted.

You can extend or superimpose the privileges for one folder to all subfolders \(and not to the reports: in order to do this, select the Extend to subfolder flag.

This choice is not permanent and if new folders are created, a new request must be made.

Each time a main folder or a subfolder is created, DAC sets the privilege to _Access denied_, so that you can decide which users should be given access to it at a later time. The same happens when a folder is created by a cut and paste operation: the privilege for the copied folder changes to _Access denied_.

Reports created \(or copied and pasted\) in a folder always have _Read_ set as default privilege.

## Drill-Thtough

A Drill-through can recall an object from a report such as:

* Another report
* A Page
* An App
* A Web Page

The drill-through \(in short DT\) can be activated both from dimensional levels and from report metrics. You can also associate it with the report for opening a Page, including some forms, from which you can “command” the calling report, i.e., to filter it in real time according to the choices made in the forms \(Top-type DT\).

It is possible to set more than one DT \(up to 25\) for the same report, each of which can execute different actions.

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/1.jpg)

During DT there is a [parameter transfer](https://docs.decisyon.com/report-design-studio/#_Parameters_transfer) from the report to the _called_ object: every time the opening parameters are modified, the object will not be taken by the user session cache, but it will have to be _re_–_executed_ by accessing the Data Model, of cache or on the data, according to the settings.

Once activated the user displays a predefined icon \(only in DAC\). The system allows you, however, to set custom icons.

A DT is activated by setting the properties of the **Drill-through**, group in the report editing window:

1. in _**drill-groups**_, you can define the number \[_n\]_ of DTs that you want to set in the report; for each of them, the properties _activatedrillthrough\[n\]_ are repeated_;_
2. you can activate one of the DTs set by selecting the corresponding _**activate drillthrough\[n\]**_ property, each of which enables the specific properties, needed for configuring:
3. the [DT activation mode](https://docs.decisyon.com/report-design-studio/#_Modalit%C3%A0_di_attivazione) \(_drill-through_\), that tells us whether it is on a specific report level/metric or on the whole report;
4. the [DT target object](https://docs.decisyon.com/report-design-studio/#_Oggetto_destinazione_del_1) \(_open ActionType_\);
5. the [page opening mode](https://docs.decisyon.com/report-design-studio/#_Modalit%C3%A0_apertura_pagina);
6. the setting of an[image and description associated with the DT;](https://docs.decisyon.com/report-design-studio/#_Image_and_description)
7. the [parameters transfer](https://docs.decisyon.com/report-design-studio/#_Parameters_transfer)

**Note:** _In a graphic display of a report, you can open the DT by clicking on the graphic element \(bar, join point on rows or areas\). Only one DT is open and it is the first one defined._

### **DT Activation Mode**

You can activate a DT both from a specific dimensional level or report metric, and directly from the report. This mode also allows you to “command” the calling report. From the property:

* _**drill-through**_, a pop-up opens with the list of levels/metrics or the items relating to the report \(_Top mode_\).

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/2.jpg)

The Top modes available are as follows:

* allows you to open the DT and pass the parameters of the _calling_ report to the new page;
* the _calling_ report is filtered, in real time, according to the choices made on the _called_

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/3.jpg)

In DAC this setting activates in the report a menu with the parameter values, chosen in the _called_ object

* **Show on:** Allows you to define where drill through has to be rendere
  * **Drill-through-position:**allow to select the level of the report on which to activate the DT

**Note:** _The calling report will include parametric filters, on parameters with names corresponding to those set in the object open in DT. See the following example._

**Step 1: drill-through a**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/4.jpg)

_Dashboard \(MainFilter\) which includes two form objects \(a Select element and a Checklist-type one \) is created with the list of products and clients: these will be later used to filter the calling report. The name given to the components \(in the form-name property\) is the parameter by which the report is filtered:_

_?skuid? and ?cust?_

**Step 2: drill-through a**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/5.jpg)

_We define a report including also the two levels, product and client, on which we define the two custom filters, of_ _parametric-type: the level field key is connected \(operator IN\) to the parameter defined in the Page. The parameter will be inserted manually. Remember to use question marks on both sides._

_You can activate the DT on the report \(activateDrillThrough1\) by setting the following:_

* _in the drill-Through property, choose the item_
* _in openActionType choose the item for the opening of a Page \(Page_ _Page\)_
* _in the Page property, choose the Main Filter Page, created in step 1_
* _in the drillThroughDesc property you can set the “Launch Main Filter” text as the description._

**Step 3: drill-through a**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/6.jpg)

_Accessing the report on DAC, the DT defined in the previous step is placed at the top:_

* _the symbol of the DT is displayed, along with the alternative description and a field with the text ._

_Clicking on the DT link opens the associated Page MainFilter_

_The item selection, both from the menu and from the list, begin the update of the calling report, to which the filters for product and client are applied._

_In addition, you can insert a Submit type button in the Page, so that the choices made are applied only after this has been clicked._

**Step 4: drill-through a**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/7.jpg)

_The values taken by the parameters are reported in the text field next to the DT._

### **DT Destination Object**

The settings for the object open by a DT are chosen with the property _**openActionType**_:

* **REPORT –** _–_ Opens another report.

This item enables the property:

* _**report**_ for the selection, in the catalog, of the report to open \(see [example](https://docs.decisyon.com/report-design-studio/#ExampleDT)\)
* **PAGE** – Opens a Page.

This item enables the property:

* _**Page**_ to select one of the Pages created with Page Designer \(see [example](https://docs.decisyon.com/report-design-studio/#_Drill-through:_Custom_SQL)\)
* **OPEN URL** – Opens a page or web application, using the report parameters.

This item enables the property:

* _**drill-through-URL**_ where you specify the URL page address \(see [example](https://docs.decisyon.com/report-design-studio/#_Drill-through_su_un_report)\).

**Example DT to a Report**

**Step 1:drill-through on a Report**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/8.jpg)

_We associate the drill-through with the level MONTH \(drill-through property\) and do NOT select the option_ _openNewWindow; the destination report \(“01 – Test pageby shared”\) will be, then, open in the same page as the initial one._

_NOR do we select the apply-sel-as-filter property, therefore the values, exported through drill-through, will not affect any filter on the destination report data._

**Step 2: Drill-through on a Report**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/9.jpg)

_From the DAC, the initial report will display then the drill-through on the values of the level MONTH. If you click to open one of them, the target report will be displayed in the same page as the initial one._

Example – DT to a Page

**Step 1: Drill-through to a Page**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/10.jpg)

_We associate the drill-through with one of the report dimensional_ _levels \(Project in this case\) using, as before, the drill-through property. We ask the system to open, when we click on the drill executed from the Web module, a Page \(Project Details\) in a new page measuring 650 by 600 pixels._

_Furthermore, we specify that we want to filter the data of the target page \(apply-sel-as-filter\) with a “view-filter”, using the values exported from the report._

**Step 2: Drill-through to a Page**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/10.jpg)

_We then insert the report in a Page presenting it both as Crosstab element and as graph. You can perform the drill-through to the target Page both from the Crosstab object and from the Graph object, both associated with the initial report. The only difference is that, in the graph, the symbol that indicates the drill-through is not visible, but if you move the mouse to the values of the Project level, you can see the pointer, indicating possibility of connecting to the new Page._

**Step 3: Drill-through to a Page**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/11.jpg)

_Using the drill-through, on one of the values of the Project level \(ex. APPLICATION\), we will be able to open the linked page with a report that has been correctly filtered by the value of the exported level._

**Example DT to a URL**

**Step 1: Drill-through to an External Application**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/12.jpg)

_We have a web application that allows users to analyze the development stages of a software and that is used to display and/or edit the corresponding use_ _cases_ _\(UseCase, acronym UC\). The application uses the UC\_ID\_Name parameter, the username of the current UC. We want to call this application from a DAC report_.

**Step 2: Drill-through to an External Application**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/13.jpg)

_In the report we insert a level with the UCs of the software._

**Step 3: Drill-through to an External Application**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/14.jpg)

We define a URL-type DT :

* in _openActionType_ we choose the item _Open URL_
* in the _drill-through-URL_ property we insert the application address
* in the _request-param-names_ property we set the name of the parameter UC recognized by the application, different in this example from the name of the level

**Step 4: Drill-through to an External Application**

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/DesignStudio/Report/DrillThrough/15.jpg)

_Using he drill-through in DAC, the system exports the value you have clicked on \(in the example: “4.0.0.0~FS.KPI.GEK.001”\) and_ _the application interprets it correctly by displaying the page for that specific UC._

_Note that the parameter relating to the UC is not the only parameter exported from the drill-through, even if it is the only one actually used._

## Aggregation of Levels \(Drill-down /Roll-up\)

By default reports are presented as not aggregated . You can request the aggregation of levels:

* by **layout**, with the  command where aggregation is carried out on all dimensional levels on rows and/or columns,

![](../../.gitbook/assets/image%20%2833%29.png)

* by **dimension** through the ![](file:///C:\Users\sdifranc\AppData\Local\Temp\msohtmlclip1\01\clip_image002.png) command where aggregation is carried out respecting the fact that levels belong to the same dimension

![](../../.gitbook/assets/image%20%289%29.png)

![](../../.gitbook/assets/image%20%283%29.png)

Default aggregation is applied both to row levels and to column levels, but can be changed through the _**group-drill-axis**_ property _\(Drill_ group_\)_, which allows you to choose which axis of the report is to be aggregated: &lt;rows_-only&gt; or_ &lt;cols-_only_&gt;.

The drill operation can be executed in two different ways:

* By preserving the hierarchy link in the report
* By deleting the _calling_ level from the report and inserting it in _an_ external path \(for Roll-up\)

This behavior is set by using the _**hierarchical-drill**_ property \(in the _Drill_ group\): see example below.

The examples below show reports displayed according to the kind of aggregation chosen.

Step 1: **No aggregation**![](../../.gitbook/assets/44%20%282%29.png)![](../../.gitbook/assets/45%20%281%29.png)

_By default the report is displayed with no aggregation as in this figure. The report displayed here includes one metric and three dimensions; of these, Category and Product belong to the same dimensional level, while Customer group belongs to a different level._

Step 2: **Aggregation by layout**![](../../.gitbook/assets/47%20%281%29.png)\*\*\*\*![](../../.gitbook/assets/46.png)

_If you choose aggregation by layout, all levels presented in the report will be aggregated_

Step 3: **Aggregation by dimension**

.![](../../.gitbook/assets/48.png)![](../../.gitbook/assets/49%20%281%29.png)

_If you choose aggregation by dimension, only levels belonging to the same dimension will be aggregated. In this example, category and product belong to the same dimensional level._

Example: Drill-down /Roll-up \(hierarchy-drill, group-drill-axis\)

Step 1: **Hierarchical-drill &lt;active&gt;**

![](../../.gitbook/assets/50%20%282%29.png)

_For drill-down, we just have to select the point in the graph and this will update, giving the lower level. In the example, by selecting the HEALTHCARE Customer Group, the graph widens to include a section with the products of the selected Customer._

_For roll-up, you again select the point of the parent level \(HEALTHCARE\)._

Step 2: Hierarchical-drill &lt;NO active&gt;

![](../../.gitbook/assets/51%20%281%29.png)

![](../../.gitbook/assets/52.png)

_In this second example, the Drill-down on the Customer Group FINANCIAL involves:_

* _Deleting the Customer Group level and displaying only the products related to that group._
* _Activating a path external to the report \( \Main\FINANCIAL \). By clicking on Main the report will revert to the initial state and display only the Customer Groups._

## Report Populated with Data from SQL Query

In DAC, reports can be defined on the basis of a SQL query. The reports created this way will continue to support most of the features of multi-dimensional analysis offered by the environment.

These reports will define the cubes and dimensions valid exclusively for the current report, which will be integrated with data from BI cubes.

This feature allows you to achieve the following improvements:

* _**Flexibility of mapping**_

A transactional environment, difficult to map through a structure of cubes and dimensions, can easily be analyzed.

* _**Speeding up mapping**_

You do not need to configure cubes-dimensions-metrics in order to read data from one or more tables, thus speeding up the process of mapping in the event of an impromptu analysis.

In the event data structures are mapped on which several reports have to be created, the more powerful and structured cube-dimension approach is preferred.

* _**Real-time access**_

Real-time access to a transactional database will be easier because the select query can be accurately defined.

* _**Accurate query definition**_

The ability to accurately define the report query will allow you, in the event the query generated by DAC is not optimized for the specific case, to redefine it in order to optimize it.

* _**Query customization for environment**_

The ability to accurately define the query will also allow you to write specific code for your environment.

* _**Multi-source reading**_

The SQL query, as for OLAP cubes, can be defined on JDBC data sources, Excel, CSV, XML.

* _**On-the-fly integration on the report**_

The SQL query can be integrated _on-the-fly_ within the report with the data in OLAP cubes, or other SQL queries.

For example, a report can be defined which accesses an OLAP cube, a query on DB2 query and a query on CSV files.

The system will allow you to configure 1 .. n SQL within a report, that will automatically be transformed into cubes only usable in the report where they are defined.

Both the cubes and the metrics created using the query will be distinguished from BI cubes and metrics by a different color, and the cube name coincides with that of the folder where the query is defined

![](../../.gitbook/assets/53.png) ![](../../.gitbook/assets/54.png)

In the section at the bottom of the _Editing_ _Report_ window , the section for defining the query is opened from the **SQL folder** macro:

* in the upper pane, you define the connection to the data source
* at the bottom you define the select query
* the commands on the right allow you to define the mapping of the cube's dimensions and metrics

![](../../.gitbook/assets/55%20%281%29.png)

This methodology allows you to define:

* Reports on SQL cubes
* Reports on multiple SQL cubes \(Join\)
* Report on SQL cubes and OLAP cubes

### Datasource Connection

You can define the connection to the data source:

* On the same data source of the application \(see _Application in DAC_ section\)
* On a data source in the same Data Model environment
* On a remote data source, defined beforehand in the application \(see _Remote data source connections_ section\)

![](../../.gitbook/assets/56%20%282%29.png)

### Select QUERY

In the lower pane, you insert the select query:

* manually, by using a content assist \(next paragraph\) for quickly selecting the data table
* using DAC’s “query editor”.

![](../../.gitbook/assets/57%20%281%29.png)

The buttons at the top \(to the left\) support the insertion of the query:

![](../../.gitbook/assets/58%20%282%29.png)

**Note:** _There must always be an AS clause with the corresponding alias for each field selected in the query._

#### Content Assist for Manually Formulating Queries

Content assist is available to help you to write queries:

* after entering the statement _SELECT \* FROM_ a menu opens with the **list of tables** of the selected data source.
* after choosing the table on the statement _SELECT \* FROM \[table\]_ the item **Substitute** \* is enabled \(right-click of the mouse\) which replaces the columns of the table with the character "\*"; for each field the corresponding alias is inserted.
* after inserting the key word _group by_, the item **$AUTO\_GROUP\_BY$** is enabled. This will allow the system to automatically define which levels to group during the query execution phase.

![](../../.gitbook/assets/59%20%281%29.png)

### Mapping Cubes \(dimensions and metrics\) of the QUERY

The default folders _Query 1, Query 2, Query_ 3 each contain data select queries; the data will then be _mapped_ to a new cube.

For each query, you define which fields are related to the metrics \(metrics mapping\) and which ones relate to the levels \(levels mapping\).

![](../../.gitbook/assets/60%20%281%29.png)

The new cube is created as soon as you select the OLAP folder:

* In the metrics and dimensions of the editing report window, the new cubes are visible \(yellow color\)
* By default, all query fields are mapped as levels
* The cube name coincides with that of the query folder

![](../../.gitbook/assets/61%20%282%29.png)

You can change the name of the cube by renaming the query folder \(right-click the item _Rename_\).

![](../../.gitbook/assets/62%20%282%29.png)

#### Metrics Mapping

You can define metrics mapping using the ![](../../.gitbook/assets/63%20%282%29.png) button:

* a pop-up box opens with the list of selected fields in the SQL query.
* from these, you select those that relate to the measures.
* the system generates a first level metric for each measure chosen

![](../../.gitbook/assets/64.png)

#### Mapping of Dimensional Levels \(key-description relationship\)

The mapping of levels is defined automatically: all fields that are not mapped as metrics are defined as levels.

If the table contains both the key and the description fields, you define their association in the pop-up box, opened by clicking the ![](../../.gitbook/assets/65%20%282%29.png) button:

* all the fields selected in the query and NOT _mapped_ as metrics are listed on the left
* the same fields are shown on the right
* for the key fields on the left, select the respective description field on the right

![](../../.gitbook/assets/66%20%281%29.png)

This setting allows you to have a report with the descriptive part displayed, while the key field is used for the JOIN.

#### Alias

Clicking the ![](../../.gitbook/assets/67%20%281%29.png)button opens a window which allows you to define the aliases of the levels and metrics.

This operation is crucial for obtaining clearer descriptive headings without being subject to database rules, which do not allow spaces and special characters in field names.

![](../../.gitbook/assets/68%20%281%29.png)

### Reports on SQL Cubes

The simplest application of this feature is the mapping of a single QUERY cube and execution of a report populated by this data only.

The next example shows the necessary steps and the final result.

#### Example: Report Constructed on Data Extracted from SQL Query

Step 1: **Report Populated from QUERY Cube**

![SNAGHTML937592](../../.gitbook/assets/69%20%281%29.png)

_Creating a new report on a QUERY cube:_

* _Open the SQL folder and define the query in the Query1 panel._
* _The query selects the sales data_

Step 2: **Metrics Mapping**![](../../.gitbook/assets/70.png)

_In the second step you map the metrics:_

* _Click the button to map metrics_
* _From the fields in the sales table you select those relating to the metrics \(SALES\_QTY, SALES\_UNIT\_PRICE, SALES\_VAL\)._

Step 3: **Creating and Running a QUERY Cube**

![](../../.gitbook/assets/71%20%281%29.png)

_Select the OLAP folder and the system creates the QUERY cube just defined:_

* _under metrics, the new cube Query1 is shown, with the first-level metrics on fields mapped in the previous step_
* _the new cube Query1 is always shown under dimensions: the levels linked to the cube are those not defined as metrics._
* _Select a first level metric in the new cube and two levels; the report is run and the result shown in the figure is obtained_

### Reports on multiple SQL Cubes \(Join\)

A more complex application of the query feature is to define multiple cubes of this type.

In this case, you need to define the **join criteria** for relating the two cubes:

* The relationship between the two cubes is defined by assigning the same alias name to the join fields, in the two queries.

_We’ll use the sales table and the budget table, linked by the product, as an example._

_In defining both select queries, you must assign the same ALIAS NAME to the product field:_

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><em><b>Query 1:</b></em>
        </p>
        <p><em><b>select</b></em>
        </p>
        <p><em>ID_CUSTOMER</em>  <em><b>as</b></em>  <em>ID_CUSTOMER,</em>
        </p>
        <p> <em>ID_PRODUCT</em>  <em><b>as</b></em>  <em>ID_PRODUCT,</em>
        </p>
        <p><em>SALES_QTY</em>  <em><b>as</b></em>  <em>SALES_QTY,</em>
        </p>
        <p><em><b>from</b></em>  <em>FT_SALES</em>
        </p>
      </th>
      <th style="text-align:left">
        <p><em><b>Query 2</b>:</em>
        </p>
        <p><em><b>select</b></em>
        </p>
        <p><em>BDG_SALES_QTY</em>  <em><b>as</b></em>  <em>BDG_ _QTY,</em>
        </p>
        <p><em>BDG_SALES_VAL</em>  <em><b>as</b></em>  <em>BDG_VAL,</em>
        </p>
        <p> <em>ID_PRODUCT</em>  <em><b>as</b></em>  <em>ID_PRODUCT</em>
        </p>
        <p><em><b>from</b></em>  <em>FT_BUDGET</em>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

The next example details the definition of two QUERY cubes and the final result is presented

Step 1: Definition of the queries for the two cubes \(same ALIAS on the JOIN fields\)

![](../../.gitbook/assets/72.png)

_Two SQL queries are defined: for loading sales data and budget data:_

* _both queries have the same alias for the product field._

_You map the respective metrics on both queries, using the button shown in the figure. You rename the cubes SALES and BUDGET respectively._

Step 2: Creating QUERY cubes and reports in MULTICUBE ANALYSIS

![](../../.gitbook/assets/73.png)

_Selecting the OLAP folder creates two SQL cubes: BUDGET and SALES, with the metrics and the levels set in the SQL section._

* _You select the levels and the newly created cube metrics for creating the report._

_If you access the Query viewer window \(SLQ button shown in the figure\), you’ll see the join performed by the report on the two cubes, in relation to the product column._

_By running the report you get the result shown in the figure \(bottom\)._

### Report on SQL Cubes and OLAP Cubes

The cubes that are created by using SQL queries can be related to those of BI: the cube just needs to have a column that can be related with a level of the BI cube.

Just **assign the logical name of the level as an alias of the** **column** to define the relationship between the QUERY cube and the BI cube.

The system facilitates the association of the name of the level with a _content_ _assist_ that proposes the logical names of the application levels: the default alias is deleted and the levels menu opens.

![](../../.gitbook/assets/74.png)

Step 1: **Creating a QUERY Cube on Sales**

![](../../.gitbook/assets/75%20%281%29.png)

_A report is created with a SQL cube of sales data and the BI Budget cube. These are linked by the product code, which is defined in the same way in the two fact tables._

_The select query is defined in the sales table. You delete the alias of the product and through the content assist you select the respective product level._

Step 2: Analysis eport on QUERY Cube and BI Cube

![](../../.gitbook/assets/76%20%281%29.png)

_The report is created by using both the levels and metrics of the Sales QUERY cube, and the levels of the BI BUDGET cube._

## Export to Excel Format

You can export a report in simple mode or by using a file template, defined beforehand, where you set what to export in detail, from the data to the elements constituting the reports, or the user parameters, using the appropriate TAGs. You will be able to export the report only when it is published on RunTime

Exporting the report can be subdivided into several Excel spreadsheets. The subdivision depends on the occurrences of a dimensional level.

In addition to previous features, other properties allow you to set the layout; while in the

· _**full-export**_ \(_Excel_ group_\)_ property you can enable the full export of the report. The property is enabled by default and if disabled, limits the export to just the rows and columns displayed.

· _**export-report-parameters** \(Excel Group\)_ enables the export of the parameters of the report with the corresponding values.

### Excel Export with Large Amounts of Data

It is possible to export the reports containing large amounts of data, by activating the **full-export** properties.

The generated file will contain all the rows in the report, relating to the selection made in page-by.

When the two properties are activated, the export in Excel will not report all the formatting characteristics defined in the report, except for those set via the _**Headers**_, _**Columns**_ and _**Rows**_ properties of the same report. In addition, in this mode, the use _of a template and the definition of a break level are not supported._

The formatting applied to rows and columns is also maintained when the report is exported in Excel format. If the type of font is customized, however, at the time of exporting, the font “ARIAL” is set by default.

The size of the font is executed by the system, which makes it similar to the original.

**Note: \(known limitations\)**

The template cannot contain images.

The presence of images in the template could cause the image to be canceled or even make it impossible to open the exported Excel document.

The exported Excel document needs to be saved again with Excel if static images are exported.

Excel has its own way of managing images. If a spreadsheet of the exported document contains 2 or more images, any change in the spreadsheet could cause the images to be distorted. To solve this issue, just open the exported document with Excel, save it with the same name, close the document and then reopen it.

### Exporting with Template

The prerequisite for exporting a report using a template is the existence of an Excel file to be used as a template \(xlsx format\), built and saved in the system and on the basis of which the exported Excel documents will be produced.

You can set the export with template via the following properties:

* _**export-with-template**_ enables the export through a template \(by default the property is disabled\)

– _**template**_ name of the file containing the template which needs to be saved in the repository:

– _**auto-adjust-col-width**_ abjusts the size of each column to the contents of the largest cell. If disabled, the size of each collumn will be the same as the one definited in the template.

The template may consist of one or more Excel spreadsheets. The cells may have any formatting.

A set of specific TAGs will allow you to customize the export. Therefore, the export operation will replace each TAG with the object indicated.

If the template contains TAGs that are incorrect or are associated with non-existent objects, the resulting report will contain some cells in red, signaling the error in question.

### TAG Exporting Reports in Excel

The list of export TAGS of a report is shown below \(the TAGS are not case sensitive\).

Each TAG is inserted in only one Excel cell, but the associated object can contain multiple cells, spread over multiple rows and columns. To do this, you need to use formatting TAGS, to prevent an object from overwriting another:

· &lt;NEW\_ROW/&gt; Inserts new rows, as many as the number contained in the object associated with the TAGS on it. Object TAGs are associated with &lt;NEW\_ROW/&gt; only if they are located on the same column and there are only empty cells between them.

· &lt;NEW\_COL/&gt; Inserts new columns, as many as the number contained in the object associated with the TAG on the left of it. Object TAGs are associated with &lt;NEW\_COL/&gt; only if they are located on the same row and there are only empty cells between them.

<table>
  <thead>
    <tr>
      <th style="text-align:left"><em>EXPORT TEMPLATE TAGS</em>
      </th>
      <th style="text-align:left"><em>Exported object</em>
      </th>
      <th style="text-align:left"><em>Excel cell occupation</em>
      </th>
      <th style="text-align:left"><em>&lt;NEW_ROW/&gt; and &lt;NEW_COL/&gt;use</em>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&lt;MODEL/&gt;</b>
      </td>
      <td style="text-align:left">Application name</td>
      <td style="text-align:left">1 Cell</td>
      <td style="text-align:left">Not possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;OBJECT_TITLE:</b>
      </td>
      <td style="text-align:left">Title of the report;</td>
      <td style="text-align:left">1 Cell</td>
      <td style="text-align:left">Not possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;OBJECT_DESCRIPTION/&gt;</b>
      </td>
      <td style="text-align:left">Report description</td>
      <td style="text-align:left">1 Cell</td>
      <td style="text-align:left">Not possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;OBJECT_BODY/&gt;</b>
      </td>
      <td style="text-align:left">Report body</td>
      <td style="text-align:left">Number of rows by number of columns in the report body</td>
      <td style="text-align:left">Possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;PAGE_BY/&gt;</b>
      </td>
      <td style="text-align:left">Page-by report</td>
      <td style="text-align:left">Number of cells on the row equal to 2 times the number of page filters</td>
      <td
      style="text-align:left">Only &lt;NEW_COL/&gt; possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;METRICS/&gt;</b>
      </td>
      <td style="text-align:left">Report metrics</td>
      <td style="text-align:left">
        <p>1 cell for title (row above)</p>
        <p>3 cells for each metric (subsequent rows)</p>
      </td>
      <td style="text-align:left">Possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;LEVELS/&gt;</b>
      </td>
      <td style="text-align:left">Report levels</td>
      <td style="text-align:left">
        <p>1 cell for title (row above)</p>
        <p>2 cells for each level (subsequent rows)</p>
      </td>
      <td style="text-align:left">Possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;DIRECT_FILTERS/&gt;</b>
      </td>
      <td style="text-align:left">Direct report filters</td>
      <td style="text-align:left">
        <p>1 cell for title (row above)</p>
        <p>3 cells for each filter (subsequent rows)</p>
      </td>
      <td style="text-align:left">Possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;RANGE_FILTERS/&gt;</b>
      </td>
      <td style="text-align:left">Report range filters</td>
      <td style="text-align:left">
        <p>1 cell for title (row above)</p>
        <p>3 cells for each filter (subsequent rows)</p>
      </td>
      <td style="text-align:left">Possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;CUSTOM_FILTERS/&gt;</b>
      </td>
      <td style="text-align:left">Custom report filters</td>
      <td style="text-align:left">
        <p>1 cell for title (row above)</p>
        <p>3 cells for each filter (subsequent rows)</p>
      </td>
      <td style="text-align:left">Possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;FILTERS/&gt;</b>
      </td>
      <td style="text-align:left">Report filters: range, direct and custom filters</td>
      <td style="text-align:left">Cells occupied by &lt;DIRECT_FILTERS/&gt;, &lt;RANGE_FILTERS/&gt;, &lt;CUSTOM_FILTERS/&gt;</td>
      <td
      style="text-align:left">Possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;METADATA/&gt;</b>
      </td>
      <td style="text-align:left">Report elements: metrics, levels and filters</td>
      <td style="text-align:left">Cells occupied by &lt;METRICS/&gt;, &lt;LEVELS/&gt;, &lt; FILTERS/&gt;</td>
      <td
      style="text-align:left">Possible</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>&lt;USER ATTRIBUTE:%attribute%/&gt;</b>
        </p>
        <p><b>(%attribute% user parameter)</b>
        </p>
      </td>
      <td style="text-align:left">Value of the attribute %attribute%</td>
      <td style="text-align:left">1 Cell</td>
      <td style="text-align:left">Not possible</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&lt;REPEAT/&gt;</b>
      </td>
      <td style="text-align:left">Enables the export to multiple Excel sheets, according to the settings
        in the xlsBreakLevel property</td>
      <td style="text-align:left">1 Cell</td>
      <td style="text-align:left">Not possible</td>
    </tr>
  </tbody>
</table>

**Note:** _All formulas, 2D and 3D references, formatting, statical information in cells, merged cells, references to cells or groups of cells with name, are maintained and updated on the basis of the number of rows and columns that might be generated during export._

### Level Exporting to Several Excel Spreadsheets

You can set the subdivision of a report export into multiple Excel spreadsheets in the following properties:

* _**xlsBreakLevel**_ lets you select a level of the report and set it as break level for exporting: therefore it allows you to export each instance of the level chosen in a separate Excel spreadsheet; if the item \[Total\] is present, a spreadsheet will also be generated for the aggregated data.
* **excel-font-size-adapt:** it allow a value to be set that will be subtracted from the size of the font of the sells in the report. This will automatically re-dimension the size of the font when exporting in excel.
* **excel-template- additional-reports**: Allow you to set the number of additional reports to export to the Excel template.
  * **additional-report-to export:** Select an additional report to export with the first.

**Info:** When the property **excel-template- additional-reports**: is enable for the Editabel Crosstab, the additional sheets will be used only as a reference and won’t be used for the import operation.

## Editable Report Introduction

The Editable Report is a particular report that allows to interact with the report data. It’s possible to insert, delete and modify the data and select which user groups can modify them.

In addition to the restriction on user groups, it is also possible to decide which column can be edited by configuring the columns-definitions property of the main group.

To allow the end-users, to use an Editable Report, it is necessary to associate the report with the Dcy Smart Grid Widget \(see the widget Smart Grid documentation\).

You can change or insert new data importing **Excel** files. You will have the possibility to download the excel template of the report, modify the data and export again the file to update the data.

The editable report feature, is available for all the OLAP report while for the SQL reports you can associate it with the widget, but are not editable.

### How to make a report editable

To activate the report editing, access the report properties &gt;&gt; Editing group of the Properties folder.

The properties allow you to:

* **enable-editing:** Enable the table to modify the data
* **data-deletion-message:** Set a message to be displayed when a report data is deleted
* **editing-grants :** select which user group can modify the data of an editing report.
* **read-only-filter:** Set a SQL filter for making matching Report's rows read-only
* **insert-query:** Define inset query to manage how the data are added to the Report. It' is also possible to use parameters available in the page.
* **update-query:** Define Update query to manage how the Report data are updated. It' is also possible to use parameters available in the page.
* **delete-query:** Define Date query to manage how the data are deleted from the Report. It' is also possible to use parameters available in the page.
* **enable-audit:** Enable the audit logging for all the operations performed on the data of the Report
  * **audit-datasource:** Set the data source where to store the audit logging data
  * **audit-table-name:** The table storing the audit logging data
* IT’s possible to write the query of editable report even when there are no metrics available in the report .
* It’s possible to use the system variable in the CRUD statement.

The **Column-Definition** properties of Main group defines report columns settings.

It’s possible to configure the column definition properties "Key", "mandatory" and "read-only" even without enabling the property "enable-editing". In this way the smart grid widget can use them even when enable-editing is disabled.

After enabling the report to modify data, it will be necessary to associate it with a Smart Grid Widget.

**Column item details:**

* **Column**: show the list of levels and metrics present in the report.
* **Data Type:** a drop-down menu allows selection of data type \(Number, String/Text , Date, Epoch, URL, Picture/Icon, Boolean\)
* **Date Pattern**: Sets the pattern the date type column value must comply with.
* **Input type:** Sets the type of data to be entered allowing the use of the suitable input interface \(Number, Text, Checkbox, Date, Value List\)
  * **data-type** = _Number_
    * **reportColNumMin:** set the minimum value.
    * **reportColNumMax:** set the maximum value.
  * **data-type** = _Text_
    * **reportColTextMxL:** set the maximum length for the text to be inserted.
    * **reportColTextMnL:** set the minimum length for the text to be inserted.
    * **reportColTextRgx:** set the regular expression for the text to be inserted.
  * **data-type** = _Value List_
    * **values**: select the type of insertion of the value list
    * **report**: Define the report associated to the object
    * **id-column**: Allow you to select which column of the associated report will be used
    * **description-column**: Allows you to select which column of the associated report will be used as description.
    * **params-binding**: Allow you to configure for each parameter available in the associated report its binding with a column of the configuring report or a parameter coming from the page.
* **Define Value:** If column with input type "Value list", allows you to configure the id value to use in order to open the drop down with a default value.
* **Visible:** Set if the column is visible. The columns defined as "not visible" are exported as hidden columns in the XLS file
* **Key**: Set if the column is a key column.
* **Mandatory:** Set if the column is mandatory.
* **Read only**: Set if the column is read only.
* **Auto-increment:** Set if the column is auto incremented

**NOTA:** The Smart Grid Widget is not present in the widget catalog of the Page Designer, therefore it must be imported into the application via the Widget Designer.

The enable-editing properties can not be enabled in the following case:

* When the report is built on a read-only data source
* When an ID formula in applied on the levels
* When the report is a SQL report

**API**: DAC Expose a REST Api to write \(insert, update, delete\) rows of a Report. Please see the REST API documentation on RunTime.

Please see how to use the Editable Report with the widget SmartGrid.

Example - How to use the editable report into the Smart Grid Widget [View!](page-designer.md)

### Load Data Via excel

Importing data via excel file allows to edit and insert data within a report. Only a business user with writing permission can import data via Excel. Permission can be assigned to user only if “enable-editing” property of the report is flagged. In addition, the “enable-editing” property on the widget must also be enabled.

Those are the operations allowed:

* **Update:** allows you to update all the rows of the report exported via Excel file. During the data import, only the non-Read-Only columns are updated and a check will be made on the key fields. Data whose key values ​​are not present in Excel should not be changed.
* **Insert:** Allows to insert new lines into the report. In this case the data already present in the table is not updated.
* **Insert / Update:** Allows you to insert and update multiple rows simultaneously.
* **Delete / Update:** allows you to delete and update multiple lines at the same time. The table will be updated with only the data present in the excel file. Therefore all the lines not present in the excel file will be deleted in the table.

The type of operation, allowed when importing data via Excel, is defined in the Page Designer through the property \(import-operation-type\) of the widget.

Before importing data from an Excel template into a report, the system validates the excel template and its data.

**Structural Validation Criteria:**

* All columns mapped in the sheet must be valid \(existing column header\).
* The Excel Template must contain a column for each corresponding column of the Report.

**Data Validation Criteria**

* Each row of the Excel Template must contain non-null values for the corresponding key columns of the Report and mandatory metrics;
* Each cell of the Excel Template must contain a value of the corresponding Report columns' datatype.

In case any of the above criteria are not meet, the Excel Template is invalid.

The system will return to the business user a detailed description of result:

* **Structural invalidation:**
  * Invalidating reason;
  * Missing columns \(if any\).
* **Data invalidation:**
  * Coordinates of the invalid cells;
  * Invalidating reason.

You can enable import into Excel in case your report doesn't use metrics

