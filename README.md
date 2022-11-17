Hi, I'm Matt

This is my software engineering journey. You can find most of the things I was working on and how I developed my software engineering skills.
I will be slowly updating it to include all my personal and professional work and experience. 


# Year 1998

It was exciting time writing software using Assembler and Pascal for DOS. Now it is only the history.
You can find my all assembler source codes and binaries in [8086](https://github.com/Jandini/8086) repository.
The code can be executed only under [DosBox](https://www.dosbox.com/).

## Debugging and software modifications in DOS

I "modified" software which helped me to learn touch typing. The software was called "Maszynistka" which translates to "
Typist". Maszynistka was a free software with the caveat that the unregistered version had a splash screen. 
You need about ten minutes of your time and clicking space key before you can start using it. 

I used Turbo Debugger for DOS and figured out how to skip the splash screen. 
Like in many cases it is a simple NOP over the splash screen call.
The challenge was that the code of the software is compressed/encrypted. 
You cannot make the change permanently to MASZ.EXE binaries.

This assembler code is acting as debugger and is doing exactly what I was doing manually with Turbo Debugger:
- Load MASZ.EXE into memory without executing it.
- Set break point after the code is decompressed/decrypted.
- Execute the program and let it decompress/decrypt the code.
- The break point calls the trace and trap procedures to find the code address in memory.
- Apply NOP slide over the call to the splash screen.
- Continue execution of modified code.

Program "Maszynistka" with the splash screen...

![MASZ-SPLASH](https://user-images.githubusercontent.com/19593367/202403492-828171a2-2e4c-411d-8bbb-70e77b00bed5.gif)

... and the same after running it with [CRACK.ASM](https://github.com/Jandini/8086/blob/main/CRACK/CRACK.ASM) written in Assembler.

![MASZ-CRACK](https://user-images.githubusercontent.com/19593367/202403750-d7bf8743-2d03-4e1d-a2c0-8b5eba3237f0.gif)


## Writing [TSRs](https://en.wikipedia.org/wiki/Terminate-and-stay-resident_program) for DOS

TSR is Terminate and Stay Resident program which allowed to run your program in the background and let the DOS operating system continue. 
This is where the journey with concept of viruses starts. 



## Drawing pictures in text mode

The picture was manually created in [X.ASM](https://github.com/Jandini/8086/tree/main/COMPRESS) (1536 bytes) and [compressed](https://github.com/Jandini/8086/blob/main/COMPRESS/COMPRESS.PAS) to C.ASM file (584 bytes). Then compressed picture in C.ASM was [converted](https://github.com/Jandini/8086/blob/main/COMPRESS/CONVERT.PAS) to assembler's byte array in [OUT.ASM](https://github.com/Jandini/8086/blob/main/COMPRESS/OUT.ASM).
The code to draw the picture was added later. 


https://github.com/Jandini/8086/blob/main/COMPRESS/OUT.ASM

![COMPRESS](https://user-images.githubusercontent.com/19593367/202412547-cdae0eb8-6506-4fe1-b2cb-262794c50241.gif)

![PICTURE](https://user-images.githubusercontent.com/19593367/202411411-d234abaf-d036-4784-9df4-464369b797c2.gif)









