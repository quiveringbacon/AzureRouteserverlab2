# Azure Routeserver lab2 with C8000v

This creates a hub vnet and a c8000v that is peered with a route server, and is advertising a default route and natt'ing the inside address space for internet access. 2 spoke vnets are peered to the hub. VM's are created in all 3 vnets. You'll be prompted for the resource group name, location where you want the resources created, your public ip, and username and password to use for the VM's and NVA. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip. This also creates a logic app that will delete the resource group in 24hrs. The topology will look something like this:

![RSlab2-csr1000v](https://github.com/quiveringbacon/AzureRouteserverlab2/assets/128983862/83a384ba-9754-4b99-aa3f-e0d70ed9d094)


You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone https://github.com/quiveringbacon/AzureRouteserverlab2.git ./terraform". Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.
