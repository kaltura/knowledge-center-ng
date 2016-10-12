---
layout: page
title: "Creating Profile XSD And Custom KMC View XML For Kaltura Custom Metadata Profile"
date: 2012-04-11 01:24:51
---

The custom data feature enables you to define custom metadata that will be added to every entry in your content. 

This article explains how to manually create a custom data XSD for the Kaltura Management Console (KMC). 

<p class="mce-note-graphic">
  <span style="font-size: 14px; background-color: #f2f4d5;">You can define custom fields in the KMC: Under </span><a href="http://www.kaltura.com/index.php/kmc/kmc4#account|metadata" target="_blank" style="font-size: 14px;">Settings>Custom Data</a><span style="font-size: 14px; background-color: #f2f4d5;">, click Add New Schema. See </span><a href="http://knowledge.kaltura.com/node/343" target="_blank" style="font-size: 14px;">What fields can be configured in the Kaltura custom metadata schema</a><span style="font-size: 14px; background-color: #f2f4d5;"> and </span><a href="http://knowledge.kaltura.com/node/346" target="_blank" style="font-size: 14px;">How to add a schema?</a><span style="font-size: 14px; background-color: #f2f4d5;">.</span>
</p>

<p class="mce-heading-2">
  Custom Data Structure
</p>

The custom data structure includes all data for each field: Name, UI label, type, min occur and max occur restrictions, allowed values for list types, and all other parameters that you define. The custom data structure is saved on the server as an XSD. Custom data is saved as *Metadata Profile*. 

The custom data XSD must fulfill the following requirements:

*   Make the XSD a complex metadata structure, not a flat hierarchic structure.
*   Name the main XSD element *metadata*. 
*   Place all custom fields under the XSD *metadata* element. 

<p class="mce-heading-3">
  Supported Custom Data Fields
</p>

 The following types of custom fields are supported:

*   textType <span>– Values are free text.</span>
*   dateType <span>– <span>A date field</span></span>
*   objectType <span>– <span>A list to a different entry (asset) that can be used to create compound structure. Examples include Related Videos and linking a trailer to a full-length film.</span></span>
*   listType <span>– <span> Similar to the textType. Allows the publisher to define a list of fields to use. After you enter the values, a select box element enables you to select a value from the existing list (for example, countries or months.)</span></span>

<div>
  Add the custom field types to the XSD as follows:
</div>

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;xsd:complexType name="textType"&gt;
    &lt;xsd:simpleContent&gt;
      &lt;xsd:extension base="xsd:string"/&gt;
    &lt;/xsd:simpleContent&gt;
 &lt;/xsd:complexType&gt;
 
&lt;xsd:complexType name="dateType"&gt;
    &lt;xsd:simpleContent&gt;
      &lt;xsd:extension base="xsd:long"/&gt;
    &lt;/xsd:simpleContent&gt;
&lt;/xsd:complexType&gt;
  
&lt;xsd:complexType name="objectType"&gt;
    &lt;xsd:simpleContent&gt;
      &lt;xsd:extension base="xsd:string"/&gt;
    &lt;/xsd:simpleContent&gt;
 &lt;/xsd:complexType&gt;
  
&lt;xsd:simpleType name="listType"&gt;
    &lt;xsd:restriction base="xsd:string"/&gt;
 &lt;/xsd:simpleType&gt;
</pre>

<p class="mce-heading-2">
  Custom Data View
</p>

The custom data view is an XML that describes the way custom fields appear in the KMC entry's Custom Data tab. If an XML is not defined, the default KMC view will be used.

When you create your XSD manually, you usually need to create your own view to display all of the hierarchic levels in your custom data structure.

<p class="mce-procedure">
  To create an XML for a custom data view
</p>

1.  Create an XML with the following format:<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;layouts&gt;
	&lt;layout id="KMC"&gt;
&lt;/layout&gt;
&lt;/layouts&gt;
</pre>
    
    The KMC uses the *KMC* layout content to display the custom data in the entry's Custom Data tab. Add every component you want to display to the “KMC” layout. 

