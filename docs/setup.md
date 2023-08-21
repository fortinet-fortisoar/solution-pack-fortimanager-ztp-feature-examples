| [Home](../README.md) |
|--------------------------------------------|

# Setup FortiManager ZTP Flow - Feature Examples

Setting up the **FortiSOAR/FortiManager ZTP Flow (ZTPF)** integration depends a lot on how you want to use the solution pack. The general order of setup consists of the following tasks and will vary based on what objectives you are trying to accomplish:
  - Install the [FortiManager ZTP Flow (ZTPF) Framework](https://github.com/fortinet-fortisoar/solution-pack-fortimanager-ztp-framework/blob/release/1.0.0/README.md) Solution Pack
  - Select your FortiManager Manager record in FortiSOAR.
    - Execute `Device Model - Create Randomly`.
    ![](./docs/res/execute-create-device-models-randomly.png)
    - Enter `101-108` to create `FG00101-FG00108` device models in FortiManager to test the first 8 ZTP Profiles. 
    ![](./docs/res/execute-create-device-models-randomly-input.png)

  - Navigate to the Dashboard `ZTP Profile and Phase for Devices` and inspect the ZTP Profiles in action.
**Profile Summary Dashboard**
![](./docs/res/ztpf-feature-example-dashboard.png)
**Device Details Dashboard**
![](./docs/res/ztpf-feature-example-summary.png)

| [Contents](./contents.md) |
|---------------------------|