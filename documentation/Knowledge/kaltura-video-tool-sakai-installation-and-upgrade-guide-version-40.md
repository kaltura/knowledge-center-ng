---
layout: page
title: "Kaltura Video Tool for Sakai Installation and Upgrade Guide Version: 4.0"
date: 2016-01-26 17:09:36
---

<div class="WordSection1">
    <p>
      <a name="top"></a>
    </p>
    
    <p>
      This guide describes how to install, configure and upgrade the Kaltura Video Tool for Sakai. 
    </p>
    
    <p>
      The following topics are described:
    </p>
  </div>
  
  <div class="WordSection2">
    <p>
      [collapsed title="Installation Process"]
    </p>
    
    <h2>
      <a name="installation_process"></a>Installation Process
    </h2>
  </div>
  
  <div class="WordSection4">
    <h2>
      Before you begin
    </h2>
    
    <p class="Note">
      IMPORTANT NOTE: To support the latest Kaltura module, you are required to create three tables on the Sakai database. If the auto.ddl property is set to true on sakai.properties, these tables are automatically created when the Tomcat server is restarted with the latest code changes. In case auto.ddl is turned off on the server side, the administrator is required to manually run the kaltura.sql located inside:<br /><strong>sakai-extension/impl/src/main/resources/ddl/sql</strong>
    </p>
    
    <h2>
      Installing the Kaltura Video Tool for Sakai Application
    </h2>
    
    <p class="Procedure">
      To install the Kaltura Video Tool for Sakai application
    </p>
    
    <ol>
      <li>
        Download the Sakai-extension from <a href="https://github.com/kaltura/sakai-extension/releases" target="_blank">github</a> to get the latest changes available for Sakai – Kaltura integration using LTI.
      </li>
      <li>
        Copy the contents of the Sakai-extension to a new directory named kaltura-new.
      </li>
      <li>
        Move the kaltura-new directory inside your Sakai codebase root directory. For example: if the Sakai codebase resides in /usr/workspace/sakai, run: mv kaltura-new /usr/workspace/sakai/
      </li>
      <li>
        Update sakai/pom.xml to build the new module. Open sakai/pom.xml and add this line to<br /><p>
          <modules> section
        </p>
        
        <p>
          <module>kaltura-new</module>
        </p>
      </li>
      
      <li>
        Open the sakai-new/pom.xml and modify the <parent><version>10-SNAPSHOT</version></parent> by removing any text and leaving just the Sakai version you are using.<br />For example: <parent><version>10.4snapshot</version></parent>
      </li>
      <li>
        Build sakai : mvn clean install.
      </li>
      <li>
        Shutdown your Tomcat server by navigating to the Tomcat folder (usually located in /opt/sakai/tomcat) and navigating to its bin directory, executing the “./shutdown.sh” command and cleanup dirs : tomcat/webapps  , components,work/Catalina/localhost,shared/lib,temp, common/lib/sakai-*
      </li>
      <li>
        Deploy the latest Sakai code from inside the Sakai code base folder.
      </li>
      <li>
        Run maven command:<br />mvn sakai:deploy -Dmaven.tomcat.home=path to tomcat home
      </li>
      <li>
        Restart the Tomcat server.
      </li>
      <li>
        Add the following to your sakai.properties and restart your server:<ol style="list-style-type: lower-alpha;">
          <li>
            Make sure to fill in your partner ID, Admin Secret and KAF instance.<br />in sakai.properties, those are:<br /><p>
              #Kaltura LTI Authentication<br />kaltura.launch.key=###CHANGEME### --> Your partner ID<br />kaltura.launch.secret=###CHANGEME### --> Your admin secret
            </p>
            
            <p>
              kaltura.host=###CHANGEME### --> Your KAF instance hostname
            </p>
          </li>
          
          <li>
            There are additional “optional” configurations that you can configure.
          </li>
        </ol>
      </li>
    </ol>
    
    <pre class="brush: php;fontsize: 100; first-line: 1; "># Kaltura REST API authentication

# Kaltura RESTful API authorization code TTL (in milliseconds)

