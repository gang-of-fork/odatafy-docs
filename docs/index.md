# Odatafy Documentation
This page contains the documentation for the odatafy ecosystem. It focuses on the core module, odatafy-parser, and gives an overview over the plugins, which are documented in their respective README files. This documentation only covers the support of the oData v4 query options in the [Feature-Support](https://gang-of-fork.github.io/odatafy-docs/feature-support/) section. If you want to learn how the query options work, please refer to the [oData v4 URL documentation](http://docs.oasis-open.org/odata/odata/v4.01/odata-v4.01-part2-url-conventions.html).

## What is odatafy?
Odatafy is an ecosystem of npm modules that aim to help you create [oDatav4](https://www.odata.org/documentation/) compatible REST-APIs, thus allowing you to accelerate development and save time and money by helping you to implement an API that is based on the very-well established oData v4 standard. As it is by far the most tideous task, odatafy currently only supports query operations.

## How does odatafy work?
The odatafy ecosystem is composed mainly of three parts: the core, plugins and showcases.
### The core
The core is the [odatafy-parser npm module](https://www.npmjs.com/package/odatafy-parser), which is a parser consisting of multiple [peg.js](https://www.npmjs.com/package/pegjs) grammars working together to parse an oData v4 URL and translate it into an Abstract Syntax Tree (AST). The structure of this AST is documented in the [oDataParseResult section](https://gang-of-fork.github.io/odatafy-parser/modules.html#oDataParseResult) of our [typedoc documentation](https://gang-of-fork.github.io/odatafy-parser/). Now you could use the core on its own and program a translator for database queries on top of the AST. Luckily, we already did this for you by offering Plugins. 
### Plugins
Plugins are the most essential part of developing an application with odatafy. Plugins are npm packages built on top of the AST, that the [odatafy-parser](https://www.npmjs.com/package/odatafy-parser) provides. Currently, we are maintaining two plugins:  
- [odatafy-mongodb](https://www.npmjs.com/package/odatafy-mongodb): Convert odata v4 requests to MongoDB Aggregation Queries with the `parseODataUrl()` function  
- [odatafy-mongoose](https://www.npmjs.com/package/odatafy-mongoose): Effortlessly generate Service Metadata Files and Expand Mappings for odatafy-mongodb from mongoose   schemas


### Showcases
Finally, to bring it all together, we have created a few applications using the odatafy ecosystem for you to play around with and to guide you through using odatafy in your application.  
- [odatafy-mongodb-example](https://github.com/gang-of-fork/odatafy-mongodb-example): A simple RESTful API leveraging all available plugins. Feel free to try out some odata queries [here](https://example.odatafy.gang-of-fork.de/)!  
- [odatafy-flutter-app](https://github.com/gang-of-fork/odatafy-flutter-app): A flutter app built on top of the odatafy-mongodb-example app that dynamically generates an admin dashboard for data querying and manipulation based on the Service Metadata and oDatav4 API provided by [odatafy-mongodb](https://www.npmjs.com/package/odatafy-mongodb) and [odatafy-mongoose](https://www.npmjs.com/package/odatafy-mongoose).
 
## Examples 
The below examples show how to implement the most common scenarios in an express.js service.
### Transform a query into an AST using odatafy-parser
### Transform a query into a MongoDB aggregation query using odatafy-mongodb
### Generate an ExpandMapping and enable $expand using odatafy-mongodb and odatafy-mongoose
### Generate the Service Metadata File using odatafy-mongoose