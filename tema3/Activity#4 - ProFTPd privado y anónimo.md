
Activity#4 ProFTPd - FTP privado y anónimo

Actividades:

  1. Configura proftpd para que los usuarios accedan al directorio /home/ftp (puedes usar DefaultChdir). ¿Cual es la diferencia entre DefaultRoot y DefaultChdir?

Para configurar ProFTPD para que los usuarios accedan al directorio /home/ftp, podemos hacer uso de la directiva DefaultChdir en el archivo de configuración. Aseguramos de tener los permisos adecuados en el directorio:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/21b0d5d5-3e91-4774-b279-e76f1e7fe1f2)

     
  3. No se permitirá subir ni eliminar nada de la carpeta ftp
     
  4. Configura el acceso mediante usuario anónimo
     
  6. Permite que el usuario anónimo pueda escribir si accede desde la red 10.6.0.x

