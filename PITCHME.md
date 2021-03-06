---?image=assets/images/gitpitch-audience.jpg
@title[Platform Build Lab]
<br><br><br><br><br>
## <span class="gold"   >UEFI & EDK II Training</span>

#### UEFI Aware Operating System 

<br>
<span style="font-size:0.75em" ><a href='http://www.tianocore.org'>tianocore.org</a></span>
Note:
  PITCHME.md for UEFI / EDK II Training  UEFI Aware OS

  Copyright (c) 2020, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.



---  
@title[Lesson Objective]
<BR>
### <p align="center"<span class="gold"   >Lesson Objective </span></p><br>

<!---  Add bullets using https://fontawesome.com/cheatsheet certificate
-->
<br>
 @fa[certificate gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Explain How the OS and UEFI Work together </span><br>
 @fa[certificate gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Explain the UEFI Requirements for UEFI aware OS</span><br>
 @fa[certificate gp-bullet-yellow]<span style="font-size:0.9em">&nbsp;&nbsp;Explain How Secure Boot Fits with UEFI</span> <br>
 @fa[certificate gp-bullet-magenta]<span style="font-size:0.9em">&nbsp;&nbsp;What about coreboot?</span> 


---?image=assets/images/binary-strings-black2.jpg
@title[UEFI Aware OS Requirements Section]
<br><br><br><br><br>
### <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;UEFI Aware OS Requirements</span>
<span style="font-size:0.9em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Common Requirements</span>
 
---?image=/assets/images/slides/Slide4.JPG
@title[UEFI Operating Systems]
### <p align="right"><span class="gold" >UEFI Operating Systems</span></p>

Note:
Many OS already use UEFI to boot from and use UEFI Runtime Services



---?image=/assets/images/slides/Slide6.JPG
<!-- .slide: data-transition="none" -->		 
@title[UEFI Boot Flow review]
<p align="right"><span class="gold" ><b> UEFI - PI & EDK II Boot Flow </b></span><span style="color:white;">&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;<b>Review</b> </span></p>

Note:
SEC Function <Br>

Review -Boot Execution Flow

+++?image=/assets/images/slides/Slide7.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Boot Flow review 02]
<p align="right"><span class="gold" ><b> UEFI - PI & EDK II Boot Flow </b></span><span style="color:white;">&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;<b>Review</b> </span></p>
 
Note:
Review -Boot Execution Flow
 

+++?image=/assets/images/slides/Slide8.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Boot Flow review 03]
<p align="right"><span class="gold" ><b> UEFI - PI & EDK II Boot Flow </b></span><span style="color:white;">&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;<b>Review</b> </span></p>
 
Note:
Review -Boot Execution Flow
 

+++?image=/assets/images/slides/Slide9.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Boot Flow review 04]
<p align="right"><span class="gold" ><b> UEFI - PI & EDK II Boot Flow </b></span><span style="color:white;">&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;<b>Review</b> </span></p>
 
Note:
Review -Boot Execution Flow

Boot to OS with UEFI Services available


---
@title[UEFI OS Requirements]
#### <p align="right"><span class="gold" >UEFI OS Requirements</span></p>
 
@snap[north-west span-35 fragment]
@css[text-yellow](<br><br>&nbsp; <br>&nbsp;)
@box[bg-lt-blue-pp text-white  waved  ](<b>UEFI Drivers:</b> Boot devices/console<br>&nbsp;)
@snapend

@snap[north span-35 fragment]
@css[text-yellow](<br> <br>&nbsp;<br>&nbsp;)
@box[bg-royal text-white waved ](<b>UEFI OS Installer</b><br><br>&nbsp;)
@snapend
  
@snap[north-east span-35 fragment]
@css[text-yellow](<br><br>&nbsp; <br>&nbsp;)
@box[bg-green-pp text-white waved ](<b>UEFI OS Loader</b><br><br>&nbsp;)
@snapend
 
@snap[south-west span-35 fragment]
@box[bg-yellow text-blue  waved ](<b>Disk Partition/formats</b><br>&nbsp;)
@css[text-yellow]( <br>&nbsp;)
@snapend
  
@snap[south span-35 fragment]
@box[bg-brick text-white waved ](<b>Firmware Requirements</b><br><br>)
@css[text-yellow]( <br>&nbsp;)
@snapend
 
@snap[south-east span-35 fragment]
@box[bg-purple-pp text-white waved ](<b>Set Boot Path to Boot UEFI OS</b><br>&nbsp;)
@css[text-yellow]( <br>&nbsp;)
@snapend
  
 
  
Note:
- What is the list of things you need to have in the BIOS/ FW?
- UEFI drivers for boot devices and console – storage devices / 
- UEFI loader need / Elilo for Linux - / RH published need to be there
  - For windows 
  - Transfers con
- UEFI installer –  - Requirements WIN has this so far
- Disk partition and Disk formats - need GPT  / FAT32 disk format
- Firmware requirements
- Boot manager
- BIOS Setup
- Nvram Large enough to store device path

- After installation, set boot path to boot to OS as default system behavior
 

---
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes ]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436"><b>UEFI System Classes&nbsp;&nbsp;</b></span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>

@snap[north-west span-45 fragment]
@css[text-yellow](<br>&nbsp; <br>&nbsp;)
@box[bg-brick text-white    ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>UEFI Class 0</b></span><span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;Boots Legacy - int 19 ONLY<br>&nbsp;&nbsp;&nbsp;&nbsp;Legacy BIOS &lpar;16 bit&rpar;<br>&nbsp;&nbsp;&nbsp;&nbsp;No UEFI Interfaces<br>&nbsp;</span></p>)
@snapend

