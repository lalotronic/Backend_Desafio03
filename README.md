# Backend_Desafio03
Pasos para hacer correr el proyecto
   1.instalar vite npm install vite<br>
   2.npm init -y<br>
   3.npm install express<br>
   4.npm install pg<br>
   5.instalamos cors npm install cors<br>

creamos el index.js  con los requerimientos de:
-crear una ruta GET que devuelva los registros de la tabla de la BD
-crear una ruta POST que reciba y almacene un nuevo registro.
las funciones las dejamos en consultas.js

datos de prueba:
titulo:
Chris Evans
URL:
https://i.pinimg.com/736x/b9/14/bd/b914bdfc044fef5bc42e29a601709a85.jpg
Descripcion:
Actor conocido por su papel como Capitán América


nota: en la funcion agregarPost del App.js front, cambie url por img
  const agregarPost = async () => {
    const post = { titulo, img: imgSrc, descripcion };
    await axios.post(urlBaseServer + "/posts", post);
    getPosts();
  };
