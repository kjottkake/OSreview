# Operating Systems Review Questions and Problems.


## Chapter 10 File Systems

1. In an EXT-filesystem, how many inodes does a file have?
	1.1 What the hell are inodes?
	The Linux file system relies on inodes.


2. Hva menes med ekstern og intern fragmentering i forbindelse med en fil?

3. Hva er en fildeskriptor (fd)?

4. Filerharenrekketilhørendemetadata,somforeksempelfilnavn,eier,rettigheter, timestamps etc. Hvor er disse dataene lagret i Linux-filsystemet (EXT)?

5. Hvorforkanfilsystemetbliskadetdersomdatamaskinenfa ̊renkræsjna ̊rdetikke er et journalling filsystem?

6. Beskriv litt fordeler og ulemper med stor og liten blokkstørrelse i filsystemer.

7. Hvordanvilytelsenoppfattesomoperativsystemetbenytterwrite-troughcaching na ̊r man skriver til en minnepenn, sammenlignet med a ̊ skrive til samme min- nepenn uten a ̊ benytte cache? Hva med lesing?

8. Hvorstorefilerkanvihaietfilsystembasertpa ̊inoderogdouble-indirectadresser- ing na ̊r vi antar 32-bits diskblokkadresser og diskblokkstørrelse pa ̊ 8KB?

9. (This question is from Tanenbaum) Is the open system call in UNIX absolutely essential? What would the consequences be of not having it?

10. Antaetfilsystemsombenytterenbitmaptila ̊holderedepa ̊ledige/bruktediskblokker. Filsystemet befinner seg pa ̊ en 4GB diskpartisjon og benytter blokkstørrelse pa ̊ 4KB. Beregn størrelsen pa ̊ bitmap’n.

11. Forklar sa ̊ detaljert du kan hva hvert ledd i kommandolinjen
ls -tr | tail -n 1 | xargs tail -n 2 gjør basert pa ̊ følgende eksempel:
     mysil@spock: ̃$ ls -ltr | tail -n 3
     -rw-rw-r--  1 mysil mysil  113248 juli   5 10:54 a.jpg
     drwx--x--- 13 mysil mysil    4096 juli   9 10:15 Desktop
     -rwxrwxr-x  1 mysil mysil      76 juli   9 11:39 unifi.tftp
     mysil@spock: ̃$ ls -tr | tail -n 3
     a.jpg
     Desktop
     unifi.tftp
     mysil@spock: ̃$ ls -tr | tail -n 1 | xargs tail -n 2
     timeout 60
     put firmware.bin
     mysil@spock: ̃$

12. Skriv en kommandolinje i bash som teller antall PDF-filer (filer som heter noe med pdf) i din hjemmekatalog (home directory).

