# Azure-Firewall-into-existing-environment

[<img src="http://azuredeploy.net/deploybutton.png"/>](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fkblackstone%2FPaloAltoNetworks%2Fmaster%2FAzure-1FW-4-interfaces-NewAS-existing-environment%2FAzureDeploy.json)

This template was created to support the deployment of a 4 interface Palo Alto Networks firewall into an existing Microsoft Azure environment that has the following items already deployed:

                    -Load Balancer - If being used (does not need to exist yet)
                    -VNET - with subnets
                    -Storage Account for the firewall VHD
                    -Resource Group for Firewall
            

FEATURES:
- Creates the Availability Set for the firewall.
- The firewall deploys with 4 interfaces.  1 MGMT and 3 data plane into an existing environment.
- It is possible to choose the version of software the firewall is running. 7.1 or 8.0 (Latest)
- The deployment SKU can also be choosen during deployment.  BYOL, Bundle1 or Bundle2 are the available options.
- Static IP addresses assignment is used for all the firewall interfaces.


The following Storage Account types are supported:

                    -Standard_LRS
                    -Standard_GRS
                    -Standard_RAGRS
                    -Premium_LRS
                    
The following VMs are supported:

                    -Standard_D3
                    -Standard_D4
                    -Standard_D3_v2
                    -Standard_D4_v2
                    -Standard_A4
                    -Standard_DS3_v2
                    -Standard_DS4_v2
        
NOTE: Make sure the VMs are supported in the specific Storage Account Type and Azure Region.

After deploying, this firewall can be intetgrated into a load balancer setup via the Azure Portal.

# Support

This template/solution is released under an as-is, best effort, support policy. These scripts should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself. Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under the best effort policy.

For assistance from the community, please post your questions and comments either to the GitHub page where the solution is posted or on our Live Community site dedicated to public cloud discussions at https://live.paloaltonetworks.com/t5/AWS-Azure-Discussions/bd-p/AWS_Azure_Discussions