2.  For each XSD element you want to display, add a corresponding view component to the KMC layout. For each component, include the following attributes:  
    <table class="LightList-Accent11" style="width: 590px;" border="1" cellspacing="0" cellpadding="0">
      <tbody>
        <tr>
          <td valign="top" width="127">
            <p style="text-align: left;">
              <strong>Attribute name</strong>
            </p>
          </td>
          
          <td valign="top" width="197">
            <p style="text-align: left;">
              <strong>Description</strong>
            </p>
          </td>
          
          <td valign="top" width="79">
            <p style="text-align: left;">
              <strong>Required</strong>
            </p>
          </td>
          
          <td valign="top" width="187">
            <p style="text-align: left;">
              <strong>Example</strong>
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="127">
            <p style="text-align: left;">
              <strong>compPackage</strong>
            </p>
          </td>
          
          <td valign="top" width="197">
            <p style="text-align: left;">
              The package of the component
            </p>
          </td>
          
          <td valign="top" width="79">
            <p style="text-align: left;">
              Yes
            </p>
          </td>
          
          <td valign="top" width="187">
            <p style="text-align: left;">
              <em>mx.containers.</em> for VBox
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="127">
            <p style="text-align: left;">
              <strong>metadataData</strong>
            </p>
          </td>
          
          <td valign="top" width="197">
            <p style="text-align: left;">
              The property with the information that the user inserts. The value of the metadataData attribute must be a valid property of this UI component.
            </p>
          </td>
          
          <td valign="top" width="79">
            <p style="text-align: left;">
              Yes (if exists)
            </p>
          </td>
          
          <td valign="top" width="187">
            <p style="text-align: left;">
              <em>text</em> for textInput. <em>selectedItem</em> for comboBox.
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="127">
            <p style="text-align: left;">
              <strong>dataType</strong>
            </p>
          </td>
          
          <td valign="top" width="197">
            <p style="text-align: left;">
              The type of the input that should be received from the user
            </p>
          </td>
          
          <td valign="top" width="79">
            <p style="text-align: left;">
              Yes (if exists)
            </p>
          </td>
          
          <td valign="top" width="187">
            <p style="text-align: left;">
              <em>String</em> for textInput. 
            </p>
            
            <p style="text-align: left;">
              <em>Boolean</em> for check box.
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="127">
            <p style="text-align: left;">
              <strong>name</strong>
            </p>
          </td>
          
          <td valign="top" width="197">
            <p style="text-align: left;">
              The name of the corresponding element in the XSD
            </p>
          </td>
          
          <td valign="top" width="79">
            <p style="text-align: left;">
              Yes
            </p>
          </td>
          
          <td valign="top" width="187">
            <p>
               
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="127">
            <p style="text-align: left;">
              <strong>Id</strong>
            </p>
          </td>
          
          <td valign="top" width="197">
            <p style="text-align: left;">
              The ID for special components that require special handling from the code.
            </p>
          </td>
          
          <td valign="top" width="79">
            <p style="text-align: left;">
              Yes, for the following components
            </p>
            
            <ul>
              <li style="text-align: left;">
                container
              </li>
              <li style="text-align: left;">
                VBox (for a list of check boxes)
              </li>
              <li style="text-align: left;">
                uniqueId (for text input that  generates unique IDs)
              </li>
              <li style="text-align: left;">
                comboBox
              </li>
              <li style="text-align: left;">
                multiVBox
              </li>
            </ul>
          </td>
          
          <td valign="top" width="187">
            <p>
               
            </p>
          </td>
        </tr>
        
        <tr>
          <td valign="top" width="127">
            <p style="text-align: left;">
              <strong>styleName</strong>
            </p>
          </td>
          
          <td valign="top" width="197">
            <p style="text-align: left;">
              The styleName of the component
            </p>
          </td>
          
          <td valign="top" width="79">
            <p style="text-align: left;">
              No
            </p>
          </td>
          
          <td valign="top" width="187">
            <p>
               
            </p>
          </td>
        </tr>
      </tbody>
    </table>

For example, for the following element in the XSD:

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;xsd:element id="md_TextUnlimited" name="TextUnlimited" minOccurs="0" maxOccurs="1” type=”textType”&gt; &lt;xsd:annotation&gt; &lt;xsd:documentation&gt;&lt;/xsd:documentation&gt; &lt;xsd:appinfo&gt; &lt;label&gt;TextUnlimited Level 0&lt;/label&gt; &lt;key&gt;TextUnlimited Level 0&lt;/key&gt; &lt;searchable&gt;true&lt;/searchable&gt; &lt;description&gt;&lt;/description&gt; &lt;/xsd:appinfo&gt; &lt;/xsd:annotation&gt; &lt;/xsd:element&gt;</pre>

Add a corresponding component in the view XML as follows:

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;TextInput id=”textInput” compPackage=”mx.controls.” metadataData=”text” dataType=”String” styleName=”dynamicTextInput” width=”300” name=”TextUnlimited”/&gt;</pre>

<h2 class="mce-heading-2">
  <strong>Advanced </strong><strong>Custom Data View Uses</strong>
</h2>

<div>
  The custom data view supports the following advanced uses:
</div>

