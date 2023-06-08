## auto.tfvars syntax for SDDC Module
These are the syntax and sample format for providing inputs to the modules via <b>*.auto.tfvars</b> files.
<b>"key"</b> must be unique to every resource that is created.Comments preceed with <b>##</b>.

## SDDC

- **Syntax**



- **Example**

```
// Copyright (c) 2021, 2022, Oracle and/or its affiliates.
############################
# SDDCs
# SDDC - tfvars
# Allowed Values:
# vcn_name must be the name of the VCN as in OCI
# vlan_name must be the name of the vlan as in OCI
# subnet_id can be the ocid of the subnet or the name as in OCI
# compartment_id and network_compartment_id can be the ocid or the name of the compartment hierarchy delimited by double hiphens "--"
# Example : compartment_id = "ocid1.compartment.oc1..aaaaaaaahwwiefb56epvdlzfic6ah6jy3xf3c" or compartment_id = "AppDev--Prod" where "AppDev" is the parent of "Prod" compartment
# Sample import command for SDDC:
# terraform import "module.sddc[\"<<sddc terraform variable name>>\"].oci_ocvp_sddc.sddc" <<sddc ocid>>
############################
sddcs = {
      sddc-std22 =  {
          compartment_id                = "AppDev"
          display_name                  = "sddc-std22"
          availability_domain           =  0
          is_hcx_enabled                = "true"
          vmware_software_version       = "7.0 update 3"
          initial_sku                   = "HOUR"
          initial_host_shape_name       = "BM.Standard.E4.128"
          initial_host_ocpu_count       = "32"
          esxi_hosts_count              = 3
          instance_display_name_prefix  = "sddc-std2"
          is_shielded_instance_enabled  = "false"
          ssh_authorized_keys           = "sddc-std2"
          network_compartment_id        = "Network"
          vcn_name                      = "vcn-sddc"
          provisioning_subnet_id        = "Subnet-sddc"
          nsx_edge_uplink1vlan_id       = "VLAN-sddc-std2-NSX Edge Uplink 1"
          nsx_edge_uplink2vlan_id       = "VLAN-sddc-std2-NSX Edge Uplink 2"
          nsx_edge_vtep_vlan_id         = "VLAN-sddc-std2-NSX Edge VTEP"
          nsx_vtep_vlan_id              = "VLAN-sddc-std2-NSX VTEP"
          vmotion_vlan_id               = "VLAN-sddc-std2-vMotion"
          vsan_vlan_id                  = "VLAN-sddc-std2-vSAN"
          vsphere_vlan_id               = "VLAN-sddc-std2-vSphere"
          hcx_vlan_id                   = "VLAN-sddc-std2-HCX"
          replication_vlan_id           = "VLAN-sddc-std2-Replication Net"
          provisioning_vlan_id          = "VLAN-sddc-std2-Provisioning Net"
          workload_network_cidr         = ""
            defined_tags = {
                    "Oracle-Tags.CreatedOn"= "2023-06-05T16:57:49.375Z" ,
                    "Oracle-Tags.CreatedBy"= "oracleidentitycloudservice/abc@oracle.com" ,
                    "Tracking.Creator"= "oracleidentitycloudservice/abc@oracle.com" ,
                    "Tracking.Created_time"= "2023-06-05T16:57:49.375Z" ,
                    "AAA.Env"= "Prod"
            }
    },
   sddc-std1 =  {
          compartment_id                = "AppDev"
          display_name                  = "sddc-std1"
          availability_domain           =  0
          is_hcx_enabled                = "true"
          vmware_software_version       = "7.0 update 3"
          initial_sku                   = "HOUR"
          initial_host_shape_name       = "BM.Standard.E4.128"
          initial_host_ocpu_count       = "32"
          esxi_hosts_count              = 3
          instance_display_name_prefix  = "sddc-std"
          is_shielded_instance_enabled  = "false"
          ssh_authorized_keys           = "sddc-std1"
          network_compartment_id        = "Network"
          vcn_name                      = "vcn-sddc"
          provisioning_subnet_id        = "Subnet-sddc"
          nsx_edge_uplink1vlan_id       = "VLAN-sddc-std-NSX Edge Uplink 1"
          nsx_edge_uplink2vlan_id       = "VLAN-sddc-std-NSX Edge Uplink 2"
          nsx_edge_vtep_vlan_id         = "VLAN-sddc-std-NSX Edge VTEP"
          nsx_vtep_vlan_id              = "VLAN-sddc-std-NSX VTEP"
          vmotion_vlan_id               = "VLAN-sddc-std-vMotion"
          vsan_vlan_id                  = "VLAN-sddc-std-vSAN"
          vsphere_vlan_id               = "VLAN-sddc-std-vSphere"
          hcx_vlan_id                   = "VLAN-sddc-std-HCX"
          replication_vlan_id           = "VLAN-sddc-std-Replication Net"
          provisioning_vlan_id          = "VLAN-sddc-std-Provisioning Net"
          workload_network_cidr         = "172.16.0.0/24"
            defined_tags = {
                    "Oracle-Tags.CreatedOn"= "2023-06-05T11:00:51.077Z" ,
                    "Oracle-Tags.CreatedBy"= "oracleidentitycloudservice/abc@oracle.com" ,
                    "Tracking.Creator"= "oracleidentitycloudservice/abc@oracle.com" ,
                    "Tracking.Created_time"= "2023-06-05T11:00:51.077Z"
            }
    },

}
```