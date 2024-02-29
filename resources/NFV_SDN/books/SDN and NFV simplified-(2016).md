# SDN and NFV Simplified - Jim Doherty

## Notes
- A hypervisor is an operating system of operating systems. A hypervisor is a VM monitor. It manages multiple VMs running on a physical machine. Page 26

- 2 types of hypervisor - Type 1 or bare metal (does not have OS), Type 2 (has OS). Xen is type 1, KVM is type 2. Page 28

- Hypervisor also works as a switch for the VMs

- In a virtualized environment (vituralized data center) resource pools (CPU pool, memory pool etc) are created from connected physical servers and VMs pull resources from these pools. Page 40

- To create virtualized environment (vituralized data center) VMs must have the abilities to move across the physical machines and also across networks. Chapter 6 is important. Page 59

- VM managers provide a unique MAC address for each VM created and also assign a virtual NIC (vNIC) or multiple vNICs (can also be done manually). The key point here is that it is the OS that is assigned an IP address, the VM is identified by its MAC, so when the VM migrates away from the physical host to
another location on the network, the IP address will remain the same rather than
changing each time the VM moves to a new physical host. If not for this, the
mobility of a VM would be restricted to a LAN segment, and consequently VMs would not be able to migrate across a Layer 3 network. (Confused... MAC to VM but IP to OS ??) Page 63

- physical location of VMs may
change mid-session (during VM migrations  - vMotion). Virtual data center design must account for this to ensure performance is not impacted. Page 69

- One of the big changes in data center networking is the emergence of virtualization-aware switches that allow for dynamic configuration of the switches in response to the creation, suspension, or movement of a VM. Page 70. Also check page 73.

- VTEPs are used on physical switches to bridge together virtual
network and physical network segments. Page 81

- **Server Virtualization:** Server virtualization is the abstraction of applications and operating systems
from physical servers. This allows for the creation of VMs (app and OS pairs) that offer much greater usage efficiency on physical servers and afford enormous flexibility with regard to provisioning of applications.
**Network Virtualization:** Network Virtualization refers to the creation of logical groupings of endpoints
on a network. In this case, the endpoints are abstracted from their physical locations so that VMs (and other assets) can look, behave, and be managed as if they are all on the same physical segment of the network.
**Network Functions Virtualization:** NFV refers to the virtualization of Layer 4 through 7 services such as load
balancing and firewalling. Basically, this is converting certain types of network appliances into VMs, which can then be quickly and easily deployed where they are needed. NFV came about because of the inefficiencies that were created by virtualization. 
**Software-Defined Networking:** SDN refers to the ability to program the network. SDN is a newer technology, one that was born as a result of virtualization and the shift of where the “chokepoint” is in data communications. In short, the ability to set up or make changes to a network cannot keep up with the ability to provision applications with a click of a button. SDN makes the network programmable. SDN is made possible by separating the control plane (the brains of the network) from the data plane (the muscle of the network).(Page 94)

- All four of the above technologies are designed to improve the mobility, agility, and flexibility of networks and data communication. However, virtualization network virtualization, and network functions virtualization can all work on existing networks because they reside on servers and interact with “groomed” traffic sent to them. SDN, however, requires a new network topology and SDN- aware devices where the data and control planes are separate and programmable. (page 95)

- Indeed, the most common reason
for virtualizing the network is precisely to get VM mobility and vMotion to
work.

## Research Ideas
- VM aware switching. Virtual Machine Migration/placement. Chapter 7 . Page 67

- service chaining... can routing rules be chained based on nature of traffics?

## Related papers
https://arxiv.org/pdf/2201.03999.pdf

https://par.nsf.gov/servlets/purl/10174516

https://www.researchgate.net/profile/Maanak-Gupta/publication/344372050_An_Attribute-Based_Access_Control_for_Cloud_Enabled_Industrial_Smart_Vehicles/links/5f6d402692851c14bc9492e9/An-Attribute-Based-Access-Control-for-Cloud-Enabled-Industrial-Smart-Vehicles.pdf

https://e-tarjome.com/storage/panel/fileuploads/2020-01-27/1580123093_E14222-e-tarjome.pdf


