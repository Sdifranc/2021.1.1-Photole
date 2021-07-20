# Languages Administrations

## Introduction

DAC allows you to import new languages in addition to the default ones within the application. The Label Management module is available for business labels, while the Languages Administration module is used for system labels.  
System labels are the labels that appear on all interfaces of the DAC. By contracting the Language Administration module, the user will have the possibility to load his own language and have the DAC fully translated into the desired language.  
From the Vertical Toolbar select the Administration Languages menu item under the Administration group.

The list of languages to support is the following:

* **Distributed**: the language is available out of the box
* **Supported but not distributed**: it’s possible only to add the languages as business lables, but not system labels
* **Not supported**: it’s not possible to ass this language

| **Language** | **Distributed** | **Supported, not distributed** | **Not Supported** |
| :--- | :--- | :--- | :--- |
| English | ![:check\_mark:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/check_mark_64.png) |  |  |
| Italian | ![:check\_mark:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/check_mark_64.png) |  |  |
| French |  | ![](../../.gitbook/assets/image%20%285%29.png) |  |
| Chinese |  | ![](../../.gitbook/assets/image%20%285%29%20%283%29.png) |  |
| Spanish |  | ![](../../.gitbook/assets/image%20%285%29%20%2814%29.png) |  |
| Portuguese |  | ![](../../.gitbook/assets/image%20%285%29%20%282%29.png) |  |
| Hungarian |  | ![](../../.gitbook/assets/image%20%285%29%20%287%29.png) |  |
| Turkish |  | ![](../../.gitbook/assets/image%20%285%29%20%2813%29.png) |  |
| Polish |  | ![](../../.gitbook/assets/image%20%285%29%20%285%29.png) |  |
| German |  | ![](../../.gitbook/assets/image%20%285%29%20%2812%29.png) |  |
| Russian |  | ![](../../.gitbook/assets/image%20%285%29%20%288%29.png) |  |
| Swedish |  | ![](../../.gitbook/assets/image%20%285%29%20%284%29.png) |  |
| Bulgarian |  | ![](../../.gitbook/assets/image%20%285%29%20%2811%29.png) |  |
| Latvian |  |  | ![:cross\_mark:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/cross_mark_64.png) |
| Malaysian |  |  | ![:cross\_mark:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/cross_mark_64.png) |
| Japanese |  |  | ![:cross\_mark:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/cross_mark_64.png) |
| Korean |  |  | ![:cross\_mark:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/cross_mark_64.png) |
| Thilandese |  |  | ![:cross\_mark:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/cross_mark_64.png) |
| Vietnamese |  |  | ![:cross\_mark:](https://pf-emoji-service--cdn.us-east-1.prod.public.atl-paas.net/atlassian/cross_mark_64.png) |
| Czech |  | ![](../../.gitbook/assets/image%20%285%29%20%2815%29.png) |  |
| Danish |  | ![](../../.gitbook/assets/image%20%285%29%20%289%29.png) |  |
| Finland |  | ![](../../.gitbook/assets/image%20%285%29%20%2816%29.png) |  |
| Kazakstan |  | ![](../../.gitbook/assets/image%20%285%29%20%281%29.png) |  |
| Ukraine |  | ![](../../.gitbook/assets/image%20%285%29%20%2810%29.png) |  |
| India \(marathi\)\* |  | ![](../../.gitbook/assets/image%20%285%29%20%286%29.png) |  |

|  |
| :--- |


The label management window shows the list of languages present in the DAC, which can be applied for the multilingual system labels. For each language there is an identification code, the name of the language, the version number of the DAC and the date The last column contains the language management menu. For the English and Italian languages it is not possible to make any type of changes as they are the default languages in the system.

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/RunTime/LanguagesAdministration/1.png)

### How to import a new language

To load a new language select the button at the top left \(+\)

From the “Add a new language” panel, select one of the languages ​​supported by the system.

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/RunTime/LanguagesAdministration/2.png)

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/RunTime/LanguagesAdministration/3.png)

Notice that a new row has been inserted in the table for the chosen language.

The next step is to translate all system labels for the selected language.

![](https://dac-docs.s3-us-west-1.amazonaws.com/ImgSito/RunTime/LanguagesAdministration/4.png)

Access the menu and select “Export labels” to export the labels to an excel file. For each exported label, the translation must be entered.

It is recommended to keep the formatting of the downloaded file as any structural modification of the document would cause malfunction during the import phase. Therefore limit yourself to the translation of the label only.

Once all the labels have been translated, the file must be imported. The menu is accessed and the “Import Labels” item is selected and the file is associated. System labels are imported into the application for the selected language.

### How to update a language

The management of system labels also includes updating the labels in the loaded language. In case the existing labels have been imported in a version older than the current version, an update is required. Through the update button it will be possible to download the excel file containing only the labels introduced in the subsequent version \(s\) with respect to the language version. Once the translations have been entered, they will need to be imported using the Import Labels function.

