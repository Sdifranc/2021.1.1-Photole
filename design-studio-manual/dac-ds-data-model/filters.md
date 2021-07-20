# Filters

A filter specifies the conditions that the data must meet so that:

* it may be displayed in a report
* or it may be used in the calculation of filtered metrics.

The difference between the two types of application is that in the first type all the metrics will be affected by the filter, while in the second type the condition is only applied to the filtered metric.

The filters are subdivided into two groups:

* **Direct filters** where the condition is expressed on the dimensional levels, used to limit the data on the analysis lines \(dimensions\);
* **Range filters** where the condition is expressed on the values of the metrics

In these filters, in addition to expressing the condition, data partitioning may also be defined on which it must be applied. Range Filters cannot be applied to Metrics.

DAC also defines the filters exclusively used by the single report \(see Report Administrator, chap., Report, Exclusive Filters section.\)

You can use a parameter in the condition in Filters. In these cases, the condition is applied after you have valued the parameter.

Making a Filter parametric is especially useful when a report \(or Metrics\) is used on Pages. The parameter can be valued with one of the form objects or by a level exported from a report.

## **Direct Filters**

A direct filter is defined in the window opened from the menu item:

**Data Model&gt;&gt;**&gt;&gt;**Direct Filters** , or the button on the tool bar

![](https://docs.decisyon.com/wp-content/uploads/2021/01/DF1.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

The filter condition may be expressed compared to the dimensional levels of the application. When typing the formula, you are supported by a Content Assist.

The system defines the formula of the filter by combining various conditions relating to the different dimension levels. Example: Product@ID = ‘1’ AND MONTH@Description = ‘JANUARY’.

Since the application of a filter in a report implies that all the levels in a filter are applicable to at least one metric of the report, using filters with many conditions may reduce their applicability in the reports: therefore we advise creating base filters to be applied to the report at the same time. The filter of the previous example may actually be divided into 2 filters:

Filter 1: Product@ID = ‘1’ Filter 2: MONTH@Description = ‘JANUARY’

To obtain the AND condition, just associate both filters with the report.

In the formula of the filter it is possible to enter a SQL instruction: for example, a filter with the products belonging to categories 1 and 2.

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df2.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

### Filter Condition on Dimensional Levels

If you want to apply a Filter condition on dimensional levels, you must select the level you want on the left side of the page.

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df3.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

Dimensional levels are structured for Cubes. You must first select the Cube at the top of the hierarchy, and then the levels.

In the cub’s list are available the dimensions not associated to the cube.

The “field @ID” key fields and “Field@DS ” description field are indicated for each level. You set these fields when you are creating the Dimension \(see Mapping dimensional levels section\). The Filter condition can be expressed on the “ID” or on the “Description”.

Double-click to display the selected dimensional level in the formula definition field area. This is where you can enter a Filter condition.

**Note**: The names of the levels listed in the selection area correspond to the displayed names set when you created the Dimension. An exception is made if the dimensional levels use the same name displayed. In this case, the logical name of the level is indicated.

For example, if you define two levels with the displayed name “Customer Type”, the following respective logical names appear on the list: Customer\_Type1@Description, Customer\_Type2@Description.

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df4.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

As shown in the figure, several functions and operators are available if you want to create a new Filter. You can also manually enter the SQL instructions in the formula definition area \(the green check allows you to validate the formula entered\).

The top button allows you to select the values of the key field or description of the level selected. A window opens listing the values of both fields. The value selected appears in the foreground. The figure below shows that the Customer Type@Description field has been selected.

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df5.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

A search field also allows you to quickly narrow the search area.

Once you have identified the values to be filtered, check them. When you close the window, they will be indicated in the formula definition area.

The predefined functions to be used to write the Filter condition are in the **formula definition area** at the top.

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df6.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

* The String function section contains functions for managing strings. These functions return the following values:
  * **Starts with** – they start with a specified value
  * **End with** – they end with a specified value
  * **Matches** they are equal to the specified word \(for the characters\).
  * **Contains** which contain the one specified
* The Set Function section contains the set operators, which verify:
  * **in** and **in values** – the value equaling one of the values of a specified list \(pertinent operator\).The second operator automatically opens the value window of the selected level.
  * **not in** the value does not equal one of the values in a specified list \(non- pertinent operator\).
  * **between** the value belonging to an interval, defined by a lower and upper limit**.**
* The section to the right lists the **logical operators:**
  * **AND** among several conditions, to return the elements that satisfy all conditions at the same time
  * **OR** among several conditions, to return the elements that satisfy at least one of the conditions
  * **AND NOT** among several conditions, to return the elements which do not satisfy the condition after the instruction
  * **OR NOT** among several conditions, to return the elements that satisfy at least one of the conditions \(the second is denied\).

### Content Assist on Filter Conditions

A content assist is active when you define Filter conditions. It suggests possible commands such as the list of dimensional levels, entering certain operations, DAC tags or user variables.

With an **initial mouse** **click** on the formula definition area, you activate a menu with the dimensional levels of the application \(in alphabetical order\).

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df7.png)

