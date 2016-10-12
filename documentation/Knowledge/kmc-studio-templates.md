---
layout: page
title: "KMC Studio Templates"
date: 2012-03-11 00:16:13
---

 

## Terminology

**UIconf **– UI configuration document, generally refers to player UIconf (see below), but also holds player features (see below).

**Player UIconf** – An XML file that describes the player layout. KDP reads this file in order to know what features it should show or load.

**Player Features** – An XML file that is used by the studio to determine which features a certain player instance has.

**Template, Full Template** – The template that defines the features the player derived from this template can have, and determines the general layout of the player. A template UIconf is organized in the same way as any other player UIconf, separated into template features (sometimes referred to as "Full Template Features") and template player UIconf ("Full Player").

There are different templates for playlist players, multiple playlists players, hovering controllers players, simple players, and other types of players.

**Feature** – a button or a set of buttons, a plugin or any functionality KDP has.

 

<p class="Copyright">
  <strong>Player UIconf vs. Player Features File</strong>
</p>

<p class="Copyright">
  The KDP uses the player UIconf, the KMC Studio uses the player features file.
</p>

<p class="Copyright">
  A features file declares the optional features for a certain player, and the options for each feature. The template's features file is the full features file for this template, while the features file saved for each player holds only the selected features and their attributes, or the differences from the full template.
</p>

<p class="Copyright">
  For example: The player UIconf will indicate you want to show your watermark on the bottom-left corner. This information will be saved in the player's features file, and should be available when you want to edit the player. There will be no indication whether to display the watermark or not, or to select the position where the watermark icon should display.  This information is saved in the template features file.
</p>

<p class="Copyright">
  <strong>Under the Hood – Where the Magic Happens</strong>
</p>

<p class="Copyright">
  A player's features file holds the ID of the template from which it was created. This template is loaded when the player is edited. The info stored in the player's features file is then applied to the general template –including the player features selected, and the values for the attributes of those features. The attribute values are used to build the Features’ tab accordion menu, and to adjust the controls of the other wizard tabs.
</p>

<p class="Copyright">
  When you apply changes to the player (either click "Save" or "Preview"), the full player UIconf is taken from the template and updated according to the selected features. At the same time, the player feature’s file is derived from the full template features according to the user's selections.
</p>

<p class="Copyright">
  Obviously, a player's template cannot change even if the latest templates used for the Studio are updated. A player is always edited using the actual template that was used to create it.
</p>

<p class="Copyright">
  <strong>God is in the details – Adding Your Own Feature</strong>
</p>

This section refers to the accordion component in the "Features" tab of the studio. Other panels are not configurable. When referring to a “features file” we refer to the “template's features file”, unless noted otherwise.

### Adding Accordion Menu Tabs

The features UIconf's "features" node consists of "feature" nodes. These are the contents of the features accordion.

A "feature" node which has its "showCheckbox" attribute set to "false" declares a new accordion tab. All the features in the file down to the next accordion header will be inserted under this tab.

For example:  The next line creates the “controls” tab shown in the image:

<p class="Code">
  <feature featureLabel="Controls" showCheckbox="false"/>
</p>

<p class="Copyright">
   <img src="{{site.url}}/assets/305">
</p>

<h3 class="mce-sub-heading">
  Adding features
</h3>

<p class="Copyright">
  This section describes the configuration of the "Options" screen for different types of features. Features are added in the same order that they will display in the accordion. Let’s go over the different feature types:
</p>

<h4 class="mce-sub-heading">
  General Feature
</h4>

A general feature affects only one node in the player UIconf, like the watermark, the stars rating, or the volume controller.

The main "feature" tag should have the following attributes:

*   showCheckbox="true" - The value "true" indicates this is a player feature, rather than an accordion header.
*   id - The value should be the same as the ID of the element you are manipulating in the player UIconf file.
*   featureLabel - The text shown in the accordion near the checkbox for this feature.
*   "k\_param=selected" and "k\_value=true" indicates that if this feature is selected by default (k\_value=true) or not (k\_value=false).

The contents (children) of the "feature" tab are UI elements that describe the form for this feature.  The following elements are eligible.

<p class="Sub-Heading mce-sub-heading">
  Layout elements
</p>

<p class="Code">
   <Spacer/>, <Label/>, <Seperator/>
</p>

These elements should not have ID attributes.

<p class="Sub-Heading mce-sub-heading">
  Data elements
</p>

*   "id" - used internally. Make sure your component has a unique ID.
*   "k\_param" - holds the name of the attribute on the relevant XMLnode that will be manipulated by this component. "k\_value" holds its default value.
*   <CheckBox/> - elements cannot be used for true/false selections. They are used for cross-screens features and should not be used for other purposes.
*   <Input/> -  for free text
*   <ComboBox/> - elements have inner elements stating their "dataProviders", items with data and label. The label is shown in the dropdown, while the actual value used is the "data".  A ComboBox node might look like this:  
    {syntaxhighlighter brush: xml;fontsize: 100; first-line: 1; }<ComboBox id="timerType" k\_param="timerType" k\_value="forwards"> <item> <data>forwards</data> <label>Count Forwards</label> </item> <item> <data>backwards</data> <label>Count Backwards</label> </item> </ComboBox>{/syntaxhighlighter} 
*   <NumericStepper/> - supports minimum, maximum attributes. int value type only.
*   <ColorPicker /> - uses uint (color) value type.

