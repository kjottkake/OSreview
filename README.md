# Operating Systems Review Questions and Problems.



## Chapter 10 File Systems

1. In an EXT-filesystem, how many inodes does a file have?
	
	1.1 What the hell are inodes?
	https://www.howtogeek.com/465350/everything-you-ever-wanted-to-know-about-inodes-on-linux/
	
	The Linux file system relies on inodes.

	In the Linux ext4 file system, the inode and directory structures work together to provide an underpinning framework that stores all the metadata for every file and directory. They make the metadata available to anyone who requires it, whether that’s the kernel, user applications, or Linux utilities, such as ls, stat, and df.

	Answer: I guess it's got only 1?


2. Hva menes med ekstern og intern fragmentering i forbindelse med en fil?

	2.A What the hell is fragmentation to begin with?

	https://afteracademy.com/blog/what-is-fragmentation-and-what-are-its-types

	In contiguous memory allocation whenever the processes come into RAM, space is allocated to them. These spaces in RAM are divided either on the basis of fixed partitioning(the size of partitions are fixed before the process gets loaded into RAM) or dynamic partitioning (the size of the partition is decided at the run time according to the size of the process). As the process gets loaded and removed from the memory these spaces get broken into small pieces of memory that it can’t be allocated to the coming processes. This problem is called fragmentation.

	2.1 What is external fragmentation?

	https://www.geeksforgeeks.org/difference-between-internal-and-external-fragmentation/

	![External Fragmentation](https://media.geeksforgeeks.org/wp-content/uploads/20200729172413/2581.png)


	2.2 What is internal fragmentation?

	![Internal Fragmentation](https://media.geeksforgeeks.org/wp-content/uploads/20190924115421/Untitled-Diagram-146.png)

	Internal fragmentation happens when the memory is split into mounted size blocks. When a method or a program runs, it uses alloted blocks. Internal fragmentation is then the difference between the required space and the memory allocated. 


3. Hva er en fildeskriptor (fd)?

In layman's terms, all a file descriptor is: is a list of numbers corresponding to what file is open in the OS. This list of numbers are always positive integers. 

A simple example would be you have the following files open with the following file descriptor keeping track of which file is open:

hw.txt    101
oblig.txt 102
listofstuff.txt 103

4.  Filer har en rekke tilhørende metadata, som for eksempel filnavn,
    eier, rettigheter, timestamps etc. Hvor er disse dataene lagret i
    Linux-filsystemet (EXT)?

	It is stored in the inodes.

5.  Hvorfor kan filsystemet bli skadet dersom datamaskinen får en kræsj
    når det ikke er et journalling filsystem?


## Previous Exam Questions:

IMT2282 Operativsystemer - eksamen august 2020

1. Når man ikke bruker fortegn, hva er det største tallet man kan lagre i et 5 bits register?

31

IMT2282 Operativsystemer - eksamen mai 2020

1. Hva er hensikten med å lage abstraksjoner i ett operativsystem?

Vi lager abstraksjoner for å kunne håndtere kompleksitet. Vi gjemmer de komplekse detaljene bak mer enkle abstraksjoner. Slik kan vi lage kode som nytter abstrasjoner, og dermed ikke blir maskinvare-spesifikk.

3. Hvordan benyttes SP og BP til å holde kontroll på en funksjons stack-frame? Hva skjer med disse registrene
når en ny funksjon startes?

Stack pointer og base pointer peker hhv. på topp og bunn av nåværende
stack frame. Når en ny funksjon starter vil returpeker pushes på stacken,
som gjør at SP flytter seg videre automatisk. For å definere ny stack-frame
pusher den nye funksjonen eksisterende BP på stacken før den flytter BP til
å peke samme sted som SP. Alt som fra nå pushes vil legges til den nye
"stack-frame"-en

5. Processes

Hva er busy waiting

At en prosess venter i en while-løkke til en hendelse (typisk en spinlock som endrer verdi) intreffe

6. En mutex er en variabel som

Kan benyttes til å låse kritisk sektor.

7. Når en context switch forekommer så utfører operativsystemet et sett med instruksjoner som velger hvilken
prosess som skal få kjøre som nestemann. Hvorfor er disse instruksjonene alltid tilstede i minne (RAM)?

Fordi context switch må være så raskt som mulig, og det er ikke tid til å hente inn koden fra disk når den skal kjøres, den må være tilstede i minne til enhver tid.






