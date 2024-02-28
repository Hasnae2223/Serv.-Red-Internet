
                                            Activity#5 ProFTPd - Virtual Host


Actividades:
1. Crea un directorio para el usuario virtual “informatica” en /home/ftp/informatica

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/250d8157-77fd-4c5e-ac27-444b54f3d4fb)

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/d4b7b32b-ed7f-4692-9f5c-2520d5349160)

2. Cambia el propietario del directorio creado anteriormente mediante “chown” al usuario ftp

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/1d46bd91-88f1-47d6-835b-9d0404389f6d)

3. Crea un usuario virtual “informatica” mediante “ftpasswd”

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/f3396111-b9a6-4aaa-b241-f3cee2251503)

4. Haz los cambios necesarios en el fichero de configuración de proftpd

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/b2b52c9e-4cc2-4fd1-833a-f2a9a01a6258)

Guarda y cierra el archivo de configuración.

Reinicia el servicio ProFTPD para aplicar los cambios: sudo service proftpd restart

5. Crea un sitio virtual para “informatica.marisma.local”

sudo nano /etc/proftpd/proftpd.conf

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/45d09a97-60d7-48ee-8914-76d35266034e)

Guarda y cierra el archivo de configuración. 

Reinicia el servicio ProFTPD para aplicar los cambios: sudo service proftpd restart

6. Modifica el fichero de zona del DNS para que resuelva adecuadamente

Para ello abrimos el archivo de zona 

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/8d37dc61-4258-4154-b926-7cf9f0e5a916)

Agregamos una entrada para "informatica.marisma.local"
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/b2f0cbf7-6695-4bd8-b2b9-b66b651f83a1)

Guarda y cierra el archivo.

Reinicia el servidor DNS para aplicar los cambios. sudo service bind9 restart

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/3eb7690e-2810-4bea-b02f-85c6460a3c2e)
