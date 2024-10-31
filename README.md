Comando para obtener la imagen de Docker:

docker pull juanjo440/api:v2

Comando para ejecutar el contenedor de Docker:

docker run -d -p 8080:8080 juanjo440/api:v2

Lista de estudiantes:
http://localhost:8080/estudiantes

Detalles de estudiantes por actividad, deoende de actividad_id:
http://localhost:8080/estudiantes/actividad?actividad_id=1

Lista de actividades:
http://localhost:8080/actividades

Detalles de actividad por ID:
http://localhost:8080/actividades/get?id=1
