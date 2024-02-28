                                            Activity#6 ProFTPd - TLS

Actividades:

1. Lee el artículo anterior y configura proftp para acceso seguro mediante TLS

Instalar ProFTPD con soporte TLS:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/75a6b599-baf9-4a2d-bdb6-829952cc3411)

Genera certificados TLS:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/51c214b6-aed7-4fc2-b964-4061d1f7d8d7)

Configura ProFTPD para TLS

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/9c5b2049-adf9-43fa-96fb-bac3318ece90)

Guardar y cerrar el archivo de configuración. Reiniciar ProFTPD para aplicar los cambios
sudo service proftpd restart

2. Crea un usuario del sistema

Usando useradd: sudo adduser nombre_de_usuario

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/00f48b46-de5d-4c19-a08e-b37e15e133a2)

3. Instala filezilla

Actualiza la lista de paquetes: sudo apt update

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/29c356e0-457f-4e83-8f5d-816202ff8def)

Instala FileZilla: sudo apt install filezilla

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/db25fe7d-6e7a-4bf8-9423-a335d98c0870)

4. Configura filezilla para usar una conexión TLS y comprueba que funciona correctamente.

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/85e6bab2-98aa-4532-a568-d5e04cd7584c)

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/cde0d30f-787a-419e-a0f9-c17d6ed5aa17)

