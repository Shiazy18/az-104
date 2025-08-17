# Monitor and maintain Azure resources

`IP flow verify` allows you to test whether traffic is allowed to or from a virtual machine based on NSG (Network Security Group) rules. It specifically helps in identifying whether a particular port (like 33000) is blocked or allowed, which is essential for troubleshooting connectivity between VMs.

`Azure Monitor Network Insights`  gives you a high-level view of the health and topology of your network resources

`Azure Virtual Network Manager` because it's used for centralized network management and policy enforcement across VNets, not for diagnosing connectivity issues like blocked ports.

when a `peering connection is in a Disconnected state`, you must `delete the existing peering` first in order to modify the address space.

Alert rule can send:

- 12 text messages every hour
- 60 emails every hour

`Azure Backup` supports backing up individual disks using the Recovery Services vault. Managed disks can be backed up independently of the virtual machine to which they are attached. This allows for granular control over disk-level backups. It can backup `entire VM` also. Focus on the word entire.

## Azure Network Watcher

`Connection troubleshoot` is specifically designed to validate outbound connectivity from an Azure virtual machine (VM) to an external host. This feature checks the end-to-end connection and identifies if the connection succeeds or fails, providing insights into network latency, packet loss, and the point of failure.

`IP flow verify` checks whether a specific packet is allowed or denied by security rules, but it does not validate the entire outbound connection path.

`Next hop` shows the next hop a packet will take to reach its destination but does not validate the outbound connection itself.

`NSG flow logs` provides a record of traffic through network security groups (NSGs) but does not validate outbound connectivity.

`Traffic Analytics` analyzes traffic patterns and usage but does not validate specific outbound connections.