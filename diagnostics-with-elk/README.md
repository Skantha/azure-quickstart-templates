# Install ELK on a Ubuntu machine

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSkantha%2Fsemantic-logging%2Felk%2FELK%2FAzureRM%2Felk-simple-on-ubuntu%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

This template deploys an Azure Linux cluster and installs Elasticsearch, Logstash and Kibana.
The user can specify a custom Logstash configuration using the encodedConfigString parameter or specify an existing storage account to use as input. 

Below are the parameters that the template expects:

|Name   |Description    |
|:---   |:---|
|adminUsername  |The admin user name. |
|adminPassword  |The admin password. |
|dnsNameForPublicIP |Public dns name for the Kibana VM.   |
|encodedConfigString    |Base64 encoded string which is the Logstash configuration. <a href="http://codepen.io/juliusl/pen/ZGJJQB" target="_blank">Click here to create a logstash configuration</a>. If you enter a value here then the next three parameters are ignored. Otherwise if you would like to specify the WAD storage account details then set this to "na" and provide values for the next three parameters. Default value is "na". |
|existingDiagnosticsStorageAccountName    |The name of the existing storage account that has diagnostics data.  |
|existingDiagnosticsStorageAccountKey    |The key for the existing storage account that has diagnostics data.  |
|diagnosticsTableNames    |The table names in the existing storage account that have diagnostics data. Separate table names using semicolon (;).  |

#Notes & Limitations
- This template uses the Elasticsearch template from: https://azure.microsoft.com/en-us/documentation/templates/elasticsearch/

