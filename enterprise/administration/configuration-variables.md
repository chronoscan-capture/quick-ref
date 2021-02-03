# Enterprise / Administration / Configuration variables


> ## System parameters (wci_params)
----

* #### **Logfile**
    * _Log files are located under folder C:\chronoscanlog\_  
    * [ ] Logfile OFF
    * [X] Logfile ON
    > **Note:** Having the log file enabled may affect the application performance
* #### **md5salt**
    * _Type_: String | Readonly
    * _Description_: Encrypt hash
    * _Default_: Auto-generated md5 hash
* #### **wci_batches_panel_allow_operators_delete_batches**
    * _Type_: Boolean
    * _Description_: [Allow|Do not allow] [operator|indexer|editor] users to delete batches on the 'Batches' tab section of the application
    * _Default_: false
* #### **wci_dashboard_allow_filtering_by_imap_fields**
    * _Type_: Boolean
    * _Description_: [Allow|Do not allow] Filtering the dashboard batches lists by [IMAP Senders|IMAP Recipients] 
    * _Default_: false
    * _Image_ <br /><img src="./_images_/imap_filters.png" width="420" height="auto">
* #### **wci_dashboard_autorefresh_seconds**
    * _Type_: Number
    * _Description_: It determines the time (**in seconds**) that the dashboard information takes to auto-refresh
    * _Default_: 5
* #### **wci_dashboard_hide_export_error_batches_for_nonadmin**
    * _Type_: Boolean
    * _Description_: If set to _true_, non admin users won't see batches with errors under the ready to export dashboard inbox list
    * _Default_: false
* #### **wci_dashboard_max_items**
    * _Type_: Number
    * _Description_: It determines the number of records per page to show in the dashboard inboxes lists
    * _Default_: 100
    * _Image_: _*In this example the variable has been set to 5_ <br /><img src="./_images_/max_items_dashboard.png" width="420" height="auto"> 
* #### **wci_diagnosis_input_server_url**
    * _Type_: String
    * _Description_: Url for opening the diagnosis and information web application for the _Input server_
    * _Default_: http://localhost:9007/
* #### **wci_diagnosis_output_server_url**
    * _Type_: String
    * _Description_: Url for opening the diagnosis and information web application for the _Output server_
    * _Default_: http://localhost:9009/
* #### **wci_diagnosis_proc_server_url**
    * _Type_: String
    * _Description_: Url for opening the diagnosis and information web application for the _Processing server_
    * _Default_: http://localhost:9008/
* #### **wci_indexview_max_session_timeout_seconds**
    * _Type_: Number
    * _Description_: If the index view remains without user activity for longer than this time (**in seconds**), current batch will be saved and current session will be closed.
    * _Default_: 360
* #### **wci_input_root**
    * _Type_: String
    * _Description_: Root directory for hotfolder configurations
    * _Default_: C:\WCI_INPUT_ROOT
* #### **wci_instance_title**
    * _Type_: String
    * _Description_: Name for enterprise instance title
    * _Default_: Your configuration name
* #### **wci_license_number**
    * _Type_: String
    * _Description_: License number information
    * _Default_: 
* #### **wci_lists_max_page_values**
    * _Type_: Number
    * _Description_: Number of items to appear on fields with lists on [Search|Characters introduction]
    * _Default_: 15
    * _Image_: _*In this example the variable has been set to 2_ <br /><img src="./_images_/wci_lists_max_page_values.png" width="420" height="auto"> 
* #### **wci_mainurl**
    * _Type_: String
    * _Description_: Url for enterprise Web application
    * _Default_: http://localhost:10000
* #### **wci_max_log_days**
    * _Type_: Number
    * _Description_: If greater than 0, the table containing logs will only keep records that are greater than today minus *value* days
    * _Example_: If you just want to keep log records for the last 7 days, set this value to 7
    * _Default_: -1 (Disabled)
* #### **wci_max_smtp_notifications_days**
    * _Type_: Number
    * _Description_: If greater than 0, the table containing smtp notifications will only keep records that are greater than today minus *value* days
    * _Example_: If you just want to keep smtp notification records for the last 7 days, set this value to 7
    * _Default_: -1 (Disabled)
* #### **wci_max_system_notifications_days**
    * _Type_: Number
    * _Description_: If greater than 0, the table containing system notifications will only keep records that are greater than today minus *value* days
    * _Example_: If you just want to keep system notification records for the last 7, set this value to 7
    * _Default_: -1 (Disabled)
