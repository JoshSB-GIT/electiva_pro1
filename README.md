# README PARA ELECTIVA

### Instalar servidor JSON
```
npm install -g json-server
```
Crear un db.jsonarchivo con algunos datos.
```
{
  "posts": [
    { "id": 1, "title": "json-server", "author": "typicode" }
  ],
  "comments": [
    { "id": 1, "body": "some comment", "postId": 1 }
  ],
  "profile": { "name": "typicode" }
}
```
Iniciar servidor JSON
```
json-server --watch db.json
```
Ahora, si va a http://localhost:3000/posts/1 , obtendrá

{ "id": 1, "title": "json-server", "author": "typicode" }
Además, al realizar solicitudes, es bueno saber que:

Si realiza solicitudes POST, PUT, PATCH o DELETE, los cambios se guardarán de forma automática y segura db.jsonen lowdb .
El JSON del cuerpo de su solicitud debe incluir un objeto, al igual que la salida
```
GET. (por ejemplo {"name": "Foobar"})
```
Los valores de identificación no son mutables. idSe ignorará cualquier valor en el cuerpo de su solicitud PUT o PATCH. Solo se respetará un valor establecido en una solicitud POST, pero solo si aún no se ha tomado.
Una solicitud POST, PUT o PATCH debe incluir un Content-Type: application/jsonencabezado para usar el JSON en el cuerpo de la solicitud. De lo contrario, devolverá un código de estado 2XX, pero sin que se realicen cambios en los datos.
