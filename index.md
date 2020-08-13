## Aviatrix ACE (Aviatrix Certified Engineer) Multi-Cloud Networking Associate Exam Study Notes

# Aviatrix
Aviatrix Systems is a software company headquartered in Santa Clara, California, the heart of Silicon Valley. Aviatrix software provides a platform for companies to build networking and security infrastructure in the public cloud. The platform provides architecture applicable to both single and multiple public cloud deployments. Currently, the software supports public clouds such as AWS, Azure, GCP, and OCI.
Aviatrix Systems was the recipient of the Gartner Cool Vendor award in Cloud Computing in 2017 and is the pioneer of Multi-Cloud Network Architecture (MCNA).

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

# Multi Cloud Network Architecture (MCNA)
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



# AWS Direct Connect virtual interfaces
You must create one of the following virtual interfaces to begin using your AWS Direct Connect connection.

- **Private virtual interface:**\
A private virtual interface should be used to access an Amazon VPC using private IP addresses.

- **Public virtual interface:**\
A public virtual interface can access all AWS public services using public IP addresses.

- **Transit virtual interface:**\
A transit virtual interface should be used to access one or more Amazon VPC Transit Gateways associated with Direct Connect gateways. You can use transit virtual interfaces with 1/2/5/10 Gbps AWS Direct Connect connections. For information about Direct Connect gateway configurations, see Direct Connect gateways.

# Azure Firewall
Azure Firewall is a cloud native network security service. It offers fully stateful network and application level traffic filtering for VNet resources, with built-in high availability and cloud scalability delivered as a service. You can protect your VNets by filtering outbound, inbound, spoke-to-spoke, VPN, and ExpressRoute traffic. Connectivity policy enforcement is supported across multiple VNets and Azure subscriptions. You can use Azure Monitor to centrally log all events. You can archive the logs to a storage account, stream events to your Event Hub, or send them to Log Analytics or your security information and event management (SIEM) product of your choice.

## Azure Firewall and network virtual appliances
Network security solutions can be delivered as appliances on premises, as network virtual appliances (NVAs) that run in the cloud or as a cloud native offering (known as firewall-as-a-service).
Customers often ask us how Azure Firewall is different from Network Virtual Appliances, whether it can coexist with these solutions, where it excels, what’s missing, and the TCO benefits expected. 

### - Network virtual appliances (NVAs)
Third party networking offerings play a critical role in Azure, allowing you to use brands and solutions you already know, trust and have skills to manage. Most third-party networking offerings are delivered as NVAs today and provide a diverse set of capabilities such as firewalls, WAN optimizers, application delivery controllers, routers, load balancers, proxies, and more. These third party capabilities enable many hybrid solutions and are generally available through the Azure Marketplace. For best practices to consider before deploying a NVA, see Best practices to consider before deploying a network virtual appliance.

### - Cloud native network security
A cloud native network security service (known as firewall-as-a-service) is highly available by design. It auto scales with usage, and you pay as you use it. Support is included at some level, and it has a published and committed SLA. It fits into DevOps model for deployment and uses cloud native monitoring tools.

# Internet Protocol Security (IPSec)
In computing, Internet Protocol Security (IPsec) is a secure network protocol suite that authenticates and encrypts the packets of data to provide secure encrypted communication between two computers over an Internet Protocol network. It is used in virtual private networks (VPNs).

### Working of IPsec 
IPsec connections include the following steps:

- **Key exchange:**\
Keys are necessary for encryption; a key is a string of random characters that can be used to "lock" (encrypt) and "unlock" (decrypt) messages. IPsec sets up keys with a key exchange between the connected devices, so that each device can decrypt the other device's messages.

- **Packet headers and trailers:**\
All data that is sent over a network is broken down into smaller pieces called packets. Packets contain both a payload, or the actual data being sent, and headers, or information about that data so that computers receiving the packets know what to do with them. IPsec adds several headers to data packets containing authentication and encryption information. IPsec also adds trailers, which go after each packet's payload instead of before.

- **Authentication:**\
IPsec provides authentication for each packet, like a stamp of authenticity on a collectible item. This ensures that packets are from a trusted source and not an attacker.

