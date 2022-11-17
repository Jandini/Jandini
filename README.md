Hi, I'm Matt

This is my software engineering journey. You can find most of the things I was working on and how I developed my software engineering skills.
I will be slowly updating it to include all my personal and professional work and experience. 


# Year 1998

It was exciting time writing software using Assembler and Pascal for DOS. Now it is only the history.
You can find my all assembler source codes and binaries in [8086](https://github.com/Jandini/8086) repository.
The code can be executed only under [DosBox](https://www.dosbox.com/).

## Debugging and software modifications in DOS

This is not something to be proud of. I cracked the software that allowed me to learn touch typing. The software is called "Maszynistka" which translates to "typist". Maszynistka was free and has all the features with the caveat that the unregistered version has a splash screen. 

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

The source code is available here in [CRACK](https://github.com/Jandini/8086/tree/main/CRACK) folder. 

Program "Maszynistka" with and without 🙈 splash screen...

![MASZ](https://user-images.githubusercontent.com/19593367/202326038-f85dea69-d224-47d9-81e6-dcff419f1941.gif)



