
Activity#4 ProFTPd - FTP privado y anónimo

Actividades:

  1. Configura proftpd para que los usuarios accedan al directorio /home/ftp (puedes usar DefaultChdir). ¿Cual es la diferencia entre DefaultRoot y DefaultChdir?

Para configurar ProFTPD para que los usuarios accedan al directorio /home/ftp, podemos hacer uso de la directiva DefaultChdir en el archivo de configuración. Aseguramos de tener los permisos adecuados en el directorio:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/b0512aa8-181d-45f9-bd5d-0401855fcc41)

Guardamos y reiniciar el servicio ProFTPD

sudo service proftpd restart

  2. No se permitirá subir ni eliminar nada de la carpeta ftp
     
Ajustamos la configuración de la siguiente manera:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/17c625e5-7975-47af-949b-835d59ab83c6)

guardar el archivo de configuración y reiniciar el servicio ProFTPD:
sudo service proftpd restart

  3. Configura el acceso mediante usuario anónimo
     
Para ello gregamos lo siguiente, guardar y cerrar:

<Anonymous /home/ftp>
  User ftp
  Group ftp
  AnonRequirePassword on
  AnonRoot /home/ftp
  <Limit WRITE>
    DenyAll
  </Limit>
</Anonymous>

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/a3395c62-72bd-4806-a0ee-9eb8d5c41b7b)

  4. Permite que el usuario anónimo pueda escribir si accede desde la red 10.6.0.x

Para ello, ajustamos la configuración de la siguiente manera:

<Anonymous /home/ftp>
  User ftp
  Group ftp
  AnonRequirePassword on
  AnonRoot /home/ftp
  <Limit WRITE>
    Allow from 10.6.0
  </Limit>
</Anonymous>

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/4f8d231f-7457-4eb6-a952-77008cdd4f0e)
