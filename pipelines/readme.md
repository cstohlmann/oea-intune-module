# Pipeline

This pipeline copies and stores the raw Intune Reports data pulled via Graph API to Stage 1 datalake storage in CSV format.

The tutorial explaining how to set up this pipeline template to extract your own data, can be found [here](https://github.com/cstohlmann/oea-intune-module/tree/main/docs/documents).

<strong> Notes: </strong>
 - The pipeline template can be manually triggered to query data from the Intune Reports through Graph API. When triggered, the pipeline pulls data for all current devices connected within a education system. Intune devices report data is saved to Stage 1 of the data lake as a timestamp for the CSV filename.
 - It is recommended that you walk through the [Microsoft_Graph module](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules/Microsoft_Graph) prior to using this module, as many of the components for here (e.g. setting up a linked service to Graph API) relate to the Graph Reports API module.
