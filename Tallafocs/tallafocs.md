# Tallafocs
1. Què es un sistema tallafocs? Quina és la seva finalitat?
  * Un sistema firewall és un sistema de seguretat de xarxa que controla les connexions que entren i surten en una xarxa basat en unes normes de seguretat.
2. Quines generacions de tallafocs hi ha hagut i què millorava cadascun?
  * Hi han 3 generacions de tallafocs:
    * Generació 1: Filtratge de paquets
      * La primera generació mirava les adreces de xarxa i els ports dels paquets i determinava si els acceptava o els bloquejava. Va ser creat el 1988.
    * Generació 2: Filtres d'estat
      * La segona generació operava també amb la 4ª capa del model OSI, la capa de transport, i assignava uns estats als paquets. Aquests estats podien ser:
        * Principi d'una nova connexió
        * Paquets d'una connexió existent
        * Ninguna connexió coneguda.
      * Es va crear durant els anys 1989-1990
    * Generació 3: Capa d'aplicació
      * La tercera generació és un aplicatiu que "entén" certes aplicacions i protocols, com el FTP, DNS i HTTP. Això és útil per a detectar si algúna aplicació/servei que no volem intenta accedir, aixi podem bloquejar l'accés, o si estàn utilitzant algún protocol per saltar-se el firewall.  
      Hi han hagut diferents versions, però la més nova és la del 2012 que conté:
        * IPS: Intrusion Prevention System. Sistema de prevenció d'intrusions.
        * Identificació de l'usuari
        * WAF: Web Application Firewall. Aplicatiu tallafocs per a web.
3. Quines capes té el model OSI?
  * Les capes del model OSI son:
    1. Nivell d'aplicació
    2. Nivell de presentació
    3. Nivel de sessió
    4. Nivell de transport
    5. Nivell de xarxa
    6. Nivell d'enllaç de dades
    7. Nivell físic
4. Quines capes té el model TCP/IP? En aquest cas feu una breu descripció de les funcionalitats de cada capa.
  1. Capa
5. A quina capa/capes sol treballar tradicionalment un tallafocs?

# Tallafocs Linux
1. Busqueu quins són els tradicionals sistemes de tallafocs incorporats en linux i anomeneu-los
2. Quins dels anteriors tallafocs estan instal.lats al fedora de classe? Com ho comproveu?
3. Algun dels anteriors tallafocs es troba activat?
4. Instal.leu el servidor web httpd o nginx i activeu-ne el servei (dnf installl ...  ; systemctl ....). Indiqueu les comandes i comproveu que des d'una altra màquina podeu accedir via web a la vostra IP (digueu-li a un company). Hauria de sortir la plana per defecte.
5. Activeu el servei firewalld. Indiqueu com ho feu.
6. Comproveu si ara es pot seguir accedint.

# Win7
1. Porta aquest SO algun tallafocs incorporat?
2. Arrenqueu una màquina win7 a isard.escoladeltreball.org
3. Indiqueu com arribar al tallafocs (passos i pantalles)
4. Es troba activat en aquest windows?
5. Busqueu un altre tallafocs per windows. Indiqueu la plana web i les prestacions que ens dona. Intenteu que NOMÉS sigui tallafocs.