<p class="Copyright">
  To allow a UI element in the form to change values that do not correspond to the same ID as the feature, we can set the ‘applyTo’ attribute, in its tag with the corresponding UIconf element ID.
</p>

<p class="Copyright mce-heading-4">
  Cross-Screens Feature
</p>

The Cross Screens feature affects UI elements in more than one screen, for example, the buttons shown on the player before the video starts, on pause, on hover and after video ends. Handling these features is based on the elements' IDs in the player UIconf.

In the player UIconf, controller buttons that can benefit from this type of unified behavior should be named XXXControllerScreen, where XXX is the feature ID. Start screen buttons should be XXXStartScreen, end screen buttons XXXEndScreen, pause screen buttons XXXPauseScreen, and buttons that show on the player on hover XXXPlayScreen. These buttons should be positioned inside the relevant screen node so that the KDP will handle them correctly.

For example, a "share" button that appears before the video starts playing should be declared as: <Button id="shareBtnStartScreen" ../>

On the features file end, the feature ID should be the same as the prefix for the UIconf elements (XXX above). There should be a main checkbox for the buttons that appear on top of the video, its ID is traditionally showOnVideoControllers. The exact name doesn't matter, but consistency is important. The features file should have an ID so that it will be processed.

The inner checkboxes should be named according to the screen in which they appear, so that when concatenated to the feature ID they will be the same as the names given to the UIconf elements described previously (StartScreen, PlayScreen, PauseScreen, EndScreen).

The checkbox for the controller button should be named ControllerScreen. This button can either be an icon button or a label button. The selection between the two is done using a ‘combobox’ with k\_value=k\_buttonType, and a ‘dataprovider’ that holds the optional values: buttonIconControllerArea for icon buttons and buttonControllerArea for label buttons. In order to allow customization of the button's label and tooltip, input fields with attributes k\_param=label and k\_param=tooltip are used, with the default values held in their k_value attributes.

Checkboxes will not work in features forms anywhere else or in any other manner of use. If you need a yes-no selection element, use a dropdown with two values.

### Examples

<h4 class="mce-sub-heading">
  General Feature
</h4>

The following feature node will create this feature options screen in the Studio.

<img src="{{site.url}}/assets/308">

 {syntaxhighlighter brush: xml;fontsize: 100; first-line: 1; }<feature showCheckbox="true" specialFeature="true" featureLabel="Your Watermark" id="watermark" selected="true" k\_param="selected" k\_value="true"> <Spacer/> <Label label="Your Watermark" bold="true"/> <Label label="Brand your player with your own logo displayed as a watermark on the video. Upload an image to a location on the web and provide the link below."/> <Spacer/> <Label label="Watermark URL"/> <Input id="watermarkPath" k\_param="watermarkPath" k\_value="http://www.kaltura.com/content/uiconf/kaltura/kmc/appstudio/kdp3/exampleWatermark.png"/> <Label label="Watermark landing page url"/> <Input id="watermarkClickPath" k\_param="watermarkClickPath" k\_value="http://www.kaltura.com/"/> <Spacer/> <Label label="Watermark location on the video:"/> <ComboBox id="watermarkPosition" k\_param="watermarkPosition" k\_value="bottomLeft"> <item> <data>bottomLeft</data> <label>Bottom Left</label> </item> <item> <data>bottomRight</data> <label>Bottom Right</label> </item> <item> <data>topLeft</data> <label>Top Left</label> </item> <item> <data>topRight</data> <label>Top Right</label> </item> </ComboBox> <Label label="Padding"/> <NumericStepper id="padding" k\_param="padding" k\_value="5"/> </feature>{/syntaxhighlighter}

<p class="CodeCxSpFirst">
   
</p>

<h4 class="mce-sub-heading">
  Cross Screens Feature
</h4>

The following feature node will create this feature options screen in the Studio.{syntaxhighlighter brush: xml;fontsize: 100; first-line: 1; }<feature showCheckbox="true" featureLabel="Full Screen Button" id="fullScreenBtn" selected="true" k\_param="selected" k\_value="true"> <Spacer/> <Label label="Full Screen Button" bold="true"/> <Label label="This button allows users to switch to full screen mode, and back to regular mode."/> <Spacer/> <Label label="Location & Playing States:"/> <CheckBox id="showOnVideoControllers" label="Video Area" selected="true" k\_param="selected" k\_value="true"> <CheckBox label="Before play" id="StartScreen" selected="false" k\_param="selected" k\_value="false"/> <CheckBox label="During play, when mouse is on screen" id="PlayScreen" selected="false" k\_param="selected" k\_value="false"/> <CheckBox label="When paused" id="PauseScreen" selected="false" k\_param="selected" k\_value="false"/> <CheckBox label="End play" id="EndScreen" selected="false" k\_param="selected" k\_value="false"/> </CheckBox> <Seperator/> <CheckBox label="Controls Area" id="ControllerScreen" selected="true" k\_param="selected" k\_value="true"/> <Label label="Display in controls area as:"/> <ComboBox id="Display" k\_param="k\_buttonType" k\_value="buttonIconControllerArea"> <item> <data>buttonIconControllerArea</data> <label>Icon</label> </item> <item> <data>buttonControllerArea</data> <label>Label</label> </item> </ComboBox> <Label label="Button Label:"/> <Input id="Label" k\_param="label" k\_value="fullscreen"/> <Seperator/> <Spacer/> <Label label="Tooltip Text:"/> <Input id="Tooltip" k\_param="tooltip" k_value="Toggle fullscreen"/> </feature>{/syntaxhighlighter}

 