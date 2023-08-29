#### What will i do 
- Download the Linux Kernel source code 
- Configure the development environment
- Compile the Kernel and boot it 

#### Download the Linux Kernel source code 
[Source code for Linux](https://kernel.org/)

When you compile Linux kernel the `.config` file is a super central thing. The Linux kernel has 11000 different options  and the config file stores all of selections for this options. 

At the start point while pulling Kernel source code there are no config file, it is because Linux don't tells You how to config your build. 

You can run `make config` to create config file but there will be 11000 configs to select manually. 

If You specify `make defconfig`  it will give You the default config structure for Kernel. 

The best option is to take the config file from Your distribution because it knows which drivers, progrms are available for You etc. 

> When building Kernel the compilation puts entire config file into Kernel as a string resource and You can just ask Kernel "Hey! Give me Your config file"
>
```bash
 zcat /proc/config
``` 
That is the configuration for Your Kernel. 

