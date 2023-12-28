| [Home](../README.md) |
|----------------------|

# Contents

The **FortiManager ZTP Flow - Feature Examples** solution pack contains the following resources.

## Record Sets

|**Name**|**Description**|
| :- | :- |
|  ZTP Profiles  |  ZTP Profile Records designed to assign to testing Models in FortiManager matching the name `FG0#` for each feature test and can often be auto-assigned. |
|  Metafield Templates  |  Metafield Template Records are used in ZTP Profiles to handle various Feature Examples.  |
|  Scripts  |  Records to run various scripts on devices in the Feature Examples. |
|  Attachments  | Example spreadsheets used in custom playbooks with metadata lookup examples are included in this pack. |

## Feature Tests (ZTP Profiles)

This solution pack provide various examples of ZTP Profiles that can be used to test some common features needed in building an automation solution. You can use the automatic assigning of these profiles by creating devices matching the names already put in the ZTP Profile `Assignment Search` or you can manually assign a profile to one or more devices to perform the feature test. 

| Feature Test ID | Profile Name | Description | 
| --------------- | ------- | ----------- |
| FT001 | Prompt User for Metadata via FortiSOAR | The metafield `loopback0_ip` is empty and FortiSOAR Users are prompted to complete through a system manual input task. |
| FT002 | Prompt User for Metadata and Monitor FG config before proceeding | The metafield `loopback0_ip` is empty and the metafield `lo0_exists` needs to be set to `yes` before the profile will complete. The `lo0` interface is checked using an API call to FMG to check `/global/system/interface` for the device on a `20 second` loop loop until seen. |
| FT003 | Metadata Source via Custom Playbook | Use two custom playbooks to populate the metafields `ip_table` and `ip_table_lookup`.  |
| FT004 | Monitor Metafield from FG config before proceeding | Performs the same steps as **FT001** but with a `60 second` loop. |
| FT005 | Assign Device to Multiple Device Groups | Simply assign a device to the device groups `FT005a`,`FT005b`,`FT005c`. The device groups are created in FMG if they do not exist. |
| FT006 | Assign Device to Groups from Device Metafield | Create the metafield `platform` and `device_groups`. The `device_groups` field dynamically contains one group based on the device model and one on the device series. |
| FT007 | Retrieve Device Config | Use a ZTP Phase to retrieve the config from a live device. This will cause an expected ZTP Phase error if run on a device model. |
| FT008 | Lookup Metadata in Spreadsheet from Hostname | Includes sample spreadsheets in the Attachment section of FortiSOAR. Use a custom playbook to search for `CSV` and `XLSX` files in the FortiSOAR Attachment records that are tagged as type `metadata`. Reach each file, in order of oldest to newest, and find and append metadata to the device record as found. |
| FT009 | Clone of **FT008** and is never assigned due to order priority. | To show `order priority` working this profile has the same `Assignment Search` regex as FT008 but will not match on the device names due to order. |
| FT010 | Install Site VLANs using DeviceDB Config | Create the metafield `site_id`, `site_subnet`, `vlan_cidr`, and `vlan_count`. The `site_subnet` is derived from taking a `/24` from `10.48.0.0/12` using the `site_subnet`. |
| FT011 | Install Site VLANs using DeviceDB Config and Run Interface Report | Performs the same steps as **FT010** but then runs the same `Markdown Report` linked in **FT013**. |
| FT012 | Install Site VLANs using DeviceDB Config and set ZTP Profile Next to Run a Report | Performs the same steps as **FT010** but then sets the `ZTP Profile Next` to the ZTP Profile `FT013 - Run Device Interface Report` to chain a second profile with **FT013**.  |
| FT013 | Run Device Interface Report | Call the API of FMG for the device interfaces using a `Markdown Report` script template and append the device `Report Markdown` field for reporting. |

| [Installation](./docs/setup.md) | [Usage](./docs/usage.md) |
|---------------------------------|--------------------------|