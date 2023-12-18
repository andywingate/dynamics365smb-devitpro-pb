> [!TIP]  
> If the same code needs to run both in the UI but also in the background (in a scheduled task or with a job queue entry) or in a web service call (SOAP/OData/API), then use `if GuiAllowed() then` calls to encapsulate AL code that interact with the user. For more information, see [System.GuiAllowed() Method](../methods-auto/system/system-guiallowed-method.md).