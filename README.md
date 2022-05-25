# NSM_GP-IKT_2_0_policyinitative
Example Azure Policy initative with mapping to NSM grunnprinsipper for IKT sikkerhet. Deploy and assign to management group scope. 


#### Deploy definition to management group scope
````powershell

# Change the variables below to contain the right values for your management group ID, location and json file location

$location = 'norwayeast'
$mgId = 'Contoso-MG'
$templateFile = 'C:\git\policy\initiative\NSM_GP-IKT_2_0.json'

New-AzManagementGroupDeployment -ManagementGroupId $mgId -Location $location -TemplateFile $templateFile -Verbose

````                             


#### Add to Regulatory Compliance dashboard in Defender for Cloud

https://docs.microsoft.com/en-us/azure/defender-for-cloud/custom-security-policies?pivots=azure-portal

> !!! Current version is missing the hierarchy mapping of IDs and control domain in the Azure portal view. See additional documentation for the example mappings between specific controls and azure policies. [Details of the NSMs grunnprinsipper for IKT-sikkerhet v2.0 policy initiative](/NSM_GP_IKT_2_0.md) !!!

#### Example screenshot from Defender for Cloud - Regulatory Compliance dashboard
![Example screenshot](/regulatory_compliance_example.png)