*   If an element has the attribute *maxOccurs=unbounded,* Kaltura wraps the corresponding component with a *multi* component. A *multi* component is a special Kaltura component that contains *add* and *remove* buttons, which enables the user to add or remove an element multiple times.

<p style="padding-left: 30px;">
  For example, the following element in the XSD:
</p>

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;xsd:element id="md_DateUnlimitedLevel1"   name="DateUnlimitedLevel1" minOccurs="0" 
maxOccurs="unbounded" type="dateType"&gt;
		&lt;xsd:annotation&gt;
			&lt;xsd:documentation&gt;&lt;/xsd:documentation&gt;
			&lt;xsd:appinfo&gt;
				&lt;label&gt;DateUnlimited Level 1&lt;/label&gt;
				&lt;key&gt;DateUnlimited Level 1&lt;/key&gt;
				&lt;searchable&gt;false&lt;/searchable&gt;
				&lt;description&gt;&lt;/description&gt;
			&lt;/xsd:appinfo&gt;
		&lt;/xsd:annotation&gt;
&lt;/xsd:element&gt;</pre>

<p style="padding-left: 30px;">
  Will have the following corresponding components in the view XML:
</p>

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;MultiComponent id="multiVBox" compPackage="com.kaltura.edw.view.customData." name="DateUnlimitedLevel1"&gt; 
&lt;DateField id="dateField" compPackage="mx.controls." metadataData="selectedDate" dataType="Date" dateChooserStyleName="dynamicDateChooser" yearNavigationEnabled="true" name="DateUnlimitedLevel1"/&gt;
&lt;/MultiComponent&gt;
</pre>

*   If an element has one or more children, Kaltura wraps the children in a container component to display the children in an indented hierarchic structure in the KMC. The container component appears as follows:

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;VBox id="container" compPackage="mx.containers." name="elementName"&gt;</pre>

*   The component view supports a *related entries table* component. This component is specifically for custom data. To use this component, your element must contain the *objectType* type**.**

<p style="padding-left: 30px;">
  The component view appears as follows:
</p>

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;EntryIDLinkTable id="entryLinkTable" compPackage="com.kaltura.edw.view.customData." metadataData="dataArray" dataType="Array" name="elementName" maxAllowedValues="1"/&gt; </pre>

<p class="mce-note-graphic">
  <strong>Add the “maxAllowedValues” property only if you want to restrict the number of related entries to 1.</strong>
</p>

*    The following views are supported for ListType: 
*   comboBox
*   The dataType is String. (A label, not an item, is selected.)
*   the *metadataData* is "*selectedItem"*.
*   Add a *dataProvider* attribute. The value of this attribute is one string, containing all optional values separated by commas. Use the same values as the values in the XSD. For example, *dataProvider="1,2,3,4"* will create a list with four values, which are the four enumerated numbers.

<p style="padding-left: 90px;">
  For example:
</p>

<pre class="brush: as3;fontsize: 100; first-line: 1; ">&lt;ComboBox id="comboBox" compPackage="mx.controls." metadataData="selectedItem" dataProvider="opt1,opt2,opt3,opt4" dataType="String" styleName="dynamicComboBox" width="204" height="25"/&gt;</pre>

*   List of check boxes
*   Create a checkbox for each element. 
*   Wrap all check boxes in a VBox. 
*   The label of each check box must match an optional value.

<p style="padding-left: 30px;">
  For example:
</p>

<pre class="brush: xml;fontsize: 100; first-line: 1; ">&lt;VBox id="VBox" compPackage="mx.containers." name="ListUnlimitedLevel1"&gt;
&lt;CheckBox id="checkBox" compPackage="mx.controls." metadataData="selected" dataType="Boolean" label="one"/&gt;
&lt;CheckBox id="checkBox" compPackage="mx.controls." metadataData="selected" dataType="Boolean" label="two"/&gt;					
&lt;/VBox&gt;
</pre>

<p class="mce-procedure">
  To create a custom metadata profile
</p>

Call the following API calls to create a metadata profile:

**Service:** metadataProfile

**Action:** add

**MetadataProfile:**

        **metadataObjectType: **ENTRY

        **metadataProfileName:** Any name besides “KMC_PROFILE”

**xsdData:** A string representation for the structure XSD

**viesData:** A string representation for the view XML

<p class="mce-procedure">
   <span>To update a custom metadata profile</span>
</p>

<span></span>Call the following API calls to update an existing metadata profile:

**Service**: metadataProfile

**Action**: update

**Id**: The ID of the profile to update

**MetadataProfile**:

<p style="text-align: left;">
                <strong>metadataObjectType</strong>: ENTRY
</p>

**xsdData**: (Optional) Updates the custom data XSD data.

**viewsData**: (Optional) Updates the custom data view data. 