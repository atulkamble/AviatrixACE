## Aviatrix ACE (Aviatrix Certified Engineer) Multi-Cloud Networking Associate Exam Study Notes

### Aviatrix
Aviatrix Systems is a software company headquartered in Santa Clara, California, the heart of Silicon Valley. Aviatrix software provides a platform for companies to build networking and security infrastructure in the public cloud. The platform provides architecture applicable to both single and multiple public cloud deployments. Currently, the software supports public clouds such as AWS, Azure, GCP, and OCI.
Aviatrix Systems was the recipient of the Gartner Cool Vendor award in Cloud Computing in 2017 and is the pioneer of Multi-Cloud Network Architecture (MCNA).

### Multi Cloud Network Architecture (MCNA)
MCNA is unlike any other architecture because it embraces, controls, and manages not only the native cloud constructs but also provides advanced services beyond what the Cloud Services Providers (AWS, Azure, GCP, and OCI) can provide. It provides a consistent and repeatable architecture across multiple clouds, being the first in the industry to do so, making it an essential part of the present and future of the public cloud.
Aviatrix creates a purpose-built Multi-Cloud Network Architecture (MCNA) by implementing a data plane through dynamic and software-defined routing with a centralized control plane. Security is built into the network architecture through segmentation, encryption, ingress and egress filtering, and security services insertion. Aviatrix also leverages orchestrating cloud-native constructs, where necessary, in building and controlling the enterprise network and life-cycle management of the overall architecture. 
The architecture is valid for single-cloud-single-region, single-cloud-multiple-regions, or multiple-clouds-multiple-regions and can be easily referenced by both green and brownfield businesses with no issues. This is a common and repeatable architecture across multiple clouds, which creates simplicity and abstraction for the users by hiding all the underlying complexities and limitations of Cloud Service Providers. Because this architecture functions as a reference, it is vendor-agnostic.Architecture defines four distinct layers at a high level. These are Cloud Core, Cloud Security, Cloud Access, and Cloud Operations.

### The Components of the MCNA
1. The Cloud Core has the applications connecting to the Global Transit Layer, which is a unified, global data plane across multiple/single clouds.
2. The Cloud Access Layer is where the on-prem components connect to the cloud.
3. The Cloud Security should be embedded in the Cloud Core Layer and the Cloud Access layer, because the public cloud is a shared infrastructure. This can be seen in the MCN Architecture when the Cloud Security layer cuts through the others.
4. Similarly, the Cloud Operations layer makes Day 1, 2, and 3 operations accessible to all the parts of the cloud. This allows troubleshooting and visibility.

## The Benefits of the MCNA Approach
- The architecture is easily replicated in the Aviatrix controller.
- There is a normalized data plane.
- Service insertion and chaining are easily configured through the transit layer.

## Aviatrix Platform
- **A Centralized Controller**\
Aviatrix offers a centralized controller to make complex networking easy and does not require any background knowledge of networking command-line interfaces.
This controller is also the entry-point for multi-cloud automation, which can be done using Application Programming Interface or Terraform.
It is a browser-based, point-and-click management console that orchestrates both native (AWS, Azure, GCP, and OCI) constructs and advanced services from Aviatrix. This centralized controller also deploys Aviatrix Gateway instances for multi-cloud, on-premise, and edge connectivity.

- **A Distributed and Common Data-Plane**\
The Aviatrix platform embraces native cloud constructs and extends the functionality using advanced networking and security, which are both provided by Aviatrix Controller and Gateways.
The Aviatrix gateways can be considered as service nodes, providing a robust and common data-plane within a Cloud or across multiple Clouds.
As part of the data-plane, these gateways work to provide services such as transit routing, high-performance encryption, egress and ingress control, edge connectivity, on-premise connectivity, and user-VPN services.

- **Operational Visibility**\
CoPilot, one of Aviatrix's many services, allows users to have full operational visibility in their network, all while informing them if their cloud network has any issues.

- **Multiple Accounts and Clouds**\
Aviatrix is also able to integrate multiple accounts and clouds seamlessly and on one single interface. This allows customers to interconnect AWS, Azure, and Google Cloud with the same point and click flow.

- **Security & Compliance**\
To help its service run smoothly, Aviatrix provides many security and compliance measures. It allows users to manage security domains, such as the Development domain and the Production domain, and also allows for Virtual Private Cloud connectivity through Connection Policies. Users are able to easily apply firewall filters based on tags or specific address ranges, CIDR, protocols, and ports.
Aviatrix services are also integrated with AWS GuardDuty to block malicious activity automatically at the Virtual Private Cloud network level.

# AWS Direct Connect virtual interfaces
You must create one of the following virtual interfaces to begin using your AWS Direct Connect connection.

