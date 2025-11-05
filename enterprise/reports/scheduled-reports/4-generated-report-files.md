
## Enterprise / Reports / Scheduled reports / 4. Generated report files

> All report files are excel format

Only one xls file is generated with the following name format:

* ${report_given_name}_YYYYMMDDhhmmss-${execution_type:(auto|manual)}.xls

This file contains 4 sheets:

<img src="./_images_/scheduled_reports/excel_sheets.jpg" width="520" height="auto" />

1. **Execution information**
    * Information about the task configuration and the executed process
2. **Report 1**
    * Corresponds to the main report
3. **Report 2**
    * Corresponds to the secondary report, usually the totals report
4. **SQL**
    * Sql command executed for the corresponding reports 


