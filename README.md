# ArcGIS Pro Resources for Go.Data users

## Go.Data SITREP Toolbox for ArcGIS Pro
Pro Toolbox
{: .label .label-purple }

[`GoData ArcGISPro SITREP`](https://github.com/LangsterGA/godata2arcgis) toolbox was developed by the Go.Data team to access case and contact data and automate the process of generating situation report (SITREP) maps during an outbreak investigation managed with Go.Data. From within ArcGIS Pro, the toolbox allows a GIS user to extract raw case and contact data and generate pre-programmed variable summaries, with the option to join to GIS and be used to develop a multitude of common SITREP maps. It bypasses the need for a GIS user to be familiar with the Go.Data system or to have to wait for data to be distributed from others, which is important when you are producing the same maps on a daily basis throughout the course of an outbreak response. The user simply logs into Go.Data via the toolbox dialog, extracts, summarizes, and joins to a GIS layer supplied by the user.

SITREP map products can be used in briefing and status documents, or printed and used as reference during field operations. Maps can be shared as images and be incorporated into SITREP publications or incident management slide shows and dashboards. More details about the SITREP summary files, as well as some sample SITREP maps, are located here [<add link to github repo where more detailed info about summary tables should be shown].


![GoData](/images/ToolBoxAnime.gif)

## Toolbox prerequisites 
The Go.Data outbreak administrator must add you as a user to Go.Data and provide you the information below. Currently, the toolbox works with server-based installations of Go.Data. (Do they need to sign into Go.Data once and change their pass?)
- ***Go.Data URL***: The URL of your server where Go.Data is, for example: "https://godata.moh.org/"
- ***Username***: The email address you use as a user name to access Go.Data
- ***Password***: The password you use to access Go.Data
- ***Outbreak***: The name of the outbreak you want to extract data for. Within the toolbox dialog, a drop-down list will populate with outbreaks you have been given access to by the outbreak administrator.

## Step 1: Download the Go.Data ArcGIS Pro toolbox from [here](https://github.com/LangsterGA/test)
## Step 2:  Open ArcGIS Pro and add the toolbox to your project
[To do this](https://pro.arcgis.com/en/pro-app/latest/help/projects/connect-to-a-toolbox.htm), go to the “View” tab on the ribbon and click on the “Catalog Pane” icon. In your catalog pane, right-click on the “Toolboxes” item, select “Add Toolbox”, and then navigate to the folder where you downloaded the toolbox to add it.
## Step 3: Open Create SITREP tables dialog
Right-click and select 'Open'.

![GoData](/images/dialogOpen.png)
## Step 4: Fill in the Go.Data-related parameters ***(first four items)***
After typing your password, hit your tab button and the Outbreak section will populate with the ones you have access to. Select the outbreak you want to extract data from.
## Step 5: Fill in output-related parameters
Specify folders where you want your raw csvs and your summary csvs. Please note that you do not have to generate summary data - you can just extract raw data with the tool. However, if you want to join to GIS using this tool, you have to use the Output summary files option. Also, if you are generating summary data, you must also specify a file geodatabase to write the summary tables. If you join to a GIS layer, the features classes that are created are written here too. Even if you do not join summary data to GIS, you must specify the file geodatabase. 

If you would like more information or if you have feedback, please email godata@who.int and add "GIS:" at the beginning of the subject line. If you are experiencing a bug or have a feature request, please submit an issue [here](add link to where Pro issues can be submitted if we want to do this)