@snap[north-east span-45 fragment]
@css[text-yellow](<br>&nbsp; <br>&nbsp;)
@box[bg-green-pp text-white  ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>UEFI Class 1</b></span><span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;Boots Legacy - int 19 ONLY<br>&nbsp;&nbsp;&nbsp;&nbsp;Uses UEFI / PI Interfaces <br>&nbsp;&nbsp;&nbsp;&nbsp;Only legacy BIOS <b>runtime</b> inteface<br>&nbsp;</span></p>)
@snapend

@snap[south-west span-45 fragment]
@box[bg-purple-pp text-white   ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>UEFI Class 2</b></span><span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;Boots Legacy - int 19 or UEFI<br>&nbsp;&nbsp;&nbsp;&nbsp;Uses UEFI / PI Interfaces <br>&nbsp;&nbsp;&nbsp;&nbsp;legacy BIOS runtime inteface w/ <b>CSM</b><br>&nbsp;</span></p>)
@css[text-yellow]( &nbsp;)
@snapend

@snap[south-east span-55 fragment]
@box[bg-grey-50 text-black](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;<b>Limited Benefits</b></span><span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;<b>&check;</b>&nbsp;&nbsp;OEMs/ODMs Internal <br>&nbsp;&nbsp;&nbsp;&nbsp;<b>&check;</b>&nbsp;&nbsp;Double code development <br>&nbsp;&nbsp;&nbsp;&nbsp;<b>&check;</b>&nbsp;&nbsp;Coompromised security <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - MBR exposure<br>&nbsp;</span></p>)
@css[text-yellow]( &nbsp;)
@snapend


+++
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes 02]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436"><b>UEFI System Classes&nbsp;&nbsp;</b></span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>


@snap[north-west span-45 ]
@css[text-yellow](<br>&nbsp; <br>&nbsp;)
@box[bg-brick text-white    ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>UEFI Class 0</b></span><span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;Boots Legacy - int 19 ONLY<br>&nbsp;&nbsp;&nbsp;&nbsp;Legacy BIOS &lpar;16 bit&rpar;<br>&nbsp;&nbsp;&nbsp;&nbsp;No UEFI Interfaces<br>&nbsp;</span></p>)
@snapend

@snap[north-east span-45 ]
@css[text-yellow](<br>&nbsp; <br>&nbsp;)
@box[bg-green-pp text-white  ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>UEFI Class 1</b></span><span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;Boots Legacy - int 19 ONLY<br>&nbsp;&nbsp;&nbsp;&nbsp;Uses UEFI / PI Interfaces <br>&nbsp;&nbsp;&nbsp;&nbsp;Only legacy BIOS <b>runtime</b> inteface<br>&nbsp;</span></p>)
@snapend

@snap[south-west span-45 ]
@box[bg-purple-pp text-white   ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>UEFI Class 2</b></span><span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;Boots Legacy - int 19 or UEFI<br>&nbsp;&nbsp;&nbsp;&nbsp;Uses UEFI / PI Interfaces <br>&nbsp;&nbsp;&nbsp;&nbsp;legacy BIOS runtime inteface w/ <b>CSM</b><br>&nbsp;</span></p>)
@css[text-yellow]( &nbsp;)
@snapend


@snap[south-east span-45 ]
@box[bg-royal text-white   ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>UEFI Class 3</b></span><span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;Boots <b>Only</b> UEFI<br>&nbsp;&nbsp;&nbsp;&nbsp;Uses UEFI / PI Interfaces <br>&nbsp;&nbsp;&nbsp;&nbsp;Only runtime UEFI intefaces<br>&nbsp;</span></p>)
@css[text-yellow]( &nbsp;)
@snapend

+++
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI System Classes 02]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436"><b>UEFI System Classes&nbsp;&nbsp;</b></span><span style="font-size:0.6em" ><font color="#FFC000">(based on firmware interfaces)<font></span></p>


