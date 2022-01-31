# ArcGIS Pro Resources for Go.Data users

## Go.Data SITREP Toolbox for ArcGIS Pro
Pro Toolbox
{: .label .label-purple }

[`GoData ArcGISPro SITREP`](https://github.com/LangsterGA/godata2arcgis) toolbox was developed by the Go.Data team to access case and contact data and automate the process of generating situation report (SITREP) maps during an outbreak investigation managed with Go.Data. From within ArcGIS Pro, the toolbox allows a GIS user to extract raw case and contact data and generate pre-programmed variable summaries, with the option to join to GIS and be used to develop a multitude of common SITREP maps. It bypasses the need for a GIS user to learn how to retrieve data from within the Go.Data system or to have to wait for data to be distributed from others. The user simply logs into Go.Data via the toolbox dialog and extracts, summarizes, and joins data to a GIS layer supplied by the user.

SITREP map products can be used in briefing and status documents, or printed and used as reference during field operations. Maps can be shared as images and be incorporated into SITREP publications or incident management slide shows and dashboards. More detailed information about the SITREP summary files, which fuel the maps, is located here [<add link to github repo where more detailed info about summary tables should be shown].


![GoData](/images/ToolBoxAnime.gif)

## Toolbox prerequisites 
The Go.Data outbreak administrator must provide you the information below. Currently, the toolbox only works with server-based installations of Go.Data. (Do they need to sign into Go.Data once and change their pass?)
- ***Go.Data Server URL***: The URL of your server where Go.Data is
- ***Email address***: The email address you use to access Go.Data
- ***Password***: The password you use to access Go.Data
- ***Outbreak name***: You will have the option to choose which outbreak to extract from. The list will only populate with outbreaks you have been given access to by the outbreak administrator.

## Step 1: Download the Go.Data ArcGIS Pro toolbox from [here](https://github.com/LangsterGA/test)

If you would like more information or if you have feedback, please email godata@who.int. If you are experiencing a bug or have a feature request, please submit an issue [here](https://github.com/WorldHealthOrganization/godataR/issues)
