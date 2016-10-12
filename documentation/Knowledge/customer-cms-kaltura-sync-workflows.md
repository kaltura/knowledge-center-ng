---
layout: page
title: "Customer CMS-Kaltura Sync Workflows"
date: 2012-02-02 21:38:53
---

The three-phased tactic detailed here targets two goals:

*   **Reduce risk**: Avoid performing a “heart transplant” integration where the customer’s CMS is completely replaced with Kaltura’s in one step, requiring to also handle all known integration points with the CMS beforehand (or be ready to quickly fix breakage in overlooked integration points)
*   **Reuse effort**: Code required for synchronizing new content will be first developed to be used for migration of legacy content, also allowing customer’s developers to fully test their code over time before going live and get acquainted with Kaltura’s APIs.

The three-phased tactic includes the following synchronization phases:

1. <a name="migrate_legacy"></a>[**Migration of legacy content**:][1]

 [1]: http://knowledge.kaltura.com/customer-cms-kaltura-sync-workflows-migrating-legacy-content

<p style="padding-left: 30px;">
  ○ Business Requirement: Have the Kaltura-powered customer player play all legacy content created by customer and supported by Kaltura, while retaining customer’s CMS as an active Master.
</p>

<p style="padding-left: 30px;">
  ○ Technical Process: Bulk-generate Kaltura entries (media assets) using the existing flavors (video files CDN urls), thumbnails (urls) and metadata already produced by customer and stored in their CMS. These new entries will then be linked to the original CMS objects by assigning each CMS object with a corresponding Kaltura entry id (requires adding a new attribute/field to CMS object).
</p>

<p style="padding-left: 30px;">
  ○ Success Criteria: The Kaltura-powered player will be able to play all migrated content, from Kaltura, using the assigned entry id, without having to modify any other CMS-related customer processes.
</p>

2. <a name="slave_publish"></a>[**Customer CMS (Master)->Kaltura (Slave) publishing (Interim workflow)**][2]:

 [2]: http://knowledge.kaltura.com/customer-cms-kaltura-sync-workflows-customer-cms-master-kaltura-slave-publishing-interim-workflow

<p style="padding-left: 30px;">
  ○ Business Requirement: Have the Kaltura-powered customer player play all new content created by customer come launch date, until the customer is ready to switch over to Kaltura as Master CMS.
</p>

<p style="padding-left: 30px;">
  ○ Technical Process: Retain current publishing workflow performed by customer but also generate Kaltura entries using the flavors (urls), thumbnails (urls) and metadata produced and stored in the customer’s CMS. These new entries will then be linked to the original CMS objects by assigning each CMS object with a corresponding Kaltura entry id.
</p>

<p style="padding-left: 30px;">
  ○ Success Criteria: The Kaltura-powered player will be able to play all new content, from Kaltura, using the assigned entry id, without having to modify any other CMS-related customer processes.
</p>

3. <a name="CMS_slave_publish"></a>**[Kaltura (Master)->Customer CMS (Slave) publishin][3]g**:

 [3]: http://knowledge.kaltura.com/customer-cms-kaltura-sync-workflows-katura-master-customer-cms-slave-publishing

<p style="padding-left: 30px;">
  ○ Business Requirement: Have Kaltura manage the entire publishing workflow, while retaining customer’s CMS as an active Slave, allowing to switch publishing over to Kaltura internally without being forced to affect other integration points.
</p>

<p style="padding-left: 30px;">
  ○ Technical Process: Pending on customer’s decision and planning to detach existing integration points from CMS and re-attach them directly to Kaltura (e.g. have these load/store content from/to Kaltura)
</p>

<p style="padding-left: 30px;">
  ○ Success Criteria: The Kaltura-powered player will be able to play all new content directly from Kaltura; Content will be directly managed on Kaltura; Customer’s website will be powered by Kaltura’s APIs; Other integration points will be connected to Kaltura in a phased approach.
</p>