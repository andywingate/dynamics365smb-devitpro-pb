---
title: User assistance model
description: Learn about the user assistance model for Dynamics 365 Business Central and how your solution can comply with it.
author: SusanneWindfeldPedersen
ms.custom: evergreen
ms.topic: article
ms.date: 12/30/2024
ms.author: solsen
ms.reviewer: solsen
---

# [!INCLUDE[prod_long](developer/includes/prod_long.md)] User assistance model

The [!INCLUDE[prod_short](developer/includes/prod_short.md)] user assistance model is based on the following principles:

- Get started

    Home pages give easy access to key tasks so users can easily get started with work every day. Embedded user assistance implemented as teaching tips help users understand new or unfamiliar pages, and checklists make it easy to get started in a new company.  
- Get unblocked

    Embedded user assistance implemented as tooltips answers most immediate questions about what fields and actions do.
- Learn more

    The Help menu and *Learn more* links on tooltips and teaching tips provide context-sensitive access to Help articles with more information.

Apps, extensions, and customizations are expected to follow the same model by applying tooltips to controls on page objects, and by providing links to Help for their functionality. Learn more about customizing and extending the user assistance in [Contribute to the help](help/contributor-guide.md) and [Configure the help experience](deployment/configure-help.md).  

In this article, we'll talk about the user assistance model itself and what it does.  

## Help users get started

The user assistance concept of *Get Started* isn't just about getting started with [!INCLUDE[prod_short](developer/includes/prod_short.md)] on the first day. It's also about getting started all the other days, and about doing infrequent and unfamiliar tasks. Any new product can be baffling at first. For infrequent tasks, even after months of using the product, users can find it hard to remember where that report is, or how to fill in that page.  

The default version of [!INCLUDE [prod_short](includes/prod_short.md)] online includes in-product tours to introduce the first users of a new tenant to the general user interface and the most used pages. The in-product search makes it easy to find pages or reports - provided that you remember what they're called.  

We strive to make [!INCLUDE [prod_short](includes/prod_short.md)] easy to get started with in the browser and in the apps for desktop and mobile devices. Assistance in the shape of wizards is helpful for setup or filling in data for a complicated report, for example. Home pages that are designed for a particular role or job help users get started with their daily work – they can easily get to their most important tasks, and that means that [!INCLUDE[prod_short](developer/includes/prod_short.md)] helps them get their work done more efficiently. Similarly, in-product links to videos give new users a quick introduction to how the product works.  

### Onboarding checklist

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]

To help users set up [!INCLUDE [prod_short](includes/prod_short.md)] on the first day, partners can add required steps to the checklist. The checklist is intended to help users fill in necessary information and help themselves get familiar with [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in [Get users started with the checklist](administration/onboarding-checklist.md).  

### Teaching tips and tours

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]

[!INCLUDE [ua-teaching-tips](includes/ua-teaching-tips.md)]

> [!NOTE]
> Teaching tips supplement the tooltips that provide descriptions for all fields and actions.  

[!INCLUDE [ua-tooltips-teachingtips](includes/ua-tooltips-teachingtips.md)]

Learn more in [Teaching tips and in-app tours for onboarding users](administration/onboarding-teaching-tips-tours.md).  

### Help pane

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

When the user opens the Help pane, they see content and links to learn more based on where they are in the product. Once users discover the Help pane, they're more likely able to help themselves get unblocked.  

The Help pane shows up to four types of links:

[!INCLUDE [ua-help-pane-links-default](includes/ua-help-pane-links-default.md)]

If the automatically generated links don't answer the user's question, then the user can use the *Search* field to search Microsoft's content, both documentation and e-learning material. Currently, search in the [!INCLUDE [prod_short](includes/prod_short.md)] Help pane can't access sites other than the *learn.microsoft.com* site, including Microsoft Learn.  

## Help users get unblocked

Even the best designed user interface can still be confusing to some. It can be difficult to predict what users will find confusing, and that's why the base application includes descriptions for all controls and actions that can be accessed when you choose the caption of the control or action. In combination with descriptive captions and instructional text, these tooltips, or callouts, constitute the larger part of our current implementation of *embedded user assistance*, which is an important principle in today's world of software design.  

The tooltips help users unblock themselves by providing an answer to the most likely questions the users might have, such as "What data can I input here?" or "What is the data used for?". Keep tooltips in mind when you develop the user interface of your solution.  

