# getAssessorParcels-python
This python script gets tabular data and shapfiles and coverts the data to a File Geodatabase - in turn ready to load into ArcSDE.

Description/Purpose:
* This script automates the process of getting the latest version of the Assessor’s GIS parcel data.  The geography portion of their data is separate from the tabular portion of their data.
* The processing for this script is done locally in C:\temp\ParcelData.
* Note: Each step of the process is logged in a text file, and can be viewed at any time (even when running):  C:\temp\ParcelData\getParcelsLog.txt.

Step 1: Delete all existing data in folder.
Step 2: Create new file geodatabase, add table and appropriate fields.
Step 3: Copy Shapefile from Assessor’s shared directory into local temp directory.
Step 4: Download and extract (unzip) tabular portion of data via Assessor’s secure FTP site.
Step 5: Load tabular data into appropriate fields in newly-created FGDB table
Step 6: Join newly-created tabular data from FGDB to Shapefile in local directory
Step 7: Export Shapefile (retain the join) to the scratch FGDB in local directory.
Step 8: Kick-off .NET-console-app file to load this data into SDE. 
