# UNIDAD-4-BASE-DE-DATOS-EJERCICIO-14
1. Entidades Principales y Tablas del Sistema
miembro: Almacena la información de los usuarios registrados en la plataforma comunitaria. Sus campos principales son id_usuario (clave primaria), tipo_perfil, nombre, apellido, correo y contrasenia.

receta: Registra las recetas de cocina compartidas. Sus atributos incluyen id_receta (clave primaria), dificultad, porciones, titulo, descripcion, tiempo_prep y id_usuario (clave foránea que vincula la receta con el miembro creador).

ingrediente: Contiene el catálogo de alimentos e insumos disponibles. Posee id_ingrediente (clave primaria), nombre, unidad_medida, informacion_nutricional y modo_uso.

2. Tablas de Detalle e Interacción
detalle_receta: Tabla asociativa que relaciona las recetas con los ingredientes necesarios y las cantidades requeridas. Posee una clave primaria compuesta por (id_receta, id_ingrediente) y el campo numérico cantidad.

resenia: Administra las calificaciones y comentarios realizados por los usuarios sobre las recetas. Sus campos son id_resenia (clave primaria), puntuacion, comentario, fecha_publicacion, además de las claves foráneas hacia receta y miembro.

3. Restricciones e Integridad Referencial (Foreign Keys)
fk_detalle_ingrediente y fk_detalle_receta: Conectan el detalle de la receta con los ingredientes y recetas correspondientes.

fk_receta_miembro: Asegura que toda receta pertenezca a un miembro registrado en el sistema.

fk_resenia_miembro y fk_resenia_receta: Garantizan que cada reseña esté vinculada de forma coherente a un autor (miembro) y a una receta válida.

IMAGEN DE EJEMPLO DE UNA CONSULTA:
<img width="1203" height="365" alt="image" src="https://github.com/user-attachments/assets/1ce5a521-f06a-4a30-850a-268dad516c36" />
