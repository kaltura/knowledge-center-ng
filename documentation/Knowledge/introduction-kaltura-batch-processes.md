---
layout: page
title: "Introduction to Kaltura Batch Processes"
date: 2011-12-31 11:54:22
---

The Kaltura batch management module implements a modular and distributed architecture, designed to answer the growing business and operational needs for site elasticity and smart distribution of system resources. The purpose of this document is to describe the architecture of the Kaltura batch management module with special emphasis on understanding the batch tasks and services that play a part in the Kaltura content ingestion flow.

<p class="mce-heading-2">
  <a name="What_is"></a>What is Batch processing?
</p>

(From <a href="http://en.wikipedia.org/wiki/Batch_processing" target="_blank">Wikipedia</a>)  
Batch processing is the execution of a series of <a href="http://en.wikipedia.org/wiki/Computer_program" target="_blank">programs</a> ("<a href="http://en.wikipedia.org/wiki/Job_(software)" target="_blank">jobs</a>") on a <a href="http://en.wikipedia.org/wiki/Computer" target="_blank">computer</a> without manual intervention.  Batch jobs are set up so they can be run to completion without manual intervention, so all input data is preselected through <a href="http://en.wikipedia.org/wiki/Script_(computer_programming)" target="_blank">scripts</a> or <a href="http://en.wikipedia.org/wiki/Command-line_parameter" target="_blank">command-line parameters</a>.  This is in contrast to "online" or <a href="http://en.wikipedia.org/wiki/Interactive_computing" target="_blank">interactive programs</a>which prompt the user for such input.  A program takes a set of data files as input, process the data, and produces a set of output data files.  This operating environment is termed as "batch processing" because the input data are collected into <a href="http://en.wikipedia.org/wiki/At_(Unix)" target="_blank">batches</a> on files and are processed in batches by the program. 

<p class="mce-heading-2">
  <a name="Kaltura_Batch_Task"></a>Kaltura Batch Task
</p>

A Kaltura Batch Task is a stand-alone task which is designed to be executed within the Kaltura Platform by a batch process.  Kaltura batch tasks are initiated by a Kaltura API call that is triggered either by a specific end-user workflow or by an internal batch processing flow management entity. 

When created, each batch task is stored within a dedicated data base record holding all information related to its specific type, its executing state, its priority and other operational information.  For more information on batch tasks type classification, please refer to the Kaltura Batch Tasks Type Classification section. 

<p class="mce-heading-2">
  <a name="Kaltura_Batch_Service"></a>Kaltura Batch Service
</p>

A Kaltura Batch Service is a configurable set of parameters defining a specific service that handles a batch task of a specific type in a specific way.  A batch service is defined by parameters such as service name, the type of batch tasks it should handle, the name of the process that should be executed to operate the service, the maximum number of instances each service can operate at a given time, the execution schedule of the service and other operable parameters.  There are 3 main types of batch services:

*   **Batch Execution Service**  
    A batch service that executes a full operation on a specific type of batch tasks. 
*   **Batch Closure Service**  
    A batch service that only handles the finalization of a previous operation on a specific type of batch tasks. 
*   **Batch Periodic Service**  
    A batch service that is mainly used for system maintenance operations, and does not handle batch tasks. 

<span> </span>

For more information on the Kaltura batch services, please refer to the [Kaltura Default Batch Services][1] section. 

 [1]: https://admin.kaltura.com/admin_console/index.php/batch/learn-more#Kaltura_Default_Batch

<p class="mce-heading-2">
  <a name="Kaltura_Batch_Process"></a>Kaltura Batch Process
</p>

A Kaltura Batch Process is one instance of a specific Kaltura batch service, executing the specific actions and logic needed for handling a specific type of batch tasks.  Upon execution, each batch process checks for the next relevant pending batch task to be handled and operates on it. 

<p class="mce-heading-2">
  <a name="Kaltura_Batch_Jobs_API"></a>Kaltura Batch Jobs API
</p>

A set of specific APIs used for implementing the internal and external flows related to the Kaltura batch processing implementation.

<p class="mce-heading-2">
  <a name="Kaltura_Batch_Scheduler"></a>Kaltura Batch Scheduler
</p>

The Kaltura Batch Scheduler is a continual process, responsible for the scheduling of the batch services assigned to it.  It schedules the execution of batch processes according to the load of pending batch tasks in the system and according to the scheduling rules defined in its configuration for the different batch services.  The Kaltura batch scheduler is assisted by a special batch periodic service, named Scheduler Helper, providing the batch scheduler with relevant information on the current state of batch processes and batch tasks. 

A Kaltura Batch Scheduler can run as a single scheduler within the platform deployment or run as one of many schedulers in a scaled-up platform configuration.  The defined set of batch services controlled by each batch scheduler can be extended, reduced or adjusted in run-time according to system functional and scalability needs. 

<p class="mce-heading-2">
  <a name="Internal_Batch_Processing"></a>Internal Batch Processing of a Single Batch Task
</p>

The following diagram illustrates the internal processing flow of a single batch task (import)

<img src="../../assets/229.img">

1.  A new import task is added via Kaltura API as the first step of a content ingestion flow for a new rich-media file, following an end-user import action.
2.  The Batch Scheduler executes a new batch process for executing the import job service.
3.  The Import batch process asks for the next pending import task via Kaltura API.
4.  The Import batch process updates the import batch task state to "Started".
5.  The Import batch process transfers the rich-media file from its original location to the Kaltura platform.
6.  The Import batch process updates the import batch task state to "Done".
7.  The Import batch process releases the import batch task and ends.

<span class="mce-heading-2"><a name="Batch_Processing_Flow"></a>Batch Processing Flow of a Successful Entry Ingestion</span>

The following diagram describes the internal batch processing flow for full ingestion of rich-media files by the Kaltura online video platform - from import (detailed above) to full transcoding into various 'transcoding flavors' for playback.  This is a simplified flow of a successful ingestion process. 

<img src="../../assets/230.img">

1.  The **Import batch process** transfers the new video file from its original location to the Kaltura platform
2.  A** convert profile batch task** is created as a parent task to all the batch tasks related to the transcoding of the video file.  An** extract media batch task** is created as well. 
3.  The **extract media batch process** extracts media related parameters from the headers of the video file that is about to be transcoded into web quality formats (flavors).  This information is then passed over to the Kaltura **transcoding decision layer** for deciding on the optimal quality flavors and transcoding options to be used.  Based on these decisions a suitable **convert batch task** is created for each one of the transcoding flavors to be generated. 
4.  Each **convert batch process** (4a, 4b, 4c) handles transcoding of the original media file into a specific transcoding flavor.  In this example: 2 **convert batch tasks** are processed by**convert batch processes** that utilize the FFmpeg transcoding engine and one **convert batch task** is processed by a **convert batch process** that utilizes the On2 transcoding engine.  Upon success, **post convert batch tasks **are created
5.  Each **post-convert batch process** (5a, 5b, 5c) processes the relevant **post convert batch task** for creating a thumbnail image and for extracting and storing media info about the created flavor for later use. 
6.  When all previously described** post convert batch tasks** have completed successfully, the new entry is available for web publishing in all of the required web quality flavors. 

<span class="mce-heading-2"><a name="Kaltura_Batch_Tasks_Type"></a>Kaltura Batch Tasks Type Classification</span>

<span>The following table lists the different types of batch tasks currently handled by the batch processing module. </span>

<table style="width: 650px;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <th width="50%">
        Batch Task Type Classification (Internal Type ID)
      </th>
      
      <th width="49%">
        Batch Sub Types Classification (Internal Sub Type ID)
      </th>
    </tr>
    
    <tr>
      <td rowspan="5" width="50%">
        Convert (0)
      </td>
      
      <td width="49%">
        On2 (1)
      </td>
    </tr>
    
    <tr>
      <td width="49%">
        FFmpeg (2)<p>
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="49%">
        Mencoder (3)<p>
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="49%">
        Encoding.com (4)<p>
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="49%">
        FFmpeg-Aux (5)<p>
           
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="50%">
        Import (1)
      </td>
      
      <td width="49%">
        N/A
      </td>
    </tr>
    
    <tr>
      <td width="50%">
        Flatten (3)
      </td>
      
      <td width="49%">
        N/A
      </td>
    </tr>
    
    <tr>
      <td width="50%">
        Bulk Upload (4)
      </td>
      
      <td width="49%">
        N/A
      </td>
    </tr>
    
    <tr>
      <td width="50%">
        <p>
          Download (6)
        </p>
      </td>
      
      <td width="49%">
        <p>
          N/A
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="50%">
        <p>
          Convert Profile (10)
        </p>
      </td>
      
      <td width="49%">
        <p>
          N/A
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="50%">
        <p>
          Post Convert (11)
        </p>
      </td>
      
      <td width="49%">
        <p>
          N/A
        </p>
      </td>
    </tr>
    
    <tr>
      <td rowspan="2" width="50%">
        <p>
          Extract Media (14)
        </p>
      </td>
      
      <td width="49%">
        <p>
          Entry Input (0)
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="49%">
        <p>
          Flavor Input (1)
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="50%">
        <p>
          Send Email (15)
        </p>
      </td>
      
      <td width="49%">
        <p>
          Per email type
        </p>
      </td>
    </tr>
    
    <tr>
      <td width="50%">
        <p>
          Send Notification (16)
        </p>
      </td>
      
      <td width="49%">
        <p>
          Per server notification type
        </p>
      </td>
    </tr>
  </tbody>
</table>

## <a name="Kaltura_Default_Batch"></a>Kaltura Default Batch Services

The Kaltura online video platform includes a set of default batch services that are required for system operation.  The following table describes these services:

<table style="width: 100%;" border="1" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <th style="text-align: center;" width="154">
        Service Name
      </th>
      
      <th style="text-align: center;" width="163">
        Service System Name
      </th>
      
      <th style="text-align: center;" width="174">
        Service Classification
      </th>
      
      <th style="text-align: center;" width="114">
        Batch Tasks Handled By This Service
      </th>
      
      <th style="text-align: center;" width="636">
        Description
      </th>
    </tr>
    
    <tr>
      <td style="text-align: center;" valign="top" width="154">
        Import Service
      </td>
      
      <td valign="top" width="163">
        KAsyncImport
      </td>
      
      <td valign="top" width="174">
        <a href="https://admin.kaltura.com/admin_console/index.php/batch/learn-more#">Batch Execution Service</a>
      </td>
      
      <td valign="top" width="114">
        Import
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles the physical transferring of rich-media files imported by content managers and/or by end-users from their original location to the Kaltura platform
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Bulk Upload Service
      </td>
      
      <td valign="top" width="163">
        KAsyncBulkUpload
      </td>
      
      <td valign="top" width="174">
        Batch Execution Service
      </td>
      
      <td valign="top" width="114">
        <a href="https://admin.kaltura.com/admin_console/index.php/batch/learn-more#">Bulk Upload</a>
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles the processing of a bulk upload operation.  Analyzes bulk upload csv and creates multiple import batch tasks to be processed separately
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Bulk Upload Closer Service
      </td>
      
      <td valign="top" width="163">
        KAsyncBulkUploadCloser
      </td>
      
      <td valign="top" width="174">
        Batch Closure Service
      </td>
      
      <td valign="top" width="114">
        Bulk Upload
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Finalize bulk upload operation based on the completion status of all batch tasks related to the ingestion process of the uploaded files
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Extract Media Service
      </td>
      
      <td valign="top" width="163">
        KAsyncExtractMedia
      </td>
      
      <td valign="top" width="174">
        Batch Execution Service
      </td>
      
      <td valign="top" width="114">
        <a href="https://admin.kaltura.com/admin_console/index.php/batch/learn-more#">Extract Media</a>
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Extract media related information from media files to serve as an input for optimal transcoding operation
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Convert Service
      </td>
      
      <td valign="top" width="163">
        KAsyncConvert
      </td>
      
      <td valign="top" width="174">
        Batch Execution Service
      </td>
      
      <td valign="top" width="114">
        Convert
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles the actual transcoding of one video file from one format to a specific quality flavor.  Based on the transcoding requirements and system load, the convert service can operate transcoding action by utilizing one of the transcoding engines that are configured in the system. 
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Divert Conversion Service
      </td>
      
      <td valign="top" width="163">
        KAsyncDivertConvert
      </td>
      
      <td valign="top" width="174">
        Batch Execution Service
      </td>
      
      <td valign="top" width="114">
        Convert
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles real-time diversion of a convert task from one transcoding engine to another (specifically divert convert tasks to encoding.com if operable within the specific deployment and when needed for balancing system transcoding load)
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Convert Closer Service
      </td>
      
      <td valign="top" width="163">
        KAsyncConvertCloser
      </td>
      
      <td valign="top" width="174">
        Batch Closure Service
      </td>
      
      <td valign="top" width="114">
        Convert
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles the finalization of a specific convert task (specifically handles the finalization of convert being handled by encoding .com or by a distributed scheduler)
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Post Convert Service
      </td>
      
      <td valign="top" width="163">
        KAsyncPostConvert
      </td>
      
      <td valign="top" width="174">
        Batch Execution Service
      </td>
      
      <td valign="top" width="114">
        Post Convert
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles the last steps of a specific convert task including thumbnail creation and extracting media info from created flavors. 
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Convert Profile Closer Service
      </td>
      
      <td valign="top" width="163">
        KAsyncConvertProfileCloser
      </td>
      
      <td valign="top" width="174">
        Batch Closure Service
      </td>
      
      <td valign="top" width="114">
        Convert Profile
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles the finalization of in-progress convert tasks related to one entry when not all tasks were finalized before a defined timeout
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Download Closer Service
      </td>
      
      <td valign="top" width="163">
        KAsyncBulkDownloadCloser
      </td>
      
      <td valign="top" width="174">
        Batch Closure Service
      </td>
      
      <td valign="top" width="114">
        Download
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles the completion of entry download flow, specifically responsible for triggering an email to the end-user with the download location
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Mailer Service
      </td>
      
      <td valign="top" width="163">
        KAsyncMailer
      </td>
      
      <td valign="top" width="174">
        Batch Execution Service
      </td>
      
      <td valign="top" width="114">
        Send Email
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles all system generated emails sent by the Kaltura platform upon different events. 
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Notification Service
      </td>
      
      <td valign="top" width="163">
        KAsyncNotifier
      </td>
      
      <td valign="top" width="174">
        Batch Execution Service
      </td>
      
      <td valign="top" width="114">
        Send Notification
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles all server notifications sent by the Kaltura platform to web components (server/client) that are integrated with The Kaltura notification system
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Shared Imports Cleanup Service
      </td>
      
      <td valign="top" width="163">
        DirectoryCleanupLocalImport
      </td>
      
      <td valign="top" width="174">
        <a href="https://admin.kaltura.com/admin_console/index.php/batch/learn-more#">Periodic Batch Service</a>
      </td>
      
      <td valign="top" width="114">
        <a href="https://admin.kaltura.com/admin_console/index.php/batch/learn-more#">N/A</a>
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        <a href="https://admin.kaltura.com/admin_console/index.php/batch/learn-more#">This is a scheduled maintenance service that cleans up the 'byproducts' of an import task</a>
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Shared Thumbnails Cleanup Service
      </td>
      
      <td valign="top" width="163">
        DirectoryCleanupLocalThumb
      </td>
      
      <td valign="top" width="174">
        Periodic Batch Service
      </td>
      
      <td valign="top" width="114">
        N/A
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        This is a scheduled maintenance service that cleans up the 'byproducts' of a thumbnail creation process
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Shared Converts Cleanup Service
      </td>
      
      <td valign="top" width="163">
        DirectoryCleanupLocalConvert
      </td>
      
      <td valign="top" width="174">
        Periodic Batch Service
      </td>
      
      <td valign="top" width="114">
        N/A
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        This is a scheduled maintenance service that cleans up the 'byproducts' of a convert task
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Database Cleanup Service
      </td>
      
      <td valign="top" width="163">
        KAsyncDbCleanup
      </td>
      
      <td valign="top" width="174">
        Periodic Batch Service
      </td>
      
      <td valign="top" width="114">
        N/A
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        This is a scheduled maintenance that handles database cleanup
      </td>
    </tr>
    
    <tr>
      <td valign="top" width="154">
        Scheduler Helper Service
      </td>
      
      <td valign="top" width="163">
        KScheduleHelper
      </td>
      
      <td valign="top" width="174">
        Periodic Batch Service
      </td>
      
      <td valign="top" width="114">
        N/A
      </td>
      
      <td style="text-align: left;" valign="top" width="636">
        Handles all communication between the Batch Schedulers deployed in the Kaltura platform and the Kaltura API/DB
      </td>
    </tr>
  </tbody>
</table>

<span><br /></span>

 