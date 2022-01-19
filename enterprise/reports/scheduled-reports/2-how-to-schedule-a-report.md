
## Enterprise / Reports / Scheduled reports / 2. How to schedule a report

To schedule a report go to the Reports menu and **select the desired report**.  

Currently we can schedule two reports:
* Reports 1 - Activity
* Reports 2 - Workflow

Once we are on the desired report, we will see the <b>new 'Schedule report' button</b>:

<img src="./_images_/scheduled_reports/btn_schedule.jpg" width="520" height="auto">  

> When we click on the **Schedule report** The following can happen:

1. We get an alert if the current view we are working on is not saved yet. **Only saved views can be scheduled** so we won't be able to until we save it
2. A dialog window opens to create or edit (if the view is already scheduled) the scheduled task for the current view

    <img src="./_images_/scheduled_reports/dialog_schedule1.jpg" width="520" height="auto">  
    <br/>
    <span class="caption">Task editor window</span>

## Form settings explanation
<br/>

| Setting                   | Description                       |
|---------------------------| ----------------------------------|
| **Starting date**         | The starting date for the task to start yyyy-mm-dd |
| **Time**                  | The stating time for the task to start hh:mm |
| **Repeat task**           | <ul><li>If checked, the task becomes **Recurring** so it will repeat according to the **Repeat every** configuration</li> <li>If unchecked, the task is considered **Scheduled** and will only execute **once** </li></ul> |
| **Repeat every**          | If the task is **Recurring** we choose here the running interval for it: <ul><li>Month</li><li>Week</li><li>Day</li><li>Hour</li></ul> |
| **Destination directory** | <ul><li>Folder were we want the report file to be generated on </li><li>**Default directory is:** &nbsp;&nbsp;&nbsp;&nbsp;%program_data_dir%/TempReports/Scheduled </li><li> If you choose a diferent destination, make sure you it has writing permissions on it from the machine you are configuring the task, otherwise the report won't be able to generate </li> |
| **File name**             | <ul><li>Desired file name for generated report</li><li>**Default filename is** ${report_identifier}.${view_name}.xls</li> <li>File name will always be **automatically appended** with the following string:<ul><li>timestamp with format: **_YYYYMMDDhhmmss-${execution_type}** </li><li>Where ${execution_type} can be: <ul><li>**auto**: If the execution has been automatic</li><li>**manual**: If the execution has been triggered by an user</li></ul></li></ul></li> </ul>             |
| **Send via E-mail**       | <ul><li>If checked, the generated report for this task will also be sent via E-mail to desired recipients</li><li>**It requires the SMTP configuration for sending E-mails to be correctly configured**</li></ul> |
| **Recipient**             | Desired recipients <ul><li>Can be selected from the drop down</li><li>Can also be manually entered</li><li>*Separate E-mail addresses with a semicolon ';' for multiple recipients</li></ul> _**E-mail addresses must be a valid chronoscan user**_  |
| **Active**                | Activates o deactivates the task |


> Info: Whenever one of these fields are changed; **Starting date**, **Time**, **Repeat task** or  **Repeat every** the 'Next execution information panel' will be refreshed to know when the task will be executed 

<img src="./_images_/scheduled_reports/next_exec_info_panel.jpg" width="520" height="auto">  
<br/>
<span class="caption">Next execution information panel</span>

!> Remeber to hit the 'Save' button when settings are changed and want to be applied

> All scheduled tasks can be managed and monitored on the '[Scheduled reports](./enterprise/reports/scheduled-reports/3-managing-and-monitoring-scheduled-reports-tasks)' section (_See next page_)
