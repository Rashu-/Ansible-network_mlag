# Ansible-network_mlag

Ansible role that configures mlag for networking devices. 

The configuration of the role is done so that it shouldn't be necessary to modify the role for any configuration.
All settings can be configured by changing role parameters or by declaring new config as variable.

Please report any issues or send PR.

nxos specific: 
channel-group number is made by removing 'port-channel' from the name attribute of the interface variable.
nxos_linkagg - lacp feature has to be enabled before using mode active/passive. If l2 mlag the interface should already be layer2 (switchport).
nxos_vpc_interface - vpc feature has to be enabled and vpc domain and peerlink configured. Port channel interface has to exist on the device. If vpc already configured on port channel you need to remove it first.
add these to virtual chassis readme as well.

## Examples

```yaml
---


  

```

## Role variables

```yaml
# Define the mlag interface details to be configured (see README for examples)
interfaces: { }

```


## License

Apache


## Author

Dan Murarasu
