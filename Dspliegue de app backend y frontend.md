# Pratica Dspliegue de app backend
***
## Informe de la practica de como desplegar una app backent y frontend
### 1.Creamos una carpeta en donde va a estar nuestro proyecto dentro de esa carpeta vamos a crear otra llamada db.
![Captura de pantalla (1)](https://user-images.githubusercontent.com/91167276/204599362-c6848133-64b5-434d-89d2-c4aa31734860.png)
### 2.Una vez dentro de la carpeta db vamos a crear nuestro archivo yml el cual va a contener nuestros contenedores.
![Captura de pantalla (2)](https://user-images.githubusercontent.com/91167276/204858400-2420f388-d504-4a95-94ed-265e963d8320.png)
### 3.Ejecutamos el archivo yml una vez que ya se haya editado.
![Captura de pantalla (4)](https://user-images.githubusercontent.com/91167276/204860156-704bf559-7120-4670-a1ef-7cd29001ee75.png)
### 4.Ahora nos dirigimos al puerto 8090 para crear un nuevo servidor el cual contendra la base de datos.
![Captura de pantalla (5)](https://user-images.githubusercontent.com/91167276/204861317-467baa60-c5aa-448a-843a-2a152844a6ad.png)
#### 4.1.Colocamos las credenciales que tenemos configurados en el contenedor.
![Captura de pantalla (6)](https://user-images.githubusercontent.com/91167276/204862469-840d4e06-d53e-46fc-ae8f-2a0f0ad73bf6.png)
#### 4.2.Una vez realizado ese proceso tendremos creado el servidor con la base de datos.
![Captura de pantalla (7)](https://user-images.githubusercontent.com/91167276/204863309-48c84c25-79b9-4bd0-b493-b7129873efa7.png)
### 5.Ahora vamos a clonar en la carpeta db el git donde se encuentra el back-end.
![Captura de pantalla (8)](https://user-images.githubusercontent.com/91167276/204864808-f34a071f-8862-4649-be49-ba6176d06ad4.png)
#### 5.1.Una vez clonado vamos a localizar nuestro archivo application.yml para poder editarlo.
![Captura de pantalla (9)](https://user-images.githubusercontent.com/91167276/204867002-6f5f3f41-4e1c-49b8-bd63-239e2b2f5102.png)
#### 5.2.Dentro del archivo editamos el datasource y enableCors. En el datasource ponemos las credenciales del contenedor que creamos anteriormente y en el enableCors ponemos la url 3000.
![Captura de pantalla (10)](https://user-images.githubusercontent.com/91167276/204867936-6f3f82b2-bbf6-415c-a37a-f49161b73e99.png)
### 6.Ahora vamos a buscar el archivo de la configuracion de los Cors para editarlo.
![Captura de pantalla (11)](https://user-images.githubusercontent.com/91167276/204868808-4169de37-b715-4ba4-b949-12a361af5807.png)
#### 6.1.Una vez dentro del archivo lo que haremos sera actualizar el allowebOrigins ahi colocaremos la ruta 3000.
![Captura de pantalla (12)](https://user-images.githubusercontent.com/91167276/204870043-601d363e-5024-4688-8953-899a398408d0.png)
### 7.Ahora nos dirijiremos hacia la carpeta controller para poder editar el archivo.
![Captura de pantalla (13)](https://user-images.githubusercontent.com/91167276/204871298-1770f941-69a3-43ed-ba72-4ba19b46245e.png)
#### 7.1.Nos situamos en los origins el cual actualizaremos por la ruta 3000.
![Captura de pantalla (14)](https://user-images.githubusercontent.com/91167276/204872034-82a6365d-24f8-4d9c-9050-3ca8768a98b7.png)
### 8.Ahora vamos a crear el contenedor maven con el siguiente comando que debe la red del contenedor y la ubicacion del archivo
![Captura de pantalla (15)](https://user-images.githubusercontent.com/91167276/204875084-488ac194-6aa8-4232-96d5-ce22a3f39434.png)
### 9.Una vez creado el maven procedemos el archivo Docker file.
![Captura de pantalla (16)](https://user-images.githubusercontent.com/91167276/204875929-989ee8e2-9d80-4de9-96dc-b6ae3ab12661.png)
#### 9.1.Agregamos lo siguiente en el archivo y guardamos.
![Captura de pantalla (17)](https://user-images.githubusercontent.com/91167276/204876765-132edd33-0df0-4f08-81fe-56fed2b744b0.png)
### 10.Ahora creamos la imagen con el siguiente comando.
![Captura de pantalla (18)](https://user-images.githubusercontent.com/91167276/204877312-aa5e58ad-3077-4edf-8be0-3079444558a0.png)
### 11.Luego de que se crea la imagen creamos el contenedor con el siguien comando.
![Captura de pantalla (19)](https://user-images.githubusercontent.com/91167276/204877806-3b31bf46-f0c3-41d6-b429-880b178f0665.png)
### 12.Para crear el Front-end vamos a dirigirnos a la primera carpeta que creamos y ahi clonaremos el repositorio
![Captura de pantalla (20)](https://user-images.githubusercontent.com/91167276/204878845-a050c6c4-b23c-4195-955f-457a73ef809d.png)
### 13.Nos dirijimos a la carpeta services para editar el archivo
![Captura de pantalla (21)](https://user-images.githubusercontent.com/91167276/204879341-72836522-745a-4fa0-bc66-97c613fb0c0e.png)
#### 13.1.Actualizamos la ruta de urlCrud por la que nos brinda el play with docker para el puerto 8081
![Captura de pantalla (22)](https://user-images.githubusercontent.com/91167276/204879882-556e9534-1634-4e3e-bfaa-6cff639daec1.png)
### 14.Ahora creamos el DockerFile en la carpeta que acabamos de clonar y colococamos lo siguiente dentro del archivo.
![Captura de pantalla (23)](https://user-images.githubusercontent.com/91167276/204880909-5ee1477d-cd24-4008-bd36-e98b18750cf5.png)
### 15.Prodemos a crear la imagen cin el siguiente comando.
![Captura de pantalla (24)](https://user-images.githubusercontent.com/91167276/204881371-004b0bc9-882e-494f-b131-73938f3cf22a.png)
### 16.Una vez creada la imagen vamos a crear el contenedor con el siguiente comando.
![Captura de pantalla (25)](https://user-images.githubusercontent.com/91167276/204882237-075e622d-97e0-4ecc-8b29-847f65d71252.png)
### 17.Procedemos a abrir el puerto 3000 y se nos abrira una nueva ventana donde esta creado el front-end.
![Captura de pantalla (26)](https://user-images.githubusercontent.com/91167276/204882519-923e3a4e-3e43-41d9-8e3b-4db72edf2595.png)
### 18.Le damos en usuario y nos permite ver la informacion que se encuentra en la base de datos.
![Captura de pantalla (27)](https://user-images.githubusercontent.com/91167276/204882781-971e1d79-ce26-44e7-ac20-6df92bf6a15f.png)
## LISTO.
