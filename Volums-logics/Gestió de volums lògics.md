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
