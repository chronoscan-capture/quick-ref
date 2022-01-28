
# Enterprise / Enterprise backup


> Since v1.0.2.68 <br/>Only for **administrator** users

!> Both your designated users for the WebServer service and the one for SQL Server service **must have** access and persmissions to the destination folder, otherwise the backup won't be able to generate

### New station configuration variable: <i>station_ent_bakup_dir</i>

* Determines the destination folder path for your enterprise backups
* Make sure the users designated for your services **have permissions on it**
* Default: <i>_%program_data%/EntBackups/</i>

### Generating a backup

To generate a backup for the current chronoscan enterprise configuration access your user drop down menu and select the _backup_ option

<img src="./_images_/ent-backup/menu.jpg" width="420" height="auto">  

#### Backup settings

<img src="./_images_/ent-backup/bak_sett.jpg" width="420" height="auto">  

You can choose if you only want to backup the file system chronoscan configuration. (This is all the directory structure of your ProgramData) and the SQL database.

> Omiting the WorkDir directory is highly recommended since that directory is usually too big

After selecting desired backup click on Accept and your backup will start generating.

<img src="./_images_/ent-backup/bak_prog.jpg" width="420" height="auto">  


> Creating a backup this way might take several minutes, depending on the size of the files to backup and the database and the application can't be used until finished or canceled

If everything is correct a zip file named '**entbak_{yyyymmddhhmmss}.zip**' will be generated in the specified path.

<img src="./_images_/ent-backup/bak_dir.jpg" width="420" height="auto"  class="border bordered">  




