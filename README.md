
#TESTING ROUTES
  
*** GET ***  
~~~
http://localhost:8080/api/products/
~~~
![alt text](./src/public/images/image.png)

*** GET WITH LIMIT ***
~~~
http://localhost:8080/api/products?limit=2
~~~
![alt text](./src/public/images/image-1.png)


*** GET WITH ONLY ONE ID ***
~~~
http://localhost:8080/api/products/65c3c3dc9f4f587f03702d27
~~~
![alt text](./src/public/images/image-2.png)


*** POST ADDING PRODUCT ***
~~~
http://localhost:8080/api/products/
~~~
![alt text](./src/public/images/image-3.png)


*** PUT (update or modify) ***
~~~
http://localhost:8080/api/products/65c38fa361c4b50ea3a967ee
~~~
![alt text](./src/public/images/image-5.png)


*** DELETE ***
~~~
http://localhost:8080/api/products/65cd149f5395807bae01c23d
~~~
![alt text](./src/public/images/image-6.png)


*** SHOW PRODUCTS HANDLEBARS & DB ***
~~~
http://localhost:8080/
~~~
![alt text](./src/public/images/image-7.png)


*** REALTIME PRODUCTS (add and delete) ***
~~~
http://localhost:8080/realtimeproducts
~~~
![alt text](./src/public/images/image-8.png)


*** CHAT WITH MONGO ATLAS ***
~~~
http://localhost:8080/chat
~~~
![alt text](./src/public/images/image-9.png)
![alt text](./src/public/images/image-10.png)


*** POST CART (creating new cart) ***
~~~
http://localhost:8080/api/carts/
~~~
![alt text](./src/public/images/image-11.png)


*** GET CART WITH PRODUCTS ***
~~~
http://localhost:8080/api/carts/65c3fe3f50b2ba8808589904
~~~
![alt text](./src/public/images/image-12.png)


*** POST (adding new product to cart, "quantity" is needed)**
~~~
http://localhost:8080/api/carts/65c755ca554811a89e0606e8/product/65c3c3dc9f4f587f03702d27
~~~
![alt text](./src/public/images/image-13.png)



#Aspectos a incluir

1- Agregar el modelo de persistencia de Mongo y mongoose a tu proyecto.✅

2- Crear una base de datos llamada “ecommerce” dentro de tu Atlas, crear sus 
colecciones “carts”, “messages”, “products” y sus respectivos schemas.✅

3- Separar los Managers de fileSystem de los managers de MongoDb en una sola
carpeta “dao”. Dentro de dao, agregar también una carpeta “models” donde vivirán
los esquemas de MongoDB. La estructura deberá ser igual a la vista en esta clase. ✅

4- Contener todos los Managers (FileSystem y DB) en una carpeta llamada “Dao”. ✅

5- Reajustar los servicios con el fin de que puedan funcionar con Mongoose en
lugar de FileSystem. ✅

6-NO ELIMINAR FileSystem de tu proyecto.✅

7- Implementar una vista nueva en handlebars llamada chat.handlebars, la 
cual permita implementar un chat como el visto en clase. Los mensajes deberán
guardarse en una colección “messages” en mongo (no es necesario implementarlo
en FileSystem). El formato es: ✅

{user:correoDelUsuario, message: mensaje del usuario}✅

8- Corroborar la integridad del proyecto para que todo funcione como lo ha hecho hasta ahora.✅

#DEPENDENCIES
    - express "^4.18.2"
    - express-handlebars: ^7.1.2"
    - socket.io: ^4.7.4
    - mongoose: "^8.1.1"