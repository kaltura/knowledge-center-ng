---
layout: page
title: "HTML5 Testing Process and Methodology"
date: 2012-04-16 16:16:18
---

 

## **Testing Major Releases**

### **What do we test?**

*****[Progression][1][][1]*****

 [1]: #prog

[********Regression********][2]

 [2]: #reg

[***********On-Sites Tests***********][3]

 [3]: #onsite

For each major release we use the following testing methodologies:

***<a name="prog"></a>Progression***

Newly added features are reported in a [Release Notes Page][4] that describes the contetn of the new version. The content includes:

 [4]: http://html5video.org/wiki/Kaltura_HTML5_Release_Notes

*   New features as described by the product team
*   Bugs as reported by customers and QA

<span>Each new feature or bug fix, is tested as stand alone, and as part of a common work flow as explained in this article.</span>  
  


***<a name="reg"></a>Regression***

Regression tests are meant to prevent malfunctions at customers' sites, and to insure that existing functionality will not break.

The common methodology is to adhere to one strict flow (for example, same entry, same metadata/cue points), However, so that we can enlarge the coverage over time without extending the amount of tests, we may at times compromise on the strict flow. We have a predefined set of tests that we run as a regression for each version. By changing these tests slightly every run, we gain a larger variety of tests, so the test cases are not changed but values are. For example, every regression test includes adding cue points to an entry and playing the entry.  The entry may be changed, and the cue points' exact pin points may be changed, but the flow is the same.

Regression also includes testing the relevant plugins.

***<a name="onsite"></a>On-Sites Testing***

HTML5 is expected to support customizations at customers' sites and maintain backwards compatibility. We use a list of the 50 most viewed sites (HTML5 wise), with the highest potential to be viewed by mobile and set those sites as a reference for our on-sites testing. This methodology allows us to ensure backward compatibility when releasing a new version of the HTML5 library.

To see the new library in action we replace the HTML5 library that is currently used (latest on production) with the candidate version. This allows us to:

1.  Add extra tests to detect more issues that might be revealed in the field but were not detected in the lab (including quality and performance issues among other).
2.  Maintain a reference for next releases: Nothing should break on these sites as we deliver new versions. Functionality that is not working correctly is considered as regression and must be fixed before releasing.
3.  Get familiar with customers' configurations, settings, sites, and use cases. We document all information obtained for each site tested, and include the information as part of the use cases tracked in our Quality Center.

Replacing the library is not possible in every site due to configuration settings.

## **Bug Fixing Strategy and Testing**

***Testing real use cases:*** We focus our tests on cases that are actually used by customers, while edge cases that are considered relatively rare, are not necessarily covered. For example: There are known issues with features that we are aware of, and that are reported. Lesser and not commonly used known issues are not at the top our priorities to fix.

***Bug fixing:*** Regression bugs are our top priority. Then, we fix bugs found during development that are prioritized according to common customer flows. Our plans include refractoring the HTML5 library and to address all the known issues.

## **Browsers and Devices Support Matrix**

We follow the <a href="{{site.url}}/documentation/Knowledge/browsers-and-mobile-devices-tested-kaltura-players.html" target="_blank">Graded Browsers and Devices Support Matrix</a> which is defined by our product team. Roughly, most tests are conducted on the following platforms, in the order they are listed:

1.  iPad 1,2 (4 & 5)
2.  iPhone (4 & 5)
3.  IE 9
4.  Android devices (Tablet and phones)
5.  FF and Chrome

Most of our tests are done on the iPad. We mostly test on IE9, which is the most problematic browser using HTML5 library. Testing this wide array of browsers and devices dramatically enlarges the testing matrix.

Most of our tests on mobile devices are done on the iPad and we extensively test on IE9, which is the most problematic browser when using HTML5 library. Testing this wide array of browsers and devices dramatically enlarges the testing matrix, which enhances our analysis of common usage in the field.

We use strategic risk management to determine which browsers and devices we test. This strategy allows us to cope with the huge matrix of supported broswers and devices. We reduce the amount of tests, by analysing the usage in field, and then determine which devices and browsers will be most tested.

<p class="mce-heading-2">
  <strong>QA Tests Cycle</strong>
</p>

The following lists the steps for testing the HTML5 library:

1.  After a new HTML5 library is delivered to QA, the library is installed on the QA environment.
2.  Run Progression and Regression tests.
3.  Upload to the staging environment /production for testing purposes only (not released to all customers yet).
4.  During this time – bugs are reported to the Quality Center and fixed (having as many development cycles as required).
5.  Perform On-Sites tests.
6.  Resolve additional bugs from On-Sites tests – (customer's sites' oriented fixes).
7.  Identify the release candidate.
8.  When the release is ready, relevant bugs are fixed, and the new library and Release Notes are released.
9.  Run Post Production tests to make sure the release is available to all and works as expected.

 

<p class="mce-heading-3">
  <strong>Testing Minor Releases</strong>
</p>

When required, we provide a minor release, usually a customized version with 1-2 fixes. These fixes are 'added' to the production version. In most cases, the customizations are not published, since the customizations are tailored for a specific customer's needs. This process allows us to release a minor version quickly with low risk, which is based on an existing major version that has already been tested. These customizations are merged into a major version, when and if the customer wants to upgrade to a more advanced version. This methodology was recently added to provide shorter testing cycles. 