# Masterportal GUBEN

The Masterportal is a tool-kit to create geo web applications based on [OpenLayers](https://openlayers.org), [Vue.js](https://vuejs.org/) and [Backbone.js](https://backbonejs.org). The Masterportal is Open Source Software published under the [MIT License](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/dev/License.txt).

The Masterportal is a project by [Geowerkstatt Hamburg](https://www.hamburg.de/geowerkstatt/).

## User section

* [Download](https://bitbucket.org/geowerkstatt-hamburg/masterportal/downloads/)
* [Quick start for users](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/dev/doc/setup.md)
* [Remote interface](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/dev/doc/remoteInterface.md)
* [User documentation](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/dev/doc/doc.md)
* [User documentation online](https://www.masterportal.org/dokumentation.html)
* [Community board (User forum and issue tracker)](https://trello.com/c/qajdXkMa/110-willkommen)

## Developer section

* Contributors to the Masterportal are expected to act respectfully toward others in accordance with the [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) for open source projects.
* [Developer documentation](doc/devdoc.md)
* [Tutorial 01: Creating a new module (Scale switcher)](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/dev/doc/vueTutorial.md)
* [Community board (Developer forum and issue tracker)](https://trello.com/c/qajdXkMa/110-willkommen)

[![Sauce Test Status](https://app.eu-central-1.saucelabs.com/buildstatus/geodatenanwendungen_gv.hamburg.de)](https://app.eu-central-1.saucelabs.com/builds/dfd7abc54af1493091fbeef1b6b48ca6)


## Current portal config
- **story.json**: This file contains the data for the story, including the title, author, and chapters. It also includes an array of steps, which define the individual pages of the story. The htmlFile property of each step corresponds to an HTML file in the story folder.

- **index.html**: This is the main HTML file for the project. It includes the Vue.js library and the story.js script.

- **story.js**: This file contains the Vue.js component that renders the story. It reads the data from story.json and renders each step as a separate component.

- **step_1-1.html, step_2-1.html, etc.**: These are the HTML files that correspond to each step in the story. They contain the content and layout for each step.

### More specific configuration
Please refer to the [Official documentation](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/dev/doc/doc.md#markdown-header-portal-specific-configuration-files)
