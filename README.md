My name is Matt Janda,

I would like to share my software engineering journey over the years. You can find here some of the projects I was working on and the tools I was using.


# Year 1998

It was exciting time writing software using assembler and pascal for DOS. 
You can find all my assembler source codes and binaries in [8086](https://github.com/Jandini/8086) repository.
The code can be executed only under [DosBox](https://www.dosbox.com/). Kudos to the authors for keeping the legacy alive.

Multi-Edit was one of the text editors to write and run assembler code.

![ME_MASZ](https://user-images.githubusercontent.com/19593367/202818994-3e053783-9911-48be-be54-11750ee33fd1.gif)

I used Borlad Pascal to write and run code written in Pascal language...


## Software Reverse Engineering in DOS

I modified software which helped me to learn touch typing. The software was called "Maszynistka" which translates to "Typist". Maszynistka was free to use with the caveat that unregistered version has a splash screen. The splash screen is taking about 15 minutes before you can start using the tool.

I used Turbo Debugger to figure out how to skip the splash screen. This is how I did it... 

![TD_MASZ](https://user-images.githubusercontent.com/19593367/202817851-761425ca-0336-4240-a197-2a9984db452f.gif)

I let the program to execute until I found the splash screen call. I applied simple [NOP slide](https://en.wikipedia.org/wiki/NOP_slide) over the splash screen call. Three bytes only. The challenge was that the code of the program was encoded. I could not make permanent change to MASZ.EXE binaries. 

I wrote my own debugger. The assembler code in [CRACK.ASM](https://github.com/Jandini/8086/blob/main/CRACK/CRACK.ASM) repeats steps required to bypass the splash screen. Instead running MASZ.EXE the program can be executed via CRACK.COM which skips the splash screen.  

Program "Maszynistka" with the splash screen...

![MASZ-SPLASH](https://user-images.githubusercontent.com/19593367/202403492-828171a2-2e4c-411d-8bbb-70e77b00bed5.gif)

... and without the splash screen after running it with [CRACK.COM](https://github.com/Jandini/8086/blob/main/CRACK/CRACK.ASM)

![MASZ-CRACK](https://user-images.githubusercontent.com/19593367/202403750-d7bf8743-2d03-4e1d-a2c0-8b5eba3237f0.gif)


## [TSRs](https://en.wikipedia.org/wiki/Terminate-and-stay-resident_program) programs for DOS

TSR is Terminate and Stay Resident program which allowed to run your program in the background and let the DOS operating system continue. 
This is where the journey with concept of viruses starts. 



## Text mode pictures in assembler code

I created a number of picutres in text mode and converted them into assembler code. For example, the picture below was manually created in [X.ASM](https://github.com/Jandini/8086/tree/main/COMPRESS) (1536 bytes) and [compressed](https://github.com/Jandini/8086/blob/main/COMPRESS/COMPRESS.PAS) to C.ASM file (584 bytes). Compressed picture in C.ASM was [converted](https://github.com/Jandini/8086/blob/main/COMPRESS/CONVERT.PAS) to assembler's byte array in [OUT.ASM](https://github.com/Jandini/8086/blob/main/COMPRESS/OUT.ASM). The source code to draw the picture was added later to OUT.ASM code.

The compressed pictures converted to assembler code could easlily fit into a few sectors between MBR and BPB on the hard drive. I used similar idea in [boot loader for two operating systems](https://github.com/Jandini/Jandini/blob/main/README.md#two-operating-systems-on-one-floppy-disk).


[OUT.ASM](https://github.com/Jandini/8086/blob/main/COMPRESS/OUT.ASM)

![COMPRESS](https://user-images.githubusercontent.com/19593367/202412547-cdae0eb8-6506-4fe1-b2cb-262794c50241.gif)

[PICTURE.ASM](https://github.com/Jandini/8086/blob/main/PICTURE/PICTURE.ASM)

![PICTURE](https://user-images.githubusercontent.com/19593367/202411411-d234abaf-d036-4784-9df4-464369b797c2.gif)


## Two operating systems on one floppy disk

I worte boot loader [MULTI.ASM](https://github.com/Jandini/8086/blob/main/MULTI/MULTI.ASM) which allowed me to place two operating systems on a single floppy disk.
I added animated floppy disk picture to the code to make the boot loader a bit more fancy. User can select operating system from the menu.

Microsoft DOS 6.22

![W95-screen0-D622 (online-video-cutter com) 720x400](https://user-images.githubusercontent.com/19593367/202869923-f9ce8ce8-344f-4a5e-8b53-a9e673f08983.gif)

Microsoft DOS 4.00 for Windows 95

![W95-screen0-W95 (online-video-cutter com) 720x400](https://user-images.githubusercontent.com/19593367/202869953-7a4444dc-44f0-4039-8c0b-95d60cdf7b00.gif)

The physical image of the 1.44MB floppy disk is available in the [repository](https://github.com/Jandini/8086/blob/main/MULTI/floppy.flp).


# Year 2006

## Hard drive imaging via IDE ports for DOS

I wrote a simple hard drive imaging tool using [Borland Pascal](https://wiki.freepascal.org/Borland_Pascal). I used [Turbo Vision](https://en.wikipedia.org/wiki/Turbo_Vision) library to create user interface. The software was communicating with hard drive directly via [Integrated Drive Electronics (IDE)](https://en.wikipedia.org/wiki/Parallel_ATA#IDE_and_ATA-1) ports.

![IDE](https://user-images.githubusercontent.com/19593367/202914760-7c92e881-efb1-4f33-b8b1-5045124ddf71.gif)

Running under Windows 98 with virtual hard drive...

![ezgif-1-36dfefd664](https://user-images.githubusercontent.com/19593367/202930593-f7812490-64f4-4a5b-a478-9a5179d69eae.gif)


This was my last software written for DOS. You can find the code in [IDE repository](https://github.com/Jandini/IDE).


## Software Reverse Engineering with SoftICE

[SoftICE](https://en.wikipedia.org/wiki/SoftICE) was my favourite debugger for Windows XP/2000. 

This is one projects I was working on, where I needed to bypass certian software behaviour...

![ezgif-4-45d0f61e6a](https://user-images.githubusercontent.com/19593367/202902998-ccb67e05-fb02-4c4b-b76a-4bcda79b5f3f.gif)


# Year 2018

## Lightweight Document Review Platform

I designed simple and fast document review platform for Electronic Discovery. 
With a small team of talented developers we delivered excellent product.

User can drag and drop data through the web browser.
The data is automatically processed and published for review.



![iv](https://user-images.githubusercontent.com/19593367/207027210-7e28ef89-10f0-4957-8dc6-08e370e93f8b.gif)

Key features

* Isolated, self serived client workspaces. 
* Role based access to client's workspaces.
* Client can create projects, add users and assign them to the projects.
* Drag and drop files like archives, mailboxes or standalone documents.
* User can open multiple projects in separate web browser tabs.



# Year 2020



## Capture The Flag 

I created simple [.NET framework for playing CTF](https://github.com/Jandini/Janda.CTF). 

I participated in multiple Capture The Flag events organized by [SANS](https://www.sans.org/uk/) on [My ranges.io](https://ranges.io/my-events?filter=finished)

| Name                                           | Finished At              | Challenges             | Position                 | Points                        |
| ---------------------------------------------- | ------------------------ | ---------------------- | ------------------------ | ----------------------------- |
| **SANS Community CTF**                         | 14:00 on 17 Oct 2020 BST | **35** of 37 completed | **21**st of 1055 players | **12,750** of 13,500 possible |
| **SANS Community CTF - November**              | 13:00 on 23 Nov 2020 GMT | **61** of 62 completed | **27**th of 1690 players | **19,850** of 20,350 possible |
| **Cyber Camp 2020**                            | 04:59 on 7 Jan 2021 GMT  | **37** of 39 completed | **26**th of 360 players  | **10,050** of 11,550 possible |
| **Global Community CTF: Mini BootUp**          | 18:00 on 19 Feb 2021 GMT | **32** of 32 completed | **17**th of 360 players  | **8,500** of 8,500 possible   |
| **Intermediate: Global Community CTF: BootUp** | 23:00 on 23 Apr 2021 BST | **13** of 24 completed | **88**th of 1293 players | **2,300** of 7,500 possible   |
| **Global Community CTF: Bootup**               | 23:00 on 16 Oct 2021 BST | **36** of 45 completed | **20**th of 889 players  | **1,934** of 4,630 possible   |

![ezgif-5-766ce72835](https://user-images.githubusercontent.com/19593367/202913808-0cccea17-21a7-4027-a371-08e4baf39231.gif)



# Year 2022

## Github and Jira metics in Kibana

![ezgif-2-2c0cd0e8e7](https://user-images.githubusercontent.com/19593367/203609416-8f783f07-eac5-40db-9643-4bdf11622236.gif)




