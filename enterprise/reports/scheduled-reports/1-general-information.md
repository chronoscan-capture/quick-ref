
## Enterprise / Reports / Scheduled reports / 1. General information


!> **Scheduled reports run on the WebServer process** <br/>This process must be running for the scheduled reports tasks to execute correctly

* Available since ChronoScan version 1.0.2.67
* Only **administrators** can schedule reports
* Currently **two** reports can be scheduled
    * Reports 1 - Activity
    * Reports 2 - Workflow
* We can schedule as many views as we have saved for each report
* If you delete a view that has a scheduled task configured, the scheduled task will automatically disappear as well

#### How the processes are managed

* Any scheduled task will only work if the WebServer process is running:
    * If the server is down tasks won't be enqueued, therefore those reports won't be generated
* When a scheduled task changes to '**PENDING**' state the current process Id will be assigned to it:
    * If that process ends but antoher process starts and the task is still pending, the new process will take over that task and the new process will be assigned to it
* When a scheduled task is '**RUNNING**' and the process server goes down:
    * In this case the task will result on an error since the process that was executing ended on the meantime
* Tasks **timeout after 10 minutes** on '**RUNNING**' state

> More info about this on [3. Managing and monitoring scheduled reports tasks](./enterprise/reports/scheduled-reports/3-managing-and-monitoring-scheduled-reports-tasks) but is recommended to read the documentation on this order:

* 1. General information (_You are here_)
* [2. How to schedule a report](./enterprise/reports/scheduled-reports/2-how-to-schedule-a-report)
* [3. Managing and monitoring scheduled reports tasks](./enterprise/reports/scheduled-reports/3-managing-and-monitoring-scheduled-reports-tasks)

