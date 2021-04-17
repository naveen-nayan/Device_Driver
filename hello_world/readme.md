## First module hello_world

### Install Raspberrypi Kernel Header
Use below command to install kernel header for raspberrypi

`sudo apt install raspberrypi-kernel-headers`
	 
### Compile the Driver

   Use below command to compile the Driver in working directory
   
   `sudo make`

| ![Driver compiled output](https://github.com/naveen-nayan/Device_Driver/blob/main/hello_world/make%20command.PNG) |
|:--:|
| *Compiled driver output* |


 ### Load The Device Driver and view loaded module
 
   Use below command to lad the module in kernel
    
   `sudo insmod hello_world_module.ko`

| ![View loaded module](https://raw.githubusercontent.com/naveen-nayan/Device_Driver/main/hello_world/lsmod.PNG) |
|:--:|
| *View loaded module using `lsmod`* |

### View Module output

  We can use `dmseg` or see `/var/log/syslog` to see msg output
  
  Here i am using `tail -n 3 /var/log/syslog` to see last three line output
  
| ![View module output](https://raw.githubusercontent.com/naveen-nayan/Device_Driver/main/hello_world/syslog.PNG) |
|:--:|
| *module output in syslog due to init macro from hello_world module* | 


### View Module Details

  We can see module details using `modinfo hello_world.ko`
  
| ![View module Details](https://raw.githubusercontent.com/naveen-nayan/Device_Driver/main/hello_world/module%20info.PNG) |
|:--:|
| *module Details* |



### Unload Module

  To unload the modulefrom kernal we can use `sudo rmmod hello_world.ko` or `sudo rmmod hello_world`
  
  Here i am using `tail -n 4 /var/log/syslog` to see last four line output
  
| ![Unload module Details](https://raw.githubusercontent.com/naveen-nayan/Device_Driver/main/hello_world/syslog2.PNG) |
|:--:|
| *module output in syslog due to exit macro from hello_world module* |
