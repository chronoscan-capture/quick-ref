

## Enterprise / Reports / Scheduled reports / 3. Managing and monitoring scheduled reports tasks

Under the Reports menu on the aplication top menu, we now have the option **Scheduled reports**.

<img src="./_images_/scheduled_reports/menudd.jpg" width="520" height="auto" />  

when we enter this option, we will be able to manage and monitor the existing scheduled tasks

<img src="./_images_/scheduled_reports/scheduled_tasks_manager.jpg" width="520" height="auto" />  
<br/>
<span class="caption">Managing and monitoring scheduled tasks</span>

On the table we have the following information for each task and a column for different actions.  
If this report is empty, there are no scheduled tasks created yet. To schedule reports check the documentation: [2. How to schedule a report](./enterprise/reports/scheduled-reports/2-how-to-schedule-a-report)

### Information columns

* Report name
* Original view name
* Report filename
* Type of task (scheduled/recurring)
* Repeating interval
* **Last execution date**
<ul>
    <li><img src="./_images_/wci_icons/24x24/check.png" width="18" height="auto" /> Succesful execution</li>
    <li><img src="./_images_/wci_icons/24x24/stopwatch2.png" width="18" height="auto"/> Execution in process</li>
    <li><img src="./_images_/wci_icons/24x24/error.png" width="18" height="auto" /> Unsuccesful execution</li>
</ul>
* **Next execution date**
* Active

### Action columns

<img src="./_images_/scheduled_reports/actions.jpg" width="161" height="auto" />
<br/>
<span class="caption">Actions column</span>

<ul>
    <li><img src="./_images_/wci_icons/24x24/folder.png" width="18" height="auto" /> <b>Open destination folder</b></li>
    <li>
        <img src="./_images_/wci_icons/24x24/gearwheel.png" width="18" height="auto">  
        <b>Open <a href="#/./enterprise/reports/scheduled-reports/2-how-to-schedule-a-report?id=form-settings-explanation" target="_blank"> task editor window </a></b>
    </li>
    <li>
        <img src="./_images_/wci_icons/24x24/spreadsheed_data.png" width="18" height="auto" /> <b>Open executions report for the task</b>  
        <ul style="margin-top: 6px;">
            <li style="list-style-type: none;">
                <img src="./_images_/scheduled_reports/executions_report.jpg" width="520" height="auto" />
                <br/>
                <span class="caption">Executions report</span> 
                <br/>
                <h4>Relevant information on this report</h4>
                The column '<b>status</b>' can be:
                <ul>
                    <li><b>PENDING:</b> The task entered the enqueued state, this happens 10 minutes before the execution date and is waiting for the exact <b>Next execution</b> date to start running</li>
                    <li><b>RUNNING:</b> The task is actually running</li>
                    <li><b>FINISHED:</b> The task ended successfuly</li>
                    <li><b>ERROR:</b> The task did't finish successfully and an error occurred. An error log will explain on the the column '<b>error_log</b>'</li>
                </ul>
                The column '<b>Emailing status</b>' can be:
                <ul>
                    <li><b>[Sent to] configuration is off</b>: This means send report via E-mail is not active</li>
                    <li>
                        <b>(recipient e-mail address) (operation status):</b>
                        <ul>
                            <li><b>(success)</b>: E-mail sent</li>
                            <li><b>(error)</b>: Emai couldn't be sent</li>
                            <li><b>(denied)</b>: E-mail not sent, entered E-mail is not a valid chronoscan user</li>
                        </ul>
                    </li>
                </ul>
            </li>
        </ul>
    </li>
    <li><img src="./_images_/wci_icons/24x24/media_play.png" width="18" height="auto" /> <b>Trigger the task manually</b></li>
</ul>

### How the tasks processes are managed

!> **Scheduled reports run on the WebServer process** <br/>This process must be running for the scheduled reports tasks to execute correctly

* This means that any scheduled task will only work if the WebServer process is running:
    * If the server is down tasks won't be enqueued, therefore those reports wont be generated
* When a scheduled task changes to '**PENDING**' state the current process Id will be assigned to it:
    * If that process ends but antoher process starts and the task is still pending, the new process will take over that task and the new process will be assigned to it
* When a scheduled task is '**RUNNING**' and the process server goes down:
    * In this case the task will result on an error since the process that was executing it ended on the meantime
* Tasks **timeout after 10 minutes** on '**RUNNING**' state



