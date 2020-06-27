# k8s
Deploy K8s cluster usging vagrant (Windows only-)

Note* You cannot remove NAT adapter from the Vagrant, cant help, but it will do your job as required. Also Bridge is not required but it wil be good to have one which you could later use it.

Vagrantfile Network configuration details used;
1. 1 x NAT (Which is default)
2. 1 x Bridge Adapter 
3. 1 x Host-only private network 

Its simple to use this script, I have set to use "ubuntu/bionic64" Linux.

How to find Bridgde Adapter device name in MS Windows:

1. Method1 - "route print" 
2. Method2 - "netsh int ipv4 show interfaces"
3. Method3 - "Get-WMIObject Win32_networkadapter | Select-Object Name, AdapterType, InterfaceIndex | Format-List"
3. Method4 - or lastly use GUI

You can connect to the machines as below;
vagrant staus 
vagarnt ssh master
vagarnt ssh node2
vagarnt ssh node2

Try pining to systems once you connect to the any of the machine 
"ping node2.local"

To see all vagrant machines status at once
"vagrant global-status"


----------------------------

Offical Ubuntu version on which can be used in here, you can also find more release information on https://releases.ubuntu.com/

1. "ubuntu/focal64"   -> "Ubuntu 20.04 LTS (Focal Fossa)"
2. "ubuntu/eoan64"    -> "Ubuntu 19.10 (Eoan Ermine)" 
3. "ubuntu/bionic64"  -> "Ubuntu 18.04.4 LTS (Bionic Beaver)" 
4. "ubuntu/xenial64"  -> "Ubuntu 16.04.6 LTS (Xenial Xerus)" 
5. "ubuntu/trusty64"  -> "Ubuntu 14.04.6 LTS (Trusty Tahr)" 
6. "ubuntu/precise64" -> "Ubuntu 12.04.5 LTS (Precise Pangolin)" 
