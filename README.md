Azure Virtual Network with an Additional Subnet (Portal)
📖 Overview

I built an Azure Virtual Network (VNet) with a default subnet and added an additional subnet to prepare for future workloads. This exercise reinforced address planning, subnetting, and portal navigation.

Skills demonstrated: Azure Networking · VNet/Subnets · CIDR planning · Resource Groups

🔧 Settings I Used
Item	Value
Resource Group	555 bcee5c6e-create-a-virtul-network
Region	East US
VNet Name	vnet-demo
VNet Address Space	10.0.0.0/16
Subnet #1 (default)	10.0.0.0/24
Subnet #2 (Serversubnet)	10.0.1.0/24

You can substitute your own names/regions—these reflect what I actually used.

🗺️ Quick Topology
vnet-demo (10.0.0.0/16)
├─ default      (10.0.0.0/24)
└─ Serversubnet (10.0.1.0/24)

🚀 Step-by-Step (Azure Portal)
1) Create the Resource Group

Azure Portal → Resource groups → Create

Subscription: (your sub)

Resource group: 555 bcee5c6e-create-a-virtul-network

Region: East US

Review + create → Create

2) Create the Virtual Network

Create a resource → Networking → Virtual network

Resource group: 555 bcee5c6e-create-a-virtul-network

Name: vnet-demo · Region: East US

IP addresses tab → IPv4 address space: 10.0.0.0/16

Subnets → keep default at 10.0.0.0/24

Review + create → Create

3) Add the Additional Subnet

Open vnet-demo → Subnets → + Subnet

Subnet name: Serversubnet

Subnet address range: 10.0.1.0/24

Save

4) Verify the Configuration

In vnet-demo:

Address space shows 10.0.0.0/16

Subnets shows default (10.0.0.0/24) and Serversubnet (10.0.1.0/24)

(Optional) Deploy a test VM into Serversubnet to confirm IP assignment.

✅ Results

VNet created with a /16 address space for future growth.

One default /24 subnet plus a second Serversubnet /24 for workload separation.

Portal workflow validated end-to-end (RG → VNet → Subnets → Verify).

🧠 Lessons Learned

Difference between VNet address space and subnet ranges (aggregate vs. carved segments).

Why adding a second subnet helps with segmentation (e.g., app tiers, future NSGs/UDRs).

Faster, cleaner portal navigation for Azure networking tasks.
