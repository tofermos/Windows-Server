
# Perfils mòbils.

>:Nota: Recordeu si feu importació de màquines virtuals o restaureu imatges, revisar les IP i MAC

Primer crearem una carpeta per a que tots el usuaris del domini guarden el seu perfil. Això, a més facilitarà el Backup si se'ns demana.

1.  Crear un carpeta Perfils.
2.  La compartim ( Permisos SHARE ) amb permisos d'escriptura als usuaris del domini que vullguem.


> Comprovarem inciciant la sessió en dos PC clients amb el mateix usuari.

<img width=70% src="WINDOWSSERVER/permisosPerfils.png"></img>

Assigna l'adreça en les PROPIETATS de cada usuari.
Podeu entrar executant el **dsa.msc**

<img width=60% src="WINDOWSSERVER/permisosPerfils2.png"></img>
<img width=60% src="WINDOWSSERVER/permisosPerfils3.png"></img>

Avantatges:
* Possibilitat d'iniciar la sessió en qualsevol PC client i disposar del teu perfil ( Escriptori, Documents, Baixades...)
* Possibilitat de que l'Operador de còpies de seguretat programe un backup del nostre perfil.
Desavantages:
* La càrrega del perfil des del servidor fins el PC client genera un tràfic a la xarxa local que pot notar-se en iniciar tots el usuaris al mateix temps.
* Els usuaris poden desprocupar-se del tamany de les seues dades i acabar, entre tots, ocupant massa espai de disc dur al servidor.

