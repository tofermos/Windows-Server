# ACCÉS REMOT

Des d'un client ( Windows 10 Pro ) creem una Connexió Remota amb el Servidor. Necessitareu:
* Que el servidor tinga habilitat l'accés remot.
* Que l'usuari en concret estiga habilitat per usar-lo.
* Que el Firewall no tinga cap regla impedint-ho.

<img width=60% src="seguretataccescompartitremot/HabilitarPropiedadesdelSistema.png"></img>

Podem comprovar-ho també excutant des del cmd el **sconfig**

<img width=60% src="seguretataccescompartitremot/sconfig.png"></img>

## Modificació de la GPO Default Domain Policy

Obrim la consola d'Administració de Directives de Grup.
Des de l'Administrador de Servidor o excutant **gpmc.msc**

<img width=60% src="seguretataccescompartitremot/GPOControlRemoto1.png"></img>

Editem la Directiva del Domini per Defecte (Default Domain Police).

<img width=60% src="seguretataccescompartitremot/GPOControlRemoto2.png"></img>

Es tracta donar a l'usuari el dret de inciar sessió de forma remota.

<img width=60% src="seguretataccescompartitremot/GPOControlRemoto3.png"></img>

Devem observar el valor per defecte en la pestanya "Explicación". En este cas només podien iniciar sessió d'escriptori remot en el servidor els Administradors de domini.

<img width=60% src="seguretataccescompartitremot/GPOControlRemoto4.png"></img>

<img width=60% src="seguretataccescompartitremot/GPOControlRemoto5.png"></img>

>**Note**
>Recordeu executar el **gpupdate /force**
>En cas contrari no ens permetrà l'autenticació



Note
Recordeu executar el gpupdate /force En cas contrari no ens permetrà l'autenticació

gpupdate /force

Accès des del client

Firewall

Revisem les restriccions possibles del FireWall.

    Regles entrants.
    Aplicacions permeses.

```
gpupdate /force
```











## Accès des del client

<img width=60% src="WINDOWSSERVER/8.png"></img>

<img width=60% src="gpo/gpoRemot3.png"></img>
<img width=60% src="gpo/gpoRemot4.png"></img>

## Firewall
Revisem les restriccions possibles del FireWall. 
*  Regles entrants.
*  Aplicacions permeses.

<img width=60% src="seguretataccescompartitremot/AdministracionRemota.png"></img>
<img width=60% src="seguretataccescompartitremot/FirewallEscritorioRemoto.png"></img>


