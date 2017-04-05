# Gestió de volums Lògics  
## Descripció del que són  
Els volums lògics són com uns discs durs virtuals a partir del disc dur físic. Aquests es poden particionar, juntar...  
## Què volen dir les següents sigles  
* PV: Physical Volume ~ Identificació dels discs físics. 
---
* ***pvcreate /dev/vda  (crea un PV del disc vda)***  
* ***pvs (llista els pv)***
---
* VG: Volume Group ~ Discs virtuals. Conjunt de PV que formen el VG. El seu tamany varia el tamany dels PV.
---
* ***vgcreate multimedia /dev/vda (crea el disc multimedia a partir del pv anterior)***  
* ***vgs (mostra els VG existents)***
---
* LV: Logical Volume ~ Particions. Particions creades a partir del VG anterior. El seu tamany es pot modificar sempre i quan no superi el del VG. El següent còdig mostra com fer-ho, indicant el volum que li donem i el nom.
---
* ***lvcreate -L +50M -n videos /dev/multimedia***  
* ***lvs (mostra els VL existents)***
---
## Entorn de pràctiques: Explicar com farem la pràctica detalladament (màquina virtual i afegir tres discs de 200M)  
> Per a aquesta pràctica farem servir una virtualització de Fedora 24 amb 3 discs VirtiO de 200 M cadascún, en un equip host Fedora 24.  
## Pràctica 1: Creació d'un volum lògic a partir d'un dels tres discs durs (vda per exemple). Aquest volum lògic ha de ser del total de capacitat del disc. El volum de grup s'ha de dir practica1 i el volum lògic dades.  
Per a crear un volum lògic del total, primer identificarem un dels discs (PV), farem un grup amb aquest PV i crearem un LV amb el total de l'espai existent.
1. Seleccionem el disc dessitjat, en aquest cas /dev/vda :
---
*** pvcreate /dev/vda ***  
---
2. Creem el VG anomenat "practica1" :
---
*** vgcreate practica1 /dev/vda ***
---
3. Creem el volum lògic anomenat "dades" :
---
*** lvcreate -l 100%FREE -n dades /dev/practica1 ***
---
