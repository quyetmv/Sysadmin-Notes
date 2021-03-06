#Installation#
Open the Server Manager and install the DHCP role.

We will make the following assumptions for these docs:

 - DNS Domain: mydomain.com
 - DNS Server: 192.168.0.7
 - DHCP Scope Name: Workstations
 - DHCP Scope Range: 192.168.0.100 - 192.168.0.254
 - Subnet: /24
 - Gateway: 192.168.0.1

WINS is an antiquated technology and should not be enabled. The installer will require you to setup at least one dhcp scope. Plugin the above information.

You can now open the DHCP management tool to perform further configuration of your DHCP scopes. If you are running this DHCP server in an Active Directory environment, you will need to authorize this DHCP server else domain member computers will now allow themselves to obtain IPs from this new server. To do this, on a domain controller, open the DHCP management tool and right click on the up-most DHCP node entry, click on Manage Authorized Servers. Add the new server and click Authorize.