# Rest Server con NODE JS y MySQL
Este proyecto consta de un Rest Server utilizando el lenguaje de programacion TypeScript y las tecnologias de NodeJS y MySQL  
Este servidor puede realizar las cuatro operaciones fundamentales en una base de datos Create, Read Update y Delete (CRUD)

## Indice
1. [Instalacion](#Instalacion)
2. [End-points](#Endpoints)
3. [Tecnologias y herramientas utilizadas](#tecnologiasHerramientas)

<h2 id="Instalacion">Instalacion</h2> 

1. [Descargue el archivo zip del proyecto y descomprima](https://github.com/IsaacCuautle/Rest-Server-con-NODE-JS-y-MySQL/releases/download/main/Rest-Server-con-NODE-JS-y-MySQL.zip)
3. Configure las variables de entorno (.env)
4. Inicie una terminal dentro de la carpeta del proyecto y ejecute `npm i` para descargar las dependencias necesarias
5. Mediante su sistema gestor de base de datos (SGBD) de confianza utilize el archivo `node.dump` para restaurar la base de datos y su tabla
6. Dentro de la misma terminal ejecute el comando `node .\dist\app.js` para iniciar el proyecto


<h2 id="Endpoints">End-points</h2> 

### End-point: Create User
esta ruta nos permite crear un usuario, simpre y cuando se cumplan los parametros necesarios para ello en el body de la peticion (incluir un nombre de usuario y un email)
### Method: POST
>```
>localhost:8000/api/users/
>```
#### Body (**raw**)

```json
{
    "name": "Iza",
    "email": "Iza@gmail.com"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: Find Users
En esta ruta podemos obtener todos los usuarios existentes en nuestra base de datos, por lo cual no es necesario incluir parametros en el body
#### Method: GET
>```
>localhost:8000/api/users/
>```

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: Find User
Esta ruta nos permite buscar por un usuario en especifico, para ello basta con conocer su id y colocarlo seguido de una diagonal invertida en la ruta, como ejemplo aqui se busca por el usuario con id 2
#### Method: GET
>```
>localhost:8000/api/users/2
>```

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: Update User
Esta ruta permite actualizar los datos de un usuario existente en la base de datos para ello se debe incluir en el body los campos y sus respectivos cambios (si solo se actualizara un campo se pueden omitir los demas)
#### Method: PUT
>```
>localhost:8000/api/users/11
>```
#### Body (**raw**)

```json
{
    "name": "Izza",
    "email": "Izza@gmail.com"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: Delete User
Esta ruta permite la eliminacion logica de los usuarios, cambiando su estado de 0 a 1, de esta manera se conserva la integridad referencial en la base de datos
#### Method: DELETE
>```
>localhost:8000/api/users/10
>```

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

<h2 id="tecnologiasHerramientas">Tecnologias y herramientas</h2> 

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Nodemon](https://img.shields.io/badge/NODEMON-%23323330.svg?style=for-the-badge&logo=nodemon&logoColor=%BBDEAD)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![NPM](https://img.shields.io/badge/NPM-%23CB3837.svg?style=for-the-badge&logo=npm&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
