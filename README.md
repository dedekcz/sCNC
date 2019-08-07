# sCNC
## Proč a a jak to vzniklo

- Potřeba vyrobit levný a jednoduchý stoj, snadno vyrobitelný v prostředí [PrůšaLabu](https://prusalab.cz/) nebo domácí dílny

- Cvičební stroj pro členy  [PrůšaLabu](https://prusalab.cz/) 

- Komunitní projekt + OpenSource projekt

- Ovládaní stoje jako téma pro další plánované workshopy
- Cílem je obrábění MDF, překližky nebo plexiskla. Hliníkové obrábění není cílem projektu, avšak není úplně vyloučeno.
  

## Aktuální stav / Červenec 2019

Vzhledem ke snadné dostupnosti hliníkových profilů a krokových motorů, byl jako vzor vybrán projekt Dremel CNC [ Dremel CNC -  youtube.com](https://www.youtube.com/results?search_query=dremel+cnc) + ovládací software GRBL *(Arduino Uno + CNC Shield V.3)* s následujícími modifikacemi:

-   Vodicí tyče 8mm na 12mm = zvýšena tuhost a přesnost stroje  
   
-   Předepnuté matice na trapézovém šroubu
    
-   Modifikované díly z plastu (drobné změny v uchyceni koncových spínačů, vložené matice pro lepší uchycení, apod.)  
    
 
## Dokumentace

### Mechanika (Hardware)

 -   Hliníkový profil 3030
     + délka 300 mm x 4 (osa X)
     + délka 600 mm x 2 (osa Y)
 -   Motory NEMA 17
 -   Spojka Motor- vodící tyč x mm (2 ks)
 -   Vodící tyče 12mm:
  	 + délka 345 mm x 2 (osa X) 	 
	 + délka 500 mm x 2 (osa Y)
	 + délka 145 mm x 2 (osa Z) 

 -  Linearní ložisko 12mm x 8
 -  Trapézový šroub
    + délka 320 mm x 2 (osa X) - separatni 
    + délka 500 mm x 1 (osa Y) - integrovany s motorem
    + délka 130 mm x 1 (osa Z) - integrovany s motorem
    
 -   Vodící matice 2ks (osa X)
    
 -   Vodící matice s pružinou 2ks (osa Y)
    

 -   Spojovací materiál
     1. šrouby
     + Imbus s válcovou hlavou
     + Uchycení motorů
     + Uchycení vodící matice
     + Imbus s čočkovou hlavou
     + Uchycení držáku motorů
     2.   matice
     +  4 hraná matice
     +  6 hranná samojístící
     +  Matice do profilu
    
 -   Pracovní deska MDF (358 mm x 600 mm x 18 mm)
    

### Software

-  Controller: [GRBL v1.1f 20170801](https://github.com/gnea/grbl/releases) 
    
-  Ovládací SW:  [bCNC](https://github.com/vlachoudis/bCNC/wiki)
    

### Elektronika
- Dremel 3000

-  Arduino UNO
    
-   CNC Sheild v3
    
-   Řadiče krokových motorů x 4 DRV8825
    
-   Koncové spínače x 3
- Napájecí zdroj 12V / 5A
    

### Konfigurace kroků

### Konfigurace napájení motorů 
Pro každou osu nastaveno 1.2 A viz [https://www.youtube.com/watch?v=AVlee67TQxs](https://www.youtube.com/watch?v=AVlee67TQxs)

## Konfigurace GRBL
```
$0=10
$1=255
$2=0
$3=0
$4=0
$5=0
$6=0
$10=1
$11=0.010
$12=0.002
$13=0
$20=0
$21=1
$22=1
$23=0
$24=500.000
$25=1000.000
$26=250
$27=3.000
$30=1000
$31=0
$32=0
$100=800.000
$101=800.000
$102=800.000
$110=2000.000
$111=2000.000
$112=2000.000
$120=100.000
$121=100.000
$122=100.000
$130=300.000
$131=500.000
$132=60.000
```
## Stack 
[scncworkspace.slack.com](https://scncworkspace.slack.com) 

  

## Budoucnost
- Stavba *verze2.* ve které aplikujeme návrhy na vylepšení, které vznikly během pravidelných setkání každou středu v [PrůšaLabu](https://prusalab.cz/) 


<!--stackedit_data:
eyJoaXN0b3J5IjpbMjAzNzg5NTc1LDEzNjM3MzA0MTUsNzQ3ND
k1MzAzLDE0ODM1MTY4NywtMTk1Mjk5MjU1OF19
-->