# Default: 60000 ms (1 minute)

#kaltura.rest.authorization.ttl=60000

 

# Kaltura RESTful API authorization override code

# Allows access to /kaltura/user/{userId} endpoint without sending in persistent auth_code

# Default: c48cb080-852b-11e4-80c2-0002a5d5c51b

#kaltura.authorization.override.code=c48cb080-852b-11e4-80c2-0002a5d5c51b

 

#Kaltura LTI Authentication

# Fill in your KAF instance

kaltura.launch.key=

# Fill in you Kaltura Partner ID

kaltura.launch.secret=

#Fill in your Kaltura Admin Secret

kaltura.host=https://1111.kaf.kaltura.com#Fill in your KAF instance hostname 

kaltura.ckeditor.url=https://11111.kaf.kaltura.com/browseandembed/index/browseandembed

#fill in the correct KAF instance

 

#antisamy will remove src entries in &lt;iframe&gt; tags by default for Kaltura, as that

#domain is not registered in the high security policy.  Therefore, enable low security through

#setting:

content.cleaner.default.low.security=true

#review the sakai.default.properties file included in source for more information about this

#setting

#OPTIONAL, if set, Kaltura ckeditor embed call will be replaced with a simple form

#for testing

#kaltura.ckeditor.debug=true

 

#optional, if set, kaltura site copy related jobs will attempt the given number of times to check the status on kaltura server.

#jobs.max.attempt=10

 

#if set, post request is sent to kaltura to copy media items on kaltura server on site import

kaltura.archive.support.enabled=true

 

#add Kaltura to archive merge services

archive.merge.filtered.services=AnnouncementService,AssignmentService,ContentHostingService,CalendarService,ChatEntityProducer,DiscussionService,MailArchiveService,SyllabusService,RWikiObjectService,DiscussionForumService,WebService,LessonBuilderEntityProducer,KalturaEntityProducer

#if set, kaltura will copy items embedded in CK editor when site copy request is initiated

kaltura.site.copy.incontext=true


#optional, turn on debug for lti requests from kaltura modules. Default is false

#kaltura.my-media.debug=off

#kaltura.course-gallery.debug=off

#kaltura.ckeditor.debug=off

