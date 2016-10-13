---
layout: page
title: "Uploading a List of Users to the Kaltura Platform"
date: 2014-10-13 09:28:21
---

<div class="page" title="Page 1">
  <div class="layoutArea">
    <div class="column">
      <p>
        <strong>Overview</strong>
      </p>
      
      <p>
        The Kaltura Web Services platform provides a tool whereby a partner can add and update multiple end-users via its Application Programming Interface (API). The API allows partners to manage end users in two ways: singular actions with a single API call, or mass update by sending a CSV file. The platform accepts a text file in Comma-Separated- Values (CSV) format where each user to be added or updated represents a single line. The API also provides an option where a list of one or more email addresses can be provided which will receive a report of success or failure for each supplied user record.
      </p>
      
      <p>
        <br /><strong>File Format<br /></strong>
      </p>
      
      <div class="page" title="Page 1">
        <div class="layoutArea">
          <div class="column">
            The format for the CSV file is described in a Knowledge Center article <a href="{{site.url}}/documentation/Knowledge/end-users-csv-usage-and-schema-description.html" target="_blank">End-Users CSV - Usage and Schema Description</a><p>
              It is included here by reference.
            </p>
            
            <p>
              <strong>The Kaltura API</strong>
            </p>
            
            <div class="page" title="Page 1">
              <div class="layoutArea">
                <div class="column">
                  <p>
                    The Kaltura API is a RESTful API where each call is an action within a specified service. The service which supports the multiple user function is “user” and the action is “addFromBulkUpload”. We provide API client libraries in most, if not all, popular programming languages. The examples included at the end of this document use the PHP 5.3 client library. Client libraries can be downloaded from <a href="http://www.kaltura.com/api_v3/testme/client-libs.php" target="_blank" title="Kaltura API SDK - Native Client Libraries">http://www.kaltura.com/api_v3/testme/client-libs.php</a>
                  </p>
                  
                  <div class="page" title="Page 1">
                    <div class="layoutArea">
                      <div class="column">
                        <p>
                          The API is stateless on the server side. State can be maintained by the client. The authentication and authorization features require that the client first create a session identifier containing the Kaltura Session (KS) string. It is recommended to use internal method in the client library in order to create the KS. This string must be included with all subsequent API calls which use the same credentials and permissions. The client libraries simplify this by persistently retaining the KS and including it in each API call.
                        </p>For full information about the Kaltura API Architecture see 
                        
                        <a href="Introduction%20to%20the%20Kaltura%20API%20Architecture" target="_blank">Introduction to the Kaltura API Architecture</a>.<p>
                          <strong style="font-size: 10px;">The AddFromBulkUpload API Call</strong>
                        </p>
                        
                        <div class="page" title="Page 1">
                          <div class="layoutArea">
                            <div class="column">
                              <p>
                                After you start a session in the API client, you can make the addFromBulkUpload call (in the "user" service) which sends your CSV file to the platform for processing.
                              </p>
                              
                              <p>
                                The objects used by the PHP client library can be automatically loaded by using the PHP __autoload magic function. This function is  called whenever an unrecognized class is referenced. The function translates the namespace of the class into a file path and issues a require_once() to load the file.
                              </p>
                              
                              <p>
                                To make the addFromBulkUpload call, instantiate the BulkUploadJobData object and set the emailRecipients property to the desired email addresses. The addresses must be a comma-separated list expressed as a string. Do not quote the individual addresses. The BulkUploadUserData object will not be used in this call, but is a parameter of the addFromBulkUpload action, so pass a null as that parameter. You may now make the addFromBulkUpload call via the user object of the client ($client->user- >addFromBulkUpload()). The results are sent in an email to the supplied addresses.
                              </p>
                              
                              <p>
                                <strong>Sample User Bulk Upload Script</strong>
                              </p>
                              
                              <div class="page" title="Page 2">
                                <div class="layoutArea">
                                  <div class="page" title="Page 2">
                                    <div class="layoutArea">
                                      <pre class="brush: php;fontsize: 100; first-line: 1; ">&lt;?php

/**
* Make sure we can load the Kaltura API client classes based on the namespace * @param string $classname
*/

function __autoload($classname) {
       $path = str_replace('\\', '/', $classname);
       $path = "./".$path.".php";
       require_once($path);
}

//set verbose_logging to a class which implements the Kaltura\Client\ILogger interface if your

 //want to see all API requests and responses
$verbose_logging = false;
//the endpoint of the API service. For SaaS, use www.kaltura.com

$endpoint = 'https://www.kaltura.com/'; //Initialize the client object

$client = null;
 //Initialize the configuration object
$kaltura_config = null;
 //This is your partner (account) id
$partner_id = '&lt;your partner id&gt;';
//This is your admin secret string (available from the KMC)

$secret = '&lt;your admin secret&gt;;
 //This is your user id (usually an email address)
$user_id = '&lt;your partner user id&gt;';
 //The path to the CSV file
$fileData = 'C:\fakepath\userupload.csv';
//The list of email addresses to receive the upload report (comma-separated string)

$report_list = 'user1@domain.com,user2@domain.net';
try {

 //Create this object to contain the client configuration
       $kaltura_config = new Kaltura\Client\Configuration($partner_id);
 //Instantiate an ILogger to log API calls
       if (is_object($logger)) {
             $kaltura_config-&gt;setLogger($verbose_logging);
}

 //What is the endpoint of the web services platform?
       $kaltura_config-&gt;setServiceUrl($endpoint);
 //Create the client using the configuration object
       $client = new Kaltura\Client\Client($kaltura_config);
 //Use an admin session for these calls
       $type = Kaltura\Client\Enum\SessionType::ADMIN;
 //Use the session service
       $session_service = $client-&gt;getSessionService();
 //Start the session.  Get the KS as a response
       $ks = $session_service-&gt;start($secret, $user_id, $type,$partner_id, 360000);
 //Tell the client to use the KS we just received
       $client-&gt;setKs($ks);
}
catch (Exception $e) {
       die('Failed to start session: '.$e-&gt;getMessage());
}

//Create a BulkUploadJobData object to contain the report email addresses

$bulkUploadData = new \Kaltura\Client\Type\BulkUploadJobData();
 //Set the list of addresses to receive the upload report
$bulkUploadData-&gt;emailRecipients = $report_list;
 //We aren't going to use the bulkUploadUserData object, but pass a null in the call
$bulkUploadUserData = null;
 //Call the addFromBulkUpload action in the user service
$result = $client-&gt;user-&gt;addFromBulkUpload($fileData, $bulkUploadData, $bulkUploadUserData);
?&gt;</pre>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>