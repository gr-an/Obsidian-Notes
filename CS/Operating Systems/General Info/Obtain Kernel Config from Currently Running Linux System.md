
In a Linux System, a kernel config file is an important component of building the kernel. Using this file, we can modify our system configuration as per our requirement or check the currently configured devices

>In a Linux system, a kernel configuration file is used to build a kernel. It contains a list of kernel options, a list of devices, and device options. We can consider it a template that the _make_ command uses to build the kernel.

**As part of kernel building process, we can set up our config file** using different configuration options like `make config` or `make menuconfig`. Using these options, we can customize the kernel configuration and generate the files required to compile and link the kernel.

#### Obtaining Kernel Configuration
The method of obtaining the kernel configuration will vary depending on the Linux distribution. For most of the known Linux distributions, we can get the kernel configuration using one of two methods.

##### From the `/proc` Directory
In Linux the `/proc` (process information) pseudo-filesystem contains the files that represent the current state of the kernel.
To obtain the currently running kernel config from `/proc`, we can decompress the `config.gz`. **This is only possible if access to the `.config` file through `/proc/config.gz` was enabled** during generation of the initial configuration. This option comes under __General setup__ in kernel configuration 
```
General setup --->
 		...
 		[*] Kernel .config support
 			[*] Enable access to .config through /proc/config.gz
 		... 
```

Using [[zcat command]] , we can decompress the `config.gz` file with `.config` extension.
```bash
zcat /proc/config.gz > filename.config
```

Or we can use [[cat command]] and [[pipe]] it to  [[gunzip command]] 
```bash
cat /proc/config.gz | gunzio > filename.config
```