* #### **wci_scan_plugin_directory**
    * _Type_: String
    * _Description_: <a href="https://www.chronoscan.org/wcidoc/running_chronoscan_web_server_through_a_reverse_proxy__helicon_ape__print.htm" target="_blank">See docs</a>
    * _Default_: &lt;&lt;default&gt;&gt;
* #### **wci_scan_plugin_host**
    * _Type_: String
    * _Description_: <a href="https://www.chronoscan.org/wcidoc/running_chronoscan_web_server_through_a_reverse_proxy__helicon_ape__print.htm" target="_blank">See docs</a>
    * _Default_: &lt;&lt;default&gt;&gt;
* #### **wci_spacedisk_warning_megabytes**
    * _Type_: Number
    * _Description_: Minimum amount in Megabytes for alert/notification of disk space being low
    * _Default_: 1000
    * _Image_: <br /><img src="./_images_/wci_spacedisk_warning_megabytes.png" width="420" height="auto"> 
* #### **wci_system_alert_IMAP_cnxfail**
    * _Type_: Boolean
    * _Description_: It [Activates|Deactivates] a system alert to notify when an IMAP connection fails.
    * _Default_: false
* #### **wci_system_alert_IMAP_cnxfail_Recipients**
    * _Type_: String
    * _Description_: Add recipients for this alert by system variables or valid email addresses. (Separated by semicolon (;) to add more than one)
    * _Default_: %station_admin_mail%
* #### **wci_system_alerts_email**
    * _Type_: Boolean
    * _Description_: It [Activates|Deactivates] global system alert email to %station_admin_email% that are notified on 'App toolbar / alerts'
    * _Default_: false
* #### **wci_system_database_version**
    * _Type_: String | Readonly
    * _Description_: It shows current database version for enterprise installation
* #### **wci_ui_header_ref**
    * _Type_: String 
    * _Description_: Url link to navigate when clicking on _wci_ui_header_title_ (Dashboard app toolbar application name)
    * _Deafult_: https://www.chronoscan.org
* #### **wci_ui_header_title**
    * _Type_: String
    * _Description_: Name to show on Enterprise app bar
    * _Default_: YOUR_CONFIGURATION_NAME
* #### **wci_ui_login_welcome_logo**
    * _Type_: String
    * _Description_: Html img element for the enterprise application logo to appear
    * _Default_: &lt;img src='wci/customerlogo.png'/&gt;
    * _Image_: <br /><img src="./_images_/logo_wci.png" width="220" height="auto"> 
* #### **wci_ui_main_title**
    * _Type_: String
    * _Description_: Explorer's tab title for enterprise web client
    * _Default_: YOUR_CONFIGURATION_NAME - Chronoscan Enterprise

> ## Global parameters
----

* #### **Amounts_correction**
    * _Type_: Boolean
    * _Description_: It [Activates|Deactivates] amounts correction for intelli-tags
    * _Default_: true

### **Notifications default parameters <i class="mdi mdi-arrow-down" style="color: #4d90fe;"></i>**
> These are global default configuration variables for every job notifications.  
Every one of them can be customized per job under 'Job / JOB_NAME / Notifications' section of the application.

!> It's important to know that if you want to add email addresses that are not system variables,  
the email has to belong to an user registered for the job the notification is active for

* #### **OnBatchCreated_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when new batches are created 
* #### **OnBatchCreated_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatchDeleted_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches are deleted 
* #### **OnBatchDeleted_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatchExportedWithErrors_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches are exporting and have validation errors
* #### **OnBatchExportedWithErrors_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatchExported_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches are exported correctly, without errors
* #### **OnBatchExported_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatchOpen_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches are open on the enterprise application
* #### **OnBatchOpen_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatchProcessed_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches are processed by the _Processing server_
* #### **OnBatchProcessed_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_New_documents_to_approve**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %job_approvers%
    * _Notification description_: It sends a notification when new batches change to the status <i>to_approve</i>
* #### **OnBatch_New_documents_to_approveActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_New_documents_to_configure**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %job_editors%
    * _Notification description_: It sends a notification when new batches enter the inbox status '_Batches waiting for configuration_'
* #### **OnBatch_New_documents_to_configureActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_New_documents_to_index**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %job_operators%
    * _Notification description_: It sends a notification when new batches enter the inbox status '_Batches waiting for manual index_'
* #### **OnBatch_New_documents_to_indexActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_New_documents_to_postclass**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %job_operators%
    * _Notification description_: It sends a notification when batches enter the status <i>poss_class</i>
* #### **OnBatch_New_documents_to_postclassActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_New_documents_to_preclass**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %job_operators%
    * _Notification description_: It sends a notification when batches enter the status <i>pre_class</i>
