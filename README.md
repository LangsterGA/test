# ArcGIS Pro Resources for Go.Data users

## Go.Data SITREP Toolbox for ArcGIS Pro
Pro Toolbox
{: .label .label-purple }

[`GoData ArcGISPro SITREP`](https://github.com/WorldHealthOrganization/godata-ESRI-SITREP-toolbox) toolbox was developed by the Go.Data team for GIS users to access case and contact data and automate the process of generating situation report (SITREP) maps during an outbreak investigation managed with Go.Data. From within ArcGIS Pro, the toolbox allows a GIS user to extract raw case and contact data and generate pre-programmed variable summaries, with the option to join to GIS data. The summary data can then be used to develop multiple common SITREP maps. Raw data is also extracted and can be explored for further potential maps or geospatial analysis. 

The toolbox has an operational impact because it bypasses the need for a GIS user to be familiar with the Go.Data system or to have to wait for data to be distributed from others. This is important when you are producing the same maps on a daily basis throughout the course of an outbreak response. The user simply logs into Go.Data via the toolbox dialog, extracts, summarizes, and joins to a GIS layer supplied by the user.

SITREP map products can be used in briefing and status documents, or printed and used as reference during field operations. Maps can be shared as images and be incorporated into SITREP publications or incident management slide shows and operations dashboards. More details about the SITREP summary files, as well as some sample SITREP maps, are located further down on this page.

![GoData](/images/ToolBoxAnime.gif)

## Toolbox prerequisites 
A Go.Data outbreak administrator must add you as a user to Go.Data and provide you the information below. Currently, the toolbox works with server-based installations of Go.Data. 
- ***Go.Data URL***: The URL of your server where Go.Data is, for example: "https://godata.moh.org/"
- ***Username***: The email address you use as a user name to access Go.Data (the administrator sets this in Go.Data)
- ***Password***: The password you use to access Go.Data - if you are using the password for the first time, log into the Go.Data URL in a browser and you will be prompted to change your password. Then use the new password with this toolbox. If you don't do that step - the tool may not function.
- ***Outbreak***: The name of the outbreak you want to extract data for. Within the toolbox dialog, a drop-down list will populate with outbreaks you have been given access to by the outbreak administrator.
- ***GIS layer (optional)***: GIS layer with a unique identifier that matches the Go.Data summary data unique identifier field (LocationID). This is only necessary if you are joining summary data ouput to a GIS layer. The user must provide this layer - no data is provided with this toolbox. Some GIS data sources are referenced on this [page](https://worldhealthorganization.github.io/godata/locations/#using-gis-data-as-a-source-for-your-location-data).

## Step 1: Download the Go.Data ArcGIS Pro SITREP toolbox from [here](https://github.com/WorldHealthOrganization/godata-ESRI-SITREP-toolbox)
## Step 2:  Open ArcGIS Pro and add the toolbox to your project
[To do this](https://pro.arcgis.com/en/pro-app/latest/help/projects/connect-to-a-toolbox.htm), go to the “View” tab on the ribbon and click on the “Catalog Pane” icon. In your catalog pane, right-click on the “Toolboxes” item, select “Add Toolbox”, and then navigate to the folder where you downloaded the toolbox to add it.

![GoData](/images/OpenSITREP.PNG)

## Step 3: Open "Create SITREP tables" dialog
Right-click and select 'Open'.

## Step 4: Fill in the required parameters ***(first five items)***
Add the link to the Go.Data site and your user name (email) and, after typing your password, hit the tab button and the next item (Outbreak) will populate with the outbreaks you have access to. Sometimes this can be a little slow - depends on your internet speed. The tool is accessing the Go.Data site via API endpoints using your credentials. Once the drop-down shows values, select the outbreak you want to extract data for and then specify the folder you want the raw csv file outputs written.

![GoData](/images/DialogCompleteFinal_75.png)
## Step 5: Fill in optional Summary data parameters
Specify folders where you want to store your summary csv outputs. Please note that you do not have to generate summary data - you can just extract raw data with the tool and end with the previous step. However, if you want to join summary files to GIS using this tool, you have to use the output summary files option. Also, if you are generating summary data, you must also specify a file geodatabase to write the summary tables (it will also create csvs). If you join to a GIS layer, the features classes that are created are written here too. Even if you do not join summary data to GIS, you must specify a file geodatabase (it will create tables there). It can be an existing one, or you can create a new one prior to running tool.

## Step 6. Fill in optional Join to Geography parameters
Specify the GIS layer that you want the summary table to join to. Note that the summary data has been programmed to summarize by the lowest level of geography used in the Go.Data system. So, if data was collected by administrative unit area level 2, then that is the level summarized. The summary data will include the location ID for the administrative areas that the system was set up with. That is the field that will be used to join to your GIS data. You will need to make sure that field matches the unique identifier in your GIS data prior to the join. If so, select the field in the GIS layer that matches the summary table locationID. If you aren't sure, just run the tool without joining to see the values in the Location ID field. Compare those with your GIS dataset and proceed accordingly - you may need to manually manipulate the data to match fields for a join.

## Description of tool outputs
The most basic output of the tool is an extract of the core epi variables within the case and contact APIs available with Go.Data. There are many more variables that can be extracted by other means and analyzed and they will vary based on the type of outbreak. Optionally, with this tool you can also generate a set of summary tables in csv format, and as tables in a file geodatabase. Optionally, if the user has a GIS dataset with a unique identifier that matches the 'locationID' field in the summary tables, the tool will join and create new feature classes for each SITREP summary theme. 

The following are what the output looks like if you use the tool fully.

Five csvs of raw outbreak data.

![GoData](/images/RawCSVs.PNG)

Four SITREP summary tables with 16 calculated fields, each of which could be used to create separate maps.

![GoData](/images/SummaryCSVs.PNG)

Four feature classes in the file geodatabase provided by user. Each feature classe includes its associated summary data.

![GoData](/images/FGDB.PNG)

## SITREP summary metadata

## Sample SITREP maps

## Other things to note...


If you would like more information or if you have feedback, please email godata@who.int and add "GIS:" at the beginning of the subject line. If you are experiencing a bug or have a feature request, please submit an issue [here](add link to where Pro issues can be submitted if we want to do this)
