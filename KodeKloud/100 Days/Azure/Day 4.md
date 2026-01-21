# Overview 

The Nautilus DevOps team is strategizing the migration of a portion of their infrastructure to the Azure cloud. Recognizing the scale of this undertaking, they have opted to approach the migration in incremental steps rather than as a single massive transition. To achieve this, they have segmented large tasks into smaller, more manageable units. This granular approach enables the team to execute the migration in gradual phases, ensuring smoother implementation and minimizing disruption to ongoing operations.

Create a Virtual Network (VNet) named `nautilus-vnet` in the `southcentralus` region with any `IPv4` CIDR block.

# What is an Azure Virtual Network?

An Azure Virtual Network (VNet) is an isolated network in Azure that allows you to securely connect Azure resources like VMs, databases, and services to each other, to the internet, and to on-premises networks.

# Solution

First we search for "virtual networks" in the search bar
![[Pasted image 20260121222141.png]]

Click on "+create"
![[Pasted image 20260121222251.png]]

Now we add our virtual network name `nautilus-vnet` and select the region `southcentralus`
![[Pasted image 20260121222526.png]]

Checking the Security and IP address tab we can leave as default:
![[Pasted image 20260121222709.png]]

Now we can Click "Review + create" and make sure all settings are correct and we can "Create" our virtual network. Which we see the deployment will be complete within a few seconds after creating it.
![[Pasted image 20260121222934.png]]

# Best Security Practices

- **Use subnets to segment resources** by function (web, app, database tiers)
- **Implement Network Security Groups (NSGs)** on subnets to control traffic flow
- **Use Azure Bastion** for secure RDP/SSH access instead of exposing VMs to the internet
