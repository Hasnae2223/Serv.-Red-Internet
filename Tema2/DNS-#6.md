Crear un fichero de zona para "marisma.local", además de la zona de resolución inversa:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/027001be-0650-4d3c-9bb4-46ac682eaea9)

Instalar Bind en ambos servidores de nombres
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/d982529d-e1a7-4b43-9783-2c4a48dac466)

sudo apt-get install bind9 bind9utils
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/b793f651-c90b-4403-93fb-99b0a8dc666c)

Configurar el archivo /etc/bind/named.conf.local
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/195dd5b0-199d-433d-b1ab-48a409ea6f41)

Crearemos directorio para las zonas:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/4e4df0a1-2983-421e-8328-c04f41ca4e1d)

Crear archivo de zona para "marisma.local" (/etc/bind/zones/marisma.local.zone):

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/e823da18-ffd4-48cd-8138-912a2a7165e5)

Ahora crearemos archivo de zona inversa:
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/c4e9e8b6-9851-4441-9b2e-3c07fa6b4392)
Ahora reeniciaremos Bind:
sudo systemctl restart bind9
![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/5cb49a98-a532-4f54-bb93-515d38bdf57a)

