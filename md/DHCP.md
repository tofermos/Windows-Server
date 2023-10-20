# EL SERVICI DHCP DE WINDOWS SERVER

Un dels servicis més típics i usats d'un servidor senzill de xarxa és l'assignació dinàmica de IP privades de la xarxa local. Veiem com instal·lem i configurem el servei.

Treballarem amb el protocol IP4

## Instal·lació

<img width=60% src=../png/DHCP/DHCP1.png>


<img width=60% src=../png/DHCP/DHCP2.png>


<img width=60% src=../png/DHCP/DHCP3.png>


<img width=60% src=../png/DHCP/DHCP4.png>


<img width=60% src=../png/DHCP/DHCP5.png>


<img width=60% src=../png/DHCP/DHCP6.png>

## Configuració

<img width=60% src=../png/DHCP/DHCP7.png>

### Creem un rang de IP

**Pasos recomanables** 
* El/s rang/s ha d'abarcar TOTES les volem a la xarxa local. Després indicarem (dins de rang) quines queden excloses:
* Exclourem les que vulguem assignar manualment (estàtiques)... ( servidors, altres routers...). Vorem que el servidor DNS i el Gateway (encaminador) ens el demana ara.
* Exclourem les que posem a disposició d'altri (administrador extern de fotocopiadores de xarxa o de càmeres IP, per exemple).
* Fer les reserves de IP per a determinades MAC: Assignem les IP ( dinàmica) però constant a un dispositiu en concret
  
<img width=60% src=../png/DHCP/DHCP8.png>

### Exclusions

<img width=60% src=../png/DHCP/DHCP9.png>

### Duració de l'assignació

<img width=60% src=../png/DHCP/DHCP10.png>


<img width=60% src=../png/DHCP/DHCP11.png>

### Gateway (porta d'enllaç) o encaminador

Indiquem la IP que hem configurat al router.

<img width=60% src=../png/DHCP/DHCP12.png>


### Servidor DNS

Indiquem la IP que té el servidor amb el servei DNS.

<img width=60% src=../png/DHCP/DHCP13.png>

## Client 

En el client devem canviar la configuració de la NIC i especificar que, ara, la IP l'assignarà el DHCP


### Gateway (porta d'enllaç) o encaminador

Indiquem la IP que hem configurat al router.

<img width=60% src=../png/DHCP/DHCP14.png>







