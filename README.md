# topological_inventory

[![Build Status](https://travis-ci.org/ManageIQ/topological_inventory-api-jsclient.svg?branch=master)](https://travis-ci.org/ManageIQ/topological_inventory-api-jsclient)

To be used by topology_inventory_ui and others.

TopologicalInventory - JavaScript client for topological_inventory
Topological Inventory
This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 0.0.1
- Package version: 0.0.1
- Build package: io.swagger.codegen.languages.JavascriptClientCodegen

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install --save @manageiq/topological_inventory
```

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/GIT_USER_ID/GIT_REPO_ID
then install it via:

```shell
    npm install GIT_USER_ID/GIT_REPO_ID --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Using the client on Insights:
```javascript

var TopologicalInventory = require('@manageiq/topological_inventory');

const SOURCES_API_BASE = '/r/insights/platform/topological-inventory/v0.0'

var defaultClient = TopologicalInventory.ApiClient.instance;
defaultClient.basePath = SOURCES_API_BASE;

let apiInstance = new TopologicalInventory.DefaultApi();

...
    let sourceData = {
        tenant_id: 1, // FIXME: where do I get it?
        name: formData.name,
        source_type_id: 1, // FIXME should come from the form
    };

    return apiInstance.createSource(sourceData).then((sourceDataOut) => {
        console.log('API call createSource returned data: ', sourceDataOut);
...
```

(original documentation below)

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var TopologicalInventory = require('topological_inventory');

var defaultClient = TopologicalInventory.ApiClient.instance;

// Configure HTTP basic authorization: UserSecurity
var UserSecurity = defaultClient.authentications['UserSecurity'];
UserSecurity.username = 'YOUR USERNAME'
UserSecurity.password = 'YOUR PASSWORD'

var api = new TopologicalInventory.DefaultApi()

var body = new TopologicalInventory.ID(); // {ID} 

api.createAuthentication(body).then(function(data) {
  console.log('API called successfully. Returned data: ' + data);
}, function(error) {
  console.error(error);
});


```

## Documentation for API Endpoints

All URIs are relative to *https://virtserver.swaggerhub.com/r/insights/platform/topological-inventory/v0.0*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*TopologicalInventory.DefaultApi* | [**createAuthentication**](docs/DefaultApi.md#createAuthentication) | **POST** /authentications | Create a new Authentication
*TopologicalInventory.DefaultApi* | [**createEndpoint**](docs/DefaultApi.md#createEndpoint) | **POST** /endpoints | Create a new Endpoint
*TopologicalInventory.DefaultApi* | [**createSource**](docs/DefaultApi.md#createSource) | **POST** /sources | Create a new Source
*TopologicalInventory.DefaultApi* | [**createSourceType**](docs/DefaultApi.md#createSourceType) | **POST** /source_types | Create a new SourceType
*TopologicalInventory.DefaultApi* | [**deleteAuthentication**](docs/DefaultApi.md#deleteAuthentication) | **DELETE** /authentications/{id} | Delete an existing Authentication
*TopologicalInventory.DefaultApi* | [**deleteEndpoint**](docs/DefaultApi.md#deleteEndpoint) | **DELETE** /endpoints/{id} | Delete an existing Endpoint
*TopologicalInventory.DefaultApi* | [**deleteSource**](docs/DefaultApi.md#deleteSource) | **DELETE** /sources/{id} | Delete an existing Source
*TopologicalInventory.DefaultApi* | [**listAuthentications**](docs/DefaultApi.md#listAuthentications) | **GET** /authentications | List Authentications
*TopologicalInventory.DefaultApi* | [**listContainerGroupContainers**](docs/DefaultApi.md#listContainerGroupContainers) | **GET** /container_groups/{id}/containers | List Containers for ContainerGroup
*TopologicalInventory.DefaultApi* | [**listContainerGroups**](docs/DefaultApi.md#listContainerGroups) | **GET** /container_groups | List ContainerGroups
*TopologicalInventory.DefaultApi* | [**listContainerImages**](docs/DefaultApi.md#listContainerImages) | **GET** /container_images | List ContainerImages
*TopologicalInventory.DefaultApi* | [**listContainerNodeContainerGroups**](docs/DefaultApi.md#listContainerNodeContainerGroups) | **GET** /container_nodes/{id}/container_groups | List ContainerGroups for ContainerNode
*TopologicalInventory.DefaultApi* | [**listContainerNodes**](docs/DefaultApi.md#listContainerNodes) | **GET** /container_nodes | List ContainerNodes
*TopologicalInventory.DefaultApi* | [**listContainerProjectContainerGroups**](docs/DefaultApi.md#listContainerProjectContainerGroups) | **GET** /container_projects/{id}/container_groups | List ContainerGroups for ContainerProject
*TopologicalInventory.DefaultApi* | [**listContainerProjectContainerTemplates**](docs/DefaultApi.md#listContainerProjectContainerTemplates) | **GET** /container_projects/{id}/container_templates | List ContainerTemplates for ContainerProject
*TopologicalInventory.DefaultApi* | [**listContainerProjects**](docs/DefaultApi.md#listContainerProjects) | **GET** /container_projects | List ContainerProjects
*TopologicalInventory.DefaultApi* | [**listContainerTemplates**](docs/DefaultApi.md#listContainerTemplates) | **GET** /container_templates | List ContainerTemplates
*TopologicalInventory.DefaultApi* | [**listContainers**](docs/DefaultApi.md#listContainers) | **GET** /containers | List Containers
*TopologicalInventory.DefaultApi* | [**listEndpoints**](docs/DefaultApi.md#listEndpoints) | **GET** /endpoints | List Endpoints
*TopologicalInventory.DefaultApi* | [**listFlavors**](docs/DefaultApi.md#listFlavors) | **GET** /flavors | List Flavors
*TopologicalInventory.DefaultApi* | [**listOrchestrationStacks**](docs/DefaultApi.md#listOrchestrationStacks) | **GET** /orchestration_stacks | List OrchestrationStacks
*TopologicalInventory.DefaultApi* | [**listServiceInstances**](docs/DefaultApi.md#listServiceInstances) | **GET** /service_instances | List ServiceInstances
*TopologicalInventory.DefaultApi* | [**listServiceOfferingServiceInstances**](docs/DefaultApi.md#listServiceOfferingServiceInstances) | **GET** /service_offerings/{id}/service_instances | List ServiceInstances for ServiceOffering
*TopologicalInventory.DefaultApi* | [**listServiceOfferingServicePlans**](docs/DefaultApi.md#listServiceOfferingServicePlans) | **GET** /service_offerings/{id}/service_plans | List ServicePlans for ServiceOffering
*TopologicalInventory.DefaultApi* | [**listServiceOfferings**](docs/DefaultApi.md#listServiceOfferings) | **GET** /service_offerings | List ServiceOfferings
*TopologicalInventory.DefaultApi* | [**listServicePlanServiceInstances**](docs/DefaultApi.md#listServicePlanServiceInstances) | **GET** /service_plans/{id}/service_instances | List ServiceInstances for ServicePlan
*TopologicalInventory.DefaultApi* | [**listServicePlans**](docs/DefaultApi.md#listServicePlans) | **GET** /service_plans | List ServicePlans
*TopologicalInventory.DefaultApi* | [**listSourceContainerGroups**](docs/DefaultApi.md#listSourceContainerGroups) | **GET** /sources/{id}/container_groups | List ContainerGroups for Source
*TopologicalInventory.DefaultApi* | [**listSourceContainerImages**](docs/DefaultApi.md#listSourceContainerImages) | **GET** /sources/{id}/container_images | List ContainerImages for Source
*TopologicalInventory.DefaultApi* | [**listSourceContainerNodes**](docs/DefaultApi.md#listSourceContainerNodes) | **GET** /sources/{id}/container_nodes | List ContainerNodes for Source
*TopologicalInventory.DefaultApi* | [**listSourceContainerProjects**](docs/DefaultApi.md#listSourceContainerProjects) | **GET** /sources/{id}/container_projects | List ContainerProjects for Source
*TopologicalInventory.DefaultApi* | [**listSourceContainerTemplates**](docs/DefaultApi.md#listSourceContainerTemplates) | **GET** /sources/{id}/container_templates | List ContainerTemplates for Source
*TopologicalInventory.DefaultApi* | [**listSourceContainers**](docs/DefaultApi.md#listSourceContainers) | **GET** /sources/{id}/containers | List Containers for Source
*TopologicalInventory.DefaultApi* | [**listSourceEndpoints**](docs/DefaultApi.md#listSourceEndpoints) | **GET** /sources/{id}/endpoints | List Endpoints for Source
*TopologicalInventory.DefaultApi* | [**listSourceOrchestrationStacks**](docs/DefaultApi.md#listSourceOrchestrationStacks) | **GET** /sources/{id}/orchestration_stacks | List OrchestrationStacks for Source
*TopologicalInventory.DefaultApi* | [**listSourceServiceInstances**](docs/DefaultApi.md#listSourceServiceInstances) | **GET** /sources/{id}/service_instances | List ServiceInstances for Source
*TopologicalInventory.DefaultApi* | [**listSourceServiceOfferings**](docs/DefaultApi.md#listSourceServiceOfferings) | **GET** /sources/{id}/service_offerings | List ServiceOfferings for Source
*TopologicalInventory.DefaultApi* | [**listSourceServicePlans**](docs/DefaultApi.md#listSourceServicePlans) | **GET** /sources/{id}/service_plans | List ServicePlans for Source
*TopologicalInventory.DefaultApi* | [**listSourceTypeSources**](docs/DefaultApi.md#listSourceTypeSources) | **GET** /source_types/{id}/sources | List Sources for SourceType
*TopologicalInventory.DefaultApi* | [**listSourceTypes**](docs/DefaultApi.md#listSourceTypes) | **GET** /source_types | List SourceTypes
*TopologicalInventory.DefaultApi* | [**listSourceVms**](docs/DefaultApi.md#listSourceVms) | **GET** /sources/{id}/vms | List Vms for Source
*TopologicalInventory.DefaultApi* | [**listSourceVolumeTypes**](docs/DefaultApi.md#listSourceVolumeTypes) | **GET** /sources/{id}/volume_types | List VolumeTypes for Source
*TopologicalInventory.DefaultApi* | [**listSourceVolumes**](docs/DefaultApi.md#listSourceVolumes) | **GET** /sources/{id}/volumes | List Volumes for Source
*TopologicalInventory.DefaultApi* | [**listSources**](docs/DefaultApi.md#listSources) | **GET** /sources | List Sources
*TopologicalInventory.DefaultApi* | [**listTasks**](docs/DefaultApi.md#listTasks) | **GET** /tasks | List Tasks
*TopologicalInventory.DefaultApi* | [**listVmVolumeAttachments**](docs/DefaultApi.md#listVmVolumeAttachments) | **GET** /vms/{id}/volume_attachments | List VolumeAttachments for Vm
*TopologicalInventory.DefaultApi* | [**listVmVolumes**](docs/DefaultApi.md#listVmVolumes) | **GET** /vms/{id}/volumes | List Volumes for Vm
*TopologicalInventory.DefaultApi* | [**listVms**](docs/DefaultApi.md#listVms) | **GET** /vms | List Vms
*TopologicalInventory.DefaultApi* | [**listVolumeAttachments**](docs/DefaultApi.md#listVolumeAttachments) | **GET** /volume_attachments | List VolumeAttachments
*TopologicalInventory.DefaultApi* | [**listVolumeTypes**](docs/DefaultApi.md#listVolumeTypes) | **GET** /volume_types | List VolumeTypes
*TopologicalInventory.DefaultApi* | [**listVolumes**](docs/DefaultApi.md#listVolumes) | **GET** /volumes | List Volumes
*TopologicalInventory.DefaultApi* | [**orderServicePlan**](docs/DefaultApi.md#orderServicePlan) | **POST** /service_plans/{id}/order | Order an existing ServicePlan
*TopologicalInventory.DefaultApi* | [**replaceAuthentication**](docs/DefaultApi.md#replaceAuthentication) | **PUT** /authentications/{id} | Replace an existing Authentication
*TopologicalInventory.DefaultApi* | [**replaceEndpoint**](docs/DefaultApi.md#replaceEndpoint) | **PUT** /endpoints/{id} | Replace an existing Endpoint
*TopologicalInventory.DefaultApi* | [**replaceSource**](docs/DefaultApi.md#replaceSource) | **PUT** /sources/{id} | Replace an existing Source
*TopologicalInventory.DefaultApi* | [**showAuthentication**](docs/DefaultApi.md#showAuthentication) | **GET** /authentications/{id} | Show an existing Authentication
*TopologicalInventory.DefaultApi* | [**showContainer**](docs/DefaultApi.md#showContainer) | **GET** /containers/{id} | Show an existing Container
*TopologicalInventory.DefaultApi* | [**showContainerGroup**](docs/DefaultApi.md#showContainerGroup) | **GET** /container_groups/{id} | Show an existing ContainerGroup
*TopologicalInventory.DefaultApi* | [**showContainerImage**](docs/DefaultApi.md#showContainerImage) | **GET** /container_images/{id} | Show an existing ContainerImage
*TopologicalInventory.DefaultApi* | [**showContainerNode**](docs/DefaultApi.md#showContainerNode) | **GET** /container_nodes/{id} | Show an existing ContainerNode
*TopologicalInventory.DefaultApi* | [**showContainerProject**](docs/DefaultApi.md#showContainerProject) | **GET** /container_projects/{id} | Show an existing ContainerProject
*TopologicalInventory.DefaultApi* | [**showContainerTemplate**](docs/DefaultApi.md#showContainerTemplate) | **GET** /container_templates/{id} | Show an existing ContainerTemplate
*TopologicalInventory.DefaultApi* | [**showEndpoint**](docs/DefaultApi.md#showEndpoint) | **GET** /endpoints/{id} | Show an existing Endpoint
*TopologicalInventory.DefaultApi* | [**showFlavor**](docs/DefaultApi.md#showFlavor) | **GET** /flavors/{id} | Show an existing Flavor
*TopologicalInventory.DefaultApi* | [**showOrchestrationStack**](docs/DefaultApi.md#showOrchestrationStack) | **GET** /orchestration_stacks/{id} | Show an existing OrchestrationStack
*TopologicalInventory.DefaultApi* | [**showServiceInstance**](docs/DefaultApi.md#showServiceInstance) | **GET** /service_instances/{id} | Show an existing ServiceInstance
*TopologicalInventory.DefaultApi* | [**showServiceOffering**](docs/DefaultApi.md#showServiceOffering) | **GET** /service_offerings/{id} | Show an existing ServiceOffering
*TopologicalInventory.DefaultApi* | [**showServicePlan**](docs/DefaultApi.md#showServicePlan) | **GET** /service_plans/{id} | Show an existing ServicePlan
*TopologicalInventory.DefaultApi* | [**showSource**](docs/DefaultApi.md#showSource) | **GET** /sources/{id} | Show an existing Source
*TopologicalInventory.DefaultApi* | [**showSourceType**](docs/DefaultApi.md#showSourceType) | **GET** /source_types/{id} | Show an existing SourceType
*TopologicalInventory.DefaultApi* | [**showTask**](docs/DefaultApi.md#showTask) | **GET** /tasks/{id} | Show an existing Task
*TopologicalInventory.DefaultApi* | [**showVm**](docs/DefaultApi.md#showVm) | **GET** /vms/{id} | Show an existing Vm
*TopologicalInventory.DefaultApi* | [**showVolume**](docs/DefaultApi.md#showVolume) | **GET** /volumes/{id} | Show an existing Volume
*TopologicalInventory.DefaultApi* | [**showVolumeAttachment**](docs/DefaultApi.md#showVolumeAttachment) | **GET** /volume_attachments/{id} | Show an existing VolumeAttachment
*TopologicalInventory.DefaultApi* | [**showVolumeType**](docs/DefaultApi.md#showVolumeType) | **GET** /volume_types/{id} | Show an existing VolumeType
*TopologicalInventory.DefaultApi* | [**updateAuthentication**](docs/DefaultApi.md#updateAuthentication) | **PATCH** /authentications/{id} | Update an existing Authentication
*TopologicalInventory.DefaultApi* | [**updateEndpoint**](docs/DefaultApi.md#updateEndpoint) | **PATCH** /endpoints/{id} | Update an existing Endpoint
*TopologicalInventory.DefaultApi* | [**updateSource**](docs/DefaultApi.md#updateSource) | **PATCH** /sources/{id} | Update an existing Source


## Documentation for Models

 - [TopologicalInventory.Authentication](docs/Authentication.md)
 - [TopologicalInventory.Container](docs/Container.md)
 - [TopologicalInventory.ContainerGroup](docs/ContainerGroup.md)
 - [TopologicalInventory.ContainerImage](docs/ContainerImage.md)
 - [TopologicalInventory.ContainerNode](docs/ContainerNode.md)
 - [TopologicalInventory.ContainerProject](docs/ContainerProject.md)
 - [TopologicalInventory.ContainerTemplate](docs/ContainerTemplate.md)
 - [TopologicalInventory.Endpoint](docs/Endpoint.md)
 - [TopologicalInventory.Flavor](docs/Flavor.md)
 - [TopologicalInventory.InlineResponse200](docs/InlineResponse200.md)
 - [TopologicalInventory.OrchestrationStack](docs/OrchestrationStack.md)
 - [TopologicalInventory.OrderParameters](docs/OrderParameters.md)
 - [TopologicalInventory.ServiceInstance](docs/ServiceInstance.md)
 - [TopologicalInventory.ServiceOffering](docs/ServiceOffering.md)
 - [TopologicalInventory.ServicePlan](docs/ServicePlan.md)
 - [TopologicalInventory.Source](docs/Source.md)
 - [TopologicalInventory.SourceType](docs/SourceType.md)
 - [TopologicalInventory.Task](docs/Task.md)
 - [TopologicalInventory.Vm](docs/Vm.md)
 - [TopologicalInventory.Volume](docs/Volume.md)
 - [TopologicalInventory.VolumeAttachment](docs/VolumeAttachment.md)
 - [TopologicalInventory.VolumeType](docs/VolumeType.md)


## Documentation for Authorization


### UserSecurity

- **Type**: HTTP basic authentication

