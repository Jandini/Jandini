My name is Matt Janda,


> This is my software engineering journey;
> How I turned ideas into small tools, the small tools into a projects and the projects into full stack applications.
> I designed and wrote from scratch most of the tools and applications presented here. Some of them are available in my public repositories. 

* [AutoByte](https://github.com/Jandini#autobyte)
* [KiBoards](https://github.com/Jandini#kiboards)
* [Terragate](https://github.com/Jandini#terragate)
* [JandaBox](https://github.com/Jandini#jandabox)
* [WinGif](https://github.com/Jandini#wingif)
* [Janda.Go](https://github.com/Jandini#janda-go)
* [Github and Jira metrics in Kibana](https://github.com/Jandini#github-and-jira-metrics-in-kibana)
* [CI/CD Pipelines in Jenkins](https://github.com/Jandini/Jandini#cicd-pipelines-with-jenkins)
* [Capture The Flag Framework](https://github.com/Jandini#capture-the-flag-framework)
* [CoolCat](https://github.com/Jandini#coolcat)
* [Lightweight Document Review Platform](https://github.com/Jandini#lightweight-document-review-platform)
* [Hard drive imaging via IDE ports for DOS](https://github.com/Jandini#hard-drive-imaging-via-ide-ports-for-dos)
* [Software Reverse Engineering with SoftICE](https://github.com/Jandini#software-reverse-engineering-with-softice)
* [Dictionary Mobile](https://github.com/Jandini#dictionary-mobile)
* [TFL Mobile](https://github.com/Jandini#tfl-mobile)
* [Media Eraser](https://github.com/Jandini#media-eraser)
* [Interrupt List Navigator](https://github.com/Jandini#interrupt-list-navigator)
* [Assembler for 8086](https://github.com/Jandini#assembler-for-8086)
* [Software Reverse Engineering in DOS](https://github.com/Jandini#software-reverse-engineering-in-dos)
* [TSR programs for DOS](https://github.com/Jandini#tsr-programs-for-dos)
* [Text mode pictures in Assembler](https://github.com/Jandini#text-mode-pictures-in-assembler)
* [Floppy Disk Boot Loader](https://github.com/Jandini#floppy-disk-boot-loader)

---
###### Year 2023
# AutoByte

[AutoByte](https://github.com/Jandini/AutoByte) is a data structure deserializer and parser for .NET. It automatically generates code based on class properties, streamlining the parsing of binary data. It simplifies handling binary data in .NET apps, making it easier to integrate and manage complex data structures efficiently.


# KiBoards

[KiBoards](https://github.com/Jandini/kiboards) Inspired by [Xunit.TestLogger](https://github.com/spekt/xunit.testlogger) provides Elasticsearch logging for Xunit and visualisations in Kibana.


# Terragate

[Terragate](https://github.com/Jandini/terragate) is simple web API gateway for terraform command line tool. 


# JandaBox

[JandaBox](https://github.com/Jandini/JandaBox) is everything what I learned while working on [Janda.Go](https://www.nuget.org/packages/Janda.Go) and much more.


HelloWorld from command line...

![jandabox](https://user-images.githubusercontent.com/19593367/234419424-3585dff7-80e4-451e-89ad-b1bd2616512e.gif)

The same HelloWorld directly from Visual Studio...

![helloworld](https://user-images.githubusercontent.com/19593367/234417970-e2892270-50a1-4fd0-90a5-f0f3abf15af4.gif)



# WinGif

No more online converters...
[WinGif](https://github.com/Jandini/WinGif) is a simple windows screen capture tool that allows to quickly create animated gif files. 
It can create animated GIF files by capturing given window title or make it from individual frames saved in PNG files.  
```
WinGif 0.2.0
Copyright (C) 2023 Matt Janda

  capture    (Default Verb) Create animated GIF by capturing active window.

  make       Make animated GIF from PNG files.

  help       Display more information on a specific command.

  version    Display version information.
```


Key features:

* Capture active windows
* Provide case sesitive, full or partial window title to trigger the capture.
* Start capture when window with given title become active. After this any active window will be captured. 
* Capture only window with given title. The capture will pause if active window is does not match given title.
* Save individual frames as PNG files.
* Make GIF file from individual frames saved in PNG files.
* Provide delay between taking screen shoots in milliseconds.
* Provide delay between GIF frames in milliseconds. (33ms delay between frames equals ~30fps)
* Allow self capture. By default WinGif will pause capturing when the window with WinGif title is active.



Self capture and "Chrome" window capture.

![wingif2](https://user-images.githubusercontent.com/19593367/207033078-c1ed8e1f-db43-41c5-9228-0a86db18efc8.gif)


Make a new gif file from png frames saved by WinGif. 

![image](https://user-images.githubusercontent.com/19593367/207031957-4e51fd1c-fc4e-4d9f-98e3-7cdfb712fd81.png)


Here we are... a GIF. 

![chrome](https://user-images.githubusercontent.com/19593367/207031114-49891e15-c160-4346-b546-b943dbfe0adc.gif)


---
###### Year 2022
# Janda.Go

[Janda.Go](https://github.com/Jandini/Janda.Go) provides .NET template for console application with dependency injection, logging, and configuration.
The template is available as [Nuget package](https://www.nuget.org/packages/Janda.Go) that can be accessed directly using `dotnet new install Janda.Go` command.

Key features: 
- GitHub actions automatically publish templates to nuget.org
- Installation through `dotnet` command
- Provides Microsoft logging and Serilog
- Binding configuration file 
- Main program exception handling

![JandaGo](https://user-images.githubusercontent.com/19593367/211174559-b45486cd-20d8-49fe-839d-7d7a50d6395d.gif)





# Github and Jira metrics in Kibana

I moved my career into management in 2018. Yet, I am still developing in my own time. 
Management is easier if you find a way to measure success of your team. 
Since my company is using Jira for project management and GitHub for development I created fully containerised platform which visualise developers participation within the projects.

Metrics service is responsible for transferring relevant data from Jira and Github into Elasticsearch and visualize through Kibana.

![ezgif-2-2c0cd0e8e7](https://user-images.githubusercontent.com/19593367/203609416-8f783f07-eac5-40db-9643-4bdf11622236.gif)

The platform consist of 3 containers: 

* Kibana
* Elasticsearch 
* Metics Loader


Key features: 

- Automatically create Kibana spaces.
- Import dashboards from ndjson files.
- Running Jira and GitHub loader services at the same time.
- Index multiple Jira projects simultaneously.
- Retries if too many requests is returned. 
- Caching to reduce number of lookups. 



Start platform with docker compose.

![metrics](https://user-images.githubusercontent.com/19593367/213830914-2b605d7c-9bea-4025-9a4d-3ed42ceac44a.gif)

Jira loader indexing issues.

![metrics2](https://user-images.githubusercontent.com/19593367/213831103-98658339-658e-4f43-bdaa-513875c3cd7f.gif)

Jira loader waits and retires when too many requests was made.

![metrics7](https://user-images.githubusercontent.com/19593367/213831073-776fc80c-4122-4101-a25b-d5e31adc38e1.gif)


## Deployment scripts for metrics services

I wrote deployment script for Ubuntu 18.04.6. The script configure operating system and deploy metrics services. 

* Install docker and docker-compose.
* Run docker-compose.
* Pull image containers for kibana, elastic search and metric. 
* Start containers.

It takes only a minute to deploy and start metrics services. The script is executed directly from the last successfull build in Jenkins:
```sh
curl -s https://jenkins.***.com/job/mjanda/job/Metrics/job/develop/lastSuccessfulBuild/artifact/ubuntu.sh | sudo bash
```


![metrics9](https://user-images.githubusercontent.com/19593367/213867286-8bb9466a-a867-4344-ac49-1d9864f3a019.gif)


# CI/CD Pipelines with Jenkins

Automatically build and push docker images to proget feed. 

![jenkins4](https://user-images.githubusercontent.com/19593367/213829270-d298a4f2-71ce-42b2-a97d-182c39fe66a3.gif)

Running Jenkins pipeline with Ocean Blue plugin.

![jenkins](https://user-images.githubusercontent.com/19593367/213829893-5efd386c-4513-4119-897b-fb75e92bbaab.gif)


---
###### Year 2020
# Capture The Flag Framework

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



# CoolCat

Teaching basics of C# programming with a bit of ASCII fun. 
The picture of [CoolCat](https://github.com/Jandini/CoolCat) was copied from my daughter's T-shirt logo. 

![image](https://user-images.githubusercontent.com/19593367/111007043-d60d0a80-8385-11eb-8fd1-438ae2170b3c.png)


---
###### Year 2018
# Lightweight Document Review Platform

I designed simple and fast document review platform for Electronic Discovery. 
I wrote back bone of the application and with a small team of talented developers completed the project.


User can drag and drop data through the web browser.
The data is automatically processed and published for review.



![iv](https://user-images.githubusercontent.com/19593367/207027210-7e28ef89-10f0-4957-8dc6-08e370e93f8b.gif)

Key features:

* Isolated, self serived client workspaces. 
* Role based access to client's workspaces.
* Client can create projects, add users and assign them to the projects.
* User can open multiple projects in separate web browser tabs.
* Drag and drop files like archives, mailboxes or standalone documents.
* Data processing powered by ICE processing engine.
* Data deduplication.
* Customizable coding templates.
* Code documents based on isseue or relevance.
* Mass code multiple documents.
* Keyword search powered by dtSearch.
* Search documents by date and coding.
* Saved searches.
* Show unseen documents.
* Show duplicate documents.
* Download documents.
* Print documents into PDF.



---
###### Year 2006
# Hard drive imaging via IDE ports for DOS

I wrote a simple hard drive imaging tool using [Borland Pascal](https://wiki.freepascal.org/Borland_Pascal). I used [Turbo Vision](https://en.wikipedia.org/wiki/Turbo_Vision) library to create user interface. The software was communicating with hard drive directly via [Integrated Drive Electronics (IDE)](https://en.wikipedia.org/wiki/Parallel_ATA#IDE_and_ATA-1) ports.

![IDE](https://user-images.githubusercontent.com/19593367/202914760-7c92e881-efb1-4f33-b8b1-5045124ddf71.gif)

Running under Windows 98 with virtual hard drive...

![ezgif-1-36dfefd664](https://user-images.githubusercontent.com/19593367/202930593-f7812490-64f4-4a5b-a478-9a5179d69eae.gif)


This was my last software written for DOS. You can find the code in [IDE repository](https://github.com/Jandini/IDE).


# Software Reverse Engineering with SoftICE

[SoftICE](https://en.wikipedia.org/wiki/SoftICE) was my favourite debugger for Windows XP/2000. 

This is one projects I was working on, where I needed to bypass certian software behaviour...

![ezgif-4-45d0f61e6a](https://user-images.githubusercontent.com/19593367/202902998-ccb67e05-fb02-4c4b-b76a-4bcda79b5f3f.gif)



---
###### Year 2008

# Dictionary Mobile

My first software written for Windows PDA. [Slowniki Mobile](https://github.com/Jandini/DictionaryMobile) was Polish English, Polish German and Polish French bidirectional dictionary client. The data was retrived from online dictionary website. 

![dict](https://user-images.githubusercontent.com/19593367/212577048-bc1f1156-3c05-4e37-bcfa-b417f88b23c9.gif)


"Slownki Mobile" running on my Windows PDA device.  

![vlc](https://user-images.githubusercontent.com/19593367/212778035-7873050a-db2b-4107-900f-51ed10d1b3a9.gif)


# TFL Mobile

Transport for London Mobile application for PDA. The source code is available in [TFLMobile](https://github.com/Jandini/TFLMobile) repository.

![tfl1](https://user-images.githubusercontent.com/19593367/212574580-7ac90a40-3122-43a1-93d3-538c4f1c8603.gif)

Search options: 
* Station or stop
* Postcode
* Address
* Place of intrest

![tfl2](https://user-images.githubusercontent.com/19593367/212574837-fa812f0a-2595-41f6-b92d-edf3b838faa9.gif)

---
###### Year 2005
# Media Eraser 

MediaEraser was compiled into three feature versions: Free (lite), Standard and Full. Each build contained only the code for the features available in given version.
The free version of MediaEraser can be still downloaded from websites like [programy.net.pl](https://programy.net.pl/program,mediaeraser.html)

![image](https://user-images.githubusercontent.com/19593367/211175133-73168ba8-11ea-4b11-8ba2-56c8d6df20dc.png)

Media Eraser 2.0a lite (free) was limited to signle file deletion below 10Kb only. The application user interface provides only file deletion settings. 

![virtualboxcrop](https://user-images.githubusercontent.com/19593367/211220488-9214c21d-0888-4741-bf71-ac6c1980954d.gif)


The full version offered many more features like:

* Recursively erase multiple file and folders from Windows explorer's context menu
* Erase entire partitions (volumes)
* Erase free space, slack space and information about files deleted without MediaEraser
* Erase entire physical hard drives

MediaEraser was fully written in C++ with WTL for GUI. MediaEraser was one of the fastest data erasing tools at the time. 

![me3 0](https://user-images.githubusercontent.com/19593367/209659443-cf010e6b-b200-41b9-8ef4-c3375ca30c4c.gif)



Erase volume settings offered **Complete volume erase (destructive)** and **Partial volume erase (safe)** erase options. 

![me9-volume-settings](https://user-images.githubusercontent.com/19593367/209660629-d5fd5522-4cb9-49e9-87f6-faf3a82a06a9.gif)



**Complete volume erase (destructive)** physically erase entire volume no matter what file system the partition is formatted to. Once the volume is erased it has to be formatted to be accessible by operating system.

![me15-volume](https://user-images.githubusercontent.com/19593367/209661455-52bc60e7-5823-4dc7-9295-7fea07519766.gif)



**Partial volume erase (safe)** option erase free space, slack space and optionally unused MFT entries. Slack space is the area of a hard drive ranging from the end of a stored file to the end of that file cluster. Unused MFT entries holds information about files deleted without MediaEraser. 

![me4-freesace-slack](https://user-images.githubusercontent.com/19593367/209660019-c861324d-26b2-41ca-812f-735a7b9f7594.gif)


Erase drive settings.

![me8-drive-settings](https://user-images.githubusercontent.com/19593367/209660608-4801b31f-0195-4723-8650-169eb96cb73d.gif)


Erase physical drive.

![me6-drive](https://user-images.githubusercontent.com/19593367/209660333-a2edc2be-54f8-49b5-b329-c729aaea3a2a.gif)
 

Erase files from Windows Explorer's context menu.

![me](https://user-images.githubusercontent.com/19593367/209666487-b871f2da-ce07-413d-bac3-36e5ec3b203c.png)


---
###### Year 1999
# Interrupt List Navigator

[Interrupt List Navigator](https://github.com/Jandini/InterruptListNavigator) is a tool written in Delphi 5 to provide a quick search for Interrupt List created by Ralf Brown. 

![image](https://user-images.githubusercontent.com/19593367/212570617-965b459e-e44f-4204-ba95-1f774e14263d.png)

The [Interrupt List](https://raw.githubusercontent.com/Jandini/InterruptListNavigator/main/res/INTER.LST) is a text file with detailed description of 8163 interrupt calls.

![notepad](https://user-images.githubusercontent.com/19593367/212570256-ab1fa619-22e7-41e5-ab48-81efcb80d51f.gif)

The tools offsers quick search by typing interrupt number with AH/AX register value or interrupt description.

![virtualboxcrop](https://user-images.githubusercontent.com/19593367/213120257-f24a4086-5f74-4139-a784-8708056d6208.gif)

Interrupt List Navigator running under Windows 10 with different font.

![interrupts](https://user-images.githubusercontent.com/19593367/212570464-e8172b53-106c-4183-b182-14c5a237476e.gif)

Key features: 

* Serach by interrupt number and AX register.
* Search by iterrupt title.
* Find keyword or phrase in text.
* Print single or multiple interrupt descriptions.
* Change display font.
* Copy interupt description to clipboard.
* Maximize window by pressing F5 key. 


---
###### Year 1998
# Assembler for 8086

It was exciting time writing software using assembler and pascal for DOS. 
You can find all my assembler source codes and binaries in [8086](https://github.com/Jandini/8086) repository.
The code can be executed only under [DosBox](https://www.dosbox.com/). Kudos to the authors for keeping the legacy alive.

Multi-Edit was one of the text editors to write and run assembler code.

![ME_MASZ](https://user-images.githubusercontent.com/19593367/202818994-3e053783-9911-48be-be54-11750ee33fd1.gif)






# Software Reverse Engineering in DOS

I modified software which helped me to learn touch typing. The software was called "Maszynistka" which translates to "Typist". Maszynistka was free to use with the caveat that unregistered version has a splash screen. The splash screen is taking about 15 minutes before you can start using the tool.

I used Turbo Debugger to figure out how to skip the splash screen. This is how I did it... 

![TD_MASZ](https://user-images.githubusercontent.com/19593367/202817851-761425ca-0336-4240-a197-2a9984db452f.gif)

I let the program to execute until I found the splash screen call. I applied simple [NOP slide](https://en.wikipedia.org/wiki/NOP_slide) over the splash screen call. Three bytes only. The challenge was that the code of the program was encoded. I could not make permanent change to MASZ.EXE binaries. 

I wrote my own debugger. The assembler code in [CRACK.ASM](https://github.com/Jandini/8086/blob/main/CRACK/CRACK.ASM) repeats steps required to bypass the splash screen. Instead running MASZ.EXE the program can be executed via CRACK.COM which skips the splash screen.  

Program "Maszynistka" with the splash screen...

![MASZ-SPLASH](https://user-images.githubusercontent.com/19593367/202403492-828171a2-2e4c-411d-8bbb-70e77b00bed5.gif)

... and without the splash screen after running it with [CRACK.COM](https://github.com/Jandini/8086/blob/main/CRACK/CRACK.ASM)

![MASZ-CRACK](https://user-images.githubusercontent.com/19593367/202403750-d7bf8743-2d03-4e1d-a2c0-8b5eba3237f0.gif)


# TSR programs for DOS

[TSR](https://en.wikipedia.org/wiki/Terminate-and-stay-resident_program) is Terminate and Stay Resident program which allowed to run your program in the background and let the DOS operating system continue. 
This is where the journey with concept of viruses starts. 



# Text mode pictures in Assembler

I created a number of picutres in text mode and converted them into assembler code. For example, the picture below was manually created in [X.ASM](https://github.com/Jandini/8086/tree/main/COMPRESS) (1536 bytes) and [compressed](https://github.com/Jandini/8086/blob/main/COMPRESS/COMPRESS.PAS) to C.ASM file (584 bytes). Compressed picture in C.ASM was [converted](https://github.com/Jandini/8086/blob/main/COMPRESS/CONVERT.PAS) to assembler's byte array in [OUT.ASM](https://github.com/Jandini/8086/blob/main/COMPRESS/OUT.ASM). The source code to draw the picture was added later to OUT.ASM code.

The compressed pictures converted to assembler code could easlily fit into a few sectors between MBR and BPB on the hard drive. I used similar idea in [boot loader for two operating systems](https://github.com/Jandini/Jandini/blob/main/README.md#two-operating-systems-on-one-floppy-disk).


[OUT.ASM](https://github.com/Jandini/8086/blob/main/COMPRESS/OUT.ASM)

![COMPRESS](https://user-images.githubusercontent.com/19593367/202412547-cdae0eb8-6506-4fe1-b2cb-262794c50241.gif)

[PICTURE.ASM](https://github.com/Jandini/8086/blob/main/PICTURE/PICTURE.ASM)

![PICTURE](https://user-images.githubusercontent.com/19593367/202411411-d234abaf-d036-4784-9df4-464369b797c2.gif)


# Floppy Disk Boot Loader

I worte boot loader [MULTI.ASM](https://github.com/Jandini/8086/blob/main/MULTI/MULTI.ASM) which allowed me to place two operating systems on a single 1.44MB floppy disk.
I added animated floppy disk picture to the code to make the boot loader a bit more fancy. User can select operating system from the menu.

Microsoft DOS 6.22

![W95-screen0-D622 (online-video-cutter com) 720x400](https://user-images.githubusercontent.com/19593367/202869923-f9ce8ce8-344f-4a5e-8b53-a9e673f08983.gif)

Microsoft DOS 4.00 for Windows 95

![W95-screen0-W95 (online-video-cutter com) 720x400](https://user-images.githubusercontent.com/19593367/202869953-7a4444dc-44f0-4039-8c0b-95d60cdf7b00.gif)

The physical image of the 1.44MB floppy disk is available in the [repository](https://github.com/Jandini/8086/blob/main/MULTI/floppy.flp).
