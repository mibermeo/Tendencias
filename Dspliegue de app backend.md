# Pratica Dspliegue de app backend
***
## Informe de la practica de como desplegar una app backent
### 1.Creamos los contenerdores de Postgres y Pgadmin tal y como lo realiamos en la practica anterior.
![a3](https://user-images.githubusercontent.com/91167276/201827028-9b5afdf3-b463-4b57-be28-b0d82179155a.JPG)
![a4](https://user-images.githubusercontent.com/91167276/201827493-af0a08bf-bd26-4615-9f65-b9ddc2196aeb.JPG)
### 2.Una vez que ya se haya creado los contenedores procedmeos a clonar el git de seguridad que contiene la app.
![Screenshot 2022-11-24 at 18-50-43 Docker Playground](https://user-images.githubusercontent.com/91167276/203875643-c3e17802-2431-4dcb-8c29-2e0c893c63d3.png)
### 3.Accedemos a la carpeta que contiene la aplicacion para modificarlo
![Screenshot 2022-11-24 at 19-00-51 Docker Playground](https://user-images.githubusercontent.com/91167276/203876252-1de478c4-251e-4cd0-89cd-1b7a6472819c.png)
### 4.Editamos la aplicacion.
![Screenshot 2022-11-24 at 19-11-07 Docker Playground](https://user-images.githubusercontent.com/91167276/203876869-e5282bf0-2574-4c19-a028-648c7f23a5a5.png)
### 5.Creamos en contendor maven.
![1](https://user-images.githubusercontent.com/91167276/203877670-a49bdec9-1204-4fe6-835e-35795d678ca0.png)
![2](https://user-images.githubusercontent.com/91167276/203877788-6890ba28-c527-4ad2-b919-5fee585cec1c.png)
### 6.Ahora creamos el docker file.
![3](https://user-images.githubusercontent.com/91167276/203879356-afcaa2ae-84eb-4b25-b934-003d48605605.png)
### 7.Procedemos a crear la imagen de sprint.boot con el comando docker build -t myapp y se nos crea.
![4](https://user-images.githubusercontent.com/91167276/203879852-d38d6d49-e8a1-49bd-9629-0f4e7727f8f9.png)
### 8. Una vez creada la imagen de sprint.boot vamos a crear el contenedor.