* #### **OnBatch_New_documents_to_preclassActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_ProcessingTime_LongerThan**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches take longer than specified on _OnBatch_ProcessingTime_LongerThanConditionalMinutes_ being processed
* #### **OnBatch_ProcessingTime_LongerThanActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_ProcessingTime_LongerThanConditionalMinutes**
    * _Type_: Number
    * _Description_: It conditions the notification for batches to take longer than this value when they process (Value is in minutes. It can be a decimal value, for instance to set it to 20 seconds = 0.33)
    * _Default_: 5
* #### **OnBatch_Status_[created]_WaitingFor**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches take longer than specified on inbox '_Batch(es) waiting to process_'
    * _Info_: The amount of time a batch has to be waiting to process in order to send the notification is configurable under 'Job / JOB_NAME / Notifications > event OnBatch_Status_[created]_WaitingFor > *minutes' column
* #### **OnBatch_Status_[created]_WaitingForActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_Status_[pre_class]_WaitingFor**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches take longer than specified on inbox '_Batch(es) waiting classification_'
    * _Info_: The amount of time a batch has to be waiting classification in order to send the notification is configurable under 'Job / JOB_NAME / Notifications > event OnBatch_Status_[pre_class]_WaitingFor > *minutes' column
* #### **OnBatch_Status_[pre_class]_WaitingForActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnBatch_Status_[ready_to_export]_WaitingFor**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when batches take longer than specified on inbox '_Batch(es) exports (Ready to export)_'
    * _Info_: The amount of time a batch has to be waiting on _ready to export_ in order to send the notification is configurable under 'Job / JOB_NAME / Notifications > event OnBatch_Status_[ready_to_export]_WaitingFor > *minutes' column
* #### **OnBatch_Status_[ready_to_export]_WaitingForActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnCommented_DocumentType_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when a document type has been commented
* #### **OnCommented_DocumentType_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnCommented_Document_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when a document has been commented
* #### **OnCommented_Document_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnDocumentImportError**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when an error ocurred while exporting
* #### **OnDocumentImportErrorActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnDocumentType_Configured_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when a document type has ben configured
* #### **OnDocumentType_Configured_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnDocumentType_NewType_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when a new document type has ben created
* #### **OnDocumentType_NewType_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnDocumentType_ToReview_Recipients**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when an existing document type has been set as 'To Review'
* #### **OnDocumentType_ToReview_RecipientsActive**
    * _Type_: Number [0|1]
    * _Description_: It [Activates|Deactivates] the notification
    * _Default_: 0 (Deactivated)
* #### **OnJob_Num_batches_to_index**
    * _Type_: String
    * _Description_: List of valid emails addresses or system variables to recieve this notification, separated by a semicolon
    * _Default_: %station_admin_mail%
    * _Notification description_: It sends a notification when n new number of batches are ready to index
    * _Info_: The conditional number and its activation is configurable under 'Job / JOB_NAME / Notifications > OnJob_Num_batches_to_index > *conditioned on number' and *active columns

> ### **End of notifications default parameters <i class="mdi mdi-arrow-up" style="color: #4d90fe;"></i>**

* #### **capture_date_search_year_max**
    * _Type_: Number
    * _Description_: Maximun date search on application
    * _Default_: 2040
* #### **capture_date_search_year_min**
    * _Type_: Number
    * _Description_: Minimum date search on application
    * _Default_: 1990
* #### **capture_dateformat**
    * _Type_: String
    * _Description_: Date format for dates recognition
    * _Default_: system
* #### **capture_decimalseparator**
    * _Type_: String
    * _Description_: Decimal separator for decimal separator recognition
    * _Default_: system
* #### **datatype_amount_default_decimals**
    * _Type_: String
    * _Description_: Amount of decimals after the decimal separator
    * _Default_: 
* #### **document_type_disable_offsets_by_default**
    * _Type_: number [0|1]
    * _Description_: It [Activates|Deactivates] offsets by default when a document type is generated
    * _Default_: 0 (Offsets are activated by default)
* #### **force_manual_index**
    * _Type_: Boolean (true|false)
    * _Description_: It forces manual index for master keys
    * _Default_: false
* #### **job_admin_email**
    * _Type_: String
    * _Description_: Default administrator email for enterprise configuration jobs
    * _Default_: %station_admin_mail%
* #### **job_default_ocr**
    * _Type_: String
    * _Description_: Default OCR engine to be used by ChronoScan
    * _Default_: %OCR_engine_type%