@snap[north-west span-45 ]
@css[text-yellow](<br>&nbsp; <br>&nbsp;)
@box[bg-grey-50 text-white    ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;@color[yellow](<b>Full Benefits</b>)</span><span style="font-size:0.7em" ><br><br>&nbsp;&nbsp;&nbsp;&nbsp;<b>&check;</b>&nbsp;&nbsp;UEFI Innovation<br>&nbsp;&nbsp;&nbsp;&nbsp;<b>&check;</b>&nbsp;&nbsp;Smaller code size / Validation<br>&nbsp;&nbsp;&nbsp;&nbsp;<b>&check;</b>&nbsp;&nbsp;Extensiblitiy<br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend

@snap[north-east span-45 ]
@css[text-yellow](<br>&nbsp; <br>&nbsp;)
@box[bg-royal text-white   ](<p align="left" style="line-height:60%"><span style="font-size:01.25em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>UEFI Class 3</b></span><span style="font-size:0.7em" ><br><br>&nbsp;&nbsp;&nbsp;&nbsp;Boots <b>Only</b> UEFI<br>&nbsp;&nbsp;&nbsp;&nbsp;Uses UEFI / PI Interfaces <br>&nbsp;&nbsp;&nbsp;&nbsp;Only runtime UEFI intefaces<br><br><br><br><br><br><br><br>&nbsp;</span></p>)
@snapend



@snap[south-west span-45 fragment]
<p align="left" style="line-height:60%">&nbsp;&nbsp;@color[yellow](<b>Only Class after 2020</b>)<span style="font-size:0.6em" ><br>&nbsp;&nbsp;&nbsp;&nbsp;@color[white](Enabling <b>Secure Boot</b> creates <br>&nbsp;&nbsp;&nbsp;&nbsp;another class&nbsp;)</span></p>
<br><br>&nbsp;
@snapend


@snap[north-east span-50 fragment]
<br>
<br>
<br>
<br>
<span style="font-size:02.25em" >@color[#ff00ff](<b>+</b>)&nbsp;&nbsp;</span>
<br>
<br>
<br>
<br>
<p align="left" style="line-height:60%"><span style="font-size:02.0em" >@color[#ff00ff](&#10132;)</span><span style="font-size:0.8em" >&nbsp;&nbsp;&nbsp;@color[white](<b>UEFI Secure Boot "ON"</b> )<br></span> </p>
@snapend


Note:
Make sure the “class” terminology is understood here before moving on

### Classes 0-2:
- Limited Benefits
- OEMs/ODMs Internal
- Development Optimization
  -  & Code Organization

### Class 3+
- Full Benefits
- UEFI Innovation
- Performance
- Extensibility


---
@title[Required UEFI Drivers: OS Install & Boot]
<p align="right"><span style="font-size:01.2em" ><font color="#e49436"><b>Required UEFI Drivers:&nbsp;&nbsp;</b></span><span style="font-size:0.8em" ><font color="#FFC000">OS Install & Boot<font></span></p>


@snap[north-west span-45 fragment]
@css[text-yellow]( <br>&nbsp;)
@box[bg-royal text-white  rounded  ](<span style="font-size:01.52em" ><b>Boot device<b></span><br>&nbsp;)
@snapend

@snap[north-east span-45 fragment]
@css[text-yellow](<br><br>&nbsp; <br>&nbsp;<br>&nbsp;)
@box[bg-green-pp text-white rounded ](<span style="font-size:01.52em" ><b>Console Output</b></span><br>&nbsp;)
@snapend

@snap[south-west span-45 fragment]
@box[bg-brick text-white  rounded ](<span style="font-size:01.52em" ><b>Console Input</b></span><br>&nbsp;)
@css[text-yellow]( <br>&nbsp;<br>&nbsp;<br>&nbsp;)
@snapend

@snap[south-east span-45 fragment]
@box[bg-purple-pp text-white rounded ](<span style="font-size:01.52em" ><b>NVRam Driver</b></span><br>&nbsp;)

@snapend



Note:
- Boot Device: hard drive controller, USB, RAID, Fiber Channel, network, etc. 
- Console Output: Graphics Output Protocol (GOP) or Serial Console (COM port)
- Console Input: Keyboard, Mouse, Touch Screen or Serial Console (COM)
- NVRAM Driver – store boot entry for OS in flash or other NVRAM (not part of boot disk partition)


---
@title[UEFI OS Loader/Installer]
#### <p align="right"><span class="gold" >UEFI OS Loader</span></p>

@snap[north-west span-100 fragment]
<br>
<br>
@fa[circle gp-bullet-magenta]<span style="font-size:0.9em">&nbsp;&nbsp;OS install process includes UEFI loader<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span style="font-size:0.7em"><font  color="#FFFF00">`/efi/boot/bootx64.efi`&nbsp;&nbsp; &nbsp;&nbsp; `/efi/redhat/grub.efi`</font></span><br>
@fa[circle gp-bullet-gold]<span style="font-size:0.9em">&nbsp;&nbsp;Call UEFI boot & runtime services to start OS</span> <br>
@fa[circle gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Exit UEFI Boot Services</span><br>
@fa[circle gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Transfer control to native OS</span><br>

@snap[east span-60 fragment]
<br>
#### <p align="right"><span class="gold" >UEFI OS Installer</span></p>
@snapend

@snap[west span-100 fragment]
@css[text-yellow]( <br>&nbsp;<br><br><br><br><br>)
@fa[circle gp-bullet-magenta]<span style="font-size:0.9em">&nbsp;&nbsp;Discover UEFI storage devices</span> <br>
@fa[circle gp-bullet-gold]<span style="font-size:0.9em">&nbsp;&nbsp;Setup storage device: GPT w/ FAT32 boot partition</span> <br>
@fa[circle gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Create boot variable &nbsp;&nbsp;<font color="#FFFF00">`BootXXXX`</font></span><br>
@snapend

Note:

#### WHICH DRIVERS?

All UEFI OS’s require that firmware contain UEFI drivers for Boot devices and console 
– mass storage device – or LAN Stack for PXE
– Boot devices: hard drive controller, usb, raid, fiber channel etc. 
– Console : GOP or UGA, keyboard (ps2 or usb), mouse (usb) or serial port (some way to control the system on install) 
- alter the boot opt for the loader
– 	Some way of interacting with user during OS installation and a boot device to store the OS
    – NVRAM driver – boot entry for OS must be stored in flash or some other nonvolatile device that is not part of the OS disk storage – Device path where the boot device is located is stored in NVRAM.
  
– Firmware must contain UEFI drivers for boot devices (OS storage) and console (user interaction)



#### As seen on the SLIDES:
– OS install process will install a UEFI loader (.efi)
– Example: /efi/boot/bootx64.efi, /efi/redhat/grub.efi
– UEFI loader will …
– Call UEFI boot & runtime services to start the OS
– Exit UEFI boot services (OS uses runtime services)
– Transfer control to native OS
– UEFI OS installer must …
– Discover UEFI storage devices
– Setup storage device (GPT w/ FAT32 boot partition)
– Install UEFI loader & create boot variable (BootXXXX)

---?image=/assets/images/slides/Slide33.JPG
@title[Disk Partition and Format]
<p align="right"><span class="gold" ><b>Disk Partition and Format</b></span></p>


Note:

- UEFI OS requires GPT partitioned disks
- One partition must be formatted FAT32
- “Service partition” for the OS boot loader
- Under /EFI/BOOT or /EFI/osname directory
- Boot0000 entry points to OS loader (.efi)


- Disk partition and Format
- UEFI requires disks be partitioned GPT – May need to wipe the drive to re-partition for GPT
On one of the partitions there must be one formatted FAT.
On the Fat partition under /EFI/boot/* the UEFI os loader must be installed.
Os loader needs to be here

- Question – boot to EFI shell with default – x64 – EFI Shell is not part of the UEFI spec but can be loaded separately. The UEFI Spec section 3 has Boot manager section. A UEFI OS will have a EFI appl that will be the OS loader.

- Can have mult partition for multi-boots on the disk – example – one for windows – one for Linux

-    Windows may have issues with EXT partitions – so there maybe some order of install – 
- Boot manager required in UEFI spec – 1st boot option could be boot to Windows Boot Manager on Windows hard disk 

- There can be mult boot option

---?image=assets/images/binary-strings-black2.jpg
@title[Interface Inside OS Runtime Section]
<br><br><br><br><br>
### <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Interface Inside OS Runtime</span>
<span style="font-size:0.9em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;UEFI Runtime Services</span>


---?image=/assets/images/slides/Slide35_1.JPG
@title[Runtime Services Table ]
<p style="line-height:80%" align="right"><span class="gold" ><b>Runtime Services Available to the<br>UEFI Aware OS</b></span></p>


Note:

As seen on this slide , Only Runtime services are available during the UEFI aware OS.  

Boot services are no longer available after the OS Loader calls ExitBootServices().

It is the responsibility of the OS Loader to call ExitBootServices() event.  
---

@title[Accessing RT Services from Windows ]
<br>
#### <p align="right"><span class="gold" >@fa[windows gp-bullet-cyan ] &nbsp;&nbsp; Accessing RT services from Windows API</span></p>

- <span style="font-size:0.8em" >GetFirmwareEnvironmentVariable: <a href="http://msdn.microsoft.com/en-us/library/windows/desktop/ms724325(v=vs.85).aspx">MSDN Link</a></span>
- <span style="font-size:0.8em" >SetFirmwareEnvironmentVariable: <a href="http://msdn.microsoft.com/en-us/library/windows/desktop/ms724934(v=vs.85).aspx">MSDN Link</a></span>
- <span style="font-size:0.8em" >Example: (determine if UEFI or Legacy BIOS)</span>

```C
 int main(int argc, char*argv[])
{
        GetFirmwareEnvironmentVariableA("",
           "{00000000-0000-0000-0000-000000000000}",NULL,0);
        if (GetLastError() ==ERROR_INVALID_FUNCTION) { 
              printf("Legacy"); // This.. is.. LEGACY BIOS....
              return 1;
        } else{
              printf("UEFI"); // This.. is.. UEFI
              return 0;
        }
        return 0;
}
```


Note:

- Code example:

This is just a code example of an application written for Windows

The links will help to find more actual examples

<pre>

 #include <windows.h>
 #include <tchar.h>
 #include <stdio.h>


 int _tmain(int argc, _TCHAR* argv[])
 {
      DWORD dwRet = 0;

     if(GetFirmwareEnvironmentVariable(
          _T(""), 
          _T("{00000000-0000-0000-0000-000000000000}"), 
          NULL ,
          0)  == 0)
    {
         if(GetLastError() == ERROR_INVALID_FUNCTION)
        {
             printf("Windows was installed using legacy BIOS\n");
        }
        else
        {
              DWORD dwTimeout = 0;
              printf("ErrCode = %ld\n",GetLastError());
              //Here errcode is 998
              printf("Windows was installed using UEFI BIOS\n");

              dwRet = GetFirmwareEnvironmentVariable(
                    _T("Timeout"), 
                   _T("{8BE4DF61-93CA-11d2-AA0D-                                00E098032B8C}"), 
                   &dwTimeout ,
                   sizeof(DWORD));
            if(dwRet)
            {
                    printf("dwTimeout = %ld\n",dwTimeout);
            }
            else
            {
                 printf("ErrCode = %ld\n",GetLastError());
                              //Here Errcode is 1314. It's meant that  //'A required privilege is not held by the client.'  //What's the meanning? How can i get this privilege?
            }   
        }
   }
 }
 

</pre>


---

@title[Accessing RT Services from Linux ]
<br>
#### <p align="right"><span class="gold" >@fa[linux gp-bullet-white fa-2x] &nbsp;&nbsp; Accessing RT services from Linux </span></p>

<span style="font-size:0.9em" > Firmware Test Suite, it includes a Linux kernel driver to help with it's interactions with UEFI. Note that this is a Linux-centric test suite, solution won't work for other OSes.</span>
- <span style="font-size:0.8em" > http://kernel.ubuntu.com/git/hwe/fwts.git</span>
- <span style="font-size:0.8em" > https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1633506</span>
- <span style="font-size:0.8em" > https://patchwork.kernel.org/patch/9323781/ </span>
- <span style="font-size:0.8em" > http://www.basicinputoutput.com/2016/03/introduction-to-firmware-test-suite-fwts.html</span>



Note:

#### Links for Linux
<pre>
 Wanted to access RT services from OS.
 >> 	1.) Are there any already such exposed OS function or utilities ?
 >> 	2.) Can we plugin our own service/function to RT at run-time. ?
 >> 

 You might want to look at Firmware Test Suite, it includes a Linux kernel driver to help with it's interactions with UEFI. Note that this is a Linux-centric test suite, solution won't work for other OSes.
  -  http://kernel.ubuntu.com/git/hwe/fwts.git
  -  https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1633506
  -  https://patchwork.kernel.org/patch/9323781/
  -  http://www.basicinputoutput.com/2016/03/introduction-to-firmware-test-suite-fwts.html
  
 On 09/05/2017 12:32 AM, Marvin H?user wrote:
 > Good morning,
 > 
 > 1.) Do you mean whether the OS exposes the Runtime Services? Windows and Linux expose the Variable Services (Linux even more, if I remember correctly) and macOS (not entirely sure about the latest version) the entire table via DeviceTree.<br>
 > 2.) Yes, you need to write a DXE Runtime Driver. One way to do it is install an UEFI Protocol and let the UEFI OS loader store its address (pay attention to allocate the structure from Runtime memory, update the pointers when going virtual and not use any Boot Services), another is to use the UEFI Configuration Table. Though remember that the OS still has hardware ownership, you might need to use Management Mode for your ideas. If you target Windows, I'm afraid software MMIs/ACPI or a shim for the RT Variable Services ("execute on variable write") are the only ways I know as you of course cannot alter the bootloader or access the System Table at runtime.<br>
 > 

</pre>



---?image=assets/images/binary-strings-black2.jpg
@title[Security with UEFI Section]
<br><br><br><br><br>
## <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Security with UEFI</span>
<span style="font-size:0.9em" > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;How does UEFI  ensure the Operating System is trusted?</span>



---
#### <p align="right"><span class="gold" >Boot Security Technologies</span></p>
<br>
<table border="0" width="100%">
	<tr>
		<td><b>Hardware Root of Trust</b></td>
		<td><span style="font-size:0.80em" >Boot Guard,  Intel&reg; TXT <br>&nbsp;</span></td>
	</tr>
	<tr>
		<td><b>Measured Boot&nbsp;</b></td>
		<td><span style="font-size:0.80em" >Using TPM<sup>1</sup> to store hash values <br>&nbsp;</span></td>
	</tr>
	<tr>
		<td><b>Verified Boot&nbsp;</b></td>
		<td><span style="font-size:0.80em" >Boot Guard &nbsp;&nbsp; + <br><b>UEFI Secure Boot </b>&nbsp;</span></td>
	</tr>
</table>

<br>
<span style="font-size:0.5em" >Resources: https://firmwaresecurity.com/2015/07/29/survey-of-boot-security-technologies/ </span>

@snap[midpoint span-35 fragment]
<br>
<br>
<br>
<br>
<span style="font-size:02.5em" >@color[#00ffff](&rBarr;)&nbsp;&nbsp; &nbsp;</span>&nbsp;
@snapend

@snap[south-east span-100]
<span style="font-size:0.45em" ><sup>1</sup>TPM - Trusted Platform Module<br><br></span>
@snapend


Note:
#### Intel Boot Guard: 
When your CPU starts up, it reads some code out of flash and executes it. 
With Intel Boot Guard, the CPU verifies a signature on that flash code before executing the reset vector

#### Intel TXT Trusted Execution Technology 


In a Secure Boot chain, each step in the process checks a cryptographic signature on the executable of the next step before it’s launched. Thus, the BIOS will check a signature on the loader, and the loader will check signatures on all the kernel objects that it loads. The objects in the chain are usually signed by the software manufacturer, using private keys that match up with public keys already in the BIOS. If any of the software modules in the boot chain have been hacked, then the signatures won’t match, and the device won’t boot the image.Because the images must be signed by the manufacturer, it’s generally impractical to sign any files generated by the platform user (such as config files).

Secure Boot is relatively self-contained. If the handful of signed objects haven’t been tampered with, the platform boots, and secure boot is done. If objects have been changed so the signature is no longer valid, the platform doesn’t boot and a re-installation is indicated.

In a Measured Boot chain, we still depend on a Root of Trust as the starting point for a chain of trust. But in this case, prior to launching the next object, the currently-running object “measures” or computes the hash of, the next object(s) in the chain, and stores the hashes in a way that they can be securely retrieved later to find out what objects were encountered. Measured Boot doesn’t make an implicit value judgement as to good or bad, and it doesn’t stop the platform from running, so Measured Boot can be much more liberal about what it checks. This can include all kinds of platform configuration information such as which was the boot device, what was in the loader config file, or anything else that might be of interest.

Measured Boot is more flexible, but also requires an important step... Somehow all those hashes have to be stored in a way that there’s very little chance that they can be manipulated, and a very high likelihood that they can be reliably reported to a management station, using a process called Attestation. Since Measured Boot doesn’t stop the platform from booting, the host OS can’t be relied upon to report the hashes.
 
In the case of Measure Boot, the Trusted Platform Module is used to record these hashes. The TPM is a small self-contained security processor that can be attached to a system bus as a simple peripheral. (See http://forums.juniper.net/t5/Security-Now/What-is-a-Trusted-Platform-Module-TPM/ba-p/281128 for more on TPM technology.)  Of the many functions a TPM can provide, one is the facility called Platform Configuration Registers (PCRs), used for storing hashes.

PCRs are registers in the TPM that are cleared only at hardware reset, and cannot be directly written

---
@title[Hardware root of Trust ]
#### <p align="right"><span class="gold" >Hardware root of Trust </span></p>

<table id="recTable">
	<tr>
		<td bgcolor="#121212"><b>Boot Guard&nbsp;&nbsp;&nbsp;</b></td>
		<td bgcolor="#121212" width="50%"><b>Intel&reg; TXT </b></td>
	</tr>
	<tr>
		<td><span style="font-size:0.75em" >CPU verifies signature<br><br>Verification occurs before BIOS code starts<br><br>Hash of signature is fused in CPU&nbsp;</span></td>
		<td width="50%"><span style="font-size:0.75em" >Uses a Trusted Platform Module (TPM) & cryptographic <br><br>Provides Measurements&nbsp;</span></td>
	</tr>
</table>

@snap[south-west span-45 fragment]
@box[bg-purple text-white rounded  ](<span style="font-size:01.50em" ><b> Verification</b>&nbsp;</span>)
<br>
<br>

@snapend

@snap[south-east span-45 fragment]
@box[bg-purple text-white rounded  ](<span style="font-size:01.50em" > <b>Measurements</b>&nbsp;</span>)
<br>
<br>

@snapend


Note:

#### Intel Boot Guard: 
With Intel Boot Guard, the CPU verifies a signature on flash code before executing. The hash of the public half of the signing key is flashed into fuses on the CPU. It is the system vendor that owns this key and chooses to flash it into the CPU, not Intel. 
This has genuine security benefits. It's no longer possible for an attacker to simply modify or replace the firmware - they have to find some other way to trick it into executing arbitrary code, and over time these will be closed off. But in the process, the system vendor has prevented the user from being able to make an informed choice to replace their system firmware


#### Intel TXT Trusted Execution Technology 
TXT - uses a Trusted Platform Module (TPM) and cryptographic techniques to provide measurements of software and platform components so that system software as well as local and remote management applications may use those measurements to make trust decisions. This technology is based on an industry initiative by the Trusted Computing Group (TCG) to promote safer computing. It defends against software-based attacks aimed at stealing sensitive information by corrupting system or BIOS code, or modifying the platform's configuration.


---?image=/assets/images/slides/Slide41.JPG
<!-- .slide: data-transition="none" -->
@title[UEFI Secure Boot  ]
### <p align="right"><span class="gold" >UEFI Secure Boot  </span></p>


Note:

- The Secure Boot feature uses authenticated firmware variables as the OS loader “root of trust”
- Software ID checking at every step of boot
- System BIOS (updated via secure process)
- Add-In Cards (Signed UEFI Option ROMs)
- OS Boot Loader (checks for “secure mode” at boot)
- Secure Boot is not required by UEFI but bay be required by specific OS leveraging UEFI 2.3.1
- Example: Microsoft Windows 8 client

- In a Secure Boot chain, each step in the process checks a cryptographic signature on the executable of the next step before it’s launched. Thus, the BIOS will check a signature on the loader, and the loader will check signatures on all the kernel objects that it loads. The objects in the chain are usually signed by the software manufacturer, using private keys that match up with public keys already in the BIOS. If any of the software modules in the boot chain have been hacked, then the signatures won’t match, and the device won’t boot the image.Because the images must be signed by the manufacturer, it’s generally impractical to sign any files generated by the platform user (such as config files).



+++?image=/assets/images/slides/Slide42.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Secure Boot 02 ]
### <p align="right"><span class="gold" >UEFI Secure Boot  </span></p>

Note:

- The Secure Boot feature uses authenticated firmware variables as the OS loader “root of trust”
- Software ID checking at every step of boot
- System BIOS (updated via secure process)
- Add-In Cards (Signed UEFI Option ROMs)
- OS Boot Loader (checks for “secure mode” at boot)
- Secure Boot is not required by UEFI but bay be required by specific OS leveraging UEFI 2.3.1
- Example: Microsoft Windows 8 client

- In a Secure Boot chain, each step in the process checks a cryptographic signature on the executable of the next step before it’s launched. Thus, the BIOS will check a signature on the loader, and the loader will check signatures on all the kernel objects that it loads. The objects in the chain are usually signed by the software manufacturer, using private keys that match up with public keys already in the BIOS. If any of the software modules in the boot chain have been hacked, then the signatures won’t match, and the device won’t boot the image.Because the images must be signed by the manufacturer, it’s generally impractical to sign any files generated by the platform user (such as config files).



+++?image=/assets/images/slides/Slide43.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Secure Boot  03]
### <p align="right"><span class="gold" >UEFI Secure Boot  </span></p>

Note:

- The Secure Boot feature uses authenticated firmware variables as the OS loader “root of trust”
- Software ID checking at every step of boot
- System BIOS (updated via secure process)
- Add-In Cards (Signed UEFI Option ROMs)
- OS Boot Loader (checks for “secure mode” at boot)
- Secure Boot is not required by UEFI but bay be required by specific OS leveraging UEFI 2.3.1
- Example: Microsoft Windows 8 client

- In a Secure Boot chain, each step in the process checks a cryptographic signature on the executable of the next step before it’s launched. Thus, the BIOS will check a signature on the loader, and the loader will check signatures on all the kernel objects that it loads. The objects in the chain are usually signed by the software manufacturer, using private keys that match up with public keys already in the BIOS. If any of the software modules in the boot chain have been hacked, then the signatures won’t match, and the device won’t boot the image.Because the images must be signed by the manufacturer, it’s generally impractical to sign any files generated by the platform user (such as config files).



+++?image=/assets/images/slides/Slide44.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Secure Boot  04]
### <p align="right"><span class="gold" >UEFI Secure Boot  </span></p>

Note:

- The Secure Boot feature uses authenticated firmware variables as the OS loader “root of trust”
- Software ID checking at every step of boot
- System BIOS (updated via secure process)
- Add-In Cards (Signed UEFI Option ROMs)
- OS Boot Loader (checks for “secure mode” at boot)
- Secure Boot is not required by UEFI but bay be required by specific OS leveraging UEFI 2.3.1
- Example: Microsoft Windows 8 client

- In a Secure Boot chain, each step in the process checks a cryptographic signature on the executable of the next step before it’s launched. Thus, the BIOS will check a signature on the loader, and the loader will check signatures on all the kernel objects that it loads. The objects in the chain are usually signed by the software manufacturer, using private keys that match up with public keys already in the BIOS. If any of the software modules in the boot chain have been hacked, then the signatures won’t match, and the device won’t boot the image.Because the images must be signed by the manufacturer, it’s generally impractical to sign any files generated by the platform user (such as config files).



+++?image=/assets/images/slides/Slide45.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Secure Boot  05]
### <p align="right"><span class="gold" >UEFI Secure Boot  </span></p>

Note:

- The Secure Boot feature uses authenticated firmware variables as the OS loader “root of trust”
- Software ID checking at every step of boot
- System BIOS (updated via secure process)
- Add-In Cards (Signed UEFI Option ROMs)
- OS Boot Loader (checks for “secure mode” at boot)
- Secure Boot is not required by UEFI but bay be required by specific OS leveraging UEFI 2.3.1
- Example: Microsoft Windows 8 client

- In a Secure Boot chain, each step in the process checks a cryptographic signature on the executable of the next step before it’s launched. Thus, the BIOS will check a signature on the loader, and the loader will check signatures on all the kernel objects that it loads. The objects in the chain are usually signed by the software manufacturer, using private keys that match up with public keys already in the BIOS. If any of the software modules in the boot chain have been hacked, then the signatures won’t match, and the device won’t boot the image.Because the images must be signed by the manufacturer, it’s generally impractical to sign any files generated by the platform user (such as config files).



+++?image=/assets/images/slides/Slide46.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[UEFI Secure Boot  06]
### <p align="right"><span class="gold" >UEFI Secure Boot  </span></p>

Note:

- The Secure Boot feature uses authenticated firmware variables as the OS loader “root of trust”
- Software ID checking at every step of boot
- System BIOS (updated via secure process)
- Add-In Cards (Signed UEFI Option ROMs)
- OS Boot Loader (checks for “secure mode” at boot)
- Secure Boot is not required by UEFI but bay be required by specific OS leveraging UEFI 2.3.1
- Example: Microsoft Windows 8 client

- In a Secure Boot chain, each step in the process checks a cryptographic signature on the executable of the next step before it’s launched. Thus, the BIOS will check a signature on the loader, and the loader will check signatures on all the kernel objects that it loads. The objects in the chain are usually signed by the software manufacturer, using private keys that match up with public keys already in the BIOS. If any of the software modules in the boot chain have been hacked, then the signatures won’t match, and the device won’t boot the image.Because the images must be signed by the manufacturer, it’s generally impractical to sign any files generated by the platform user (such as config files).

---
@title[Authenticated Variables]
### <p align="right"><span class="gold" >Authenticated Variables</span></p>

@snap[north-west span-45]
<br>
<br>
@box[bg-grey-35 text-white  rounded ](<span style="font-size:01.2em" ><b>&nbsp;</b></span> <br><br><br><br><br><br><br><br><br><br> )
@snapend


@snap[north-west span-30 ]
<br>
<br>
@box[bg-royal text-white  rounded ](<span style="font-size:01.2em" ><b>PK</b></span>)
@snapend


@snap[north-west span-35 ]
<br>
<br>
<br>
<br>
<br>
@box[bg-gold2 text-white  rounded ](<span style="font-size:01.2em" ><b>KEK</b></span>)
@snapend

@snap[north-west span-40 ]
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
@box[bg-white text-black  rounded ](<span style="font-size:01.2em" ><b>DB</b></span>)
@snapend

@snap[north-west span-40]
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
@box[bg-black text-white  rounded ](<span style="font-size:01.2em" ><b>DBX</b></span>)
@snapend



@snap[north-east span-40 fragment]
<br>
<br>
<br>
<br>
<br>
<br>
@box[bg-navy text-white  rounded ](<span style="font-size:01.2em" ><b>`SetupMode`</b></span>)
<br>
@box[bg-red-pp text-white  rounded ](<span style="font-size:01.2em" ><b>`SecureBoot`</b></span>)
@snapend


@snap[south span-100 fragment]
![SecureBoot](/assets/images/SecureBoot_shell.png)
@snapend

Note:

### PK
OEM and Platform FW-  format is RSA-2048
Key Exchange Key
#### KEK
Platform FW and OS - format is RSA-2048
Authorized Signature DB
#### DB
Authorized Signing certificates - white list
Forbidden Signature DB
#### DBX
Unauthorized Signing certificates - Black list

#### Setup Mode
#### SetupMode
- NULL  
- Secure Boot not supported 
- PK is enrolled 
- in user mode     - User mode requires authentication 
– Platform is in Setup mode – no PK enrolled


- Shell Dmpstore command show the variable "SecureBoot"

---

@title[Security Package Project Page]
<p align="right"><span class="gold" ><b>Security Package Project Page</b></span><span style="font-size:0.8em" ><a href="https://github.com/tianocore/tianocore.github.io/wiki/SecurityPkg 
"> Wiki Link</a></span></p>
<br>
<div class="left1">
     <ul>
        <li><span style="font-size:0.8em" >Wiki Link: <a href="https://github.com/tianocore/tianocore.github.io/wiki/How-to-Enable-Security#HOW_TO_ENABLE_SECURE_BOOT_SERVICE">How-to-Enable-Security</a></span></span></li>
        <li><span style="font-size:0.8em" >PDF <a href="https://github.com/tianocore-docs/Docs/raw/master/User_Docs/SigningUefiImages%20-v1dot31.pdf">How to Sign UEFI Images V1.31</a></span></span></li>
        <li><span style="font-size:0.8em" >Build command line switch - `SECURE_BOOT_ENABLE = TRUE`</span></li>
        <li><span style="font-size:0.8em" >Install the `CryptoPkg OpensslLib` : <a href="https://github.com/tianocore/edk2/blob/master/CryptoPkg/Library/OpensslLib/OpenSSL-HOWTO.txt">OpenSSL-HOWTO.txt</a></span></li>
     </ul>
</div>
<div class="right1">
   <p align="center"><span style="font-size:01.2em" ><font color="yellow"><b> </b></font></span></p>
</div>

@snap[north-east span-40 ]
<br>
<br>
<br>
<br>
<p align="center"><span style="font-size:01.2em" ><font color="yellow"><b>How To Enable Secure Boot Service</b></font></span></p>
@snapend

@snap[north-east span-45 fragment]
<br>
<br>
<br>
<br>
![wikiPic](/assets/images/wikiPic.png)
@snapend

Note:




---?image=/assets/images/slides/Slide53.JPG
@title[Windows Secure Boot Key]
<p align="right"><span class="gold" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>Windows Secure Boot Key Creation and Management Guidance</b></span></p>
<div class="left1">
     <ul>
        <li><span style="font-size:0.8em" >Windows - <a href="https://msdn.microsoft.com/en-us/windows/hardware/commercialize/manufacture/desktop/windows-secure-boot-key-creation-and-management-guidance">Secure Boot Key Creation & Management Guide  
</a></span></span></li>
        <li><span style="font-size:0.8em" >Creation and management of the Secure Boot keys and certificates in a manufacturing environment.</span></li>
        <li><span style="font-size:0.8em" >Addresses questions related to creation, storage and retrieval of Platform Keys (PKs), secure firmware update keys, and third party Key Exchange Keys (KEKs).
</span></li>
     </ul>
</div>
<div class="right1">
   <span style="font-size:01.5em" ><font color="yellow"><b>      </b></font></span>
</div>


Note:
Microsoft Link - creation and management of the Secure Boot keys and certificates in a manufacturing environment.

This document helps guide OEMs and ODMs in creation and management of the Secure Boot keys and certificates in a manufacturing environment. It addresses questions related to creation, storage and retrieval of Platform Keys (PKs), secure firmware update keys, and third party Key Exchange Keys (KEKs).

---?image=/assets/images/slides/Slide55.JPG
@title[Platforms Require Secure Boot Enabled]
<p align="right"><span class="gold" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>Many Platforms are Requiring<br>UEFI Secure Boot Enabled</b></span></p>
<br>
<br>
<div class="left1">
     <ul>
        <li><span style="font-size:0.8em" >Secure Boot now mandated for specific platforms  </span></li>
        <li><span style="font-size:0.8em" >See “Security requirements” on UEFI requirements for <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/bringup/uefi-requirements-that-apply-to-all-windows-platforms">Windows editions on SoC Platforms</a></span></span></li>
     </ul>
</div>
<div class="right1">
   <span style="font-size:01.5em" ><font color="yellow"><b>      </b></font></span>
</div>


Note:

---?image=assets/images/binary-strings-black2.jpg
@title[Coreboot Section]
<br><br><br><br><br>
## <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Coreboot</span>
<span style="font-size:0.9em" > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;How does coreboot work with UEFI  </span>

Note:
Section


---?image=/assets/images/slides/Slide46_1.JPG
@title[Intel FSP and Coreboot Diagram]

<p align="center" style="margin-top: -3px; margin-bottom: -3px"><span style="color:white; font-size:0.75em"> 
Intel®  FSP "Produced" to <br> "Consuming" Intel® Architecture Firmware </span>


Note:


---?image=/assets/images/slides/Slide81.JPG
<!-- .slide: data-transition="none" -->		 
@title[coreboot Payload]
<p align="right"><span class="gold" ><b>Coreboot Payload </b></span></p>

Note:

Coreboot in itself is "only" minimal code for initializing hardware. It does not have the media drivers nor does it provide services required by an OS. 
After the initialization, it jumps to a payload which can provide services required to load and boot an OS. http://www.coreboot.org/Payloads


UEFI payload provides UEFI services on top of coreboot that allows UEFI OS boot.
Wiki/Coreboot_UEFI_payload- 
https://github.com/tianocore/tianocore.github.io/wiki/Coreboot_UEFI_payload 

---?image=/assets/images/slides/Slide83.JPG
<!-- .slide: data-transition="none" -->		 
@title[Consumers: EDK II firmware and coreboot]
<p align="right"><span class="gold" ><b>Consumers: EDK II firmware and coreboot</b></span></p>


Note:

- Functionality is on the left side.     
- Don’t say it’s a comparison.  
- Put in payload and have in speaker notes.   Speak to this.





---  
@title[Summary]
<BR>
### <p align="center"><span class="gold"   >Summary </span></p><br>
<br>
 @fa[certificate gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Explain How the OS and UEFI Work together </span><br>
 @fa[certificate gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Explain the UEFI Requirements for UEFI aware OS</span><br>
 @fa[certificate gp-bullet-yellow]<span style="font-size:0.9em">&nbsp;&nbsp;Explain How Secure Boot Fits with UEFI</span> <br>
 @fa[certificate gp-bullet-magenta]<span style="font-size:0.9em">&nbsp;&nbsp;What about coreboot?</span> 

 

---?image=assets/images/gitpitch-audience.jpg
@title[Questions]
<br>
![Questions](/assets/images/questions.JPG =10x) 


---?image=assets/images/gitpitch-audience.jpg
@title[Logo Slide]
<br><br><br>
![Logo Slide](/assets/images/TianocoreLogo.png =10x)


---
@title[Acknowledgements]
#### <p align="center"><span class="gold"   >Acknowledgements</span></p>

```c++
/**
Redistribution and use in source (original document form) and 'compiled' forms (converted
to PDF, epub, HTML and other formats) with or without modification, are permitted provided
that the following conditions are met:

Redistributions of source code (original document form) must retain the above copyright 
notice, this list of conditions and the following disclaimer as the first lines of this 
file unmodified.

Redistributions in compiled form (transformed to other DTDs, converted to PDF, epub, HTML
and other formats) must reproduce the above copyright notice, this list of conditions and 
the following disclaimer in the documentation and/or other materials provided with the 
distribution.

THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR IMPLIED 
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND 
FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL TIANOCORE PROJECT BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES 
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, 
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, 
WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF ADVISED OF THE POSSIBILITY 
OF SUCH DAMAGE.

Copyright (c) 2020, Intel Corporation. All rights reserved.
**/

```
