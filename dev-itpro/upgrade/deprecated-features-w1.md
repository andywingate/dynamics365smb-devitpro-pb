---
title: Deprecated Features in the Base App
description: Describes the features that have been moved, removed, or replaced in the W1 version.
author: brentholtorf
ms.author: bholtorf
ms.date: 12/11/2024
ms.reviewer: bholtorf
ms.topic: conceptual
ms.custom: bap-template
---

# Deprecated Features in the Base App

This article describes the features that have been moved, removed, or replaced in the W1 version of [!INCLUDE[prod_short](../developer/includes/prod_short.md)].

[!INCLUDE [feature-deprecation](../includes/feature-deprecation.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

## Changes in 2026 release wave 1

The following features will be removed in 2026 release wave 1.

### API (v1.0) for Business Central (removed)

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| With [!INCLUDE[prod_short](../includes/prod_short.md)] you can create Connect apps. Connect apps establish a point-to-point connection between [!INCLUDE[prod_short](../includes/prod_short.md)] and a 3rd party solution or service using the standard REST API to interchange data. <br><br>In 2020 release wave 2 we introduced a new improved API where all complex properties are replaced with first-level properties or navigation properties. This change significantly improves API performance, as complex fields were previously calculated at runtime. In API v2.0, all multipart keys and non-GUID keys are replaced with unique GUID keys, and entities can be retrieved using the SystemId, which is immutable, platform-enforced, and indexed. This change improves auditing and API reading performance.<br><br>The API (v1.0) will be removed in 2026 release wave 1.<br><br>The API v2.0 contains all the functionality from API v1.0, so migration should be possible. If this isn't the case, reach out to us via [https://github.com/microsoft/ALAppExtensions](https://github.com/microsoft/ALAppExtensions).<br><br>To learn about the replacement feature, go to [Transitioning from API v1.0 to API v2.0](../api-reference/v2.0/transition-to-api-v2.0.md). |


### Legacy Power BI apps on AppSource (removed)

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| While useful to show the Power BI embed capabilities in [!INCLUDE[prod_short](../includes/prod_short.md)], the legacy Power BI apps on AppSource: <br>Dynamics 365 Business Central - CRM<br>Dynamics 365 Business Central - Finance<br>Dynamics 365 Business Central - Sales<br> have now been superseeded by the 7 Power BI apps for finance, sales, purchasing, inventory, projects, and manufacturing that were released in the 25.1 version. <br><br>To learn about the replacement features, go to [aka.ms/bcAnalytics](https://aka.ms/bcAnalytics). |


## Changes in 2025 release wave 1

The following features are marked as `obsolete:pending` in 2025 release wave 1.

### Excel reports on the Business Manager and Accountant role centres

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| While useful to some organizations, the Balance Sheet, Income Statement, Statement of Cash Flow, Statement of Retained Earnings, Sales Taxes Collected, Customer Statements, Aged Accounts Payable, and Aged Accounts Receivable Excel reports that are currently available on the Business Manager and Accountant Role Centres are hard to change. To change them requires technical skills in AL and VBA programming. We've enhanced analytics capabilities in finance in each release wave over the last three years. For example, we've added data analysis capabilities on ledger tables, reports with Excel layouts that allow users to change the layout as they see fit, and Power BI reports for finance. <br><br>To learn about the replacement features, go to [aka.ms/bcFinanceAnalytics](https://aka.ms/bcFinanceAnalytics). |

### Legacy Power BI apps on AppSource (warning)

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| While useful to show the Power BI embed capabilities in BC, the legacy Power BI apps on AppSource: <br>Dynamics 365 Business Central - CRM<br>Dynamics 365 Business Central - Finance<br>Dynamics 365 Business Central - Sales<br>have now been superseeded by the 7 Power BI apps for finance, sales, purchasing, inventory, projects, and manufacturing that were released in the 25.1 version. <br><br>To learn about the replacement features, go to [aka.ms/bcAnalytics](https://aka.ms/bcAnalytics). |


## Changes in 2024 release wave 2

The following features are marked as `obsolete:pending` in 2024 release wave 2.

### Configuration packages for setup and evaluation data

> [!IMPORTANT]
> We will remove this feature in update 25.2.

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| We've changed the way we prepare databases for new evaluation and production companies. Instead of using configuration packages to add demo and setup data, you now use the **Contoso Coffee demo data** app. We shipped the Contoso Coffee demo data app in an earlier release to cover gaps in our demo and setup data, such as Manufacturing, Service, and Warehouse. Because the app is easy to use and now provides the comprehensive setup and demo data that was previously available in configuration packages, we're removing the configuration packages. To do that, we had to change how the **Create New Company** assisted setup guide initializes new companies with data. Our changes might affect your extensions. For details about what we removed, explore the Object and What's removed listings. |
|Removed| Enum 9120 "Company Data Type (Internal)"</br> Enum 9121 "Company Data Type (Sandbox)" </br> Enum 9122 "Company Data Type (Production)"</br> Codeunit 1799 "Import Config. Package File"</br> Codeunit 1800 "Assisted Company Setup":</br>* procedure WaitForPackageImportToComplete</br>* procedure FillCompanyData</br>* procedure ExistsConfigurationPackageFile</br>* procedure FindConfigurationPackageFile</br>* procedure SetUpNewCompany</br>* event OnAfterAssistedCompanySetupStatusEnabled</br>* event OnBeforeScheduleTask</br></br> Codeunit 1805 "Import Config. Package Files"</br>Table 1802 "Assisted Company Setup Status": </br>* field Import Failed</br>* field Package Imported</br>* procedure SetEnabled</br></br>Page 9192 "Company Creation Wizard":</br>* event OnBeforeValidateCompanyType</br>* event OnBeforeValidateCompanyType</br>* event OnOpenPageCheckAdditionalDemoData|
|Replaced|In addition to making it easier to install rich demo data, this change also enables another improvement. We're loosening up the relatively rigid update policies for major and minor updates that were in place. We're giving administrators extended update periods. For major updates, we're offering five-month update periods to give more time to test and prepare. For example, partners can spread out the workload of updating customer environments, and developers can verify that all apps are compatible. We've also given administrators the ability to opt out of minor updates during a grace period. To learn more, go to [Manage environment updates more flexibly](/dynamics365/release-plan/2024wave2/smb/dynamics365-business-central/manage-environment-updates-more-flexibly).|

### User groups

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced|User groups are replaced by security groups. Security groups were introduced in Business Central in 2023 release wave 1. They make it easier for administrators to manage user permissions by allowing them to group users by department, job function, and so on. Administrators assign the permissions to the group that its members need to do their jobs. Security groups are based on groups in Microsoft 365 admin center or Azure portal. That benefits administrators because they can use their security groups with other Dynamics 365 apps. For example, if salespeople use Business Central and SharePoint, administrators don't have to recreate the group and its members.<br><br>To learn more about security groups, go to [Control Access to Business Central Using Security Groups](/dynamics365/business-central/ui-security-groups).|

## Changes in 2024 release wave 1

The following features are marked as `obsolete:pending` in 2024 release wave 1.

### Excel reports on the Business Manager and Accountant role centers

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| The Excel reports (Balance Sheet, Income Statement, Statement of Cash Flows, Statement of Retained Earnings, VAT Collected, Customer Statements, Aged Accounts Payable, and Aged Accounts Receivable) that are available from the Business Manager and Accountant role centers are being replaced by new reports. The new reports use Excel layouts that allow power users to modify the layouts with Excel and upload the new layouts to [!INCLUDE[prod_short](../includes/prod_short.md)]. The deprecated reports will be hidden from the role centers in 2025 release wave 1 and will be completely removed from [!INCLUDE[prod_short](../includes/prod_short.md)] in 2026 release wave 1.|

### API (v1.0) for Business Central (warning)

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| With [!INCLUDE[prod_short](../includes/prod_short.md)] you can create Connect apps. Connect apps establish a point-to-point connection between [!INCLUDE[prod_short](../includes/prod_short.md)] and a 3rd party solution or service using the standard REST API to interchange data. <br><br>In 2020 release wave 2, we introduced a new improved API where all complex properties are replaced with first-level properties or navigation properties. This change significantly improves API performance, as complex fields were previously calculated at runtime. In API v2.0, all multipart keys and non-GUID keys are replaced with unique GUID keys, and entities can be retrieved using the SystemId, which is immutable, platform-enforced, and indexed. This change improves auditing and API reading performance.<br><br>We're making the API (v1.0) obsolete in 2024 release wave 1 (to be removed in 2026 release wave 1).<br><br>The API (v1.0) will be removed in 2026 release wave 1.<br><br>The API v2.0 contains all the functionality from API v1.0, so migration should be possible. If this isn't the case, reach out to us via [https://github.com/microsoft/ALAppExtensions](https://github.com/microsoft/ALAppExtensions).<br><br>To learn about the replacement feature, go to [Transitioning from API v1.0 to API v2.0](../api-reference/v2.0/transition-to-api-v2.0.md). |


## Changes in 2023 release wave 2

The following features are marked as `obsolete:pending` in 2023 release wave 2.

### Legacy time sheets experience

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| You can use time sheets in Business Central to track absence, and to track time and resources that are spent on a project. In 2021 Release Wave 1 we introduced a new experience where we converted time sheet pages to document pages (instead of worksheets). Using document pages lets you access time sheets on mobile devices. We're making the legacy experience obsolete in 2023 Wave 2 (to be removed in 2024 Wave 2) and enabling the new experience as the default for all new customers. To learn about the replacement feature, go to [Use Time Sheets](/dynamics365/business-central/projects-how-use-time-sheets). |

### G/L entry aggregations when posting invoices

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced|The **Invoice Post. Buffer** table is replaced by the use of the **Invoice Posting** interface. The replacement helps resolve extensibility issues for the legacy **Invoice Post. Buffer** table. You can now use your own implementation of G/L invoice posting.
If you're a developer and want to learn more about how to extend G/L entry aggregations when posting invoices, go to [Extending G/L Entry Aggregations When Posting Invoices](/dynamics365/business-central/dev-itpro/developer/devenv-invoice-posting-example).|

### Exchange Rates Adjustment report

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced|The legacy Exchange Rates Adjustment Report is being replaced by a new capability that increases extensibility and makes it easier to comply with local and industry-specific requirements. It also gives you more control over exchange rate adjustments with a posting preview and how dimension values are post when you adjust exchange rate, and better reporting. To learn more about the new capabilities, go do [Adjusting Exchange Rates](/dynamics365/business-central/finance-how-update-currencies#adjusting-exchange-rates).
<!--If you're a developer and want to learn more about how to use the new extensible exchange rates, go to <add link to output of related documentation deliverable on exchange rates adjustment extensiblitiy-->.

## Changes in 2023 release wave 1

The following features are marked as `obsolete:pending` in 2023 release wave 1.

### French, Belgian, and Dutch features for reviewing G/L accounts

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced| Businesses in all countries/regions can benefit from the ability to review general ledger entries before posting them. In a future release, we'll deprecate the country-specific feature and replace it with one that's available in all country versions. After the feature is deprecated, you can use it to access previous reviews, but not to do new reviews. We'll archive your data according to local requirements. To learn about the replacement feature, go to [Review Amounts in General Ledger Accounts](/dynamics365/business-central/finance-review-accounts).  |

### User groups

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced | User groups let administrators manage permissions for groups of users who have the same or similar roles in the business. For example, you might create a user group for your sales department, and one for your purchasers. To make it a bit easier for administrators to manage permissions, we're replacing user groups and adding the ability to group users directly on permission sets. On the **Permission Sets** page, use the **Users** FactBox to assign the set to users.<br><br> To make it easier to reuse sets of users across other Dynamics 365 apps, we've also introduced optional security groups. Administrators can link [!INCLUDE [prod_short](../includes/prod_short.md)] security groups to their counterparts in Microsoft Entra ID or Windows Active Directory. The link let's administrators manage group memberships in Active Directory. In terms of managing permissions, security groups work in the same way as user groups. To learn more about the new security groups, go to [Control Access Using Security Groups](/dynamics365/business-central/ui-security-groups).<br><br>If you have an extension that relies on user groups, and you'd like to explore examples of how to update it to use permission sets or [!INCLUDE [prod_short](../developer/includes/prod_short.md)] security groups, go to [Migrate from User Groups to Permission Sets or Security Groups](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-user-groups). |

## Changes in 2022 release wave 2

### Permissions and Permission Set Objects

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced | In the latest enhancements to composing permissions, the following legacy objects are marked as `obsolete:pending` and replaced with new ones:<br><br>* The Log Table Permissions code unit is replaced by the Log Table Data Permissions codeunit.<br><br>* The Permissions page is replaced by the Expanded Permissions page.<br><br>* The Tenant Permissions page is replaced by the Permission Set page.<br><br>For information about other objects and methods that are being obsoleted, refer to the obsolete reasons in permission management.|

### Microsoft SharePoint Connection Setup

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced | The SharePoint connection setup feature used for OneDrive integration is obsolete and will be removed in 2023 release wave 2 (version 23). In its place, version 21 offers a new guided setup to configure OneDrive integration for system and application features. Learn more about the new setup at [Managing OneDrive Integration with Business Central](/dynamics365/business-central/admin-onedrive-integration).<br><br>The deprecation means that the  **Microsoft SharePoint Connection Setup** page (9551 Document Service Config) is marked as `obsolete:pending`. However, the platform APIs (in codeunit 9510 Document Service Management) and the document service table that make the legacy functionality possible aren't being deprecated. So any partner solutions that use the APIs directly are unaffected by this change.<br><br>Existing customers who are upgrading to version 21, and eventually version 22, can continue to use the legacy SharePoint/Onedrive integration. But we highly recommend that you transition them to the newer OneDrive integration because it's the path going forward. Switching to the newer OneDrive integration setup is a one-way operation, meaning you can't revert to the legacy setup after you've made the switch.<br><br> We aspire to resume work on SharePoint integration at a later date.|

### Bank Reconciliation Worksheet and Deposits in North American versions (US, CA, MX)

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced | We're standardizing the features for reconciling bank accounts and making cash deposits, so that more country versions can benefit from them. For more information, see [Standardizing the bank reconciliation process in North American versions](/dynamics365-release-plan/2022wave1/smb/dynamics365-business-central/standardizing-bank-reconciliation-process-north-american-versions). The current features will still allow you to view posted bank reconciliations done through the Bank Rec. Worksheet page, and posted deposits done through the Deposits features, but you can't use these features to create new entries. In October 2023, you must use the Bank Reconciliation page for bank reconciliations. The Bank Rec. Worksheet page won't be available.|

## Changes in 2022 release wave 1

The following feature is marked as `obsolete:pending` in 2022 release wave 1.

### XBRL reporting

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Removed | Over the years, XBRL has become more than just tagging your financial statement. It's seen improvements in the level of reporting detail, schemas are more flexible in their design, and ESAF has added customization capabilities. This development has meant that the XBRL implementations in the countries/regions we support are diverse, and often complex. For example, taxonomies with hundreds of schema and linkbase files have become the norm. This complexity has made XBRL reporting a task that is better managed by either dedicated software or by service providers. <br><br> We recommend that you use these service providers. Alternatively, if you have the resources in-house, acquire a dedicated XBRL reporting tool. The XBRL org provides a list of tools and services. For more information, see [Tools and Services](https://www.xbrl.org/the-standard/how/tools-and-services/).<br><br> Currently, we expect to fully remove support for XBRL in 2023 release wave 1.|

### Intercompany Setup page

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Replaced | We have consolidated settings for setting up intercompany capabilities on a single page, and have added a new feature for automatically accepting intercompany transactions in general journals. The current **Intercompany Setup** page (page 621) is replaced with a new **Intercompany Setup** page (page 653). |

## Changes in 2021 release wave 2

### Standard APIs, Beta version

The following feature will be **Removed** with [!INCLUDE[prod_short](../developer/includes/prod_short.md)] 2021 release wave 2.

|Moved, Removed, or Replaced? |    Why?|
|-----------------------------|-----|
|Removed | Beta version of the standard APIs is removed in 2021 release wave 2. At this point, Beta APIs won't be available in new releases of [!INCLUDE[prod_short](../developer/includes/prod_short.md)]. There are many improvements to v1.0 and v2.0 of the standard APIs. Improvements include more APIs, better performance and improved OData capabilities. It's recommended that integrations move to v2.0 of the standard APIs.|

### Client secret authentication in integrations between Microsoft-hosted Business Central online and Microsoft Dataverse

The following feature will be **Removed** with [!INCLUDE[prod_short](../developer/includes/prod_short.md)] 2021 release wave 2.

|Moved, Removed, or Replaced? |Why?|
|---------|---------|
|Removed | The ability to use client secret Service-to-Service authentication to connect [!INCLUDE[prod_short](../developer/includes/prod_short.md)] with Dataverse will be removed for online tenants hosted by Microsoft in March 2022. To further strengthen security, we introduced the ability to use certificate-based authentication in client secret Service-to-Service authentication 2021 release wave 1 (version 18 and later). Existing users can easily switch to certificate-based authentication. For more information, see [Upgrade Connections from Business Central Online to Use Certificate-Based Authentication](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/upgrade-certificate-based-service-to-service-authentication-dataverse-dynamics-365-integration). On-premises customers, and online tenants that are hosted by ISVs, can continue using client secret authentication for their connections to Dataverse.|

### Legacy Outlook add-in for synchronizing data

The legacy Outlook add-in for synchronizing data, such as to-dos, contacts, and tasks, between Business Central and Outlook is **Removed** in [!INCLUDE[prod_short](../developer/includes/prod_short.md)] 2021 release wave 2.

|Moved, Removed, or Replaced? |Why?|
|---------|---------|
|Removed | This add-in used Business Central web services based on outdated technology.|

> [!NOTE]
> The feature is separate from and has no effect on the [!INCLUDE[prod_short](../developer/includes/prod_short.md)] add-in for Outlook, which is described at [Using Business Central as your Business Inbox in Outlook](/dynamics365/business-central/work-outlook-addin).

## Deprecated Features in 2020 release wave 1
The following feature was marked as `obsolete:pending` in 2020 release wave 1.

### Best Price Calculations
When you have recorded special prices and line discounts for sales and purchases, [!INCLUDE[prod_short](../developer/includes/prod_short.md)] ensures that your profit on item trade is always optimal. [!INCLUDE[prod_short](../developer/includes/prod_short.md)] calculates the best price on sales and purchase documents and on job and item journal lines.

|Moved, Removed, or Replaced?|Why?|
|----|----|
|Replaced|The functionality is replaced with new calculations that you can extend to include other sources or calculation methods. The current capabilities will be available, and can be used in parallel with the new, until 2021 release wave 1. For more information, see [Extending Best Price Calculations](../developer/devenv-extending-best-price-calculations.md).|

## Deprecated Features in 2019 release wave 2
The following sections describe the features that were deprecated in 2019 release wave 2.

### The Bank Data Conversion Service
You can use AMC's bank data conversion service to convert bank data from an XML file that you export from [!INCLUDE[prod_short](../developer/includes/prod_short.md)] into a format that your bank can accept.

|Moved, Removed, or Replaced?|Why?|
|----|----|
|Moved|The functionality has been moved to an extension. It now ships as the AMC Banking 365 Fundamentals extension, which can convert bank data to formats that are used by more than 600 banks worldwide. For more information, see [Using the AMC Banking 365 Fundamentals extension](/dynamics365/business-central/ui-extensions-amc-banking).|

### Reports 204-207
You can generate external-facing documents, such as sales invoices and order confirmations, that you send to customers as PDF files.

The reports in the 204-207 range are replaced by the following updated reports in the 1304 to 1307 range:

- 204, Sales-Quote -> 1304, Standard Sales-Quote
- 205, Order-Confirmation -> 1305, Standard Sales-Order Conf.
- 206, Sales-Invoice -> 1306, Standard Sales-Invoice
- 207, Credit-Memo -> 1307, Standard Sales-Credit Memo

> [!NOTE]
> The **No. of Copies** field is removed from the new reports because of performance reasons and because selection of the quantity to print works differently on modern printers. To print a report more than once, users can list the same report multiple times on the **Report Selection** page for the document type in question.

|Moved, Removed, or Replaced? |Why?|
|---------|---------|
|Replaced|The reports in the 204-207 range are replaced by the reports in the 1304 to 1307 range. To avoid duplicated features, the reports in the 204-207 range will be removed.|
<!--This is just stubbed in. Need the actual names of the reports and a better description of the information they provided.-->

### User Personalizations and Profile Configurations
You can personalize pages and configure profiles by adding or removing fields, and [!INCLUDE[prod_short](../developer/includes/prod_short.md)] will save your changes.

|Moved, Removed, or Replaced? |Why?|
|---------|---------|
|Replaced|The shift to AL made the legacy features for personalization and configuring profiles outdated. Therefore, we've introduced new tooling. In this release, existing personalizations and configurations are discarded, and you must use the new tools to recreate them. Your new changes will be kept in future releases.|

## Objects that have been marked as obsolete
Part of deprecating features is marking the objects that comprise them as "obsolete." Before we deprecate an object, we tag it as "obsolete:pending" to alert our partners of it's deprecation. The object will have the tag for one year before we remove it from [!INCLUDE[prod_short](../developer/includes/prod_short.md)].
<!--should probably mention the other tags too. For example, "after one year we will mark the object as "ObsoleteState:Removed."-->

## Breaking Changes
When we move, remove, or replace an object, breaking changes can occur in other apps or extensions that use the object. To help our partners identify and resolve breaking changes, we have created a [Breaking Changes](https://github.com/microsoft/ALAppExtensions/blob/master/BREAKINGCHANGES.md) document. The document lists known issues and suggestions for what to do about them.

## Features that are available only in the online version
<!--Should we include a section about this?-->
Some features are available only under specific circumstances, or not at all intended for use in on-premises versions of [!INCLUDE[prod_short](../developer/includes/prod_short.md)]. For a list and descriptions of those features, see [Features not implemented in on-premises deployments](../features-not-implemented-on-premises.md).

## Related information

[Deprecated Features in the Platform - Clients, Server, and Database](deprecated-features-platform.md)  
[Deprecated Features in the Austrian Version](deprecated-features-at.md)  
[Deprecated Features in the Belgian Version](deprecated-features-be.md)  
[Deprecated Features in the Canadian Version](deprecated-features-ca.md)  
[Deprecated Features in the Czech Version](deprecated-features-cz.md)  
[Deprecated Features in the Dutch Version](deprecated-features-nl.md)  
[Deprecated Features in the Finnish Version](deprecated-features-fi.md)  
[Deprecated Features in the German Version](deprecated-features-de.md)  
[Deprecated Features in the Icelandic Version](deprecated-features-is.md)  
[Deprecated Features in the Italian Version](deprecated-features-it.md)  
[Deprecated Features in the Mexican Version](deprecated-features-mx.md)  
[Deprecated Features in the Norwegian Version](deprecated-features-no.md)  
[Deprecated Features in the Russian Version](deprecated-features-ru.md)  
[Deprecated Features in the Swedish Version](deprecated-features-se.md)  
[Deprecated Features in the Swiss Version](deprecated-features-ch.md)  
[Deprecated Features in the UK Version](deprecated-features-uk.md)  
[Deprecated Features in the United States Version](deprecated-features-us.md)  
[Deprecated Fields, and Fields Marked as Obsolete in Local Functionality](deprecated-fields.md)  
[Deprecated Tables](deprecated-tables.md)  
[ALAppExtensions repository (legacy)](https://github.com/microsoft/ALAppExtensions)  
[BCApps repository (substitute for ALAppExtensions)](https://github.com/microsoft/BCApps)  
[Best Practices for Deprecation of Code in the Base App](../developer/devenv-deprecation-guidelines.md)  
[Microsoft Timeline for Deprecating Code in Business Central](../developer/devenv-deprecation-timeline.md)  
