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
  1. Capa d'aplicació: Similar a les capes de sessió, presentacío i aplicació del model OSI.
  2. Capa de transport: Similar a la capa de transport del model OSI.
  3. Capa d'internet: Similar a la capa de xarxa del model OSI.
  4. Capa d'accés al medi: Similar a la capa d'enllaç de dades i capa física del model OSI.  
5. A quina capa/capes sol treballar tradicionalment un tallafocs?
  * Del model TCP/IP sol treballa amb la capa de transport i aplicació.

# Tallafocs Linux
1. Busqueu quins són els tradicionals sistemes de tallafocs incorporats en linux i anomeneu-los
  * Són el firewalld(més nou i instal·lat per defecte a partir de F19) i iptables.
2. Quins dels anteriors tallafocs estan instal.lats al fedora de classe? Com ho comproveu?
  * Tenim els dos instal·lats.
  * Els podem veure amb les següents comandes respectivament:
          systemctl status firewalld.service
          iptables --version
3. Algun dels anteriors tallafocs es troba activat?
  * No, els dos estàn apagats.
4. Instal.leu el servidor web httpd o nginx i activeu-ne el servei (dnf installl ...  ; systemctl ....). Indiqueu les comandes i comproveu que des d'una altra màquina podeu accedir via web a la vostra IP (digueu-li a un company). Hauria de sortir la plana per defecte.
  * Comandes per instal·lar nginx:
         # dnf install nginx
         # systemctl status nginx
         # systemctl start nginx
    * Quan un company es conecta, li surt la pàgina per defecte.
5. Activeu el servei firewalld. Indiqueu com ho feu.
  * Al activar el firewall el company ja no es pot connectar amb nosaltres.
         # systemctl start firewalld.service
6. Comproveu si ara es pot seguir accedint.
  * No, no pot accedir.

# Win7
1. Porta aquest SO algun tallafocs incorporat?
  * Si, per defecte porta el firewall de Windows.
2. Arrenqueu una màquina win7 a isard.escoladeltreball.org
3. Indiqueu com arribar al tallafocs (passos i pantalles)
  1. Panel de control -> Sistema y seguridad ->  Firewall de Windows.
4. Es troba activat en aquest windows?
  * Si, es troba activat, tant per a la xarxa privada com a la pública.
5. Busqueu un altre tallafocs per windows. Indiqueu la plana web i les prestacions que ens dona. Intenteu que NOMÉS sigui tallafocs.
 * Comodo Firewall: En la seva versió gratuita, ens permet realitzar operacions tals com controlar aplicacions que acceideixen a Internet, el tràfic que entra o surt del sistema, vigilar ports...
          Pàgina web https://www.comodo.com/home/internet-security/firewall.php


  * ZoneAlarm Free: En la seva versió gratuita, protegeix els accesos no autoritzats i evita l'enviament de dades de virus o spyware.
          sdfisdhfidsf
          https://www.zonealarm.com/es/software/free-firewall/
