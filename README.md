# Microsoft Intune Module
Microsoft Intune is a cloud-based service that focuses on the management of devices connected to a system. Microsoft Intune provides a wealth of options, from setting up which websites devices within a system can access, to extracting data of the devices linked to that system through the management of Microsoft Graph API endpoints. For the purpose of this module, we will be focusing on the collection and use of the "devices" data within Azure Synapse Analytics. 

You can use this OEA Microsoft Intune module to incorporate device data into your organization's OEA data lakes.
 
 ![alt text](https://github.com/cstohlmann/oea-intune-module/blob/main/docs/images/Intune%20visual.png)
 <p align="center">
 <emp>
 (Microsoft documentation on Intune: https://docs.microsoft.com/en-us/mem/intune/fundamentals/what-is-intune) 
 </emp>
 </p>

## Problem Statement
As education systems and institutions begin to incorporate more digital forms of learning, understanding the number of students without access to devices outside of school is vital. This "devices" data can be combined with other data sources (such as Azure Active Directory or M365 Insights data), to more accurately analyze which students do not have access to devices outside of school, or how demographics correlates with students that don't have access to devices outside of school, for example. 

Microsoft Insights data can be used for many different education purposes:
  - Education system leader reports on the number of students with multiple devices registered.
  -	School dashboards on a statistical breakdown of operating systems (OSs) being used.
  -	Class dashboards for teachers to see a statistical breakdown of students’ that do and do not have access to devices outside of school.

Pulling data using this Microsoft Intune module provides solutions to these scenarios, as well as many more instances to extract the devices used for and within school systems.

## Module Impact 
This Microsoft Intune module for OEA will leverage the Azure Synapse environment to aid education systems in bringing this data to their own Azure data lake for analysis. This includes a pipeline for extracting device data from Microsoft Intune through the Microsoft Graph API endpoint manager, providing a more detailed and accurate representation of student device accessibility outside of school. The PowerBI template included in this module can be used by system and school leaders to show:

  - Which devices are linked to the education system.
     * Number of students with more than one device
     * Day and time of day of last device check in
     * Number of devices based on different OSs (i.e. Windows, iOS/iPadOS, macOS, Android)
     * Number of devices based on ownership (i.e. School, Personal, Unknown)

This dashboard example represent only data from Microsoft Intune. When this data is combined with other data sources, they can illustrate how device patterns can relate to student demographics, etc. With such combined data, education systems can start to analyze whether new programs or interventions help to improve teaching and learning with digital tools.  

## Module Setup and Data Sources
 - Description of data sources: what it is used for, data available, data format, possible use cases or OEA packages it can be used for.
 - Explanation of how to use the module: prerequisites (like subscriptions), what types of data transfer services can be used to ingest in OEA
 
## Module Components
Sample out-of-the box assets for this OEA module include: 
1. [Tutorial](https://github.com/cstohlmann/oea-graph-api/blob/main/docs/documents/Graph%20Reports%20API%20Tutorial.pdf): A tutorial of how to use this module within your own Synapse workspace, as well as demonstration to build a custom pipeline to pull data for your education tenant from Microsoft Intune.
2. [Sample Datasets](https://github.com/cstohlmann/oea-intune-module/tree/main/datasets): Ingest sample data to understand the utility and functionality of the notebook(s).
3. [Pipeline(s)](https://github.com/cstohlmann/oea-intune-module/tree/main/pipelines): A pipeline which connects Microsoft Intune via Microsoft Graph API endpoint manager, to the Synapse workspace.
4. [Notebooks](https://github.com/cstohlmann/oea-intune-module/tree/main/notebooks): An example notebook on processing the data from stage 1 to stage 2 within Synapse. 
5. [PowerBI Templates](https://github.com/cstohlmann/oea-intune-module/tree/main/powerbi): A Power BI sample template making it easy to interact with Microsoft Intune data.

 <p align="center">
 <strong><em> (INSERT POWERBI DASHBOARD VISUAL HERE) </strong></em>
 </p>
 
The Microsoft Intune module [welcome contributions](https://github.com/microsoft/OpenEduAnalytics/blob/main/CONTRIBUTING.md).

This module was developed by [name of contributor] in partnership with [name of education system, if any]. The architecture and reference implementation for all modules is built on [Azure Synapse Analytics](https://azure.microsoft.com/en-us/services/synapse-analytics/) - with [Azure Data Lake Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction) as the storage backbone, and [Azure Active Directory](https://azure.microsoft.com/en-us/services/active-directory/) providing the role-based access control.

### Additional Information
Provide any additional information and resources.

# Legal Notices
Microsoft and any contributors grant you a license to the Microsoft documentation and other content in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode), see the [LICENSE] file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the [LICENSE-CODE] file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries. The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks. Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents, or trademarks, whether by implication, estoppel or otherwise.
