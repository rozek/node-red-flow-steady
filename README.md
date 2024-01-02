# node-red-flow-steady #

Node-RED Flow for the Steady API

This repository contains a set of simple flows for the [Steady REST API](https://developers.steadyhq.com/). [Steady](https://steadyhq.com/en) is a monetarization platform similar to [Patreon](https://www.patreon.com) or [Buy-me-a-Coffee](https://www.buymeacoffee.com/). Using the flows from this repo you may monitor and manage your subscriptions programmatically using Node-RED.

![Steady Flows Screenshot](./Steady-Flows.png)

## Installation ##

This section shows you how to install Node.js, Node-RED and the flows from this repository - feel free to skip the steps for those components you already installed before.

### Node.js ###

"_[Node.js](https://nodejs.org/en) is a cross-platform, open-source server environment that can run on Windows, Linux, Unix, macOS, and more. Node.js is a back-end JavaScript runtime environment, runs on the V8 JavaScript engine, and executes JavaScript code outside a web browser._" (according to [Wikipedia](https://en.wikipedia.org/wiki/Node.js))

Start by [installing Node.js](https://nodejs.org/en) as described on their web page.

### Node-RED ###

"_[Node-RED](https://nodered.org/) is a flow-based, low-code development tool for visual programming developed originally by IBM..._" (according to [Wikipedia](https://en.wikipedia.org/wiki/Node-RED)).

If not already done, install Node-RED as described on their "[Get Started](https://nodered.org/#get-started)" page.

### Steady Flows ###

Finally import the contents of file [Steady-Flows.json](https://raw.githubusercontent.com/rozek/node-red-flow-steady/master/Steady-Flows.json) into a new worksheet.

## Configuration ##

![Steady Configuration Flow Screenshot](./Steady-Configuration-Flow.png)

The [Steady REST endpoints](https://developers.steadyhq.com/#rest) require an "API Key" to be sent along with any request. This key can be found in your Steady "Backend" within the "API" section. Keep the key safe and do not publish it.

Now import the contents of file [Steady-Configuration-Flow.json](https://raw.githubusercontent.com/rozek/node-red-flow-steady/master/Steady-Configuration-Flow.json) - either into the same worksheet as before or into a new one. Double click on the node labelled "at start-up" and copy your Steady API key into the "payload" input field.

Upon every deployment (or whenever the Node-RED server is restarted), the API key will now be written into the context of all Steady flow nodes allowing them to access the Steady REST endpoints.

## Examples ##

![Steady Example Flows Screenshot](./Steady-Example-Flows.png)

Importing the contents of file [Steady-Example-Flows.json](https://raw.githubusercontent.com/rozek/node-red-flow-steady/master/Steady-Example-Flows.json) will finally give you a few examples which can be used to test your setup and give you an idea of how the output of the Steady flows look like.

You are now ready to use the flows from this repository for your own purposes.

## License ##

[MIT License](LICENSE.md)