- **Private virtual interface:**\
A private virtual interface should be used to access an Amazon VPC using private IP addresses.

- **Public virtual interface:**\
A public virtual interface can access all AWS public services using public IP addresses.

- **Transit virtual interface:**\
A transit virtual interface should be used to access one or more Amazon VPC Transit Gateways associated with Direct Connect gateways. You can use transit virtual interfaces with 1/2/5/10 Gbps AWS Direct Connect connections. For information about Direct Connect gateway configurations, see Direct Connect gateways.


# VNet
A Virtual Network, or a VNet, is an isolated network within the Microsoft Azure cloud. A VNet in Azure provides a range of networking functions comparable to AWS Virtual Private Cloud (VPC). These functions include DNS, routing, enabling customization of DHCP blocks, access control, connectivity between virtual machines (VM) and virtual private networks (VPN).

An Azure VNet is a representation of a network in the cloud and is logical isolation of the Azure cloud dedicated to a subscription. In the background, it's a software abstraction of a network that overlays Azure’s infrastructure to provide isolation from resources outside of the VNet, practically making it a private network.

Operationally, a VNet follows common IP routing principles to connection resources inside. So, it needs to have one or more address spaces associated with it (CIDR), which can be segmented into subnets, within which resources will reside. The scope of a virtual network is a single region; however, several virtual networks of the same or different regions can be connected together by virtual network peering.

### VNets can be used to:
Create a dedicated private cloud-only VNet to allow services and VMs within the VNet to communicate directly and securely in the cloud.
Securely extend a data center, by building traditional site-to-site (S2S) VPNs or Express Route private circuits, to securely scale capacity.
Deploy hybrid clouds by securely connecting cloud-based applications to on-premises systems.

## Key components of Azure VNets, include:
**Subnets:** Subdivide a VNet into multiple networks which can be used for more granular separation of services
**IP addresses:** Assign public or private IP addresses to an Azure VNet.
- Use public IP address for public-facing communications. A dynamic or static IP can be assigned.
- Use private IP address for connectivity within a VNet when using a VPN gateway or ExpressRoute. A dynamic IP assignment is a default, but a static IP can also be assigned.
**Network Security Groups (NSG):** Network traffic ACLs which can be applied at a subnet or NIC level for filtering
**Application Security Groups (ASG):** Group common workloads in world readable tags for use in NSGs
**Service Endpoints:** secure critical Azure services resources to your VNET
**Private Link:** private connectivity from a VNET to an Azure PaaS resource, customer-owned service, or Microsoft partner platform.
**Firewall:** Azure offers a managed Firewall service that provides the ability to define L3-7 connectivity policies for granular control of what enters and leaves the network
**Load balancing:** Load balancing solutions offered by Azure include:
- Azure Traffic Manager – comparable to Route53 in AWS
- Azure Load Balancer
- Azure Application Gateway
- Azure Front Door
**Routing tables:** As with general routing, anytime traffic needs to leave a subnet, it needs a routing function to forward packets to other subnets and networks. A router does this using a routing table, and that route table configuration is exposed in Azure for customized configuration. Route table can have rules that define where traffic should be sent to, i.e a virtual network, virtual network gateway or virtual machine.
**User Defined Route (UDR):** A static entry in a Route Table which can be used to forward traffic to a different Vnet, Network Virtual Appliance, . This can be a powerful tool to build a connection between hubs.
**Network Virtual network Appliance (NVA):** Optional, for integration of 3rd party solutions, a virtual network appliance can be inserted into a VNet. This appliance is a virtual machine that executes a network function, such as a firewall, WAN optimization or other network function. To see a list of virtual network applications that can be deployed in a virtual network, see Azure Marketplace.

# Remote User VPN
Aviatrix provides a cloud-native and feature-rich client VPN solution. The solution is based on OpenVPN® and is compatible with all OpenVPN® clients. In addition, Aviatrix provides its own client that supports SAML authentication directly from the client.



# Aviatrix Transit Architecture for Azure

- **Azure Native Transit**\
The most common design topology within Azure is the Hub and Spoke model. The hub is a virtual network (VNet) in Azure that acts as a central point of connectivity to your on-premises network. The spokes are VNets that peer with the HUB and can be used to isolate workloads, departments, subscriptions, etc... Traffic flows between the on-premises datacenter and the hub through an ExpressRoute or VPN gateway connection. It is common in these environments for spoke to spoke communication to be desired both within and across regions. To facilitate spoke to spoke communication, Azure natively provides three methods for performing this functionality. Each of these options has advantages and disadvantages however, these options can be used simultaneously for customers to apply the right transit method for the desired outcome.

