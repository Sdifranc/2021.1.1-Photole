# Preferences

## Introduction

For the connection to Microsoft Excel, proceed as follows:

1. Select Excel file \(.xlsx\) as data source type.
2. In **File Path on Client** enter the path, including the Excel file on the client. The Browse button opens the window to select the file.
3. In **File Path on Server,** enter the path, including the Excel file on the DAC server. The path must start from the name of the unit present on the AS server, which must have visibility privileges on the folder where the file resides.

## Main

The system properties relating to Data Model are grouped in the **Main** section in **\*\*the** Tools Properties\*\* window and are subdivided into the sub-groups:

* **Alert logging**
  * _**Max number of alert execution logs:**_ Allows to set the max number of logs for an alert that can be kept.
  * _**Days to keep alert execution logs :**_ Allows to set how many days logs for an alert must be kept.
* **Cache**
  * _**minHoldTimeDatamart \(min\):**_ is the minimum duration \(in minutes\) of the temporary tables used by the datamart and accessible to the user for displaying reports. Before this time, the tables will not be deleted, even if the system has rendered the cache invalid \(default value set at 20 minutes\).
* **Collaboration**
  * **storage-datasource:** set the target in which the Collaboration tables will be created.
* **Data logging –** For the times to clean the tables containing log information. You set how many days different content must be kept before it is deleted automatically. The default is 90 days for all log information tables, meaning that only the information relating to a historical period of 3 months will be kept:
  * _**Cleanup object execution log \(days\) :**_ for the table relating to the execution of the objects.
  * _**Cleanup user connections log \(days\) :**_ for the table relating to user connections.
* **Document Repository**
  * _**repository-type:**_ set the medium the Document Repository is saved.
  * _**storage-datasource:**_ data source used to store the files in the Document Repository.
* **Export**
  * **pdf-max-rows:** sets max row limit beyond which the report cannot be exported to Pdf.
  * **excel-max-rows:** sets max row limit beyond which the report cannot be exported to Excel.
  * **csv-max-rows :** sets max row limit beyond which the report cannot be exported to CSV.
* **External Editors** 
  * _**eclipse-path:**_ set the path of the Eclips executed file to use as Snipped Code Editor.
* **GoogleMap**
  * _**googleMapKey:**_ enter the URL code that contains the _Google Maps_ service activation key.
* **Internationalization**
  * _**TimeZone:**_ select the user’s time zone. AUTO identifies the time zone automatically.
  * _**enableMultiLanguage:**_ enabe and disable the multilanguage system.
  * _**default-language:**_ set the default language used by the DAC to display content in case of missing labels in the user’s preferred language.
* **Report temp tables:** In order to operate on the system’s stress levels, by limiting the number of instances of the temporary tables created during execution of the reports:
  * _**intermediateMaxRows:**_ for those of the intermediate temporary tables.
  * _**finalMaxRows**_: for the final temporary table, i.e. the table created by the system to populate the report.

    If the number of rows in the table exceeds the limit set, report running will be terminated immediately and the report will not be generated. The default value is **-1** which indicates an unlimited number of instances.

  * _**index-temp-tables:**_ t_ables_ to activate temporary table indexing on the join key for the last integration step of the partial results.
* **Storage tables schema**
  * _**report-final-tables:**_ tables containing the DataMart of the reports \(“FX” prefix\).
  * _**report-interm-tables:**_ tables created in the intermediate stages of running reports \(“DX”,”TX”,”UX” prefix\).
  * _**excel-integration-tables:**_  the screen where the integration table will be saved when the associated data source is Executive Object-
* **System**
  * system-parameters: allows you to set the system parameters useful for debugging the application. The property value must be a valid JSON object written in Key/Value pairs \(e.g. {“paramKey”:”paramValue”}\)
* **Users**
  * Subject-fullname: set the sort order to display the user lists

## Web

The configuration properties which impact DAC are in the **Web** item and affect:

* **Appearance**
  * **html-contents-allowed:** Allows you to enable direct interpretation of HTML content in the modules that support.
* **Cloud**
  * **kubernetes-endpoint:** it sets the Kubernetes.
  * **kubernetes-token:** it sets the token to authenticated to.
* **Connection**
  * **decisyonWebURL:** which allows you to define the URL to connect to DAC.If the system cannot connect to the URL entered, a warning message is displayed and the address entered is deleted. Whereas for the URL HTTPS, when the properties are validated, the SSL certificates are not considered.

_**Note:** when the App Composer container starts, the system updates the value of the DecisyonWebUrl workspace property using a variable in the dedicated container in yaml. This way if the app is moved to another server or the DNS is changed, there is no need to manually update the property._

* **Landing Page**
  * **showSocialSpacesLink:**enables the display of the social spaces in the DAC homepage \(default\).
* **Login**
  * **automatic-user-creation:** if enabled, users will be autommatically created.
* **Page Navigation**
  * **page-navigation-component:** specifies the minimum time that must elapse without receiving any information from client web before a user’s
* **Sessions**
  * **webSessionExpireTimeout \(min\):** If a user does not properly log out of the system, \(e.g. if the user is disconnected from the network or the browser crashes\), the system forces user disconnection from DAC after the period set \(in minutes\) in this property \(by default, 5 min.\). This time is different from a time-out, which is due to user inactivity, and is defined in the DAC _web.xml_ configuration file.  _\*\*_
  * **showWebClosureConfirm:**If you close the browser, this property enables/disables a confirmation message \(enabled by default\).
* **Toolbar Settings**
  * **show-menu-items:show-menu-items:** Allow you to select which menu item to make visible on DAC.The default value is ALL. The option are Side Nav Menu and Toolbar Options
* **User contents**
  * **maxUploadFileSize \(MB\):**

    File size is expressed in MB and the default size configured is 20 MB.

    Minimum and maximum file sizes that can be set are 0.25 MB and 5 GB respectively.which sets the maximum size for files attached by users:

    * in collaboration Page components
    * in a discussion or task
* **WebEvents**
  * **customEventManager:** allows you to enable the Custom Events.
* **WebReport**
  * **reinit-report \(OnLaunch\):** enables the automatic initialization of reports, when they are requested in DAC
  * **showReportToolbarCollapseButton:**displays/hides the button for opening**/closing** _the report Toolbar in DAC_
  * **startReportToolbarCollapsed:**displays/hides the Report toolbar in DAC when the report Toolbar in DAC is hidden \(**startReportToolbarCollapsed** _enabled_\), \(you can only open it if the button for opening the toolbar is available **showReportToolbarCollapseButton** _enabled_\).

## Email

For the connection to Microsoft Excel, proceed as follows:

1. Select Excel file \(.xlsx\) as data source type.
2. In **File Path on Client** enter the path, including the Excel file on the client. The Browse button opens the window to select the file.
3. In **File Path on Server,** enter the path, including the Excel file on the DAC server. The path must start from the name of the unit present on the AS server, which must have visibility privileges on the folder where the file resides.

