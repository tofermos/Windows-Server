# Resum
A continuació veiem com es cren o modifiquen les directives de grup. Les directives són el sistema de Windows per gestionar els DRETS (AUTORITZAR o DENEGAR) a  realitzar determinades accions en unes màquines. L'àmbit on s'aplicaran podrà ser el DOMINI o una UNITAT ORGANITZATIVA.

Ací veiem un exemple de la utilització o potència de la Unitat Organitzativa.
# Exemples de GPO

>**Note**
>Executeu des del terminal (Win+r, cmd) l'ordre **gpupdate /force** després de cada modificació. 


## EXEMPLE 1.  GPO per a capturar unitats de xarxa.

Previament caldrà compartir una carpeta...

Useu la consola **fsmgmt.msc** de CARPETES COMPARTIDES per crear, compartir i assignar permisos NTFS.

Caldrà crear una nova Directiva de Grup. Podem entrar executant **gpmc.msc**
Creem una directiva de grup que vincularem al domini o una UO (que vorem més avant) que ens interesse o al Domini.

<img width=60% src="../png/WINDOWSSERVER/CC1.png"></img>

Des d'esta consola podem gestionar molt millor els recursos compartits ( vore els ocults, eliminar algun que ha desaparegut o canviat, tancar algun fitxer o sessió que haja quedat oberta... ).

Una vegada compartida...

Creem una Directiva de Grup que per a que tots els usuaris, en iniciar sessió al domini, tinguen capturada una unitat de xarxa. D'altra forma caldría usar en "net use" des de cada màquina ( scrpit o bat en l'inici)
<img width=90% src="../png/WINDOWSSERVER/GPINICIEditar2.png"></img>

## EXEMPLE 2. CONTRASSENYES (Directives de Windows)

### GPO per a les contrassenyes dels usuaris.

Caldrà crear una nova Directiva de Grup, ( entre a la consola amb **gpmc.msc**)
Creem una directiva de grup que vincularem al domini o la UO que ens interesse o al Domini.

<img width=60% src="../png/WINDOWSSERVER/DIRECTIVA CREADA.png"></img>

>**Note** 
>Recordem que hem d'executar **gpupdate /force** per a que els canvis tinguen efecte.
>Des d'*Usuaris i equips de l'AD* , executeu *Restablir Contrassenya* d'algun usuari i proveu la nova directiva.


## EXEMPLE 3. ACCÉS REMOT PER A USUARI NO ADMINISTRADOR

Des d'un client (Windows 10 Pro) creem una Connexió Remota amb el Servidor. Necessitareu:
* Que el servidor tinga habilitat l'accés remot.
* Que l'usuari en concret estiga habilitat per usar-lo.
* Que el Firewall no tinga cap regla impedint-ho.

>:link: Consulteu el tema de **Accés per control remot**
>Inicieu una sessió remota des del client i entreu a l'explorador del Servidor.



<img width=60% src="../png/WINDOWSSERVER/8.png"></img>

### Modificació de la GPO Default Domain Policy

Si volem iniciar sessió remota al servidor amb un usuari que no és Administrador, ho haurem de configurar, evidentment, per defecte ve inhabilitat.

<img width=60% src="../png/gpo/gpoRemot.png"></img>

<img width=60% src="../png/gpo/gpoRemot2.png"></img>

<img width=60% src="../png/gpo/gpoRemoto3.png"></img>
<img width=60% src="../png/gpo/gpoRemot4.png"></img>


