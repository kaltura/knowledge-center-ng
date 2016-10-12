---
layout: page
title: "Kaltura MediaSpace/Kaltura Application Framework (KAF) Roles and Permissions"
date: 2013-11-22 00:03:45
---

<div id="main-content" class="wiki-content">
  <p>
    The following information is crucial to understanding how permissions are manifested.  KMS, includes 2 types of user roles - Applicative roles and Contextual roles.
  </p>
  
  <p>
    Application Roles - Concern what a user is entitled (or not) to do in the context of the application. 
  </p>
  
  <p>
    Contextual  Roles -  Concern what a user is entitled (or not) to do in the context of G<span class="GINGER_SOFTWARE_mark">alleries</span> / Channels.
  </p>
  
  <ul>
    <li>
      <strong>KMS applicative roles</strong><ul>
        <li>
          <span class="GINGER_SOFTWARE_mark">anonymousRole</span>
        </li>
        <li>
          <span class="GINGER_SOFTWARE_mark">viewerRole</span>
        </li>
        <li>
          <span class="GINGER_SOFTWARE_mark">privateOnlyRole</span>
        </li>
        <li>
          <span class="GINGER_SOFTWARE_mark">adminRole</span>
        </li>
        <li>
          <span class="GINGER_SOFTWARE_mark">unmoderatedAdminRole</span>
        </li>
      </ul>
    </li>
  </ul>
  
  <ul>
    <li>
      <strong>Category/Channel context roles</strong><ul>
        <li>
          Member (view)
        </li>
        <li>
          Contributor (publish)
        </li>
        <li>
          Moderator (moderate)
        </li>
        <li>
          Manager (edit settings, manage members)
        </li>
      </ul>
    </li>
  </ul>
  
  <ul>
    <li>
      <strong>Category/Channel types</strong>
    </li>
    <ul>
      <li>
        Open
      </li>
      <li>
        Restricted
      </li>
      <li>
        Private
      </li>
      <li>
        Shared Repository
      </li>
      <li>
        Public (Channel)
      </li>
    </ul>
  </ul>
  
  <p>
    The table below summarizes the permissions for different user application & context roles, in the context of channels / galleries.  
  </p>
  
  <div class="table-wrap">
    <table class="confluenceTable">
      <tbody>
        <tr>
          <td class="confluenceTd">
            <p>
              <strong>Applicative role</strong>
            </p>
            
            <p>
              <strong> </strong>
            </p>
            
            <p>
              <strong> </strong>
            </p>
            
            <p>
               
            </p>
            
            <p>
              <strong>Type</strong>
            </p>
          </td>
          
          <td class="confluenceTd">
            <p align="center">
              <strong>anonymousRole</strong><br />(User not logged in)
            </p>
          </td>
          
          <td class="confluenceTd">
            <p align="center">
              <strong>viewerRole</strong><br />(Doesn’t have My Media, so can’t publish)
            </p>
          </td>
          
          <td class="confluenceTd">
            <p align="center">
              <strong>privateOnlyRole</strong>
            </p>
          </td>
          
          <td class="confluenceTd">
            <p align="center">
              <strong><span class="GINGER_SOFTWARE_mark">adminRole</span> </strong><strong>&</strong>
            </p>
            
            <p align="center">
              <strong>unmoderatedAdminRole</strong>
            </p>
            
            <p align="center">
              (Uploaded entries by these <span class="GINGER_SOFTWARE_mark">roles</span> will automatically be approved if the account has moderation enabled)
            </p>
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd">
            <p align="center">
              <a name="open" rel="nofollow"></a>Open
            </p>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories
            </p>
            
            <ul>
              <li>
                Can view only, if <em>allowAnonymous=true</em>
              </li>
              <li>
                Can’t participate (publish, moderate, manage)
              </li>
            </ul>
            
            <p>
               
            </p>
            
            <p>
              Channel
            </p>
            
            <ul>
              <li>
                Can’t access at all (since channels require log-in) if public channels option is not checked
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Can view (regardless of contextual role)
              </li>
              <li>
                Can’t publish (doesn’t have My Media)
              </li>
              <li>
                Other participation (moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Can view (regardless of contextual role)
              </li>
            </ul>
            
            <p>
               
            </p>
            
            <p>
              Categories (for backward compatibility with KMS 4.6):
            </p>
            
            <ul>
              <li>
                Can publish only if <span class="GINGER_SOFTWARE_mark">Contributor</span> (even though the Category is Open) [this is the only difference from <span class="GINGER_SOFTWARE_mark">adminRole</span>]
              </li>
            </ul>
            
            <p>
               
            </p>
            
            <p>
              Channels
            </p>
            
            <ul>
              <li>
                Doesn’t need to be a member to publish (Channel is Open, as in KMS 4.6)
              </li>
            </ul>
            
            <p>
               
            </p>
            
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Other participation (moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Can view (regardless of contextual role)
              </li>
              <li>
                Can publish everywhere (since admin)
              </li>
              <li>
                Other participation (moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd">
            <p align="center">
              Restricted
            </p>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Can’t view or participate (publish, moderate, manage) since not logged in
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Same as <a href="http://knowledge.kaltura.com/kaltura-mediaspacekaltura-application-framework-kaf-roles-and-permissions#open" class="external-link" rel="nofollow">Open</a>.
            </p>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Can view (regardless of contextual role)
              </li>
              <li>
                Other participation (publish, moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Can view (regardless of contextual role)
              </li>
              <li>
                Other participation (publish, moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd">
            <p align="center">
              Private
            </p>
          </td>
          
          <td class="confluenceTd">
            <p>
              Same as <strong>Restricted</strong>
            </p>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Can’t publish (<span class="GINGER_SOFTWARE_mark">since</span> doesn’t have My Media)
              </li>
              <li>
                Viewing and Participation (moderation, management) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Viewing and Participation (publish, moderation, management) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Categories & Channels
            </p>
            
            <ul>
              <li>
                Viewing and Participation (publish, moderation, management) according to contextual <span class="GINGER_SOFTWARE_mark">role</span>
              </li>
            </ul>
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd">
            <p align="center">
              Shared Repository
            </p>
          </td>
          
          <td class="confluenceTd">
            <p>
              Channels
            </p>
            
            <ul>
              <li>
                Can’t view or participate (publish, moderate, manage) since not logged in
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <ul>
              <li>
                Can’t publish (since doesn’t have My Media)
              </li>
              <li>
                Viewing and Participation (moderation, management) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Channels
            </p>
            
            <ul>
              <li>
                Can view and publish (regardless of contextual role)
              </li>
              <li>
                Other participation (moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
            <p>
              Channels
            </p>
            
            <ul>
              <li>
                Viewing and Participation (publish, moderation, management) according to contextual role
              </li>
            </ul>
          </td>
        </tr>
        
        <tr>
          <td class="confluenceTd">
            <p align="center">
              Public
            </p>
          </td>
          
          <td class="confluenceTd">
            <p>
              Channels
            </p>
            
            <ul>
              <li>
                Can view only, if <em>allowAnonymous=true</em>
              </li>
              <li>
                Can’t participate (publish, moderate, manage)
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
             <p>
              Channels
            </p>
            
            <ul>
              <li>
                Can view (regardless of contextual role)
              </li>
              <li>
                Can’t publish (doesn’t have My Media)
              </li>
              <li>
                Other participation (moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
             <p>
              Channels
            </p>
            
            <ul>
              <li>
                Can view (regardless of contextual role)
              </li>
              <li>
                Other participation (publish, moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
          
          <td class="confluenceTd">
             <p>
              Channels
            </p>
            
            <ul>
              <li>
                Can view (regardless of contextual role)
              </li>
              <li>
                Can publish everywhere (since admin)
              </li>
              <li>
                Other participation (moderate, manage) according to contextual role
              </li>
            </ul>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div id="likes-and-labels-container">
   
</div>