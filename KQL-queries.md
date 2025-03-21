# Useful KQL queries 

let ResourceCreation=AzureActivity
| where OperationNameValue =~ 'MICROSOFT.RESOURCES/DEPLOYMENTS/WRITE';
ResourceCreation
| summarize arg_max(TimeGenerated, *) by CorrelationId
| where ActivityStatusValue =~ 'Success'
| project CorrelationId
| join kind=inner (ResourceCreation)
| summarize arg_min(TimeGenerated, *) by CorrelationId) on CorrelationId
| project TimeGenerated, Caller, Caller IpAddress, ResourceGroup, _ResourceId