- **Intra-Region Transitive Options:**
The options for spoke to spoke communication across regions follow the same patterns above with a few notable nuances.

1. **Leveraging ExpressRoute-** the most common transitive method is for customers to leverage their ExpressRoute circuits to provide spoke to spoke communication. This method requires a default (0.0.0.0/0) or summary route to be advertised from on-prem to allow spoke to spoke traffic to hairpin off the Microsoft Edge Routers. The advantage to this method is that this traffic will not incur VNET peering charges and this provides any to any spoke connectivity. The disadvantage to this approach is that bandwidth is limited by the ExpressRoute gateway SKU, traffic takes a longer path from spoke to spoke, a lack of granular control as this method provides any to any communication, and the fact that this is not a recommended approach as there is no dedicated bandwidth allocation on the Microsoft Edge Routers for this configuration.
2. **Leveraging a HUB Network Virtual Appliance (NVA)-** in this option, an NVA is deployed in the HUB VNET and User Defined Routes (UDRs) are created in each spoke to route traffic from spoke to spoke. The advantage to this approach is that traffic takes a more ideal path, does not require any route advertisements from on-prem, and potentially provides additional security functionality depending upon the NVA being leveraged. The disadvantage to this approach comes with the management of UDRs at scale, potential bandwidth limits of the NVA itself, and the configuration of NVA high availability (HA) to ensure redundancy in case of failure.
3. **VNET Peering-** the recommended approach for spoke to spoke communication is VNET peering as this leverages the MSFT backbone directly and always takes the preferred path. This option provides the lowest latency possible and has no bandwidth restrictions as opposed to the options previously discussed. The disadvantage of this model is this connectivity is a 1 to 1 mapping. Each spoke much be peered directly with another spoke in order to facilitate communication which at scale becomes a web of interconnected fully meshed VNETS. As such, customers often have challenges in managing the scale of VNET peers.


- **Inter-Region Transitive Options:**
The options for spoke to spoke communication across regions follow the same patterns above with a few notable nuances.

1. **Leveraging ExpressRoute-** this method is similar to what was described in Intra-Region however, as ExpressRoute circuits are terminated across regions the routes are propagated automatically. To facilitate cross region spoke to spoke communication, no summary or default route is required. The same advantages and disadvantages apply.
2. **Leveraging a HUB Network Virtual Appliance (NVA)-** this method is also similar to what was previously described however, the number of UDRs increases as additional routes must be defined in the HUB VNETs to facilitate routing across regions to another HUB. Additionally, a VNET peer must be leveraged between the HUB to facilitate this HUB to HUB transit path.
3. **VNET Peering-** the only change in VNET peering across regions is in naming convention. Microsoft refers to this as Global VNET Peering but still has the same advantages and disadvantages previously discussed.
Azure Virtual WAN is another native architectural approach which can also provide transitive functionality. Aviatrix Transit can integrate with Azure Virtual WAN and is not covered in detail here.

### Aviatrix Transit for Azure
Aviatrix Transit for Azure is an architecture to interconnect multiple VNets and on-prem leveraging the hub and spoke deployment model while adding additional functionality and features. 
The Aviatrix Controller is a VM that manages all networking connections from VNETs to on-prem as well as between VNETs themselves. It deploys one Aviatrix gateway (two for redundancy) in each VNet. The Transit gateway is deployed in the transit VNet and connects to on-prem over Express Route or Internet. The Transit Gateway is then peered to each spoke VNET gateway to provide end to end communication. Communication can be granularly controlled to provide any to any communication between the spokes and to/from on-prem however, the transit gateway can also block certain traffic to keep spokes isolated. Additionally, all Spoke UDRs are orchestrated from the controller based on desired traffic flows.

For cross region communication, multiple Transit Gateways can also be interconnected. Spoke VNets can communicate to remote Spoke VNets through the two connected Transit Gateways with the same granular controls mentioned previously. Additionally, route advertisements between the two transit gateways can be controlled to provide additional functionality like summarization, route exclusion, etc.
Another important advantage of using Aviatrix Transit is that all communications are encrypted by default providing additional levels of security. Azure does not provide any native encryption across the Microsoft Backbone and depends upon third party NVAs to provide this functionality should customers require it.

The Aviatrix controller also has the ability to orchestrate native VNET peering for Azure VNETs should customers not wish to deploy gateways within spoke VNETs. While customers will lose the encryption and visibility benefits across these links, all appropriate UDRs will be orchestrated to facilitate transitive communication as desired. It is also important to note that certain native limitations may apply as to the number of peerings allowed as well as restricitions to overlapping IP space when native peering is leveraged.

