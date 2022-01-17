---
path: /api/reference
title: API reference
---

## API reference

<details>
  <summary><strong>Table of Contents</strong></summary>

  * [Query](#query)
  * [Mutation](#mutation)
  * [Objects](#objects)
    * [Account](#account)
    * [AccountUsage](#accountusage)
    * [BatchCreateItemsPayload](#batchcreateitemspayload)
    * [BatchDeleteItemsPayload](#batchdeleteitemspayload)
    * [Collection](#collection)
    * [CollectionConnection](#collectionconnection)
    * [CollectionInsight](#collectioninsight)
    * [CollectionUsage](#collectionusage)
    * [CreateCollectionPayload](#createcollectionpayload)
    * [CreateItemPayload](#createitempayload)
    * [CreateModulePayload](#createmodulepayload)
    * [CreatePackagePayload](#createpackagepayload)
    * [CreateParameterPayload](#createparameterpayload)
    * [CreateServicePayload](#createservicepayload)
    * [CreateViewPayload](#createviewpayload)
    * [CreateWorkflowPayload](#createworkflowpayload)
    * [DeleteCollectionPayload](#deletecollectionpayload)
    * [DeleteItemPayload](#deleteitempayload)
    * [DeleteModulePayload](#deletemodulepayload)
    * [DeletePackagePayload](#deletepackagepayload)
    * [DeleteParameterPayload](#deleteparameterpayload)
    * [DeleteServicePayload](#deleteservicepayload)
    * [DeleteViewPayload](#deleteviewpayload)
    * [DeleteWorkflowPayload](#deleteworkflowpayload)
    * [DeployStackPayload](#deploystackpayload)
    * [DestroyStackPayload](#destroystackpayload)
    * [InvokeModulePayload](#invokemodulepayload)
    * [Item](#item)
    * [ItemConnection](#itemconnection)
    * [Log](#log)
    * [LogConnection](#logconnection)
    * [Meta](#meta)
    * [Module](#module)
    * [ModuleConnection](#moduleconnection)
    * [Package](#package)
    * [PackageConnection](#packageconnection)
    * [Parameter](#parameter)
    * [ParameterConnection](#parameterconnection)
    * [Service](#service)
    * [ServiceConnection](#serviceconnection)
    * [SetAccountAccessPayload](#setaccountaccesspayload)
    * [Subscription](#subscription)
    * [TriggerWorkflowPayload](#triggerworkflowpayload)
    * [UpdateCollectionPayload](#updatecollectionpayload)
    * [UpdateItemPayload](#updateitempayload)
    * [UpdateModulePayload](#updatemodulepayload)
    * [UpdatePackagePayload](#updatepackagepayload)
    * [UpdateParameterPayload](#updateparameterpayload)
    * [UpdateServicePayload](#updateservicepayload)
    * [UpdateViewPayload](#updateviewpayload)
    * [UpdateWorkflowPayload](#updateworkflowpayload)
    * [UserAccess](#useraccess)
    * [UserAccounts](#useraccounts)
    * [UserAccountsConnection](#useraccountsconnection)
    * [ValidateCollectionPayload](#validatecollectionpayload)
    * [ValidatePackagePayload](#validatepackagepayload)
    * [ValidateServicePayload](#validateservicepayload)
    * [ValidateViewPayload](#validateviewpayload)
    * [ValidateWorkflowPayload](#validateworkflowpayload)
    * [View](#view)
    * [ViewConnection](#viewconnection)
    * [ViewUsage](#viewusage)
    * [Workflow](#workflow)
    * [WorkflowConnection](#workflowconnection)
    * [WorkflowError](#workflowerror)
    * [WorkflowUsage](#workflowusage)
  * [Inputs](#inputs)
    * [BatchCreateItem](#batchcreateitem)
    * [BatchCreateItemsInput](#batchcreateitemsinput)
    * [BatchDeleteItemsInput](#batchdeleteitemsinput)
    * [BooleanFilterInput](#booleanfilterinput)
    * [CreateCollectionInput](#createcollectioninput)
    * [CreateItemInput](#createiteminput)
    * [CreateModuleInput](#createmoduleinput)
    * [CreatePackageFromServiceInput](#createpackagefromserviceinput)
    * [CreatePackageInput](#createpackageinput)
    * [CreateParameterInput](#createparameterinput)
    * [CreateServiceInput](#createserviceinput)
    * [CreateViewInput](#createviewinput)
    * [CreateWorkflowInput](#createworkflowinput)
    * [DateRangeFilterInput](#daterangefilterinput)
    * [DateTimeRangeFilterInput](#datetimerangefilterinput)
    * [DeleteCollectionInput](#deletecollectioninput)
    * [DeleteItemInput](#deleteiteminput)
    * [DeleteModuleInput](#deletemoduleinput)
    * [DeletePackageInput](#deletepackageinput)
    * [DeleteParameterInput](#deleteparameterinput)
    * [DeleteServiceInput](#deleteserviceinput)
    * [DeleteViewInput](#deleteviewinput)
    * [DeleteWorkflowInput](#deleteworkflowinput)
    * [DeployStackInput](#deploystackinput)
    * [DestroyStackInput](#destroystackinput)
    * [FloatFilterInput](#floatfilterinput)
    * [IDFilterInput](#idfilterinput)
    * [IntFilterInput](#intfilterinput)
    * [InvokeModuleInput](#invokemoduleinput)
    * [ItemSearch](#itemsearch)
    * [LogFilter](#logfilter)
    * [LogSearch](#logsearch)
    * [MetaInput](#metainput)
    * [SetAccountAccessInput](#setaccountaccessinput)
    * [StringFilterInput](#stringfilterinput)
    * [TriggerWorkflowInput](#triggerworkflowinput)
    * [UpdateCollectionInput](#updatecollectioninput)
    * [UpdateItemInput](#updateiteminput)
    * [UpdateModuleInput](#updatemoduleinput)
    * [UpdatePackageInput](#updatepackageinput)
    * [UpdateParameterInput](#updateparameterinput)
    * [UpdateServiceInput](#updateserviceinput)
    * [UpdateViewInput](#updateviewinput)
    * [UpdateWorkflowInput](#updateworkflowinput)
    * [ValidateCollectionInput](#validatecollectioninput)
    * [ValidatePackageInput](#validatepackageinput)
    * [ValidateServiceInput](#validateserviceinput)
    * [ValidateViewInput](#validateviewinput)
    * [ValidateWorkflowInput](#validateworkflowinput)
  * [Enums](#enums)
    * [AccessType](#accesstype)
    * [CollectionInsightInterval](#collectioninsightinterval)
    * [LogStatus](#logstatus)
    * [ModuleScope](#modulescope)
    * [PackageScope](#packagescope)
    * [TriggerMethod](#triggermethod)
    * [ViewScope](#viewscope)
    * [WorkflowStatus](#workflowstatus)
  * [Scalars](#scalars)
    * [AWSDate](#awsdate)
    * [AWSDateTime](#awsdatetime)
    * [AWSJSON](#awsjson)
    * [AWSPhone](#awsphone)
    * [AWSTime](#awstime)
    * [Boolean](#boolean)
    * [EmailAddress](#emailaddress)
    * [Float](#float)
    * [ID](#id)
    * [Int](#int)
    * [String](#string)
    * [URL](#url)
  * [Interfaces](#interfaces)
    * [Element](#element)
    * [Node](#node)

</details>

## Query
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#node">node</a></strong></td>
<td valign="top"><a href="#node">Node</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#account">account</a></strong></td>
<td valign="top"><a href="#account">Account</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#memberships">memberships</a></strong></td>
<td valign="top"><a href="#useraccountsconnection">UserAccountsConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#collection">collection</a></strong></td>
<td valign="top"><a href="#collection">Collection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#collections">collections</a></strong></td>
<td valign="top"><a href="#collectionconnection">CollectionConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">serviceId</td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#item">item</a></strong></td>
<td valign="top"><a href="#item">Item</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#items">items</a></strong></td>
<td valign="top"><a href="#itemconnection">ItemConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">collectionId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">dates</td>
<td valign="top"><a href="#datetimerangefilterinput">DateTimeRangeFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">search</td>
<td valign="top"><a href="#itemsearch">ItemSearch</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#logs">logs</a></strong></td>
<td valign="top"><a href="#logconnection">LogConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">serviceId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#logfilter">LogFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">search</td>
<td valign="top"><a href="#logsearch">LogSearch</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#module">module</a></strong></td>
<td valign="top"><a href="#module">Module</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#modules">modules</a></strong></td>
<td valign="top"><a href="#moduleconnection">ModuleConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#package">package</a></strong></td>
<td valign="top"><a href="#package">Package</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#packages">packages</a></strong></td>
<td valign="top"><a href="#packageconnection">PackageConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#parameter">parameter</a></strong></td>
<td valign="top"><a href="#parameter">Parameter</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#parameters">parameters</a></strong></td>
<td valign="top"><a href="#parameterconnection">ParameterConnection</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#service">service</a></strong></td>
<td valign="top"><a href="#service">Service</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#services">services</a></strong></td>
<td valign="top"><a href="#serviceconnection">ServiceConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#view">view</a></strong></td>
<td valign="top"><a href="#view">View</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#views">views</a></strong></td>
<td valign="top"><a href="#viewconnection">ViewConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">serviceId</td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#workflow">workflow</a></strong></td>
<td valign="top"><a href="#workflow">Workflow</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#workflows">workflows</a></strong></td>
<td valign="top"><a href="#workflowconnection">WorkflowConnection</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">serviceId</td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">after</td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">limit</td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

## Mutation
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#setaccountaccess">setAccountAccess</a></strong></td>
<td valign="top"><a href="#setaccountaccesspayload">SetAccountAccessPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#setaccountaccessinput">SetAccountAccessInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deploystack">deployStack</a></strong></td>
<td valign="top"><a href="#deploystackpayload">DeployStackPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deploystackinput">DeployStackInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#destroystack">destroyStack</a></strong></td>
<td valign="top"><a href="#destroystackpayload">DestroyStackPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#destroystackinput">DestroyStackInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#validatecollection">validateCollection</a></strong></td>
<td valign="top"><a href="#validatecollectionpayload">ValidateCollectionPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#validatecollectioninput">ValidateCollectionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createcollection">createCollection</a></strong></td>
<td valign="top"><a href="#createcollectionpayload">CreateCollectionPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createcollectioninput">CreateCollectionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatecollection">updateCollection</a></strong></td>
<td valign="top"><a href="#updatecollectionpayload">UpdateCollectionPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatecollectioninput">UpdateCollectionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deletecollection">deleteCollection</a></strong></td>
<td valign="top"><a href="#deletecollectionpayload">DeleteCollectionPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletecollectioninput">DeleteCollectionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createitem">createItem</a></strong></td>
<td valign="top"><a href="#createitempayload">CreateItemPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createiteminput">CreateItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updateitem">updateItem</a></strong></td>
<td valign="top"><a href="#updateitempayload">UpdateItemPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateiteminput">UpdateItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deleteitem">deleteItem</a></strong></td>
<td valign="top"><a href="#deleteitempayload">DeleteItemPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteiteminput">DeleteItemInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#batchcreateitems">batchCreateItems</a></strong></td>
<td valign="top"><a href="#batchcreateitemspayload">BatchCreateItemsPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#batchcreateitemsinput">BatchCreateItemsInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#batchdeleteitems">batchDeleteItems</a></strong></td>
<td valign="top"><a href="#batchdeleteitemspayload">BatchDeleteItemsPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#batchdeleteitemsinput">BatchDeleteItemsInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createmodule">createModule</a></strong></td>
<td valign="top"><a href="#createmodulepayload">CreateModulePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createmoduleinput">CreateModuleInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatemodule">updateModule</a></strong></td>
<td valign="top"><a href="#updatemodulepayload">UpdateModulePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatemoduleinput">UpdateModuleInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deletemodule">deleteModule</a></strong></td>
<td valign="top"><a href="#deletemodulepayload">DeleteModulePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletemoduleinput">DeleteModuleInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#invokemodule">invokeModule</a></strong></td>
<td valign="top"><a href="#invokemodulepayload">InvokeModulePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#invokemoduleinput">InvokeModuleInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#validatepackage">validatePackage</a></strong></td>
<td valign="top"><a href="#validatepackagepayload">ValidatePackagePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#validatepackageinput">ValidatePackageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createpackage">createPackage</a></strong></td>
<td valign="top"><a href="#createpackagepayload">CreatePackagePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createpackageinput">CreatePackageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createpackagefromservice">createPackageFromService</a></strong></td>
<td valign="top"><a href="#createpackagepayload">CreatePackagePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createpackagefromserviceinput">CreatePackageFromServiceInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatepackage">updatePackage</a></strong></td>
<td valign="top"><a href="#updatepackagepayload">UpdatePackagePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatepackageinput">UpdatePackageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deletepackage">deletePackage</a></strong></td>
<td valign="top"><a href="#deletepackagepayload">DeletePackagePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletepackageinput">DeletePackageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createparameter">createParameter</a></strong></td>
<td valign="top"><a href="#createparameterpayload">CreateParameterPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createparameterinput">CreateParameterInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updateparameter">updateParameter</a></strong></td>
<td valign="top"><a href="#updateparameterpayload">UpdateParameterPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateparameterinput">UpdateParameterInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deleteparameter">deleteParameter</a></strong></td>
<td valign="top"><a href="#deleteparameterpayload">DeleteParameterPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteparameterinput">DeleteParameterInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#validateservice">validateService</a></strong></td>
<td valign="top"><a href="#validateservicepayload">ValidateServicePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#validateserviceinput">ValidateServiceInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createservice">createService</a></strong></td>
<td valign="top"><a href="#createservicepayload">CreateServicePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createserviceinput">CreateServiceInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updateservice">updateService</a></strong></td>
<td valign="top"><a href="#updateservicepayload">UpdateServicePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateserviceinput">UpdateServiceInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deleteservice">deleteService</a></strong></td>
<td valign="top"><a href="#deleteservicepayload">DeleteServicePayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteserviceinput">DeleteServiceInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#validateview">validateView</a></strong></td>
<td valign="top"><a href="#validateviewpayload">ValidateViewPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#validateviewinput">ValidateViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createview">createView</a></strong></td>
<td valign="top"><a href="#createviewpayload">CreateViewPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createviewinput">CreateViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updateview">updateView</a></strong></td>
<td valign="top"><a href="#updateviewpayload">UpdateViewPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateviewinput">UpdateViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deleteview">deleteView</a></strong></td>
<td valign="top"><a href="#deleteviewpayload">DeleteViewPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteviewinput">DeleteViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#validateworkflow">validateWorkflow</a></strong></td>
<td valign="top"><a href="#validateworkflowpayload">ValidateWorkflowPayload</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#validateworkflowinput">ValidateWorkflowInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createworkflow">createWorkflow</a></strong></td>
<td valign="top"><a href="#createworkflowpayload">CreateWorkflowPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createworkflowinput">CreateWorkflowInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updateworkflow">updateWorkflow</a></strong></td>
<td valign="top"><a href="#updateworkflowpayload">UpdateWorkflowPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateworkflowinput">UpdateWorkflowInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#deleteworkflow">deleteWorkflow</a></strong></td>
<td valign="top"><a href="#deleteworkflowpayload">DeleteWorkflowPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteworkflowinput">DeleteWorkflowInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#triggerworkflow">triggerWorkflow</a></strong></td>
<td valign="top"><a href="#triggerworkflowpayload">TriggerWorkflowPayload</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#triggerworkflowinput">TriggerWorkflowInput</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Objects

### Account

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#permissions">permissions</a></strong></td>
<td valign="top">[<a href="#useraccess">UserAccess</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#isactive">isActive</a></strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#usage">usage</a></strong></td>
<td valign="top"><a href="#accountusage">AccountUsage</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">startDate</td>
<td valign="top"><a href="#awsdate">AWSDate</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">endDate</td>
<td valign="top"><a href="#awsdate">AWSDate</a></td>
<td></td>
</tr>
</tbody>
</table>

### AccountUsage

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#runtime">runtime</a></strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#request">request</a></strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#storage">storage</a></strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### BatchCreateItemsPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#ids">ids</a></strong></td>
<td valign="top">[<a href="#id">ID</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### BatchDeleteItemsPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#ids">ids</a></strong></td>
<td valign="top">[<a href="#id">ID</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### Collection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#service">service</a></strong></td>
<td valign="top"><a href="#service">Service</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#options">options</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#mapping">mapping</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#triggers">triggers</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#queries">queries</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#usage">usage</a></strong></td>
<td valign="top"><a href="#collectionusage">CollectionUsage</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">startDate</td>
<td valign="top"><a href="#awsdate">AWSDate</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">endDate</td>
<td valign="top"><a href="#awsdate">AWSDate</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#insight">insight</a></strong></td>
<td valign="top"><a href="#collectioninsight">CollectionInsight</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">startDate</td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">endDate</td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">query</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">interval</td>
<td valign="top"><a href="#collectioninsightinterval">CollectionInsightInterval</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CollectionConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#collection">Collection</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### CollectionInsight

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#value">value</a></strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#count">count</a></strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CollectionUsage

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#storage">storage</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateCollectionPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateItemPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateModulePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreatePackagePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateParameterPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#key">key</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#value">value</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateServicePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateViewPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateWorkflowPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteCollectionPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteItemPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### DeleteModulePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### DeletePackagePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### DeleteParameterPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteServicePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### DeleteViewPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteWorkflowPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### DeployStackPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DestroyStackPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### InvokeModulePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#response">response</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### Item

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#collectionid">collectionId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#data">data</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### ItemConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#item">Item</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Log

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#processid">processId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#workflowid">workflowId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#triggeredat">triggeredAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#status">status</a></strong></td>
<td valign="top"><a href="#logstatus">LogStatus</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#name">name</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#type">type</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#result">result</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### LogConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#log">Log</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Meta

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#author">author</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#url">url</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Module

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#repository">repository</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#modulescope">ModuleScope</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#options">options</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#events">events</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#isactive">isActive</a></strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#meta">meta</a></strong></td>
<td valign="top"><a href="#meta">Meta</a></td>
<td></td>
</tr>
</tbody>
</table>

### ModuleConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#module">Module</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Package

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#stack">stack</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#packagescope">PackageScope</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#meta">meta</a></strong></td>
<td valign="top"><a href="#meta">Meta</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### PackageConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#package">Package</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Parameter

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#key">key</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#value">value</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ParameterConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#parameter">Parameter</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Service

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#domain">domain</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#parameters">parameters</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#settings">settings</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a></td>
<td></td>
</tr>
</tbody>
</table>

### ServiceConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#service">Service</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SetAccountAccessPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Subscription

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#_empty">_empty</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### TriggerWorkflowPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#status">status</a></strong></td>
<td valign="top"><a href="#workflowstatus">WorkflowStatus</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#result">result</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#errors">errors</a></strong></td>
<td valign="top">[<a href="#workflowerror">WorkflowError</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateCollectionPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateItemPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateModulePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdatePackagePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateParameterPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#key">key</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#value">value</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateServicePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateViewPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateWorkflowPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UserAccess

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#userid">userId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#permission">permission</a></strong></td>
<td valign="top"><a href="#accesstype">AccessType</a></td>
<td></td>
</tr>
</tbody>
</table>

### UserAccounts

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#permission">permission</a></strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UserAccountsConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#useraccounts">UserAccounts</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidateCollectionPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#options">options</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#mapping">mapping</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#triggers">triggers</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#queries">queries</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidatePackagePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#data">data</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#image">image</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#repository">repository</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#packagescope">PackageScope</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidateServicePayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#parameters">parameters</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#settings">settings</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidateViewPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#content">content</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#type">type</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#isactive">isActive</a></strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidateWorkflowPayload

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#definition">definition</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### View

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#service">service</a></strong></td>
<td valign="top"><a href="#service">Service</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#content">content</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#type">type</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#viewscope">ViewScope</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#usage">usage</a></strong></td>
<td valign="top"><a href="#viewusage">ViewUsage</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">startDate</td>
<td valign="top"><a href="#awsdate">AWSDate</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">endDate</td>
<td valign="top"><a href="#awsdate">AWSDate</a></td>
<td></td>
</tr>
</tbody>
</table>

### ViewConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#view">View</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ViewUsage

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#request">request</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### Workflow

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#service">service</a></strong></td>
<td valign="top"><a href="#service">Service</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#definition">definition</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#usage">usage</a></strong></td>
<td valign="top"><a href="#workflowusage">WorkflowUsage</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">startDate</td>
<td valign="top"><a href="#awsdate">AWSDate</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">endDate</td>
<td valign="top"><a href="#awsdate">AWSDate</a></td>
<td></td>
</tr>
</tbody>
</table>

### WorkflowConnection

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#nodes">nodes</a></strong></td>
<td valign="top">[<a href="#workflow">Workflow</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#nexttoken">nextToken</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### WorkflowError

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#code">code</a></strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#message">message</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#data">data</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### WorkflowUsage

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#runtime">runtime</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

## Inputs

### BatchCreateItem

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#collectionid">collectionId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#data">data</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### BatchCreateItemsInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#items">items</a></strong></td>
<td valign="top">[<a href="#batchcreateitem">BatchCreateItem</a>]!</td>
<td></td>
</tr>
</tbody>
</table>

### BatchDeleteItemsInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#items">items</a></strong></td>
<td valign="top">[<a href="#id">ID</a>]!</td>
<td></td>
</tr>
</tbody>
</table>

### BooleanFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#ne">ne</a></strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#eq">eq</a></strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateCollectionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#options">options</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#mapping">mapping</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#triggers">triggers</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#queries">queries</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#collectionid">collectionId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#data">data</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateModuleInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#options">options</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#events">events</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#repository">repository</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#modulescope">ModuleScope</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#meta">meta</a></strong></td>
<td valign="top"><a href="#metainput">MetaInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreatePackageFromServiceInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreatePackageInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#stack">stack</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#packagescope">PackageScope</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#meta">meta</a></strong></td>
<td valign="top"><a href="#metainput">MetaInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateParameterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#key">key</a></strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#value">value</a></strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateServiceInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#parameters">parameters</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#settings">settings</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateWorkflowInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#definition">definition</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### DateRangeFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#start">start</a></strong></td>
<td valign="top"><a href="#awsdate">AWSDate</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#end">end</a></strong></td>
<td valign="top"><a href="#awsdate">AWSDate</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DateTimeRangeFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#start">start</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#end">end</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteCollectionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteModuleInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeletePackageInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteParameterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteServiceInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteWorkflowInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeployStackInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#stack">stack</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#force">force</a></strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### DestroyStackInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#force">force</a></strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### FloatFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#ne">ne</a></strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#eq">eq</a></strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#le">le</a></strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#lt">lt</a></strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#ge">ge</a></strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#gt">gt</a></strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#contains">contains</a></strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#notcontains">notContains</a></strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#between">between</a></strong></td>
<td valign="top">[<a href="#float">Float</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### IDFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#ne">ne</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#eq">eq</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#le">le</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#lt">lt</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#ge">ge</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#gt">gt</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#contains">contains</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#notcontains">notContains</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#between">between</a></strong></td>
<td valign="top">[<a href="#id">ID</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#beginswith">beginsWith</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### IntFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#ne">ne</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#eq">eq</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#le">le</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#lt">lt</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#ge">ge</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#gt">gt</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#contains">contains</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#notcontains">notContains</a></strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#between">between</a></strong></td>
<td valign="top">[<a href="#int">Int</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### InvokeModuleInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#parameters">parameters</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#payload">payload</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### ItemSearch

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#query">query</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### LogFilter

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#startdate">startDate</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#enddate">endDate</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#status">status</a></strong></td>
<td valign="top"><a href="#logstatus">LogStatus</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#workflowid">workflowId</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#processid">processId</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### LogSearch

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#query">query</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### MetaInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#author">author</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#url">url</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SetAccountAccessInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#userid">userId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#permission">permission</a></strong></td>
<td valign="top"><a href="#accesstype">AccessType</a></td>
<td></td>
</tr>
</tbody>
</table>

### StringFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#ne">ne</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#eq">eq</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#le">le</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#lt">lt</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#ge">ge</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#gt">gt</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#contains">contains</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#notcontains">notContains</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#between">between</a></strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#beginswith">beginsWith</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### TriggerWorkflowInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#payload">payload</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateCollectionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#options">options</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#mapping">mapping</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#triggers">triggers</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#queries">queries</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateItemInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#collectionid">collectionId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#data">data</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateModuleInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#options">options</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#events">events</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#repository">repository</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#modulescope">ModuleScope</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#meta">meta</a></strong></td>
<td valign="top"><a href="#metainput">MetaInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdatePackageInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#stack">stack</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#packagescope">PackageScope</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#meta">meta</a></strong></td>
<td valign="top"><a href="#metainput">MetaInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateParameterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#key">key</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#value">value</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateServiceInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#parameters">parameters</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#settings">settings</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateWorkflowInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#definition">definition</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidateCollectionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#options">options</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#mapping">mapping</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#triggers">triggers</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#queries">queries</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidatePackageInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#data">data</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#image">image</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#repository">repository</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#scope">scope</a></strong></td>
<td valign="top"><a href="#packagescope">PackageScope</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidateServiceInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#description">description</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#parameters">parameters</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#settings">settings</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidateViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#content">content</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#type">type</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#isactive">isActive</a></strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### ValidateWorkflowInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#serviceid">serviceId</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#label">label</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#summary">summary</a></strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#definition">definition</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

## Enums

### AccessType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>owner</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>admin</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>operator</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>none</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CollectionInsightInterval

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>hour</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>day</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>week</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>month</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>year</strong></td>
<td></td>
</tr>
</tbody>
</table>

### LogStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>success</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>error</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ModuleScope

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>public</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>private</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>secret</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PackageScope

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>public</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>secret</strong></td>
<td></td>
</tr>
</tbody>
</table>

### TriggerMethod

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>webhook</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>api</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>schedule</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>event</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ViewScope

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>public</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>private</strong></td>
<td></td>
</tr>
</tbody>
</table>

### WorkflowStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>success</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>error</strong></td>
<td></td>
</tr>
</tbody>
</table>

## Scalars

### AWSDate

A date string, such as 2007-12-03, compliant with the `full-date` format outlined in section 5.6 of the RFC 3339 profile of the ISO 8601 standard for representation of dates and times using the Gregorian calendar.

### AWSDateTime

A date-time string at UTC, such as 2007-12-03T10:15:30Z, compliant with the `date-time` format outlined in section 5.6 of the RFC 3339 profile of the ISO 8601 standard for representation of dates and times using the Gregorian calendar.

### AWSJSON

AWSJSON string type

### AWSPhone

AWSPhone type

### AWSTime

A time string at UTC, such as 10:15:30Z, compliant with the `full-time` format outlined in section 5.6 of the RFC 3339profile of the ISO 8601 standard for representation of dates and times using the Gregorian calendar.

### Boolean

The `Boolean` scalar type represents `true` or `false`.

### EmailAddress

A field whose value conforms to the standard internet email address format as specified in RFC822: https://www.w3.org/Protocols/rfc822/.

### Float

The `Float` scalar type represents signed double-precision fractional values as specified by [IEEE 754](https://en.wikipedia.org/wiki/IEEE_floating_point).

### ID

The `ID` scalar type represents a unique identifier, often used to refetch an object or as key for a cache. The ID type appears in a JSON response as a String; however, it is not intended to be human-readable. When expected as an input type, any string (such as `"4"`) or integer (such as `4`) input value will be accepted as an ID.

### Int

The `Int` scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1.

### String

The `String` scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.

### URL

A field whose value conforms to the standard URL format as specified in RFC3986: https://www.ietf.org/rfc/rfc3986.txt.


## Interfaces


### Element

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#createdat">createdAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#updatedat">updatedAt</a></strong></td>
<td valign="top"><a href="#awsdatetime">AWSDateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong><a name="#data">data</a></strong></td>
<td valign="top"><a href="#awsjson">AWSJSON</a></td>
<td></td>
</tr>
</tbody>
</table>

### Node

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong><a name="#id">id</a></strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>
