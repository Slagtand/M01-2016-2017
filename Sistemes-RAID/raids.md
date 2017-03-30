## 1. Resum sistemes RAID
| Tipus   | Nº min discs | Discs fallats | Capacitat      | Read speed | Write speed |
| ------- | ------------ | ------------- | ---------      | ---------- | ----------- |
| RAID 0  | 	2		 |      0	     |      100 %	  | Excel·lent | Excel·lent  |
| RAID 1  | 	2 (max)  |      1        |      50 %      | Molt bona  | Bona        |
| RAID 5  | 	3		 |      1		 | 64(3)-94(+3) % | Molt bona  | Bona        |
| RAID 6  | 	4        |      2        |      50-86 %   | Bona       | Bona        |
| RAID 10 |		4        |  1/mirror     |      50 %	  | Molt bona  | Bona        |
| RAID 50 |		6		 |  1/R5 set	 |      67-94 %	  | Excel·lent | Molt bona   |
| RAID 60 | 	8        |  1/R6 set     |      50-88 %	  | Molt bona  | Bona        |

### 2. Descripció de la metodologia utilitzada a classe per a fer proves amb màquines virtuals.

1. Executant una màquina virtual, hem fet servir un SO que ja teniem instal·lat (en aquest cas, un Debian)
2. Hem creat 3 discs de 200M cadascún per a les proves que farem.
3. Montem una raid 1 amb dos dels discs creats i ho montem a una carpeta per a poguer accedir-hi.
4. Creem un arxiu a la carpeta de la raid i eliminem un dels dos discs. Comprovem, efectivament, que tot i que sol queda un dels dos discs segueix funcionant i que hi podem seguir accedint. Si mirem l'estat de la raid, veiem que ens indica que un dels dos discs ha fallat.
5. Fem la prova d'afegir-hi un disc en calent per substituir el que ha fallat, però no ens deixa sense parar la raid i desmontar-ho del directori.
6. Fem la prova amb una raid 5, seguint els mateixos pasos, i veiem que dóna els mateixos resultats o molt similars.

### 3. Comandes i descripció de les mateixes per tal de crear un sistema RAID1

Per a crear una raid 1 hem de fer servir aquesta comanda

> > ```
> > mdadm --create /dev/md0 --level=1 --raid-devices=2 /dev/vda /dev/vdb
> > ```

*1. Després de "--create" posem el nom de la raid, en aquest cas és md0.*

*2. A "--level" indiquem quin tipus de raid serà, en aquest cas és nivell 1. També admet el nom que té, per exemple mirror.*

*3. A la següent opció "--raid-devices" indicarem el nombre de discs que volem fer servir per a la raid, en aquest cas seràn 2 discs.*

*4. Per últim, seleccionarem els discs que volem fer servir per a la raid, que en aquest cas seràn el **vda** i el **vdb**.*

*Per a sapiguer l'estat de la raid, ho podem fer a **cat /proc/mdstat** o **mdadm --detail /dev/md0** .*

### 4. Comandes i descripció de les mateixes per tal de crear un sistema RAID5

Per a crear una raid 5 hem de fer servir aquesta comanda

> > ```
> > mdadm --create /dev/md0 --level=5 --raid-devices=3 /dev/vda /dev/vdb /dev/vdc
> > ```

*1. Després de "--create" posem el nom de la raid, en aquest cas és md1.*

*2. A "--level" indiquem quin tipus de raid serà, en aquest cas és nivell 5.*

*3. A la següent opció "--raid-devices" indicarem el nombre de discs que volem fer servir per a la raid, en aquest cas seràn 3 discs.*

*4. Per últim, seleccionarem els discs que volem fer servir per a la raid, que en aquest cas seràn el **vda**, el **vdb** i el **vdc**.*

*Per a sapiguer l'estat de la raid, ho podem fer a **cat /proc/mdstat** o **mdadm --detail /dev/md0** .*

### 5. Comandes i descripció de les mateixes per tal de crear un sistema RAID6

Per a crear una raid 6 hem de fer servir aquesta comanda

> > ```
> > mdadm --create /dev/md0 --level=6 --raid-devices=4 /dev/vda /dev/vdb /dev/vdc /dev/vdd
> > ```

*1. Després de "--create" posem el nom de la raid, en aquest cas és md2.*

*2. A "--level" indiquem quin tipus de raid serà, en aquest cas és nivell 6. També admet el nom que té.*

*3. A la següent opció "--raid-devices" indicarem el nombre de discs que volem fer servir per a la raid, en aquest cas seràn 4 discs.*

*4. Per últim, seleccionarem els discs que volem fer servir per a la raid, que en aquest cas seràn el **vda**, el **vdb**, el **vdc** i el **vdd**.*

*Per a sapiguer l'estat de la raid, ho podem fer a **cat /proc/mdstat** o **mdadm --detail /dev/md0** .*

### 6. Comandes i descripció de les mateixes per tal de crear un sistema RAID10

Per a crear una raid 10 hem de fer servir aquesta comanda

> > ```
> > mdadm --create /dev/md0 --level=10 --raid-devices=4 /dev/vda /dev/vdb /dev/vdc /dev/vdd
> > ```

*1. Després de "--create" posem el nom de la raid, en aquest cas és md3.*

*2. A "--level" indiquem quin tipus de raid serà, en aquest cas és nivell 10. També admet el nom que té.*

*3. A la següent opció "--raid-devices" indicarem el nombre de discs que volem fer servir per a la raid, en aquest cas seràn 4 discs.*

*4. Per últim, seleccionarem els discs que volem fer servir per a la raid, que en aquest cas seràn el **vda**, el **vdb**, el **vdc** i el **vdd**.*

*Per a sapiguer l'estat de la raid, ho podem fer a **cat /proc/mdstat** o **mdadm --detail /dev/md0** .*
