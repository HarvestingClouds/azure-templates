# MultiNIC

<table><tr><td>Parent resource group (see documentation)</td>
<td>
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftelmosampaio%2Fazure-templates%2Fmaster%2FIaaSStory%2FIaaSStory%2FTemplates%2F11-MultiNIC%2Fprerequisites.json" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/></a>
</td></tr>
<tr><td>Backend resource group (see documentation)</td>
<td>
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftelmosampaio%2Fazure-templates%2Fmaster%2FIaaSStory%2FIaaSStory%2FTemplates%2F11-MultiNIC%2Fazuredeploy.json" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/></a>
</td></tr>
<tr><td>Parent resource group
<td>
<a href="http://armviz.io/#/?load=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fraw.githubusercontent.com%2Ftelmosampaio%2Fazure-templates%2Fmaster%2FIaaSStory%2FIaaSStory%2FTemplates%2F11-MultiNIC%2Fprerequisites.json" target="_blank"><img src="http://armviz.io/visualizebutton.png"/></a>
</td></tr>
<tr><td>Backend resource group</td>
<td>
<a href="http://armviz.io/#/?load=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fraw.githubusercontent.com%2Ftelmosampaio%2Fazure-templates%2Fmaster%2FIaaSStory%2FIaaSStory%2FTemplates%2F11-MultiNIC%2Fazuredeploy.json" target="_blank"><img src="http://armviz.io/visualizebutton.png"/></a>
</td></tr></table>

This template creates a series of multiNIC VMs in a pre-existing subnet based on a documented scenario.

Please visit [multi NIC scenario](https://azure.microsoft.com/documentation/articles/virtual-networks-create-multinic-arm-template/) to read the scenario and understand how to use this template.

Below are the parameters that the template expects.

| Name   | Description    |
|:--- |:---|
| vnetName | Name of the existing vnet |
| backEndSubnetName | Name of the existing back end subnet where the db VMs will be created |
| stdStorageName | Name of the existing the standard storage account used to store os vhds |
| prmStorageName | Name of the new premium storage account that will be used to store data SSD vhds |
| prmStorageType | Type of storage for the new premium storage account, defaults to Premium_LRS |
| osType | 0 for Windows with SQL 2014, 1 for Ubuntu  |
| dbCount | Number of VMs in the back end subnet |
| parentRG | Name of existing resource group containing necessary artifacts (see documentation) |
