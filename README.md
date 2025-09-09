# Azure Virtual Network with Additional Subnet

**Goal:** Create a virtual network with a default subnet and add an additional subnet for future workloads.  
**Skills Demonstrated:** Azure Networking, Subnetting, Resource Group Management.

---

## Steps (Milestones)

1. **Created Resource Group**
   - Name: 555 bcee5c6e-create-a-virtul-network
   - Region: East US

2. **Created Virtual Network**
   - Name: `vnet-demo`
   - Address space: `10.0.0.0/16`
   - Subnet: `default (10.0.0.0/24)`

3. **Added Additional Subnet**
   - Name: `Serversubnet`
   - Address space: `10.0.1.0/24`
   - Purpose: None (general workload subnet)

4. **Verified Configuration**
   - Checked VNet and subnet details in Azure portal
   - Confirmed correct IP ranges and configuration

---

## Lessons Learned

- Learned how to create a VNet and understand address space vs. subnet range.
- Practiced adding an additional subnet for network segmentation.
- Gained confidence using Azure Portal for network configuration.

---

## Next Steps

- Deploy a VM into the new subnet.
- Add an NSG to secure access.
- Repeat this setup using Azure CLI or Terraform for automation.
