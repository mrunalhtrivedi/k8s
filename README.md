# k8s
Deploy K8s cluster usging vagrant

Note* You cannot remove NAT adapter from the Vagrant, cant help, but it will do your job
As required it is having 1 NAT, 1 Bridge Adapter ", 1 Private ( Total 3 Adapters)

Its simple to use this script, I have set to use "ubuntu/bionic64" Linux.

How to find Bridgde Adapter device name in windows:

Method1 - In Windows command promt/Powershell/Git bash, use "route print" In first Interfaces section it will show all the devices names 
Method2 - "netsh int ipv4 show interfaces"
Method3 - use GUI

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

1. "Ubuntu 20.04 LTS (Focal Fossa)" -> ubuntu/focal64
2. "Ubuntu 19.10 (Eoan Ermine)" -> ubuntu/eoan64
3. "Ubuntu 18.04.4 LTS (Bionic Beaver)" -> ubuntu/bionic64
4. "Ubuntu 16.04.6 LTS (Xenial Xerus)" -> ubuntu/xenial64 
5. "Ubuntu 14.04.6 LTS (Trusty Tahr)" -> ubuntu/trusty64 
6. "Ubuntu 12.04.5 LTS (Precise Pangolin)" -> ubuntu/precise64
