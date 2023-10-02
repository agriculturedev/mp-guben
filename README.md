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


## Current portal configuration

**This repo only includes the files to be used with a masterportal build.**

- **story.json**: This file contains the data for the story, including the title, author, and chapters. It also includes an array of steps, which define the individual pages of the story. The htmlFile property of each step corresponds to an HTML file in the story folder.

- **index.html**: This is the main HTML file for the project. It includes the Vue.js library and the story.js script.

- **story.js**: This file contains the Vue.js component that renders the story. It reads the data from story.json and renders each step as a separate component.

- **step_1-1.html, step_2-1.html, etc.**: These are the HTML files that correspond to each step in the story. They contain the content and layout for each step.

- **[config.js](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/b9f22105106088695c2dd58eec120cce496fff63/doc/config.js.md)**: Configuration of paths to further configuration files and services
- **[config.json](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/b9f22105106088695c2dd58eec120cce496fff63/doc/config.js.md)**: Configuration of portal appearance and available contents (If the bitbucket site isn´t displayed correctly please use this link: alternative config.json documentation)
- **[services.json](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/b9f22105106088695c2dd58eec120cce496fff63/doc/services.json.md)**: lists all available layers

### More specific configuration
Please refer to the [Official documentation](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/dev/doc/doc.md#markdown-header-portal-specific-configuration-files)




# services.json

All services available for display in the Masterportal (WMS, WFS, [SensorThings-API](sensorThings.md), and more) are configured and maintained in this JSON file. The file is linked to from the *config.js* of each individual portal by the *layerConf* parameter. For an example, see the *services-internet.json* included in the *examples.zip* at *//examples/Basic/resources/*.

All layer information the portal needs to use the services is stored here. Configuration details differ between WMS, WFS, [SensorThings-API](sensorThings.md) and other services types. You may also use local GeoJSON files; see GeoJSON example.

**[services.json](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/b9f22105106088695c2dd58eec120cce496fff63/doc/services.json.md)**: lists all available layers

***

## Example
```json
[
    {
        "id": "44",
        "name": "Verkehrslage auf Autobahnen",
        "url": "https://geodienste.hamburg.de/HH_WFS_Verkehr_opendata",
        "typ": "WFS",
        "featureType": "bab_vkl",
        "outputFormat": "XML",
        "version": "2.0.0",
        "featureNS": "https://registry.gdi-de.org/id/de.hh.up",
        "gfiAttributes":" showAll",
        "gfiTheme": "default",
        "layerAttribution": "nicht vorhanden",
        "legendURL": "",
        "hitTolerance": "",
        "datasets": [
            {
                "md_id":"2FC4BBED-350C-4380-B138-4222C28F56C6",
                "csw_url":"https://metaver.de/csw",
                "show_doc_url":"https://metaver.de/trefferanzeige?cmd=doShowDocument&docuuid=",
                "rs_id":"https://registry.gdi-de.org/id/de.hh/918b8193-48d7-4f01-adc9-98a47f031191",
                "md_name":"Verkehrslage auf Autobahnen (Schleifen) Hamburg","bbox":"461468.96892897453,5916367.229806512,587010.9095989474,5980347.755797674",
                "kategorie_opendata":["Verkehr"],
                "kategorie_inspire":["Verkehrsnetze"],
                "kategorie_organisation":"Behörde für Verkehr und Mobilitätswende (BVM)"
                
            }
        ],
        "urlIsVisible": true
    }
]
```
