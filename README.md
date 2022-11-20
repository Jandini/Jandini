Hi, I'm Matt Janda

I would like to share my software engineering journey over the years. You can find most of the things I was working on and how I developed my software engineering skills.

I will be slowly updating it to include all my personal and professional work and experience. 


Here is what I was up to... 

* [Year 1998](https://github.com/Jandini/Jandini/blob/main/README.md#year-1998)
  * [Reverse Engineering in DOS](https://github.com/Jandini/Jandini/blob/main/README.md#software-reverse-engineering-in-dos)
  * [Writing TSRs for DOS](https://github.com/Jandini/Jandini/blob/main/README.md#writing-tsrs-for-dos)
  * [Drawing and compressing pictures in text mode](https://github.com/Jandini/Jandini/blob/main/README.md#drawing-and-compressing-pictures-in-text-mode)
  * [Two operating systems on one floppy disk](https://github.com/Jandini/Jandini/blob/main/README.md#two-operating-systems-on-one-floppy-disk)

# Year 1998

It was exciting time writing software using Assembler and Pascal for DOS. Now it is only the history.
You can find my all assembler source codes and binaries in [8086](https://github.com/Jandini/8086) repository.
The code can be executed only under [DosBox](https://www.dosbox.com/). Kudos to the authors to keep the legacy alive.

Multi-Edit was one of thr text editors to edit assembler code. Keyboard only... We were raised in the age where computer mouse 🖱️ was a rare thing...  

![ME_MASZ](https://user-images.githubusercontent.com/19593367/202818994-3e053783-9911-48be-be54-11750ee33fd1.gif)

I used Borlad Pascal to write and run code written in Pascal language...



## Software Reverse Engineering in DOS

I modified software which helped me to learn touch typing. The software was called "Maszynistka" which translates to "Typist". Maszynistka was free to use with the caveat that unregistered version has a splash screen. 
You needed about 15 minutes of your time before you could using it; including the fact you had to press a key on you keyboard multiple times during the splash screen. 

I used Turbo Debugger to figure out how to skip the splash screen. It was fun repeating it after so many years to get a gif here. It took only 2 minutes but then it took much longer.

![TD_MASZ](https://user-images.githubusercontent.com/19593367/202817851-761425ca-0336-4240-a197-2a9984db452f.gif)



It is a simple [NOP slide](https://en.wikipedia.org/wiki/NOP_slide) over the splash screen call.
The challenge was that the code of the program was encoded. 
You cannot make permanent change to MASZ.EXE binaries so you can run it directly. I wrote my own "debugger"... 

The code repeats my steps I have done maunally in Turbo Debugger:
- Load MASZ.EXE into memory without executing it.
- Set a few break points and jump over these far returns until the code decoded.
- Find the address where the call to splash screen ends up in the decoded code in memory.
- Apply [NOP slide](https://en.wikipedia.org/wiki/NOP_slide) over the call to the splash screen.
- Continue execution of modified code.

Program "Maszynistka" with the splash screen...

![MASZ-SPLASH](https://user-images.githubusercontent.com/19593367/202403492-828171a2-2e4c-411d-8bbb-70e77b00bed5.gif)

... and the same program without splash screen after running it with [CRACK.COM](https://github.com/Jandini/8086/blob/main/CRACK/CRACK.ASM)

![MASZ-CRACK](https://user-images.githubusercontent.com/19593367/202403750-d7bf8743-2d03-4e1d-a2c0-8b5eba3237f0.gif)


## Writing [TSRs](https://en.wikipedia.org/wiki/Terminate-and-stay-resident_program) for DOS

TSR is Terminate and Stay Resident program which allowed to run your program in the background and let the DOS operating system continue. 
This is where the journey with concept of viruses starts. 



## Drawing and compressing pictures in text mode

The picture was manually created in [X.ASM](https://github.com/Jandini/8086/tree/main/COMPRESS) (1536 bytes) and [compressed](https://github.com/Jandini/8086/blob/main/COMPRESS/COMPRESS.PAS) to C.ASM file (584 bytes). Then compressed picture in C.ASM was [converted](https://github.com/Jandini/8086/blob/main/COMPRESS/CONVERT.PAS) to assembler's byte array in [OUT.ASM](https://github.com/Jandini/8086/blob/main/COMPRESS/OUT.ASM).
The code to draw the picture was added later. 

Why would you like to compress a code of picture that is only 1.5KB ?... Well, You might want to inject your code in the place where every byte count; for example MBR or BPB of your hard drive. 


[OUT.ASM](https://github.com/Jandini/8086/blob/main/COMPRESS/OUT.ASM)

![COMPRESS](https://user-images.githubusercontent.com/19593367/202412547-cdae0eb8-6506-4fe1-b2cb-262794c50241.gif)

[PICTURE.ASM](https://github.com/Jandini/8086/blob/main/PICTURE/PICTURE.ASM)

![PICTURE](https://user-images.githubusercontent.com/19593367/202411411-d234abaf-d036-4784-9df4-464369b797c2.gif)


## Two operating systems on one floppy disk

I worte boot loader [MULTI.ASM](https://github.com/Jandini/8086/blob/main/MULTI/MULTI.ASM) which allowed me to put two operating systems on one floppy disk.
To make it a bit fancy I added animated floppy disk to the code. User can select operating system from the menu.

Microsoft DOS v6.22

![W95-screen0-D622 (online-video-cutter com) 720x400](https://user-images.githubusercontent.com/19593367/202869923-f9ce8ce8-344f-4a5e-8b53-a9e673f08983.gif)

Microsoft DOS v4.00 for Windows 95

![W95-screen0-W95 (online-video-cutter com) 720x400](https://user-images.githubusercontent.com/19593367/202869953-7a4444dc-44f0-4039-8c0b-95d60cdf7b00.gif)




# Year 2020



## Capture The Flag 

Created simple [.NET framework for playing CTF](https://github.com/Jandini/Janda.CTF). 

![71ds4p](https://user-images.githubusercontent.com/19593367/202848932-82facb7b-1815-49d8-9491-4ce78b8d2a9d.gif)



Participated in Capture The Flag events organized by [SANS](https://www.sans.org/uk/) on [My ranges.io](https://ranges.io/my-events?filter=finished)

| Name                                           | Finished At              | Challenges             | Position                 | Points                        |
| ---------------------------------------------- | ------------------------ | ---------------------- | ------------------------ | ----------------------------- |
| **SANS Community CTF**                         | 14:00 on 17 Oct 2020 BST | **35** of 37 completed | **21**st of 1055 players | **12,750** of 13,500 possible |
| **SANS Community CTF - November**              | 13:00 on 23 Nov 2020 GMT | **61** of 62 completed | **27**th of 1690 players | **19,850** of 20,350 possible |
| **Cyber Camp 2020**                            | 04:59 on 7 Jan 2021 GMT  | **37** of 39 completed | **26**th of 360 players  | **10,050** of 11,550 possible |
| **Global Community CTF: Mini BootUp**          | 18:00 on 19 Feb 2021 GMT | **32** of 32 completed | **17**th of 360 players  | **8,500** of 8,500 possible   |
| **Intermediate: Global Community CTF: BootUp** | 23:00 on 23 Apr 2021 BST | **13** of 24 completed | **88**th of 1293 players | **2,300** of 7,500 possible   |
| **Global Community CTF: Bootup**               | 23:00 on 16 Oct 2021 BST | **36** of 45 completed | **20**th of 889 players  | **1,934** of 4,630 possible   |







