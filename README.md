# Microsoft Intune Reports Module
Microsoft Intune is a cloud-based service that focuses on the management of devices connected to a system. Microsoft Intune provides a wealth of options, from setting up which websites the devices within a system can access, to extracting data of all the devices linked to that system through the management of Microsoft Graph API endpoints. For the purpose of this module, we will be focusing on the collection and use of the "devices" data within Azure Synapse Analytics. 

You can use this Open Education Analytics (OEA) Microsoft Intune Reports module to ingest device data into your organization's data lake to get a real time view of student use of devices especially outside physical school to ensure all students have sufficient ‘digital access’ for learning. This can also be combined with school and  class rosters, attendance, and grades from Student Information Systems to produce visualizations that help with intervention targeting. 
 
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

  - Which devices are linked to an education system.
     * Number of students with more than one device
     * Day and time of day of last device check in
     * Number of devices based on different OSs (i.e. Windows, iOS/iPadOS, macOS, Android)
     * Number of devices based on ownership (i.e. Corporate/School, Personal, Unknown)

This dashboard example represent only data from Microsoft Intune. When this data is combined with other data sources, they can illustrate how device patterns can relate to student demographics, etc. With such combined data, education systems can start to analyze whether new programs or interventions help to improve teaching and learning with digital tools.  

## Module Setup and Data Sources
### Data Sources
<strong><em> Description of data sources: what it is used for, data available, data format, possible use cases or OEA packages it can be used for. </strong></em>
 - Microsoft Intune Reports is used to collect "devices" data, as mentioned above. The data available includes all devices connected within a system, as well as the primary user user principal name (UPN) connected to the device, and their last check in date/time on this device. 
 - This data is formatted in CSV files; both the sample datasets and the your own data ingested through the pipeline are landed in this format. 

### Module Setup
<strong><em> Explanation of how to use the module: prerequisites (like subscriptions), what types of data transfer services can be used to ingest in OEA. </strong></em>
 - You will need a subscription to Microsoft Intune or Office 365 (for Education), in order to access the Intune data used in this module: [click here to learn more about how to sign up Intune for Education purposes](https://www.microsoft.com/en-us/education/intune).
 1. Import the [Graph Reports API pipeline template for Intune](https://github.com/cstohlmann/oea-intune-module/tree/main/pipelines) into your Synapse workspace, connect a Graph API linked service, and trigger the pipeline.
 2. Load and run the [Intune Reports module notebook](https://github.com/cstohlmann/oea-intune-module/tree/main/notebooks) into your Synapse workspace. Two spark databases (s2np_intune and s2p_intune) will be created.
 3. Download the Power BI template file [Intune Reports Module Dashboard](https://github.com/cstohlmann/oea-intune-module/tree/main/powerbi) and connect to your Synapse workspace serverless SQL endpoint. We recommend using a directQuery from the s2p_intune database.
 
## Module Components
Out-of-the box assets for this OEA module include: 
1. [Tutorial/Instructions](https://github.com/cstohlmann/oea-intune-module/tree/main/docs/documents): A tutorial and instructions of how to use this module within your own Synapse workspace, as well as demonstration to build custom queries to pull data for your education tenant from Microsoft Intune via Microsoft Graph Reports API.
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
Microsoft and any contributors grant you a license to the Microsoft documentation and other content in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode), see the [LICENSE](https://github.com/microsoft/OpenEduAnalytics/blob/main/LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the [LICENSE-CODE](https://github.com/microsoft/OpenEduAnalytics/blob/main/LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries. The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks. Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents, or trademarks, whether by implication, estoppel or otherwise.
