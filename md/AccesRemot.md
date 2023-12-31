# AUTORITZACIÓ DE L'ACCÉS REMOT

Des d'un client ( Windows 10 Pro ) creem una Connexió Remota amb el Servidor. Necessitareu:
1.  Que el servidor tinga habilitat l'accés remot.
2.  Que l'usuari en concret estiga habilitat per usar-lo.
3.  Que el Firewall no ho impedisca.
      *  Regla d'entrada bloquejant el protocol
      *  Autorització de l'aplicació de *Escritorio remoto*
   

## 1.  Habilitar el accés de remot al servidor

<img width=60% src="../png/seguretataccescompartitremot/HabilitarPropiedadesdelSistema.png"></img>

Podem comprovar-ho també excutant des del cmd el **sconfig**

<img width=60% src="../png/seguretataccescompartitremot/sconfig.png"></img>

## 2. Modificació de la GPO Default Domain Policy

Obrim la consola d'Administració de Directives de Grup.
Des de l'Administrador de Servidor o excutant **gpmc.msc**

<img width=60% src="../png/seguretataccescompartitremot/GPOControlRemoto1.png"></img>

Editem la Directiva del Domini per Defecte (Default Domain Police).

<img width=60% src="../png/seguretataccescompartitremot/GPOControlRemoto2.png"></img>

Es tracta donar a l'usuari el dret de inciar sessió de forma remota.

<img width=60% src="../png/seguretataccescompartitremot/GPOControlRemoto3.png"></img>

Devem observar el valor per defecte en la pestanya "Explicación". En este cas només podien iniciar sessió d'escriptori remot en el servidor els Administradors de domini.

<img width=60% src="../png/seguretataccescompartitremot/GPOControlRemoto4.png"></img>

<img width=60% src="../png/seguretataccescompartitremot/GPOControlRemoto5.png"></img>

>**Note**
>Recordeu executar el **gpupdate /force**
>En cas contrari no ens permetrà l'autenticació


```
gpupdate /force
```

**Usuario NO autorizado**

Si l'usuari no està autoritzat com hem vist ( o no hem executat el gpupdate ) tindrem este error:


<img width=60% src="../png/seguretataccescompartitremot/controlRemotNOGPOUsuari.png"></img>

## 3.  FIREWALL

Revisem les restriccions possibles del FireWall. 
*  Regles entrants.
*  Aplicacions permeses.

## 3.1  Regles entrants
<img width=60% src="../png/seguretataccescompartitremot/AdministracionRemota.png"></img>

**Bloqueig per Regla de Entrada al protocol**

<img width=60% src="../png/seguretataccescompartitremot/reglaFirewallEscritorioRemotoTCP1.png"></img>


## 3.2 Aplicacions no permeses

<img width=60% src="../png/seguretataccescompartitremot/FirewallEscritorioRemoto.png"></img>

**Bloqueig a l'aplicació "Escritorio remoto"**

<img width=60% src="../png/seguretataccescompartitremot/aplicacionesFirewallBloqueo.png"></img>

El **bloqueig del Firewall** ( tant en un cas com en l'altre ) dona el següent error:

<img width=60% src="../png/seguretataccescompartitremot/reglaFirewallEscritorioRemotoTCP2.png"></img>

## 4. Accès des del client correcte


<img width=60% src="../png/WINDOWSSERVER/8.png"></img>

<img width=60% src="../png/gpo/gpoRemot3.png"></img>


Veiem que existeix un **grup predefinit** d'usuaris d'accès remot:
    Usuario de escritorio remoto.


<img width=60% src="../png/gpo/gpoRemot4.png"></img>




