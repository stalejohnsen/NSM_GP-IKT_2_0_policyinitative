# NSM_GP-IKT_2_0_policyinitative
Example Azure Policy initative with mapping to NSM grunnprinsipper for IKT sikkerhet. Deploy and assign to management group scope. 

1. Deploy policy initative definition
```
$location = 'norwayeast'
$mgId = 'Contoso-MG'
New-AzManagementGroupDeployment -ManagementGroupId $mgId -Location $location -TemplateFile C:\git\policy\initiative\NSM_GP-IKT_2_0.json
```

2. Add to Regulatory Compliance dashboard in Defender for Cloud

https://docs.microsoft.com/en-us/azure/defender-for-cloud/custom-security-policies?pivots=azure-portal

> Current version missing mapping of ID and control domain. See additional documentation for mapping
![Example screenshot](/regulatory_compliance_example.png)
