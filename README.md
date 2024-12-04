# Backend_Desafio03
Pasos para hacer correr el proyecto<br><br>
   1.instalar vite npm install vite<br>
   2.npm init -y<br>
   3.npm install express<br>
   4.npm install pg<br>
   5.instalamos cors npm install cors<br>

creamos el index.js  con los requerimientos de:<br>
-crear una ruta GET que devuelva los registros de la tabla de la BD<br>
-crear una ruta POST que reciba y almacene un nuevo registro.<br>
las funciones las dejamos en consultas.js

datos de prueba:<br>
titulo:<br>
Chris Evans<br>
URL:<br>
https://i.pinimg.com/736x/b9/14/bd/b914bdfc044fef5bc42e29a601709a85.jpg<br>
Descripcion:<br>
Actor conocido por su papel como Capitán América<br>


nota: en la funcion agregarPost del App.js front, cambie url por img<br>
  const agregarPost = async () => {
    const post = { titulo, img: imgSrc, descripcion };
    await axios.post(urlBaseServer + "/posts", post);
    getPosts();
  };<br>
  datos usados en la base de datos:<br>
CREATE TABLE posts (id SERIAL, titulo VARCHAR(25), img VARCHAR(1000),
 descripcion VARCHAR(255), likes INT);

 INSERT INTO posts (titulo, img, descripcion, likes) VALUES
('Robert Downey Jr.', 'https://i.pinimg.com/736x/a6/26/7c/a6267c5922c3308c2e4a1f993e250045.jpg', 'Actor conocido por su papel como Iron Man.', 1500),
('Scarlett Johansson', 'https://i.pinimg.com/736x/fc/b2/fd/fcb2fd0ea0ffd4de11d4b27dad1fa872.jpg', 'Famosa por su papel como Black Widow.', 2000),
('Chris Hemsworth', 'https://i.pinimg.com/736x/b6/49/ea/b649ea2a34390999b28a9e3f5640a003.jpg', 'Conocido por interpretar a Thor en el MCU.', 1800);
drop table posts;
<br>
![Imagen de la página](https://github.com/lalotronic/Backend_Desafio03/edit/main/likeme.png)
  
