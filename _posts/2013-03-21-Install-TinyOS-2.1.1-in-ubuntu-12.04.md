---
layout : post
title : Install TinyOS 2.1.1 in ubuntu 12.04
category : TinyOS 
tags : TinyOS
---

TinyOS is a open source operating system for low power wireless device used in sensor networks,person area network, smart meters etc. You can find more information about tinyos from here

The following configurations are done for tiny os  2.1.1 for micaz mote

###Open /etc/apt/sources.list and add the following line at the end of file.
    
    deb http://tinyos.stanford.edu/tinyos/dists/ubuntu karmic main 
###Update apt-get and install tinyos
    
    sudo apt-get update
    
    sudo apt-get install tinyos-2.1.1

###Change the ownership of tinyos root directory to your user
    sudo chown <yourusername>:<yourusername> -R /opt/tinyos-2.1.1/ </yourusername></yourusername>
###Edit .bashrc in user home and add the following lines at the end
    export TOSDIR=$TOSROOT/tos  
    export CLASSPATH=$TOSROOT/support/sdk/java/tinyos.jar:.$CLASSPATH  

    export MAKERULES=$TOSROOT/support/make/Makerules  

    export PATH=/opt/msp430/bin:$PATH  

    source /opt/tinyos-2.1.1/tinyos.sh  
###Install the java tools using
    sudo tos-install-jni
###Install Java docs 
Go to /opt/tinyos-2.1.1/support/sdk/java 

    make   
   
    make install   
   
    make javadoc   
###Common Errors
####Unexpected operator during tos-jni-install command
####Error
    sudo tos-install-jni   
    [: 31: =: unexpected operator   
  
    Installing 32-bit Java JNI code in /usr/lib/jvm/java-1.5.0-sun/jre/lib/i386 …  
  
    done.  
####Solution
Edit /usr/bin/tos-install-jni and change 1st line from “#!/bin/sh” to “#!/bin/bash”





