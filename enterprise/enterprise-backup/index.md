
# Enterprise / Enterprise backup


> Since v1.0.2.68 <br/>Only for **administrator** users

!> Both your designated users for the WebServer service and the one for SQL Server service **must have** access and persmissions to the destination folder, otherwise the backup won't be able to generate

### New station configuration variable: <i>station_ent_bakup_dir</i>

* Determines the destination folder path for your enterprise backups
* Make sure the users designated for your services **have permissions on it**
* Default: <i>_%program_data%/EntBackups/</i>

### 1. Generating a backup from the application

To generate a backup for the current chronoscan enterprise configuration access your user drop down menu and select the _backup_ option

<img src="./_images_/ent-backup/menu.jpg" width="420" height="auto">  

#### Backup settings

<img src="./_images_/ent-backup/bak_sett.jpg" width="420" height="auto">  

You can choose if you only want to backup the file system chronoscan configuration. (This is all the directory structure of your ProgramData) and the SQL database.

> Omiting the WorkDir directory is highly recommended since that directory is usually too big. _WorkDir contains the images, pdfs, tiffs, ocr files, etc. of your batches_.

After selecting desired backup click on Accept and your backup will start generating.

<img src="./_images_/ent-backup/bak_prog.jpg" width="420" height="auto">  


> Creating a backup this way might take several minutes, depending on the size of the files to backup and the database and the application can't be used until finished or canceled

If everything is correct a zip file named '**entbak_{yyyymmddhhmmss}.zip**' will be generated in the specified path.

<img src="./_images_/ent-backup/bak_dir.jpg" width="420" height="auto"  class="border bordered">  

> If the back Up from the application takes too long or the database timesout, we recommend making a backup manually (_Next section_)


### 2. Generating a backup manually

To generate a backup manually follow this steps:

* Create a container folder for your back Up

**For the file system:**

* Go to the ProgramData directory for your ChronoScan configuration
* Copy the entire folder in your container folder
    * Omitting WorkDir is recommended

**For the Database:**

* Go to the machine where Sql server is installed
* Open Sql Server Manager Studio
* Right click on the desired database > select tasks > select back Up...

<img src="./_images_/ent-backup/sql_man_bak.jpg" width="420" height="auto">  

* Copy the .bak generated file in your container folder
* Zip your container folder. (Recommended)







