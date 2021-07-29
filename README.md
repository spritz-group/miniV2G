
### About MiniV2G
MiniV2G is a fork of [Mininet-WiFi](https://travis-ci.org/intrig-unicamp/mininet-wifi/) which in turn is a fork of [Mininet](http://mininet.org/).
It offers the simulation of Vehicle-to-Grid (V2G) environment thanks to the integration with [RiseV2G](https://v2g-clarity.com/rise-v2g/). 

MiniV2G only add V2G features and you can work with it like you were working with Mininet/Mininet-WiFi.   


### Things to keep in mind when working with MiniV2G
* You can use examples/miniedit.py to create a simple topology with a graphical interface
* Alternatively, or to create more complex project, you can write a Python files taking as example examples/v2g-cli.py
* An example of a Man-in-the-Middle attack is provided by examples/v2g-mim.py
* Keep in mind any other recommendations of Mininet-WiFi and Mininet.

### Use Cases   
Please, let us know if you are doing research with MiniV2G.

## Installation 
The installation could be intricate. We recommend using our VM with MiniV2G preinstalled. You can download it using Vagrant:
```
vagrant init blackwiz4rd/ubuntu20.04-miniv2g
vagrant up
```
[vm-ubuntu20.04-miniv2g (2.8 GB)](https://app.vagrantup.com/blackwiz4rd/boxes/ubuntu20.04-miniv2g) _(password of the VM: vagrant)_


Otherwise, you can go for a standard installation as follows:

**We highly recommend using Ubuntu version 16.04 or higher. Some new hostapd features might not work on Ubuntu 14.04.**  
step 1: $ sudo apt-get install git  
step 2: $ git clone https://github.com/donadelden/miniV2G  
step 3: $ cd miniV2G  
step 4: $ sudo util/install.sh -WlnfvG

**If you update the source code use this command to install it:**

step n: $ sudo util/install.sh -Wn # e.g. if you update v2g.py install with this command
#### install.sh options:   
-W: wireless dependencies   
-n: mininet-wifi dependencies    
-f: OpenFlow   
-v: OpenvSwitch   
-l: wmediumd
-G: V2G features with MitM support  
_optional_:  
-P: P4 dependencies    
-6: wpan tools

### Building Topologies with GUI

![](https://github.com/donadelden/miniV2G/blob/master/doc/gui.png)

I'm a beginner, I do not know Python and I would like to create a customized topology. 
In this case [MiniEdit](https://github.com/donadelden/miniV2G/examples/miniedit.py) can serve as support since they provide a GUI to generate Python scripts. 

### RiseV2G configuration properties

You can take a look at all the properties available [in this file](doc/risev2g_properties.md).

### Development
For instructions about easier development check [this helper file](doc/dev_help.md), which contains the same informations of Mininet-WiFi.

   
## Note
For the WiFi part, MiniV2G should work fine in any Ubuntu distribution from 14.04, but in some cases (only if you have problems when start it) you have to stop _Network Manager_ with either `sudo systemctl stop network-manager` or `sudo service network-manager stop`.    

### Team
Luca Attanasio (loca_attanasio@me.com)  
Denis Donadel (denisdonadel@gmail.com)  
Federico Turrin (turrin@math.unipd.it)


We are members of [SPRITZ Security and Privacy Research Group](https://spritz.math.unipd.it/) at University of Padua, Italy.

