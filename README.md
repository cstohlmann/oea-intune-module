# Microsoft Intune Module
Microsoft Intune is a cloud-based service that focuses on the management of devices connected to a system. Microsoft Intune provides a wealth of options, from setting up which websites devices within a system can access, to extracting data of the devices linked to that system through the management of Microsoft Graph API endpoints. For the purpose of this module, we will be focusing on the collection and use of that device data within Azure Synapse Analytics. 

You can use this OEA Microsoft Intune module to incorporate device data into your organization's OEA data lakes.
 
 ![alt text](https://github.com/microsoft/OpenEduAnalytics/blob/main/modules/Microsoft_Graph/docs/images/Graph%20visual.png)
 <p align="center">
 <emp>
 (Microsoft documentation on Intune: https://docs.microsoft.com/en-us/mem/intune/fundamentals/what-is-intune) 
 </emp>
 </p>

## Problem Statement
Define the problem you seek to solve using this module.

## Module Impact 
List out the impact and benefits this module will have on learners, educators and the learning process.

## Module Setup and Data Sources
 - Description of data sources: what it is used for, data available, data format, possible use cases or OEA packages it can be used for.
 - Explanation of how to use the module: prerequisites (like subscriptions), what types of data transfer services can be used to ingest in OEA
 
## Module Components
Sample out-of-the box assets for this OEA module include: 
1. [Tutorial](https://github.com/cstohlmann/oea-graph-api/blob/main/docs/documents/Graph%20Reports%20API%20Tutorial.pdf): A tutorial of how to use this module within your own Synapse workspace, as well as demonstration to build custom queries to pull data for your education tenant from Microsoft Graph Reports API.
2. [Sample Datasets](https://github.com/cstohlmann/oea-intune-module/tree/main/datasets): Ingest sample data to understand the utility and functionality of the notebook(s).
3. [Pipeline(s)](https://github.com/cstohlmann/oea-intune-module/tree/main/pipelines): A pipeline which connects Microsoft Graph Reports API to the Synapse workspace.
4. [Notebooks](https://github.com/cstohlmann/oea-intune-module/tree/main/notebooks): An example notebook on processing the data from stage 1 to stage 2 within Synapse. 
5. [PowerBI Templates](https://github.com/cstohlmann/oea-intune-module/tree/main/powerbi): A Power BI sample template making it easy to interact with Microsoft Graph Reports API data.

 <p align="center">
 (INSERT POWERBI DASHBOARD VISUAL HERE) 
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
