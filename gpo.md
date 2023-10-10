# Exemples de GPO


## EXEMPLE 1.  GPO per a capturar unitats de xarxa.

Previament caldrà compartir una carpeta...

Useu la consola **fsmgmt.msc** de CARPETES COMPARTIDES per crear, compartir i assignar permisos NTFS.

Caldrà crear una nova Directiva de Grup. Podem entrar executant **gpmc.msc**
Creem una directiva de grup que vincularem al domini o una UO (que vorem més avant) que ens interesse o al Domini.

<img width=60% src="WINDOWSSERVER/CC1.png"></img>

Des d'esta consola podem gestionar molt millor els recursos compartits ( vore els ocults, eliminar algun que ha desaparegut o canviat, tancar algun fitxer o sessió que haja quedat oberta... ).

Una vegada compartida...

Creem una Directiva de Grup que per a que tots els usuaris, en iniciar sessió al domini, tinguen capturada una unitat de xarxa. D'altra forma caldría usar en "net use" des de cada màquina ( scrpit o bat en l'inici)
<img width=90% src="WINDOWSSERVER/GPINICIEditar2.png"></img>

## EXEMPLE 2. CONTRASSENYES (Directives de Windows)

### GPO per a les contrassenyes dels usuaris.

Caldrà crear una nova Directiva de Grup, ( entre a la consola amb **gpmc.msc**)
Creem una directiva de grup que vincularem al domini o la UO que ens interesse o al Domini.

<img width=60% src="WINDOWSSERVER/DIRECTIVA CREADA.png"></img>

>**Note** 
>Recordem que hem d'executar **gpupdate /force** per a que els canvis tinguen efecte.
>Des d'*Usuaris i equips de l'AD* , executeu *Restablir Contrassenya* d'algun usuari i proveu la nova directiva.


## EXEMPLE 3. ACCÉS REMOT PER A USUARI NO ADMINSITRADOR

Des d'un client ( Windows 10 Pro ) creem una Connexió Remota amb el Servidor. Necessitareu:
* Que el servidor tinga habilitat l'accés remot.
* Que l'usuari en concret estiga habilitat per usar-lo.
* Que el Firewall no tinga cap regla impedint-ho.

>Inicieu una sessió remota des del client i entreu a l'explorador del Servidor.

<img width=70% src="seguretataccescompartitremot/habilitarescritorioremoto.png"</img>

<img width=60% src="WINDOWSSERVER/8.png"></img>

### Modificació de la GPO Default Domain Policy

Si volem iniciar sessió remota al servidor amb un usuari que no és Administrador, ho haurem de configurar, evidentment, per defecte ve inhabilitat.

<img width=60% src="gpo/gpoRemot.png"></img>

<img width=60% src="gpo/gpoRemot2.png"></img>

<img width=60% src="gpo/gpoRemoto3.png"></img>
<img width=60% src="gpo/gpoRemot4.png"></img>