#kaltura.launchmedia.debug=off</pre>
  </div>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Adding the CKEditor (Rich Text Editor) Integration"]
  </p>
  
  <h2>
    <a name="CKEditor"></a>Adding the CKEditor (Rich Text Editor) Integration
  </h2>
  
  <p>
    The following steps describe how to modify Sakai so the CK editor will work with the Kaltura-LTI Media Gallery.
  </p>
  
  <p class="Procedure mce-procedure">
    To integrate the CKEditor
  </p>
  
  <ol>
    <li>
      <p>
        Copy the "kaltura" directory into the {SAKAI_ROOT}/reference/library/src/webapp/editor/ckextraplugins
      </p>
      
      <p>
        Example: cp -R {KALTURA_LTI_ROOT}/ckeditor/kaltura {SAKAI_ROOT}/reference/library/src/webapp/editor/ckextraplugins
      </p>
    </li>
    
    <li>
      <p>
        Edit {SAKAI_ROOT}/reference/library/src/webapp/editor/ckeditor.launch.js
      </p>
    </li>
    
    <ol style="list-style-type: lower-alpha;">
      <li>
        <p>
          At about line 89, inside the definition of "toolbar_Full:", add 'kaltura' before the two references to 'Image'  (these are the buttons in the toolbar):
        </p>
        
        <p class="wysiwyg-syntaxhl brush: php;fontsize: 100; first-line: 1; ">
          is: (sakai.editor.enableResourceSearch ? ['ResourceSearch','Image','Flash','Table','HorizontalRule','Smiley','SpecialChar','PageBreak'] : ['Image','Flash','Table','HorizontalRule','Smiley','SpecialChar','PageBreak']), changes to: (sakai.editor.enableResourceSearch ? ['ResourceSearch','kaltura','Image','Flash','Table','HorizontalRule','Smiley','SpecialChar','PageBreak'] : ['kaltura','Image','Flash','Table','HorizontalRule','Smiley','SpecialChar','PageBreak']),
        </p>
      </li>
      
      <li>
        <p>
          At about line 171, add a new reference to the plugin:
        </p>
        
        <p class="wysiwyg-syntaxhl brush: php;fontsize: 100; first-line: 1; ">
          is: (function() { CKEDITOR.plugins.addExternal('movieplayer',basePath+'movieplayer/', 'plugin.js'); CKEDITOR.plugins.addExternal('wordcount',basePath+'wordcount/', 'plugin.js'); CKEDITOR.plugins.addExternal('fmath_formula',basePath+'fmath_formula/', 'plugin.js'); CKEDITOR.plugins.addExternal('audiorecorder',basePath+'audiorecorder/', 'plugin.js'); changes to: (function() { CKEDITOR.plugins.addExternal('movieplayer',basePath+'movieplayer/', 'plugin.js'); CKEDITOR.plugins.addExternal('wordcount',basePath+'wordcount/', 'plugin.js'); CKEDITOR.plugins.addExternal('fmath_formula',basePath+'fmath_formula/', 'plugin.js'); CKEDITOR.plugins.addExternal('audiorecorder',basePath+'audiorecorder/', 'plugin.js'); CKEDITOR.plugins.addExternal('kaltura',basePath+'kaltura/', 'plugin.js');
        </p>
      </li>
      
      <li>
        <p>
          At about line 190, add the following additional line:
        </p>
        
        <pre class="brush: php;fontsize: 100; first-line: 1; ">    is:
        ckconfig.extraPlugins+="movieplayer,wordcount,fmath_formula";

    changes to:
        ckconfig.extraPlugins+="movieplayer,wordcount,fmath_formula";
        ckconfig.extraPlugins+=",kaltura";
</pre>
      </li>
    </ol>
    
    <li>
      <p>
        Add the following script to the end of {SAKAI_ROOT}/portal/portal-render-engine-impl/pack/src/webapp/vm/neoskin/includeStandardHead.vm (around line 190):
      </p>
      
      <p class="wysiwyg-syntaxhl brush: php;fontsize: 100; first-line: 1; ">
        <script type="text/javascript" language="JavaScript" src="/media-gallery-tool/js/kaltura-upgrade.js"></script>
      </p>
    </li>
    
    <li>
      <p>
        Add the following script to the end of {SAKAI_ROOT}/portal/portal-render-engine-impl/pack/src/webapp/vm/morpheus/includeStandardHead.vm (around line 160):
      </p>
      
      <p class="wysiwyg-syntaxhl brush: php;fontsize: 100; first-line: 1; ">
        <script type="text/javascript" language="JavaScript" src="/media-gallery-tool/js/kaltura-upgrade.js"></script>
      </p>
    </li>
    
    <li>
      <p>
        Re-deploy the reference project.
      </p>
      
      <p class="wysiwyg-syntaxhl brush: php;fontsize: 100; first-line: 1; ">
        mvn clean install sakai:deploy -f reference/pom.xml mvn clean install sakai:deploy -f portal/pom.xml
      </p>
    </li>
    
    <li>
      <p>
        Configure Anti-Samy.
      </p>
    </li>
    
    <li>
      <p>
        Re-deploy the reference project.
      </p>
      
      <p class="wysiwyg-syntaxhl brush: php;fontsize: 100; first-line: 1; ">
        mvn clean install sakai:deploy -f reference/pom.xml
      </p>
    </li>
    
    <li>
      <p>
        Configure Anti-Samy - Anti-Samy validates potentially dangerous script code and prevents it from being stored in the datastore according to the security policy of Sakai.  There are at least two ways to address this.
      </p>
      
      <strong>If you are using default policies: set the default security policy to low enforcement.</strong><br /><br />Enable low enforcement by setting the following property in sakai.properties:<br /><pre class="brush: java;fontsize: 100; first-line: 1; ">content.cleaner.default.low.security=true</pre>Copy the "antisamy" directory into your web container's sakai directory (same directory where sakai.properties lives. Example: cp -R {KALTURA_LIT_ROOT/ckeditor/antisamy {CATALINA_HOME}/sakaiThe override low-security-policy.xml adds a new attribute, kaltura-lti-url, to the img tag.  This allows the CKEditor to save the new media item inserted by the Kaltura LTI integration.
      
      <p>
        <strong>If you are using custom policies:</strong>
      </p>Open the file antisamy/low-security-policy.xml and search for "kaltura-lti-url".  You will find two references. One is an attribute definition, and the second add the attribute to the img tag. You need to copy both configurations into your custom policy file (either low-security-policy.xml  or high-security-policy.xml).
      
      <br />You can also apply antisamy.patch (in this directory) to your custom policy file to make these changes for you
    </li>
  </ol>
  
  <p>
    After you have made these configuration changes to Sakai, stop and restart Sakai.
  </p>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Verifying that the Kaltura Video Tool for Sakai is Installed"]
  </p>
  
  <h1>
    <a name="verifying"></a>Verifying that the Kaltura Video Tool for Sakai is Installed
  </h1>
  
  <p class="Procedure mce-procedure">
    To verify that the new Kaltura Video Tool for Sakai is available
  </p>
  
  <ol>
    <li>
      Login as admin user or a user with maintain access permissions to a site.
    </li>
    <li>
      Enter the Sakai site and click on 'Site Info' from the left navigation pane.
    </li>
    <li>
      Click on 'Edit Tools'.<br />In the resulting page, you should see two new tools named 'My Media' and ‘Media Gallery’ available in the list.
    </li>
    <li>
      Select the checkbox of the desired tool you want to add to your site and click Save.<br /><span class="mce-note-graphic">If the Sakai site had an existing Media Gallery tool/page added to it, then no steps are required to update the Media Gallery tool.<br /><img src="{{site.url}}/assets/2992">
    </li>
  </ol>
  
  <p>
     
  </p>
  
  <p class="FigureList">
    <a href="#top">Back to Top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Verifying that the Kaltura Admin Tool is Available"]
  </p>
  
  <h1>
    <a name="Admin_Tool"></a>Verifying that the Kaltura Admin Tool is Available
  </h1>
  
  <p>
    To verify that the Kaltura Video Admin Tool is available
  </p>
  
  <ol>
    <li>
      Login as admin user or a user with maintain access permissions to a site.
    </li>
    <li>
      Click on 'Sites' tool from the admin user My Workspace.
    </li>
    <li>
      Search for “Admin” in the Site ID field and press Enter.
    </li>
    <li>
      In the resulting page, click on the Administration Workspace link.
    </li>
    <li>
      In the Edit Site admin page, click Add/Edit pages located toward the bottom of the page.
    </li>
    <li>
      Click New Page and enter the Title as Kaltura Admin and click Tools under Continue Editing.
    </li>
    <li>
      Click New Tool.
    </li>
    <li>
      Select the radio button next to Kaltura Admin Tool (kaltura admin) and click Save under Complete the Site Edit.
    </li>
    <li>
      Go to the Administration Workspace site and on the left navigation page the Kaltura Admin Tool should be available.<br /><img src="{{site.url}}/assets/2993">
    </li>
  </ol>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <p>
    ;[/collapsed]
  </p>
  
  <p>
    [collapsed title="Adding Kaltura My Media to My Workspace"]
  </p>
  
  <h1>
    <a name="Workspace"></a>Adding Kaltura My Media to My Workspace
  </h1>
  
  <p>
    This section describes the admin tasks on how to add My Media to My Workspace for new and existing users.
  </p>
  
  <p class="Procedure mce-procedure">
    To add My Media to My Workspace for new users in the system:
  </p>
  
  <ol>
    <li>
      Login to the Sakai Server as an admin user.
    </li>
    <li>
      Go to the Sites tool (can be found in the Administration Workspace).
    </li>
    <li>
      Search for !user site id (second text field).
    </li>
    <li>
      Click on !user site id.
    </li>
    <li>
      Click on pages button.
    </li>
    <li>
      Click on "New Page" link.
    </li>
    <li>
      Enter "My Media" for the page title.
    </li>
    <li>
      Click on the "Tools" button.
    </li>
    <li>
      Click on the "New Tool" link.
    </li>
    <li>
      Click on the check box next to "Kaltura My Media".
    </li>
    <li>
      Click on the "Save" button.
    </li>
  </ol>
  
  <p class="Procedure mce-procedure">
    To add My Media to My workspace for existing users in the system:
  </p>
  
  <ol>
    <li>
      Login into Sakai server as an admin user.
    </li>
    <li>
      Click 'Job Scheduler' link from admin user's My Workspace.<br /><img src="{{site.url}}/assets/2994">
    </li>
    <li>
      Click 'Jobs' button. On the next page, click 'New Job' button.
    </li>
    <li>
      Enter the Job Name and select the Type: 'Add My Media For Existing Users Job' and click Post.<br /><img src="{{site.url}}/assets/2995">
    </li>
    <li>
      Click on 'Triggers(0)” next to Kaltura Job.<br /><img src="{{site.url}}/assets/2996">
    </li>
    <li>
      Click on Run Job Now button. Confirm by clicking again on Run Now button in this page.<br /><img src="{{site.url}}/assets/2997">
    </li>
  </ol>
  
  <p>
    <span class="mce-note-graphic">These steps trigger a job in Sakai that adds the Kaltura Video Tool for Sakai for existing users. <br />When the job completes, an email notification is sent to the admin email address with the status. <br />The email contains the following information:<br /><strong>Subject: Status: Adding  My Media to user's My Workspace</strong><br /><strong>Email message:</strong><br /><strong>Add My Media for Existing Users Job Run status:COMPLETED/ FAILED Total number of My workspace sites:</strong><br /><strong>Number of My workspace sites updated:</strong></span>
  </p>
  
  <p>
    The email Service has to be enabled in Sakai via sakai.properties to be triggered. The admin email address to use for this notification can be configured via jobs.admin.email property in Sakai.properties.
  </p>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Adding the Kaltura Video Tool to your Sakai Course Site"]
  </p>
  
  <div class="WordSection11">
    <h1>
      <a name="adding_tool"></a>Adding the Kaltura Video Tool to your Sakai Course Site
    </h1>
    
    <p class="Procedure mce-procedure">
      To add the Media Gallery and My Media to your Sakai Course Site
    </p>
    
    <ol>
      <li>
        Log in to Sakai.
      </li>
      <li>
        Choose the site where you want to use the Media Gallery.
      </li>
      <li>
        Click <strong>Site Info</strong> on the left navigation bar.
      </li>
      <li>
        Click <strong>Edit Tools</strong> in the menu along the top of the window.
      </li>
      <li>
        Check <strong>Media Gallery and/or My Media</strong> to include the Media Gallery and My Media on your site.<br /><img src="{{site.url}}/assets/2999">
      </li>
      <li>
        Click <strong>Continue</strong> at the bottom of the screen.
      </li>
      <li>
        Click <strong>Finish</strong> at the bottom of the screen.
      </li>
    </ol>
    
    <p>
      Go back to the Sakai home page and enter the Media Gallery or My Media through the tool bar
    </p>
  </div>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Kaltura Site Copy Jobs"]
  </p>
  
  <div class="WordSection12">
    <h1>
      <a name="site_copy_jobs"></a>Kaltura Site Copy Jobs
    </h1>
    
    <p>
      The following two jobs need to be added to perform checks on Kaltura jobs created on KAF for site copy action:
    </p>
    
    <ul>
      <li>
        <strong>Add kaltura site copy batch details job</strong> – This job checks for batch record with 'NEW' status that are created to hold information about site copy request. A single batch record is associated with one or more Kaltura job entries that are created on KAF to handle copy operation of media items as part of the Site import process.
      </li>
      <li>
        <strong>Add kaltura site copy job status details job</strong>– This job checks for Kaltura job record with 'NEW' status that hold information about Kaltura copy jobs created to handle copy operations on KAF side.
      </li>
    </ul>
    
    <h2>
      Adding Kaltura Site Copy Related Jobs
    </h2>
    
    <p>
      The steps to add any of these site copy related jobs are the same as adding any job in Sakai Job Scheduler.
    </p>
    
    <p class="Procedure mce-procedure">
      To add one of the site copy related jobs from  the Job Scheduler UI:
    </p>
    
    <ol>
      <li>
        Login into Sakai server as an admin user.
      </li>
      <li>
        Click 'Job Scheduler' link from admin user's My Workspace.
      </li>
      <li>
        Click 'Jobs' button. On the next page, click 'New Job' button.
      </li>
      <li>
        Enter the Job Name and select Type and click Post.<br />This takes you back to page where the jobs are listed.
      </li>
      <li>
        Click on 'Triggers(0)” next to the Kaltura related Job.
      </li>
      <li>
        Click on 'New Trigger' on the next page.
      </li>
      <li>
        Enter the Trigger Name and Cron Expression to setup triggers for the Kaltura job and click post.
      </li>
      <li>
        Repeat the above steps to add a job and trigger for 'Add kaltura site copy job check status' job. Set the trigger to run every 20 seconds.<br /><img src="{{site.url}}/assets/2991">
      </li>
    </ol>
    
    <h3>
      Kaltura Debug Logs
    </h3>
    
    <p>
      Since these jobs are expected to run smoothly in the background, most information about the status of the Kaltura site copy jobs are set to 'debug' level. The following property can be added to sakai.properties to turn on the debugging level on the server to capture these responses from Kaltura on copy job status.
    </p>
    
    <pre class="brush: php;fontsize: 100; first-line: 1; ">log.config.count=2
log.config.1=DEBUG.org.sakaiproject.kaltura.services.CheckKalturaSiteCopyJob
log.config.2=DEBUG.org.sakaiproject.kaltura.services.KalturaEntityProducer</pre>
  </div>
  
  <p>
    <a href="#top"> Back to Top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>
  
  <p>
    [collapsed title="Upgrading from Kaltura Video Tool v3 to Kaltura Video Tool v4"]
  </p>
  
  <h1>
    <a name="upgrading"></a>Upgrading from Kaltura Video Tool v3 to Kaltura Video Tool v4
  </h1>
  
  <p>
    Remove the existing Kaltura module from the Sakai codebase and follow the steps described in the <a href="https://kaltura.sharepoint.com/community-team/Shared%20Documents/Knowledge%20Management/Work%20in%20Progress/Kaltura%20Video%20Tool%20for%20Sakai/KAF%20Version%204/Installation_Upgrade/Kaltura_Video_Tool_version4_for_Sakai_Installation_Upgrade_Guide.docx#_Installation_Process_1">installation process</a> to upgrade to latest version.
  </p>
  
  <p class="mce-note-graphic">
    <span>You must have Kaltura release version 3 and Sakai version 10.x.</span>
  </p>
  
  <p>
    Migration of content from previous versions – Please coordinate with your Kaltura representative to schedule your content migration.
  </p>
  
  <p>
    Please refer to the article <a href="{{site.url}}/documentation/Knowledge/whats-new-kaltura-video-tool-sakai-version-4.html">What's New in the Kaltura Video Tool for Sakai Verion 4</a>,  to understand the differences between the two versions.
  </p>
  
  <p>
    Main updates post migration:
  </p>
  
  <ol>
    <li>
      If an entry was private in the site gallery it will be pending moderation in the Media Gallery post migration
    </li>
    <li>
      If an entry was private in a collection, it will not appear in the channel playlist
    </li>
    <li>
      Not all collections types must be migrated, you can decide which types of collection you would like to migrate to channel playlists. You will need to provide the list of collection types you would like to migrate from the following: Instructor, Community, Personal and Owner.
    </li>
  </ol>
  
  <p>
    <a href="#top">Back to Top</a>
  </p>
  
  <p>
    [/collapsed]
  </p>