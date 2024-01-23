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