:::image type="content" source="media/ua_tooltip_standard.png" alt-text="A standard tooltip for a field on a card page.":::

These descriptions are applied to controls on pages rather than table fields. Table fields can be read-only in one page and editable in another, so the tooltips describe the difference. In [!INCLUDE [prod_short](developer/includes/prod_short.md)], this type of "What is this field?" content is embedded in the page objects, and resource files can be used for translated user interfaces. Learn more in [Working with translation files](developer/devenv-work-with-translation-files.md).  

Most tooltips end with an automatically generated link to *learn more* as described in the [Help users learn more](#help-users-learn-more) section; however, tooltips for actions do not have *Learn more* links:

:::image type="content" source="media/ua_tooltip_client.png" alt-text="A tooltip for an action without Learn More link.":::

> [!TIP]
> Users can always use the <kbd>Ctrl</kbd>+<kbd>F1</kbd> keyboard shortcut to access the *learn more* content that's configured for the currently-selected item in the user interface. In 2022 release wave 1 and later, <kbd>Ctrl</kbd>+<kbd>F1</kbd> opens the Help pane with automatically generated links to related content from Microsoft and partners.

The tooltips in [!INCLUDE [prod_short](developer/includes/prod_short.md)] are conceptually similar to *[field descriptions](/dynamics365/fin-ops-core/fin-ops/get-started/view-export-field-descriptions?toc=/dynamics365/finance/toc.json)* in Dynamics 365 Finance and related apps, and *[teaching tips](/windows/uwp/design/controls-and-patterns/dialogs-and-flyouts/teaching-tip)* in the Universal Windows Platform's Fluent Design guidelines. The onboarding framework in [2021 release wave 1](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/in-app-contextual-help-improvements) added another interpretation of teaching tips that you can add to your [!INCLUDE [prod_short](developer/includes/prod_short.md)] solution. Learn more in [Teaching tips and in-app tours for onboarding users](administration/onboarding-teaching-tips-tours.md).

### Guidelines for tooltip text

[!INCLUDE [ua-tooltips](includes/ua-tooltips.md)]

#### Examples

[!INCLUDE [ua-tooltips-examples](includes/ua-tooltips-examples.md)]

## Help users learn more

The content that Microsoft publishes under the user assistance concept of *Learn more* is intended to answer those questions that the user interface (including the tooltips) can't answer, such as where that page fits into the bigger workflow, or what comes next, or what would be the alternative.

Users can access this content either through the *Learn more* link in tooltips, by choosing the Help menu, or by using the <kbd>Ctrl</kbd>+<kbd>F1</kbd> keyboard shortcut.  

### Links in the Help pane

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

The *Learn more* links on tooltips and the <kbd>Ctrl</kbd>+<kbd>F1</kbd> shortcut now open the Help pane. In most cases, the pane shows the following types of content:

[!INCLUDE [ua-help-pane-links-default](includes/ua-help-pane-links-default.md)]

The partner-provided links are based on the mechanism for adding links through app-level and page-level configuration. Learn more in [Configure context-sensitive help](help/context-sensitive-help.md).  

The following screenshot illustrates the Help pane when it's opened from the **Purchase Invoice** page.

:::image type="content" source="media/ua_help_pane.png" alt-text="Help pane with tooltip text, page metadata link, and links to learn.microsoft.com.":::

In this case, the **Purchase Invoice** page hasn't been extended by any apps. If two apps had extended the page, their page-level and app-level configuration would be used to add links on a card after the *Related articles from Microsoft Docs* card.  

The base version of [!INCLUDE[prod_short](developer/includes/prod_short.md)] uses content that's published to an online library, ([learn.microsoft.com/dynamics365/business-central](/dynamics365/business-central/index)), so that it can also serve as onboarding material and as feature overviews that you can share with prospects. The content is written in Markdown, and our source files are available in a [public GitHub repo](https://github.com/MicrosoftDocs/dynamics365smb-docs) that you can extend for your customers.  

> [!NOTE]
> Currently, [!INCLUDE [prod_short](includes/prod_short.md)] doesn't require the Help for your own functionality to be created in a specific format. But we expect you to make it available on a website that the users of your functionality can access. Learn more in [Configure context-sensitive help](help/context-sensitive-help.md).

For the base version of [!INCLUDE [prod_short](developer/includes/prod_short.md)], free online learning is also available on Microsoft Learn. Learn more in [Business Central on Microsoft training](/learn/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs).

### Feedback and contributions

On the *learn.microsoft.com* website, each documentation article encourages you to provide feedback. We've changed the mechanism a couple of times based on feedback. Currently, we ask you to choose the **Feedback** action below the article's title. You can give the article a rating, and write a comment if you want to. The feedback goes straight to the article's author and the team that owns the docs.  

We welcome your contributions, both as pull requests with suggestions or corrections to the content, and as issues with bugs or comments. However, we can only accept contributions to the content in the [dynamics365smb-docs](https://github.com/MicrosoftDocs/dynamics365smb-docs) and [dynamics365smb-devitpro-pb](https://github.com/MicrosoftDocs/dynamics365smb-devitpro-pb) repos. Also, we cannot address issues or questions about the product.  

> [!IMPORTANT]
> If you have feedback about translations, you can report a GitHub issue in the [dynamics365smb-docs](https://github.com/MicrosoftDocs/dynamics365smb-docs) repo.  

Learn more in [Contribute to the help](help/contributor-guide.md).  

### Working in Markdown

If you fork one of our repos, you'll be authoring in Markdown. We recommend that you learn the basics by referring to the [Learn Markdown reference](/contribute/markdown-reference) section in the Learn Contributor Guide.  

The [Learn Authoring Pack for Visual Studio Code](/contribute/how-to-write-docs-auth-pack) can aid with Markdown authoring and validation in Visual Studio Code. However, you can also use other text editors to edit Markdown.  

For other tips and tricks, see [Contribute to the Help](help/contributor-guide.md) and the blog post [Collaborate on content for Business Central](https://cloudblogs.microsoft.com/dynamics365/it/2019/08/14/collaborate-on-content-for-dynamics-365-business-central/).  

## Translate the Help

If you want to deliver a [localization app](developer/readiness/readiness-develop-localization.md), or if you want to deliver your functionality in more than one country/region, you'll want to translate the Help as well as the product. We suggest that you take a look at the [Microsoft Dynamics 365 Translation Service](/dynamics365/unified-operations/fin-ops-core/dev-itpro/lifecycle-services/translation-service-overview), which is available as preview in Microsoft Dynamics Life Cycle Services. Learn more in [Translate documentation files](/dynamics365/unified-operations/fin-ops-core/dev-itpro/lifecycle-services/use-translation-service-ua).  

The user interface text, including the tooltips, is translated as part of the application. Learn more in [Working with translation Files](developer/devenv-work-with-translation-files.md).  

## Style

At Microsoft, we're in process of simplifying and unifying our style guides. To get to know the Microsoft style, use the [Microsoft Writing Style Guide](/style-guide/welcome/) as a good starting point. The [!INCLUDE [prod_short](developer/includes/prod_short.md)] follows most of the guidelines in the Microsoft Writing Style Guide with exceptions for industry terminology and other product-specific issues.  

<!--
## Get notified about changes through an RSS feed

[!INCLUDE [ua-rss](includes/ua-rss.md)]
-->

## Related information

[Configure the help experience](deployment/configure-help.md)  
[Adding help links from pages, reports, and XMLports](developer/devenv-adding-help-links-from-pages-tables-xmlports.md)  
[ToolTip property](developer/properties/devenv-tooltip-property.md)  
[InstructionalText property](developer/properties/devenv-instructionaltext-property.md)  
[Development of a localization solution](developer/readiness/readiness-develop-localization.md)  
[Translate documentation files](/dynamics365/unified-operations/dev-itpro/lifecycle-services/use-translation-service-ua)  
[Resources for help and support](help-and-support.md)  
[Blog post: Extending and customizing the Help](https://cloudblogs.microsoft.com/dynamics365/it/2019/08/14/extending-and-customizing-the-help-in-dynamics-365-business-central)  
[Blog post: Collaborate on content for Business Central](https://cloudblogs.microsoft.com/dynamics365/it/2019/08/14/collaborate-on-content-for-dynamics-365-business-central/)  
[Docs contributor guide](/contribute/)  
[Docs Authoring Pack for Visual Studio Code](/contribute/how-to-write-docs-auth-pack)  
[Microsoft Cloud Style Guide (requires login)](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2696)  
[Microsoft Writing Style Guide](/style-guide/welcome/)  
[Onboarding experiences in Business Central](administration/onboarding-experiences.md)  
[Teaching tips and in-app tours for onboarding users](administration/onboarding-teaching-tips-tours.md)  

[!INCLUDE [footer-banner](includes/footer-banner.md)]