.

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

When you **select the level**, you activate content assist to select certain special operations:

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df8.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

* **IN\(\)** allows you to enter a list of values between brackets.

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df9.png)

If the dimensional level is descriptive, the system adds quotation marks inside the brackets. Otherwise the values will be entered with no quotation marks.

* **IN\(…\)** if you have selected it, the system displays the list of values for the selected level in a new window in multi selection.

![](https://docs.decisyon.com/wp-content/uploads/2021/01/df10.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

* **IN\(?NAME\_LEVEL?\)** If you have selected it, when the report is run the system will automatically transform the level into parametric Filter.

![](../../.gitbook/assets/image%20%2829%29.png)

![](data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7)

**When you type the “%”** string, you activate a menu with the list of USER VARIABLES.

## Range Filters

Range filters define conditions on the metrics, already defined with the [Metrics Management](filters.md) module.

Filters are then associated with the reports, which apply the conditions defined to the set of data as a whole.

The dimensioned range filters apply the filter condition on the data previously [partitioned for one or more dimensional levels](filters.md); on this partitioning it is possible to [apply additional filters, of the direct type](filters.md), to refine the filter criterion further.

A range filter is created in the window opened from the menu item:

**Data Model&gt;&gt;Range Filter**

or from the toolbar, using the ![](../../.gitbook/assets/16%20%281%29.png) button.

![](../../.gitbook/assets/17%20%286%29.png)

In the _Metrics_ folder, select the metrics on which to apply the filter condition; with a double click, it is reported automatically in the formula definition area \(bottom, right\).

The system also specifies the mathematical, comparison and logical operators to be entered in the formula using the correct buttons at the top of the lower text box.

Select the dimensional levels for the [data partitioning](filters.md) in the _Dimensions_ folder.

In the _Direct Filter_ folder, select the [direct filters](filters.md) to be applied to the partitioned data.

In the next example, a simple Range Filter is defined to obtain the years with sales below a target, in a report which only has the year level.

Step 1: Simple Range Filter

![](../../.gitbook/assets/18%20%286%29.png)

_Create a simple range filter where the filter condition of the sales lower than a target of 50 million is defined: Select the Sales Val sales Metric \(double-click\) and enter the formula in the area provided._

Step 2: Simple Range Filter

![](../../.gitbook/assets/19%20%282%29.png)

_Create a report with the Year level and the metric Sales Val. the range filter is associated and the report is performed: the result will only give the years with sales below the 50 million target. The figure also shows the report prior to the application of the Range Filter._

### Partitioning for Dimensional Levels

A Range Filter applies the Filter condition on the partitioned data according to the levels in the report.

_For an annual level report, for example, a condition on the sales above a target is applied to the values of each year. If month is added to the report, the same condition is applied to the values of each month, which will be very different from the annual ones._

The next example shows this type of application: to obtain the years with sales lower than a target, in a report which has the year level and the month level.

Step 1: Dimensioned Range Filter

![](../../.gitbook/assets/20%20%282%29.png)

_Create a filter range dimensioned by year, on the same condition of the previous example \(simple range filter\), this conditions the sales lower than a target of 50 million, however in this case at annual level:_

_Select the Sales Val sales Metric \(double-click\) and enter the formula in the area provided._

_Select the Year level from the Dimensions folder._

Step 2: Dimensioned Range Filter

![](../../.gitbook/assets/21%20%284%29.png)

_To the report of the previous example \(Standard range filter\) add the Month, level to obtain the report in the figure._

_Associate the dimensioned range filter in place of the previous one: the result will only give the years with sales below the 5 million target, exactly as in the previous example \(only the year 2006 is excluded\)._

_However, if the undimensioned Filter were to be applied to this report, the result would be a report with all elements, because it would be applied to monthly sales \(no month has values below 50 million\)._

#### **Direct Filters on Partitioning**

In case the filter condition is applied to a specific data partitioning, as shown in the previous paragraph, it is also possible to filter the partitioned data.

The proposed example explains the use of this method: to obtain the years with sales, in the SOUTHERN area, lower than a target, in a report which has the year level and the month level.

Step 1: Dimensioned and Filtered Range Filter

![](../../.gitbook/assets/22%20%281%29.png)

_Create a range filter dimensioned by year, and filtered for the SUD area, with condition on the sales that are lower than a target of 15 million:_

* _Select the Sales Val sales Metric \(double-click\) and enter the formula in the area provided._
* _Select the Year level from the Dimensions folder._
* _select the Filter on the SOUTHERN area, created in a previous phase._

Step 2: Dimensioned and Filtered Range Filter

![](../../.gitbook/assets/23%20%284%29.png)

_Create a report with the Area, Year and Month levels and the metric Sales Val._

_The report for the SUD area identifies only the years 2004 and 2007 as years with turnover below 15 million._

_Associate the Range Filter created in step 1 and run the report._

_The result will only provide the years with sales below the target of 15 million for the SUD area even though the turnover for the same years for the other areas \(such as the NORD area\) is higher than the specified target._

## Parametric Filter

Regarding the parametric filters, please note that it is possible to use the logical operator **\[OR\]** in addition to the usual logical operators \(AND, OR, NOT\). OR implements a particular behavior of the filter which is described short below.

If the Filter is defined as follows:

_Level\_01@ID IN \(**?Par\_1?**\)_ _**\[OR\]**_ _Level\_02@ID IN \(**?Par\_2?**\)_

the Filter conditions will be applied when at least one of the parameters is valued, otherwise the system behaves as if no condition were to be applied.

**Note:**

_When parametric Filters are used, you cannot use the cache if the level is not in the report._

User parameters can be used in **Direct Filters**. Then data will be filtered according to which user is currently logged in the application. The parameters that can be used are described in detail in the User management, Attributes section. They are:

* _%SUBJECT\_ID%_ : User ID
* _%U\_username%_ : Username of the user
* _%U\_subjectName%_: Full name of user
* _%U\_mail% and_ %U\_phone%_: user_ e-mail address and phone number
* _%U\_attribute\_\[n\]% \(\[n\]=1-5\)\_: five attributes associated with the user

**Note:**

_If Parametric Filters are on user parameters, the automatic cache is only generated for the user who created it. The same cache cannot be used by other users running the same report._

_The absolute cache can NEVER be used by the report._

**Step 1: Parametric Filter**

![](../../.gitbook/assets/24%20%282%29.png)

_In this example in the filter condition a parameter on the region is used._

_When you validate the formula, the system asks you to value the parameter and then it performs the validation \(an error message also appears for parameter values that are not in the data warehouse\)._

**Step 2: Parametric Filter**

![](../../.gitbook/assets/25%20%283%29.png)

_Create a metric to which you apply the previous filter._

**Step 3: Parametric Filter**

![](../../.gitbook/assets/26%20%282%29.png)

_Create a report with the sales compared to the region \(level in the filter\), with the metric just created._

_The parameter is requested when the report is run \(it is no longer requested when you run it in the future; you can modify it in the testParams property of the report \[Presentation Administrator, Report section, Other specific report properties section\]._

_On the report, note that the metric is only valued for the region entered._

