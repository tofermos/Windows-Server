# Unitats Organitzatives en Windows Server (GUI)
Les UO son agrupacions o subdivisions del domini per tal de facilitar l'administració. Contenen recursos i objectes.
Estes subdivisions poden fer-s'hi en base a 3 criteris:

1-  Geogràfic o territorial ( Les típiques delegacions de les empreses )
2-  Organització interna ( agrupant departaments de l'empreses que poden equivaldre a grups d'usuaris...)
3-  Dinàmiques, de projectes on van incorporant-se o abandonant usuaris per exemple.

## Creació

<img width=60% src="UO/UO1.png"></img>

Podem aniuar-les ( unes dins d'altres ) i fer que hereten les "propietats"

## Proteccio contra eliminació i canvi accidental
Quan intentem moure o eliminar una UO tenim un missatge avisant que el canvi pot fer que deixen d'alicar-se directives o afectar als usuaris que la controlen (per exemple).
<img width=60% src="UO/uoMoverAviso.png"></img>

Si acceptem veiem que és habitual que no ens deixe.

<img width=60% src="UO/uoMoverNoPermiso.png"></img>

Per defecte es creen protegides per evitar eliminacions o canvis d'ubicació accidentals. Ho hem de desprotegir prèviament.

<img width=60% src="UO/uoVerCaracteristicasAvanzadas.png"></img>


<img width=60% src="UO/uoPtotegerContraEliminacion.png"></img>

# Delegació 

És interessant que assignem el control dels objectes i recursos de la delegació territorial/secció de l'empresa/projecte a un usuari.

<img width=60% src="UO/uo1.png"></img>

El més habitual serà que l'usuari siga Adminsitrador i puga iniciar sessió de forma remota.
