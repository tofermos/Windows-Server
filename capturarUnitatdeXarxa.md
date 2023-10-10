
# Capturar capturar unitats de xarxa.

Creem una Directiva de Grup que per a que tots els usuaris, en iniciar sessió al domini, tinguen capturada una unitat de xarxa. D'altra forma caldría usar en "net use" des de cada màquina ( scrpit o bat en l'inici)
<img width=90% src="WINDOWSSERVER/GPINICIEditar2.png"></img>

## 2 CONTRASSENYES (Directives de Windows)

## GPO per a les contrassenyes dels usuaris.

Caldrà crear una nova Directiva de Grup, ( entre a la consola amb **gpmc.msc**)
Creem una directiva de grup que vincularem al domini o la UO que ens interesse o al Domini.

<img width=60% src="WINDOWSSERVER/DIRECTIVA CREADA.png"></img>

>**Note** 
>Recordem que hem d'executar **gpupdate /force** per a que els canvis tinguen efecte.
>Des d'*Usuaris i equips de l'AD* , executeu *Restablir Contrassenya* d'algun usuari i proveu la nova directiva.






## CINQUENA PART: Perfils mòbils.

Si només tenim un PC Client. Haurem d'iinstal·lar un segon per poder fer les proves de perfils mòbils.
Recordeu, importeu o cloneu:

*   IP pcClient02 192.168.0.3 /24
*   DNS: 192.168.0.1/24
*   Reviseu el Firewall.

1.  Crear un carpeta Perfils.
2.  Compartir-la i donar permisos d'escriptura als usuaris del domini que vullguem.


> Comprova usant els dos client amb un usuari.

<img width=70% src="WINDOWSSERVER/permisosPerfils.png"></img>

Assigna l'adreça en les PROPIETATS de cada usuari.
Podeu entrar executant el **dsa.msc**

<img width=60% src="WINDOWSSERVER/permisosPerfils2.png"></img>
<img width=60% src="WINDOWSSERVER/permisosPerfils3.png"></img>
