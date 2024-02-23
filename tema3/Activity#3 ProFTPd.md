En esta practica configuraremos ProFTPD. Vamos a responder a algunas preguntas:

    1. Instala ProFTPd en Ubuntu y comprueba que funciona correctamente. Configura bind9 para que accedamos mediante un dominio del tipo: ftp.marisma.local

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/936c1843-2db9-48fc-b495-2e2ff4363f85)

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/4d793553-7582-45b9-b96c-eaf46e1c1d5a)

Configurar ProFTPd:

añadimos estas lineas en la configuracion:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/779e6988-93da-4214-9ad8-3c56917833d2)

Configuracion del Bind9: 

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/a546eab1-ec30-4e50-92e7-e3b3f0436c63)

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/48edc1e6-53b5-468c-bdc0-120db8cb0409)

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/dc9fe6c4-20ce-4b3b-935c-bf51bbc01ed1)


Crear el archivo de zona /etc/bind/zones/marisma.local.db

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/76e32692-e591-4e84-96d4-656feaa00817)

El estado del servicio:

![image](https://github.com/hasna2223/Serv.-Red-Internet/assets/119622209/ef794d3e-1989-4fb9-a6b5-438183fc56c3)


