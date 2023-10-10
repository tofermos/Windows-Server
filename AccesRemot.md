# ACCÉS REMOT

Des d'un client ( Windows 10 Pro ) creem una Connexió Remota amb el Servidor. Necessitareu:
* Que el servidor tinga habilitat l'accés remot.
* Que l'usuari en concret estiga habilitat per usar-lo.
* Que el Firewall no tinga cap regla impedint-ho.

>Inicieu una sessió remota des del client i entreu a l'explorador del Servidor

<img width=60% src="seguretataccescompartitremot/habilitarescritorioremoto.png"></img>

<img width=60% src="WINDOWSSERVER/8.png"></img>

## Modificació de la GPO Default Domain Policy

Si volem iniciar sessió remota al servidor amb un usuari que no és Administrador, ho haurem de configurar, evidentment, per defecte ve inhabilitat.

<img width=60% src="gpo/gpoRemot.png"></img>

<img width=60% src="gpo/gpoRemot2.png"></img>

<img width=60% src="gpo/gpoRemot3.png"></img>
<img width=60% src="gpo/gpoRemot4.png"></img>
