---
title: Technical support overview
description: Learn about how to support your Business Central customers, online and on-premises, troubleshoot issues, and when to escalate problems to Microsoft.
author: SusanneWindfeldPedersen
ms.topic: overview
ms.author: solsen
ms.date: 12/30/2024
ms.reviewer: solsen
---

# Technical support for [!INCLUDE[prod_long](developer/includes/prod_long.md)]

Each customer of [!INCLUDE [prod_short](developer/includes/prod_short.md)] has a partner who assists with technical support. As a [!INCLUDE[prod_short](developer/includes/prod_short.md)] reselling partner, you're an administrator of your customers' [!INCLUDE[prod_short](developer/includes/prod_short.md)] tenants, and you're the first line of support. You get requests for support from your customers that you must triage, investigate, and either resolve or escalate to Microsoft.  

In this section, learn about the tools that are available to you to help you troubleshoot your customers' [!INCLUDE [prod_short](developer/includes/prod_short.md)].  

## Configuring the support experience

Because you're the first line of support for your customers, you must make it easy for them to contact you. They can find your contact information in the [Help and Support](/dynamics365/business-central/product-help-and-support?toc=/dynamics365/business-central/dev-itpro/toc.json) page.  

> [!IMPORTANT]
> You must have set up users in your own tenant in Partner Center as either *Admin agent* or *Helpdesk agent*, and they must have *delegated administration* privileges in your customer's [!INCLUDE [prod_short](developer/includes/prod_short.md)] to support the customer. Learn more in [Delegated Administrator Access to Business Central Online](administration/delegated-admin.md).

### To supply your support contact information in the administration center

1. In the [!INCLUDE [prodadmincenter](developer/includes/prodadmincenter.md)], choose the environment that you want to specify your contact details for, such as *Production*, and then, in the **Support** menu, choose **Manage Support Contact**.
2. Fill in the **Name**, **Email address**, and the **Website** fields, so that your users know how to contact you for technical support.
3. Optionally, choose the **Apply to all environments** checkbox if you want to add the same details to all related environments for this tenant.

Your customer can now contact you if they experience problems and need help. If you also can't resolve a reported issue, escalate the issue to Microsoft. Learn more in [Managing Technical Support](administration/manage-technical-support.md).  

### On-premises deployments

In on-premises deployments of [!INCLUDE[prod_short](developer/includes/prod_short.md)], the **Help and Support** page doesn't contain the section for contacting technical support. Instead, you can enter an agreement with your customer's administrator about how and when to contact you.  

There are two other links in the **Help and Support** page that you can customize:

- Blog

    Specifies a link to where your customers can access a blog about their solution  
- Coming soon

    Specifies a link to where your customers can access a roadmap for future changes

If you choose to not modify these settings, then the links go to Microsoft's blog and release notes.

Learn more in [Configuring [!INCLUDE[webserver](developer/includes/webserver.md)] Instances](administration/configure-web-server.md).


## Getting support for extension issues

As a partner, you must identify if the issue is caused by application logic or platform behavior:

- If the issue is caused by application logic, you must identify the publisher of the extension.
- If the extension is a per-tenant extension, as a partner, you must fix the issue.
- If the extension is an AppSource extension, you must contact the AppSource partner that developed the extension.
- If the extension is published by Microsoft, you must contact Microsoft support.

## Troubleshooting and support

The [!INCLUDE [prodadmincenter](developer/includes/prodadmincenter.md)] is your primary tool to support your customers. However, you can also sign in to the customer's [!INCLUDE [prod_short](developer/includes/prod_short.md)] as the delegated admin for troubleshooting.  

Learn more in [Managing Technical Support](administration/manage-technical-support.md).  

## Monitor service health

[!INCLUDE [admin-service-health](includes/admin-service-health.md)]

### Summary of where to file bugs and issues

As a partner, you have different support channels depending on what type of issue you want support for. The following list outlines the various channels.  

[!INCLUDE [prod_support](includes/prodsupport.md)]

> [!TIP]
> When you submit your first support ticket as a partner, you must specify details about your company's support plan. If you or your colleagues do not know these details, contact your Microsoft rep.

#### Non-product related questions

On occasion, as a partner, you'll run into questions that aren't directly related to the product. The following list outlines how to get answers to those questions.

[!INCLUDE [nonprodsupport](includes/nonprodsupport.md)]

## Related information

[Inspecting and troubleshooting pages](developer/devenv-inspecting-pages.md)  
[The Business Central Administration Center](administration/tenant-admin-center.md)  
[Managing technical support](administration/manage-technical-support.md)  
[Deployment overview](deployment/Deployment.md)  
[Administration of Business Central online](administration/tenant-administration.md)  
[Administration of Business Central on-premises](administration/Administration.md)  
[Provide technical support (Microsoft Partner Center)](/partner-center/provide-technical-support)  
[Providing support to your customers (Microsoft Partner Center)](/partner-center/customer-support)  
 
[!INCLUDE [footer-banner](includes/footer-banner.md)]