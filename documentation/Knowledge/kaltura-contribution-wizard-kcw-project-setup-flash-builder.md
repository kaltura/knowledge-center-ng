---
layout: page
title: "Kaltura Contribution Wizard (KCW) Project Setup in Flash Builder"
date: 2012-04-11 10:55:50
---

<p class="mce-heading-2">
  Setting up the <span>KCW Project</span>
</p>

This article explains how developers can set up the KCW project in Flash Builder.

<p class="mce-procedure">
  To set up the project
</p>

1.  Check out the workspace from <http://kaltura.org/kalorg/kcw/trunk>.
2.  If your SDK does not include en\_US\_kaltura locale, copy the locale:<ol style="list-style-type: lower-alpha;">
      <li>
        In the command line, set the root to the bin folder that is under your current sdk folder.
      </li>
      <li>
        Run the following command: copylocale en_US en_US_kaltura
      </li>
    </ol>

3.  Set a valid sessionId (ks) in ContributionWizard->html-template->index.template.html. Ensure that the sessionId matches the partnerId that you use.
4.  Verify that the flash player version is 10.0.1:  
    Right click the ContributionWizard project and select Properties->Flex Compiler->Adobe Flash Player options.  
    <img src="{{site.url}}/assets/437">
5.  Compile the workspace.
6.  The contribution wizard includes the following modules:
<ol style="list-style-type: lower-alpha;">
  <li>
    SearchView
  </li>
  <li>
    SoundRecorder
  </li>
  <li>
    UploadView
  </li>
  <li>
    WebcamView
  </li>
</ol>

<p style="padding-left: 30px;">
  These modules are compiled under bin-debug->com->kaltura->contributionWizard->view->[Module Folder].
</p>

<p style="padding-left: 30px;">
  To run the most updated compiled modules, copy the modules from these folders to the bin-debug folder.
</p>