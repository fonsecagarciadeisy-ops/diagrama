#Base de Datos Biblioteca

Este reto es una base de datos relacional en MySQL que representa una biblioteca sencilla. Almacena libros, sus autores y las editoriales que los publican. El modelo fue diseñado en MySQL Workbench y se consulta mediante SQL.

#Descripción del modelo

La base de datos está compuesta por tres tablas:

Autores: guarda la información de cada autor. Tiene un identificador único (ID_Autor) y el nombre del autor (Nombre_Autor).

Editores: guarda la información de cada editorial. Tiene un identificador único (ID_Editor) y el nombre de la editorial (Nombre_Editor).

Libros: es la tabla central. Contiene el identificador del libro (ID_Libro), su título (Titulo_Libro) y dos llaves foráneas: ID_Autor, que apunta a la tabla Autores, e ID_Editor, que apunta a la tabla Editores.

Relaciones
Un autor puede escribir muchos libros, pero cada libro pertenece a un solo autor (relación uno a muchos entre Autores y Libros).
Una editorial puede publicar muchos libros, pero cada libro es publicado por una sola editorial (relación uno a muchos entre Editores y Libros).

De esta forma, la tabla Libros conecta las otras dos y evita repetir el nombre del autor o de la editorial en cada registro.