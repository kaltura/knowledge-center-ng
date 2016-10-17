---
layout: page
title: "Creating a Custom Module for MediaSpace "
date: 2013-02-10 15:41:07
---

<div class="tabItem">
  <h3>
    Kaltura MediaSpace Module Structure
  </h3>
  
  <p>
    A module of MediaSpace is an implementation of MVC web application, based on Zend-Framework folder structure and naming convention.
  </p>
  
  <p>
    Following is the folder structure of a MediaSpace module including typical files in each folder.
  </p>
  
  <p>
    In the below example, replace "{module}" with the name of your module, notice that the replacement should be case-sensitive, so if you see {Module} and your module's name is test you should replace with Test.
  </p>
  
  <pre class="brush: java;fontsize: 100; first-line: 1; ">{module}/
         controllers/
                     IndexController.php
         models/
                {Module}.php --- the model file of the module, without it the module will not be functional at all
         views/
               scripts/
                       index/ --- as the name of the controller we defined
                             index.phtml --- view script for indexAction within IndexController
                             other.phtml --- view script for otherAction within IndexController
         assets/ --- css, js and images to be used by the module.
         default.ini --- default settings file of the module.
         admin.ini --- settings file of the module to expose configuration options in configuration management UI
         module.info --- information file of the module to present data in configuration management UI </pre>
</div>

<div class="tabItem">
  <h3>
    Model Class
  </h3>
  
  <p>
    The model class in a MediaSpace module is responsible for "declaring" each and every feature the module extends.
  </p>
  
  <p>
    Extending a MediaSpace feature through a module is done by implementing one of the <a href="http://debbie.mediaspace.kaltura.com/kb/tab/interfaces">interfaces</a> that are available in MediaSpace.
  </p>
  
  <p>
    Your model class should implement any of the interfaces, according to the features you would like to provide through your module.
  </p>
  
  <p>
    A basic model class of the 'mymodule' module would look like the following:
  </p>
  
  <pre>class Mymodule_Model_Mymodule extends Kms_Module_BaseModel
{
}</pre>
  
  <p>
    The abstract class Kms_Module_BaseModel implements 2 interfaces:
  </p>
  
  <ul>
    <li>
      Kms_Interface_Model_ViewHook - allows modules to provide their HTML output to be included in core views of MediaSpace.
    </li>
    <li>
      Kms_Interface_Access - every module that has a controller must declare the access rules for its actions to integrate with MediaSpace's roles.
    </li>
  </ul>
</div>

<div class="tabItem">
  <div class="tabItem">
    To learn and review up to date interfaces, select the Knowledge Base tab in the MediaSpace Admin and then select Interfaces.<img src="../../assets/986.img">
  </div>
  
  <h3>
    Additional NameSpaces
  </h3>
  
  <p>
    If you need to add additional independent classes to your module, you can store them in one of the following namespaces that mediaspace includes as part of the auto-loading process.
  </p>
  
  <p>
    Note that you have to keep ZF naming convention so files will be found by the autoloader.
  </p>
  
  <ul>
    <li>
      plugins
    </li>
    <li>
      services
    </li>
    <li>
      views/helpers
    </li>
  </ul>
  
  <p>
    For example, if you want to add a class which communicates with a 3rd party API (i.e. service) you should add your file under 'services' folder (in your module).
  </p>
  
  <p>
    Your folder/file structure would look like:
  </p>
  
  <pre>{module}/
         controllers/
                     ...
         models/
                {module}.php
         views/
               scripts/
                       ...
         assets/
                ...                       
         services/
                  Thirdparty.php
         admin.ini
         default.ini
         module.info</pre>
  
  <p>
    Your class name would look like:
  </p>
  
  <pre>class {Module}_Service_Thirdparty
{
}</pre>
  
  <p>
    Note that {Module} should be replaced with the name of your module with the first character in upper case.
  </p>
</div>

<div class="tabItem">
  <h3>
    Module Assets
  </h3>
  
  <p>
    Modules can contain js, css, flv, and image files to be used in their views. The files are located in the module's 'assets' folder.
  </p>
  
  <p>
    To access the files, use a url of the form:
  </p>
  
  <pre>http://[kms url]/[build number]/[module name]/asset/[file name]</pre>
  
  <div>
    <h2>
      View Hooks
    </h2>
    
    <div class="tabItem">
      <p>
        Modules are allowed to add HTML content to different locations in KMS pages.
      </p>
      
      <p>
        This capability, in KMS, is called "View Hook" - the ability to hook into an existing view and adding output to that view.
      </p>
      
      <p>
        This is built in a way that KMS invokes (internally) page requests and uses the response as the HTML that is added in the "core" view script.
      </p>
      
      <p>
        A module that implements viewhook must have, at least, the following:
      </p>
      
      <ul>
        <li>
          Model class<ul>
            <li>
                 Declares which view hooks are implemented by the module. For each viewhook - specify which action and controller of the module should be invoked, and the importance order between other modules implementing the same viewhook.
            </li>
            <li>
                 Set access rules for any of the controllers and actions provided by the module.
            </li>
          </ul>
        </li>
        
        <li>
          At least one controller - to expose actions that are invoked as viewhooks.
        </li>
        <li>
          Relevant view scripts to serve as the output for each of the actions.
        </li>
      </ul>
    </div>
  </div>
</div>