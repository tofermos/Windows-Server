# AUTORITZACIÓ DE L'ACCÉS REMOT

Des d'un client ( Windows 10 Pro ) creem una Connexió Remota amb el Servidor. Necessitareu:
1.  Que el servidor tinga habilitat l'accés remot.
2.  Que l'usuari en concret estiga habilitat per usar-lo.
3.  Que el Firewall no ho impedisca.
    3.1  Regla d'entrada bloquejant el protocol
    3.2  Desautorització de l'aplicació de *Escritorio remoto*
   

## 1.  Habilitar el accés de remot al servidor

<img width=60% src="seguretataccescompartitremot/HabilitarPropiedadesdelSistema.png"></img>

Podem comprovar-ho també excutant des del cmd el **sconfig**

<img width=60% src="seguretataccescompartitremot/sconfig.png"></img>

## 2. Modificació de la GPO Default Domain Policy

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


```
gpupdate /force
```

### Usuario NO auorizado

Si l'usuari no està autoritzat com hem vist ( o no hem executat el gpupdate ) tindrem este error:


<img width=60% src="seguretataccescompartitremot/controlRemotNOGPOUsuari.png"></img>
## 3.  FIREWALL

Revisem les restriccions possibles del FireWall. 
*  Regles entrants.
*  Aplicacions permeses.

## 3.1  
<img width=60% src="seguretataccescompartitremot/AdministracionRemota.png"></img>

## 3.2

<img width=60% src="seguretataccescompartitremot/FirewallEscritorioRemoto.png"></img>

Vegem el **bloqueig pel Firewall** del servidor mitjançant una regla d'entrada.

### Bloqueig per Regla de Entrada al protocol

<img width=60% src="seguretataccescompartitremot/reglaFirewallEscritorioRemotoTCP1.png"></img>

### Bloqueig a l'aplicació "Escritorio remoto"

<img width=60% src="seguretataccescompartitremot/aplicacionesFirewallBloqueo.png"></img>

<img width=60% src="seguretataccescompartitremot/reglaFirewallEscritorioRemotoTCP2.png"></img>

## 4. Accès des del client correcte


<img width=60% src="WINDOWSSERVER/8.png"></img>

<img width=60% src="gpo/gpoRemot3.png"></img>
<img width=60% src="gpo/gpoRemot4.png"></img>