### Need of Aviatrix Transit for Azure
Transit architecture is about building connectivity between cloud and on-prem in the most agile manner possible. In the Transit architecture, there is one connection (not including the backup) between on-prem and a Transit Hub VNet. Everything else (the Spoke VNet to on-prem traffic) is routed through the Transit Hub VNet.

The alternative to Transit architecture is to leverage the native options already mentioned or is to build one connection (often referred to as “flat” architecture), either IPSEC over Internet or Express Route, each time you spin up a new VNet in Azure. This requires changes at the on-prem edge, which requires a change control process that takes from days to weeks. Additionally, this method often facilitates the default any to any connectivity which may require additional configuration to prevent.

### The Benefits of Aviatrix Transit for Azure
- **Simplicity** The Aviatrix Controller provides an abstraction layer and workflow to build the Transit network. You do not need to program any Azure route tables, manage the route entries or understand the significant details about Azure networking.
- **Multi Subscriptions Support** The Controller provides a single pane of glass to manage the entire cloud network of multiple Azure subscriptions.
- **Logging Service Integration** Out-of-the-box integration with Splunk, Sumo Logic, DataDog, ELK, remote syslog and Netflow.
- **Visibility** View connectivity status, network latency and traffic statistics from a central dashboard.
- **Granular Routing Control** Route redistribution can be controlled to selectively allow specific route propagation and/or summarization.
- **Advanced Networking Features** Support for Network Address Translation, NGFW Insertion, FQDN filtering, etc.
- **No Route Limits** The Aviatrix solution auto summarizes the on-prem and Spoke VNet routes so that Spoke VNet route entries do not exceed the route limits.
- **End-to-End Encryption** All traffic in flight, between Spoke VNets and between Spoke to on-prem, is encrypted.

# Aviatrix Stateful Firewall Rule
Aviatrix stateful firewall is feature on the Aviatrix gateway. It is a L4 stateful firewall that filters network CIDR, protocol and port on the packet forwarding path.
The stateful firewall allows each individual rule to be defined as Allow, Deny and Force Drop, in addition to a base rule.

- **How many rules can be configured on a gateway?**
Currently you can configure up to 500 rules on each gateway. This limitation is not due to the lack of capacity in the gateways, but is because of the implementation of how rules are sent to the gateways. In the next release (5.2), the limitation will be removed.

- **What is the API to configure stateful firewall?**
Currently the API call requires you to input the entire set of the rules for each call. There is no incremental append or delete functions.
In the next release (5.2), there will be new APIs to append new rules and delete a specific rule.

# Transit VNet using VNet peering
Azure Virtual Network (VNet) is the fundamental building block for any customer network. VNet lets you create your own private space in Azure, or as I call it your own network bubble. VNets are crucial to your cloud network as they offer isolation, segmentation, and other key benefits. Read more about VNet’s key benefits in our documentation,
With VNets, you can connect your network in multiple ways. You can connect to on-premises using Point-to-Site (P2S), Site-to-Site (S2S) gateways or ExpressRoute gateways. You can also connect to other VNets directly using VNet peering.

Customer network can be expanded by peering Virtual Networks to one another. Traffic sent over VNet peering is completely private and stays on the Microsoft Backbone. No extra hops or public Internet involved. Customers typically leverage VNet peering in the hub-and-spoke topology. The hub consists of shared services and gateways, and the spokes comprise business units or applications.

# Gateway transit
Today I’d like to do a refresh of a unique and powerful functionality we’ve supported from day one with VNet peering. Gateway transit enables you to use a peered VNet’s gateway for connecting to on-premises instead of creating a new gateway for connectivity. As you increase your workloads in Azure, you need to scale your networks across regions and VNets to keep up with the growth. Gateway transit allows you to share an ExpressRoute or VPN gateway with all peered VNets and lets you manage the connectivity in one place. Sharing enables cost-savings and reduction in management overhead.

With Gateway transit enabled on VNet peering, you can create a transit VNet that contains your VPN gateway, Network Virtual Appliance, and other shared services. As your organization grows with new applications or business units and as you spin up new VNets, you can connect to your transit VNet with VNet peering. This prevents adding complexity to your network and reduces management overhead of managing multiple gateways and other appliances.

VNet peering works across regions, across subscriptions, across deployment models (classic to ARM), and across subscriptions belonging to different Azure Active Directory tenants.


# Author Profile:
- [LinkedIn: atuljkamble](https://www.linkedin.com/in/atuljkamble) 
- [Twitter: atul_kamble](https://www.twitter.com/atul_kamble)
- [Github: atulkamble](https://www.github.com/atulkamble)
- [Medium: atul_kamble](https://medium.com/@atul_kamble)


