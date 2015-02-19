# Swagger Descriptions for Common Reuse

This repository contains manually created descriptions for those Web APIs one would like to invoke through
generic Swagger clients.

The files provided herein are just descriptions of 3rd party provided services, in order to help you use and
create simple clients for them very quickly. Unless stated otherwise we have no relationship with these 3rd
parties and therefore are neither responsible for their services nor can we help out resolving any difficulties
the 3rd party service may be experiencing.

Should you wish to add another description to this collection for the benefit of others, or should you wish to
submit some improvements to existing ones, don't hesitate to contribute. The more, the merrier!

## What's Swagger?

Taken from Swagger's own documentation:

"The goal of Swagger™ is to define a standard, language-agnostic interface to REST APIs which allows both
humans and computers to discover and understand the capabilities of the service without access to source code,
documentation, or through network traffic inspection. When properly defined via Swagger, a consumer can
understand and interact with the remote service with a minimal amount of implementation logic. Similar to
what interfaces have done for lower-level programming, Swagger removes the guesswork in calling the service."

## Using the Descriptions

The descriptions in this repository could directly be interpreted by any swagger-aware software. The only minor
thing to bear in mind is that typically swagger clients assume that the swagger descriptions are being served
from a Web server with CORS enabled. To use them locally, you may have to launch one server with CORS support.

A simple way to do this is to use a [simple Python server](https://gist.github.com/cpedrinaci/bdcac7d25685909eb966).

### Node.js
For those working with Node.js, see [swagger-client](https://www.npmjs.com/package/swagger-client) -- a very complete client.

### NodeRed
[NodeRed](http://nodered.org) is a tool for easily wiring together hardware devices, APIs and online services.

We have created a specific node -- [node-red-contrib-swagger](https://github.com/kmi/node-red-contrib-swagger) -- for simplifying the integration of Web APIs within
NodeRed flows.

The aforementioned node includes a local server able to directly serve swagger descriptions. So you won't need
to bother and launch a Web server to serve the swagger descriptions as this is already done for you transparently.
If you want to make use of the swagger descriptions of this repository within NodeRed, all you need to do is:

- install [node-red-contrib-swagger](https://github.com/kmi/node-red-contrib-swagger)
- clone this repository within the folder where node-red-contrib-swagger has been installed.

That being done all descriptions shall be automatically ready to be used!
You would find them all at [http://localhost:1880/swagger-descriptions](http://localhost:1880/swagger-descriptions)


## APIs Covered

- [InfluxDB](http://influxdb.com) Web API. This is configured for accessing locally hosted InfluxDB. You can indeed adapt the host to point it to your service and you are ready to roll.
- [Boxcar](https://boxcar.io). A notification API for pushing messages to mobile phones.

## Contributing Descriptions
Adding new descriptions is very simple. All we ask in order to retain compatibility with our NodeRed node is
that:

- every new API description is created in its own folder
- you provide the top level file at that folder named index.json
- for every inner resource you create a new folder (as per Swagger's 1.2 specification) and there you add an index.json file with the concrete details

It may be helpful to take some of the examples as a starting point.
You may also want to consider using existing [tooling support](http://editor.swagger.io/#/).
 
License
-------

Copyright 2014 Knowledge Media Institute - The Open University.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
[apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.