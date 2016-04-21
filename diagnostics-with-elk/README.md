# Analyze Diagnostics Data with ELK

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSkantha%2Fazure-quickstart-templates%2Felk%2Fdiagnostics-with-elk%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

This template deploys a Linux cluster and installs Elasticsearch, Logstash and Kibana.
The user can specify a custom Logstash configuration using the encodedConfigString parameter or specify an existing storage account to use as Logstash input source.

#Notes
- This template uses the Elasticsearch template from: <a href="../elasticsearch">azure-quickstart-templates/elasticsearch/<a/>

