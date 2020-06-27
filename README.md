# k8s
Deploy K8s cluster usging vagrant

Note* You cannot remove NAT adapter from the Vagrant, cant help, but it will do your job
As required it is having 1 NAT, 1 Bridge Adapter ", 1 Private ( Total 3 Adapters)

Its simple to use this script, I have set to use "ubuntu/bionic64" Linux.

How to find Bridgde Adapter device name in windows:
You can find adapter details name from Windows box "Control Panel\Network and Internet\Network Connections" look for the device name there.

You can connect to the machines as below;
vagrant staus 
vagarnt ssh master
vagarnt ssh node2
vagarnt ssh node2

Try pining to systems once you connect to the any of the machine 
  ping node2.local




