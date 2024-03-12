# SISTEMES OPERATIUS DE XARXA.  2n SMX-B 2023-2024 PLA DE RECUPERACIÓ. MARÇ-JUNY 2024. 

 

El pla de recuperació consistirà en dos activitats generals amb les quals es repassaran els conceptes més importants del curs.  

 

## Part 1 Windows Server. 

Esta primera part es proposa la realització d’una activitat que contemple els principals apartats referents a la configuració i administració d’un domini amb Windows Server.  

Instal·lació 

Creació i configuració dels objectes de l’Active Directory 

Comptes d’usuari i grups 

Unitats Organitzatives 

Delegació en UO. 

Backups  

RAID1 

Captura/assinació d’unitats de xarxa 

PowerShell 

Permisos Share 

Permisos NTFS 

 

### Activitat de repàs, març de 2023. WINDOWS SERVER 

Tenim una empresa amb 4 departaments que agrupen a diferents usuaris: 

    Comptabilitat:  2 usuaris 

    Administració: 2 usuaris 

    Oficina tècnica: 3 usuaris 

    Servei d’Atenció al Client: 1 usuari. 

Els departaments 1 i 2 comparteixen algunes carpetes, dos impressores i estan ubicats al mateix edifici. 

Els departaments 3 i 4 comparteixen algunes altres carpetes i estan ubicats en un altre edifici.  

L’administrador de la xarxa ha decidit autoritzar a un usuari comptable (del departament de comptabilitat ) i un enginyer ( de l’oficina tècnica ) per que tinguen drets com reiniciar contrasenyes, bloquejar comptes d’usuari o crear algun usuari nou en l’edifici on treballen. 

 

    Indica el total d’objectes d’un servici de directori com Active Directory que caldrien. 

    Una vegada debatut amb els companys, crea l’estructura en el Windows Server instal·lat i un domini que es dirà:  repas.local 

    Els usuaris de cada departament tindran una carpeta particular de treball on guardar documents propis amb el mateix nom que el departament en un disc dur del servidor  

D:\Administracio\nom_usuari 

D:\OficinaTecnica\nom_usuari 

D:\ServeiClient\nom_usuari 

D:\Comptabilitat\nom_usuari 

 

    Accediran a esta carpeta mitjançant la unitat de xarxa Z:\ 

    Assegura’t que els clients tindran IP 192.168.0.x a 192.168.0.254 i que les 10 últimes quedaran disponibles per a l’instal·lador de càmeres IP. 

Hi ha un PC amb MAC xxxx que sempre ha de tenir la 192.168.0.100/24 

    Del disc D:\ volem assegurar que, en cas d’avaria: 

    Poder regenerar-lo a partir d’un espill 

    Disposar d’un backup que es farà en un altre disc E:\ 

    A partir del mes que ve, els usuaris del comptabilitat es connectaran a la xarxa amb portàtils alguns dies o amb PC de l’empresa que no seran sempre el mateix. Caldrà que el perfil no es quede a la màquina sinó al servidor.  

    Crea una carpeta D:\GESTIONS en les que els usuaris de Comptabilitat i Administració puguen fer qualsevol modificació però no crear subcarpetes. 

    Assegura’t que els usuaris de OficinaTecnica i Servici de Client no puguen ni entrar.  

  

## Part 2 .Linux Server.  

  
### Activitat 2.

Esta primera activitat es proposa la realització d’una activitat que contemple els principals apartats referents a la configuració i administració d’un domini amb Linux Server.   

  

    Instal·lació del servidor i el GUI 

    Instal·lació del JExplorer en un client 

    Repeteix els punts 3, 7,8 i 9 de l’activitat de Windows Server 

    Per a la compartició usa SAMBA 

    Assegura’t que la carpeta OficinaTecnica només puga ser accedida des d’unes IP concretes. 

 

# AVALUACIÓ. 

## OPCIÓ 1: 

Realitzar les activitats a les hores de repàs. L'elaboració d’una memòria ( document PDF ) és opcional.  

Superar un qüestionari sobre les activitats i algun aspecte teòric bàsic. 

 
## OPCIÓ 2: 

Examen similar als fets durant el curs. 

 

  
