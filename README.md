# OPC PowerApps PCF Controls

[![Build Status](https://dev.azure.com/opc-cpvp/O365%20Cloud/_apis/build/status/PowerApps/OPC.PowerApps.PCFControls%20-%20CI?branchName=master)](https://dev.azure.com/opc-cpvp/O365%20Cloud/_build/latest?definitionId=51&branchName=master)

[![Total alerts](https://img.shields.io/lgtm/alerts/g/opc-cpvp/OPC.PowerApps.PCFControls.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/opc-cpvp/OPC.PowerApps.PCFControls/alerts/)
[![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/opc-cpvp/OPC.PowerApps.PCFControls.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/opc-cpvp/OPC.PowerApps.PCFControls/context:javascript)

Collection of PowerApps PCF Controls.

Controls:
- [Tag Picker Component](#tag-picker-component)
- [Tag Picker Grid Component](#tag-picker-grid-component)
- [Tree Component](#tree-component)
- [Task Manager Component](#task-manager-component)

Plugins:
- TagRegistrationPlugin

## Download

You can download the latest version of the managed / un-managed solution from the project's [releases](https://github.com/opc-cpvp/OPC.PowerApps.PCFControls/releases/latest).

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Follow the instructions as per the [documentation](https://docs.microsoft.com/en-us/powerapps/developer/component-framework/create-custom-controls-using-pcf) in order to configure your environment for PCF development.
You will need to disable the telemetry option for the Power Apps CLI by running the following command:

```
pac telemetry disable
```

### Building a Component

Navigate to the root folder of the component you wish to build and run the following commands:

```
npm run build
```

Note: You must run `npm install` before building the component for the first time.

### Running a Component

Navigate to the root folder of the component you wish to run and run the following commands:

```
npm run start
```

Note: You must run `npm install` before running the component for the first time.

### Testing an existing Component

After building your component, use fiddler's autoresponder to replace the content of the web resource with the content you have just built.
It should be located in the "out" folder under the component's folder. The file should be called bundle.js.

### Building the Plugin

Open the solution `OPC.PowerApps.PCFControls.sln` from Visual Studio 2019 and build the projects.

### Building the Solution

Run the following command from the `Solution` folder in order to build the solution:

```
msbuild /p:Configuration=Release /restore
```
## Tree Component

[![dependencies Status](https://david-dm.org/opc-cpvp/OPC.PowerApps.PCFControls/status.svg?path=src/Components/TreeComponent)](https://david-dm.org/opc-cpvp/OPC.PowerApps.PCFControls?path=src/Components/TreeComponent) [![devDependencies Status](https://david-dm.org/opc-cpvp/OPC.PowerApps.PCFControls/dev-status.svg?path=src/Components/TreeComponent)](https://david-dm.org/opc-cpvp/OPC.PowerApps.PCFControls?path=src/Components/TreeComponent&type=dev)

### Preview

![TreeComponent Preview](img/treeselect.gif)

The purpose of this control is to allow user to associate / disassociate hierarchical records for a many-to-many relationship in the form of a tree.

### Configuration

|Parameter|Description|Required|Bound to an attribute|
|---------|-----------|:----:|:---:|
|**Tree Entity Collection Name**|Plural name of the related entity|X||
|**Tree Entity Attribute**|The parent record attribute for the tree entity|X||
|**Name Attribute**|The attribute that will be used to display text of the node in the tree|X||
|**Id Attribute**|The attribute for the ID of the tree record|X||
|**Relationship Name**|Relationship name between the primary entity and the related entity|X||
|**Relationship Entity**|Logical name of the relationship entity|X||
|**Description Attribute**|The description attribute of the tree record, currently only used to aid searching|||
|**Extra Title Details Attribute**|The attribute of the tree entity that will add extra details to the display text of the node in the tree |||
|**Max Name Display Length (Work in Progress)**|The max amount of characters the text of the node will be displayed in the tree |||

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/opc-cpvp/OPC.PowerApps.PCFControls/tags).

## Authors

See also the list of [contributors](https://github.com/opc-cpvp/OPC.PowerApps.PCFControls/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
