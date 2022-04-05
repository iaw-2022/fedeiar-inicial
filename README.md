# Proyecto Inicial

## Idea a Implementar

La idea general de lo que se quiere implementar es un sitio web de videos de speedruns de diferentes videojuegos, donde los usuarios puedan registrarse en el sitio y subir sus speedruns de un determinado videojuego y de una determinada categoría (any%, low%, 100%, etc.), y competir por ver quién completa el videojuego en el menor tiempo posible en una dada categoría.

## Diagrama ER

![diagrama ER - proyecto IA Web](https://user-images.githubusercontent.com/42450883/161850154-8690e92e-923d-467a-85c0-1085ecde8742.jpg)

## Actualizaciones a los datos

El proyecto Framework PHP - Laravel permitirá:

- A los usuarios registrados comúnes:

1. Subir videos de speedruns como links de youtube o twitch incrustados sobre un determinado videojuego.
2. Puntuar otros videos de otros usuarios.
3. Realizar comentarios sobre los distintos videos.
4. Solicitar a los administradores que agreguen un videojuego o categoría sobre el cual puedan subir videos.

- A los usuarios administradores:

1. Lo mismo que pueden realizar los usuarios comúnes.
2. Agregar un videojuego para que los usuarios puedan subir speedruns del mismo.
3. Eliminar videos.
4. Banear usuarios (no permitirles subir más videos, ni puntuar o comentar otros videos).
5. Agregar categorías especiales a los videojuegos (además de las por defecto: any%, low&, 100%, glitchless).

## Información del Servicio Web

- El sitio web permitirá acceder a los distintos videos subidos por los distintos usuarios, buscando por:

1. El nombre del videojuego al que pertenecen. El usuario tendrá 2 opciones: una lista con todos los videojuegos registrados por los administradores, o escribiendo en un campo de texto el nombre del videojuego, mientras debajo del campo puede ver una lista desplegable con las primeras n opciones más "parecidas" al texto que escribe el usuario.
2. El nombre del video. El usuario escribe en un campo de texto el nombre del video y se despliega la misma lista mencionada anteriormente.
3. El nombre del usuario que los subió. El usuario escribe en un campo de texto el username del autor, y en el perfil del autor, puede ver una lista con todos los videos que subió.

Por cada video, además del nombre y el usuario que lo subió, podremos ver: los comentarios que los distintos usuarios escribieron sobre el mismo; sus puntuaciones positivas y negativas; y la posición que ocupan en el ranking (según su tiempo de completación) del videojuego y categoría al cuál corresponden.

- El sitio web también mantendrá perfiles por cada usuario, y por cada uno almacenará la siguiente información:

1. Nombre de usuario.
2. Mail del usuario.
3. Nacionalidad del usuario.
4. Videos subidos por el usuario.
5. Comentarios realizados por el usuario.

Para buscar el perfil de un usuario, habrá un campo de texto como se mencionó anteriormente.

## Visualización y Acceso a la Información

- Cada video tendrá su propia página, en la que se mostrará la siguiente información:

1. El video en cuestión, que será un video incrustado de youtube o twitch.
2. El videojuego y categoría al cuál pertenece.
3. El usuario que lo subió.
4. El tiempo que demoró en completarlo.
5. Las puntuaciones positivas y negativas.
6. Una lista con los comentarios, ordenados por fecha.

Para acceder a los videos, puede hacerse mediante listas o completando un campo de texto con el nombre del video. La visualización de los mismos dependerá de cómo se busca el video:

1. Si buscamos los videos de un determinado videojuego y de una determinada categoría, estos se muestran en una lista, ordenada de menor a mayor según el tiempo de completación del videojuego (es decir, según su ranking), y cada fila contiene: posición en el ranking, username del autor, tiempo de completación, y un hipervínculo que redirige al usuario a la pestaña que contiene el video y toda su información relacionada.
2. Si buscamos un video particular por su nombre, simplemente se nos redirige a su página.
3. Si buscamos los videos de un determinado usuario, estos se muestran en una lista ordenada según la fecha en el que el usuario subió los videos, donde cada fila tiene la misma información que en el item 1.

- Para poder ver todos los videojuegos registrados por los administradores, el usuario puede acceder a un listado de todos los videojuegos, y buscar algún videojuego en la lista (la cual estará ordenada alfabéticamente), o poder filtrar el videojuego que busca en un campo de texto. Al hacer click sobre algún videojuego, se redirige al usuario a una pestaña con todos los videos de ese videojuego listados, de una determinada categoría elegida por defecto. El usuario también puede elegir la categoría.

- Para poder ver los perfiles de los usuarios registrados, el usuario puede buscar en un campo de texto el nombre del usuario en cuestión, o si está en la pestaña de un determinado video, puede clickear en el nombre del usuario que lo subió, y debería redirigirlo al perfil del autor. De la misma forma, si está leyendo un comentario sobre un video, puede clickear sobre el nombre del usuario que escribió el comentario para ver su perfil.
