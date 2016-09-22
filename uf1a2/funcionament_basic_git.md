# Funcionament bàsic del GIT # 

## Clonar GIT al nostre dispositiu ##

Per començar, haurem de clonar el nostre repositori GIT desde el web on ho tinguem (en aquest cas, github) al nostre repositori local, per tal de poguer editar-ho off line i actualitzar-lo després.

1. Seleccionem el directori on volem que es guardi entran-t'hi dins amb **"cd Nomcarpeta"**.
2. Un cop seleccionat, clonarem el directori amb **"git clone url"**
    * Nota: Depenent si volem fer-ho amb HTTP o amb SSH, haurem de ficar la direcció que ens doni el propi GitHub per a cada opció.
3. Entrem al repositori amb **"cd nomrepositori"** i mirem l'estat del git amb **"git status"**. Això ens mostrarà que no hi han canvis.

## Crear nous fitxers, guardar-ho i pujar-los al repositori remot ##

1. Creem l'arxiu que volguem al repositori local.
2. Un cop editat, tornem a mirar l'estat del GIT amb **"git status"** i ens apareixerà que hi han nous arxius.
3. Afegim els nous arxius amb **"git add *"**.
    * Nota: Si volem afegir un sol arxiu seria **"git add nomarxiu"**.
4. Afegim un comentari per a aquest GIT per a poguer consultar-ho al web amb **"git commit -am "missatge""**.
5. Pujem els canvis que hem fet al repositori al web amb **"git push"**.
    * Si seleccionem fer-ho amb HTTP ens demanarà sempre l'usuari i la contrasenya. Si ho fem amb SSH ho pujarà directament (si hem vinculat el nostre compte amb el nostre dispositiu).

## Recuperar els fitxers del repositori remot ## 

1. Entrem al directori del repositori local amb **"cd directori"** .
    * Nota: Si no ho fem on és el repositori, ens donarà error.
2. Utilitzem la comanda **"git pull"** per a baixar-lo.
3. Fem els canvis que volguem o els nous arxius i ho tornem a pujar seguint els passos del punt anterior.
