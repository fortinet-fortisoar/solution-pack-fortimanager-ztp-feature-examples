| [Home](../README.md) |
|----------------------|

# Setup FortiManager ZTP Flow - Feature Examples

Setting up the **FortiSOAR/FortiManager ZTP Flow (ZTPF)** integration depends a lot on how you want to use the solution pack. The general order of setup consists of the following tasks and will vary based on what objectives you are trying to accomplish:
  - Install the Latest [FortiManager ZTP Flow](https://fortisoar.contenthub.fortinet.com//list.html?contentType=all&searchContent=FortiManager%20ZTP%20Flow) Solution Pack from the FortiSOAR Content Hub. 
  - Create a Manager record with `RPC` credentials and make sure that API calls to your FMG are working by seeing the API system results fields are filled out. These field would include `firmware`, `Platform` and `SN` that come from the `Source Data` field in the Manager record. 
  - Checkout the [Usage Guide](./usage.md) for more information on using the feature tests. 

## Integration Examples

**Profile Summary Dashboard**
![](./res/ztpf-feature-example-dashboard.png)
**Device Details Dashboard**
![](./res/ztpf-feature-example-summary.png)