- **Encryption:**\
IPsec encrypts the payloads within each packet and each packet's IP header (unless transport mode is used instead of tunnel mode — see below). This keeps data sent over IPsec secure and private.

- **Transmission:**\ 
Encrypted IPsec packets travel across one or more networks to their destination using a transport protocol. At this stage, IPsec traffic differs from regular IP traffic in that it most often uses UDP as its transport protocol, rather than TCP. TCP, the Transmission Control Protocol, sets up dedicated connections between devices and ensures that all packets arrive. UDP, the User Datagram Protocol, does not set up these dedicated connections. IPsec uses UDP because this allows IPsec packets to get through firewalls.

- **Decryption:**\
At the other end of the communication, the packets are decrypted, and applications (e.g. a browser) can now use the delivered data.

## IPsec impact on MSS and MTU?
**MSS** and **MTU** are two measurements of packet size. Packets can only reach a certain size (measured in bytes) before computers, routers, and switches cannot handle them. MSS measures the size of each packet's payload, while MTU measures the entire packet, including headers. Packets that exceed a network's MTU may be fragmented, meaning broken up into smaller packets and then reassembled. Packets that exceed the MSS are simply dropped.

IPsec protocols add several headers and trailers to packets, all of which take up several bytes. For networks that use IPsec, either the MSS and MTU have to be adjusted accordingly, or packets will be fragmented and slightly delayed. Usually, the MTU for a network is 1,500 bytes. A normal IP header is 20 bytes long, and a TCP header is also 20 bytes long, meaning each packet can contain 1,460 bytes of payload. However, IPsec adds an Authentication Header, an ESP header, and associated trailers. These add 50-60 bytes to a packet, or more.

## MTU setting on the IPSec Tunnels between the Aviatrix Gateways
All the IPSec tunnels have the TCP MSS set to 1370 bytes, by default, on Aviatrix gateway created in AWS, Azure and OCI. In GCP, the default value is 1350 bytes due to previous experience with some GCP applications. If you are running any applications which do not support fragmentation, you might have issues - please adjust the MTU on your end devices. Here are a couple examples of ssh failing due to MTU - ssh hangs due to MTU, music fails due to MTU

You can adjust the TCP MSS at “Aviatrix Console > Settings > Advanced > Tunnel > TCP MAXIMUM SEGMENT SIZE(MSS)” on the Aviatrix gateway.

Please note that it is recommended that you do not set the MTU to a value higher than 1370 bytes.

# Virtual Private Network (VPN)
A virtual private network (VPN) is an encrypted connection between two or more computers. VPN connections take place over public networks, but the data exchanged over the VPN is still private because it is encrypted.

VPNs make it possible to securely access and exchange confidential data over shared network infrastructure, such as the public Internet. For instance, when employees are working remotely instead of in the office, they often use VPNs to access corporate files and applications.

Many VPNs use the IPsec protocol suite to establish and run these encrypted connections. However, not all VPNs use IPsec. Another protocol for VPNs is SSL/TLS, which operates at a different layer in the OSI model than IPsec. (The OSI model is an abstract representation of the processes that make the Internet work.)

# Azure Express Route
Express route allows a private connection between the local network and the Microsoft cloud. Using express route organizations/users can connect to several Microsoft cloud services (cloud products e.g. Microsoft dynamics 365, Microsoft Azure and Office 365)

Connection to Microsoft services can be through the universal network or through point to point Ethernet connection via a network connectivity provider to the data center. Public internet cannot be used to establish a connection to the express route.

### Main benefits of express route
- Express route allows organizations to connect to Microsoft cloud services anywhere in the world
- Express route provides layer 3 connection between the Azure cloud and the local network
- Express route increases reliability due to the built-in redundancy
- Express route improves security and privacy by avoiding sensitive traffic going over the public internet
- Supports business Skype



# Author Profile:
- [LinkedIn: atuljkamble](https://www.linkedin.com/in/atuljkamble) 
- [Twitter: atul_kamble](https://www.twitter.com/atul_kamble)
- [Github: atulkamble](https://www.github.com/atulkamble)
- [Medium: atul_kamble](https://medium.com/@atul_kamble)
