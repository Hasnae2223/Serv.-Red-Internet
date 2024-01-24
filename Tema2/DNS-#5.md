En esta practica vamoas a instalar y configurar bin9 en primer lugar como servidor caché y por último como forwarding. 
Para ello, primero hacemos un apdate, y despues instalamos Bind en el servidoor DNS:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/3079a406-e006-4653-b757-c94bce0afaf2)

Ejecutamos el comando siguiente para instalar Bind9: sudo apt-get install bind9 bind9utils bind9-doc: 
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/4b6fca3f-b997-469b-96c1-8877df95a5c3)
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/b32ebacd-fac8-45e8-93ac-0aa7bcac521a)

Ahora que los componentes de Bind están instalados, podemos comenzar a configurar el servidor: 
Configuraramos como servidor DNS de almacenamiento en caché:
Los archivos de configuración de Bind se guardan de forma predeterminada en un directorio en. Movemos a ese directorio ahora ejecutando el siguiente:/etc/bind
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/2e753ae7-0573-4d2d-8e07-f19b3142c3da)

Para un servidor DNS de almacenamiento en caché, solo modificaremos el archivo. Lo abremos en el editor de texto con privilegios sudo:named.conf.options
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/567baa5c-ec81-436b-b08c-67da992e8147)

Para configurar el almacenamiento en caché, el primer paso es configurar una lista de control de acceso o ACL:
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/bf893f61-c764-4906-83e6-b520b0b4e755)

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/4c4d5cd8-61e4-4c76-af14-c5b085abed98)

Después, debemos establecer la directiva en "solo", ya que este servidor reenviará todas las solicitudes y no debe intentar resolver las solicitudes por sí solo.
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/def4ce2f-d219-4788-82dc-a874f414aab6)

Para evitar los errores en el rigistro cambiamos dnssec-validation auto to yes: 
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/28e633df-97ab-443b-bbc3-56fc446e0f59)

Probaremos la configuracion y reiniciaremos el enlace con el comando sudo named-checkconf, si existe algun error nos devuelve el error para corrigir si no se devolvera sin mostrar ningun resultado; 

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/7542e7b6-b8eb-4ec9-8ce3-d70614630e16)

Habilite una excepción a la directiva de firewall para Enlazar escribiendo: con el comando sudo ufw allow Bind9:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/e59f1d16-08be-47b1-8d0b-1313d9807b0a)

Después, vigilaremos los registros del servidor mientras configuraremos la máquina cliente para asegurarse de que todo va bien:
Ejecutaremos el comando siguiente:
sudo journalctl -u bind9 -f
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/2f0d6d47-6d7c-49f2-818e-0cd87472ea50)

Configurar el equipo cliente:
sudo nano /etc/resolv.conf
cambiamos las IPs:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/3874d560-096c-4d8c-b440-ff978805620b)

Ahora probaremos para asegurarse de que las consultas se pueden resolver correctamente mediante  el uso de algunas herramientas comunes:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/3f6dc46b-5594-4f4c-9b1b-6ccb7bde77d1)

Esto significa que nuestro cliente puede conectarse utilizando nuestro servidor DNS.google.com

Podemos obtener información más detallada mediante el uso de herramientas específicas de DNS como . Probamos dig linuxfondation.org

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/0f180e83-27d8-4fd4-9c21-f1ebd9378e16)

Podemos modificar el fichero  de unidad systemd que inicia Bind9:
sudo systemctl edit --full bind9

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/4856aed9-d39e-4a2b-97f1-810fec7b3033)
reeniciamos para implimentar los cambios
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/82d29433-a808-4557-8809-db347fb4c7de)

Hacer que la configuración de DNS del cliente sea permanente

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/7bdbe894-686f-4302-89d5-9ba4393dca33)
Cambiaremos el DNS, guardamos cierramosel archivo. el cliente debe usar esa configuracion en el proximo arranque.
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/9fa930ce-5926-4076-80b2-f3f41251e551)

