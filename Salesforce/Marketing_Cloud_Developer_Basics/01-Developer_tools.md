# DEVELOPER TOOLS

## Marketing Clouds APIs

Marketing Cloud offers two APs: REST (Representational StateTransfer) and SOAP (Simple Object Access Protocol). The REST aPI exposes broader access to Marketing Cloud capabilities. The SOAP API provides comprehensive access to most email functionality. These two APIs share a common authentication mechanism based in OAuth 2.

### REST API

The REST aPI for Marketing Cloud is a great way to share assets from your internal databases or applications with your Marketing Cloud account.

All new Marketing Cloud technologies implement REST API, .

* The REST API uses JSON (JavaScript Object Notation) request and response bodies and resource endpoints to support multichannel use.

* Most REST call are synchronous.

* Timeout values are 120seconds for non-tracking operations and 300 seconds for tracking and data retrieve operations.

* The maximum payload of any calls is four megabytes.


### SOAP API

As you know, SOAP APIs provide a means for applications on different operating systems. technologies, and languages to communicating using only XML. You can use this API for managing things such us tracking data, subscribers and lists, automation, content, and mos other email activities.

* The SOAP API uses SOAP envelopes to pass information between you and Marketing Cloud.
* We recommend a limit of no more than 2000 per minute for soap calls.
* Support may request your SOAP envelope to troubleshoot issues.


### SDKs

Marketing Cloud SDKs provide a cross-functional framework around de SOAP and REST APIs, allowing you to integrate APIs using native language code libraries.

## Programmatic Languages

### AMPscript

Is a scripting language that you can embed within HTML emails, text emails, lading pages, SMS messages, and push notifications from MobilePush. Marketing Cloud processes the AMPscript calls at the time of send.

### Server-Side JavaScript (SSJS)

Marketing Cloud uses JavaScript code processed by Marketing Cloud Servers. Instead of using the browser to render the JavaScript on the client-side computer, Marketing Cloud executes the JavaScript on the server when rendering.

Wondering whether to use AMPscript or SSJS?

* AMPscript es the preferred language for personalizing message content. 
* AMPscript works better than SSJS for use cases where each subscriber needs to see unique content.
* AMPscript has a shorter learning curve than SSJS for users new to scripting languages in general.
* A great number of people already know JavaScript and can immediately apply that knowledge to Marketing Cloud.
* Most users can handle the tasks they need to perform using AMPscript.

Is better use AMPscript or Platform object server-side JavaScript functions in email messages and reserve the use of Core library server-side JavaScript to landing pages and applications where AMPscripts doesn't provide appropriate functions.

### Guide Template Language (GTL)

GTL provides a declarative syntax used for creating personalized, dynamic, data-driven messages, as well as constructing cross channel templates and layouts- GTL uses the widely adopted handlebars amd mustaches template languages amd provides additional functionality, while simplifying how user interact with content and data to help them quickly build personalized journey messages. GTL works with JSON data sources supplied by script or by REST API service. Guide can also access specified lists and data extensions within a Marketing Cloud account.



