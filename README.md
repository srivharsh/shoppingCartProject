# shoppingCartProject

This is a demo project for a shopping cart appplication.
* For creating this application I've used the below technology stack
        1. Java 8
        2. Spring Boot
        3. Hibernate and JPA
        4. Postgres
        5. Maven
        6. Swagger for documentation

* Using this application we can create a shopping cart, retrieve the shopping cart, add products in the shopping cart, update products in the shopping cart, delete product in the shopping cart. 

The project consists of a directory structure comprising of six different packages to split the logic into into multiple Java classes. The packages are:
1) Controller
2) Repository
3) Service
4) Validator
5) Model 
* We've two entities in here with One-to-Many relationship between them:
        1. ShoppingCart
        2. Products
7) Exception

**Approach**: We're exposing RESTful APIs which will help the user to create a shopping cart, retrieve the shopping cart, retrieve a unique cart, get all the products from a cart, get a unique products from a cart, add products in the cart, update a product in the shopping cart, delete product in the shopping cart. Let's see them one by one.

1) createShoppingCart **POST("/api/carts")** : Create a shooping cart by passing the ShoppingCart Object.
2) getShoppingCart **GET("/api/carts")** : Get all the details of the shopping cart.
3) getShoppingCartByCartId **GET("/api/carts/{cartId}")** : Get the shooping cart by passing the ShoppingCart ID.
4) getAllProducts **GET("/api/carts/{cartId}/products")** : Get all the products by passing the ShoppingCart ID.
5) getProductFromShoppingCart **GET("/api/carts/{cartId}/products/productId")** : Get a uinque product from the shoppingCart by passing the ShoppingCart ID and product ID.
6) addProduct **POST("/api/carts/{cartId}/products")** : Add a product in a shopping cart by passing the cart id and the Product Object
7) updateProduct **PUT("/api/carts/{cartId}/products/{productId}"** : Update a particular product in a shopping cart by passing the cart id and the product ID.
8) deleteCart **DELETE("/api/carts/{cartId}/products/{productId}"** : Delete a particular product in a shopping cart by passing the cart id and the product ID.

**Running the application:** To run the application, simply follow the below steps:
1) Download the shoppingCartProject.zip file and unzip it.
2) Import the unzipped file in any of the IDE (Eclipse/STS) by right click > import > Maven > Existing Maven Projects > Next > Browse for the unzipped file location > Finish.
3) Once the import is done do a Maven Update. Right Click > Maven > Update Project > Select the Project > Click on OK. The project will start updating the maven project.
4) Once the update is done, right click on project > Run As > Spring Boot App. The application will start.
5) Wait until you see :
INFO[0;39m [35m4248[0;39m [2m---[0;39m [2m[  restartedMain][0;39m [36mc.c.d.s.ShoppingCartDemoApplication     [0;39m [2m:[0;39m **Started ShoppingCartDemoApplication in 9.518 seconds (JVM running for 11.769)**

Your application is **up** now!

You can use **postman** to test the RESTAPIs.
1) www.localhost:9090/api/carts **GET**
2) www.localhost:9090/api/carts **POST**
3) www.localhost:9090/api/carts/{cartId} **GET**
4) www.localhost:9090/api/carts/products **GET**
5) www.localhost:9090/api/carts/{cartId}/products/productId **GET**
6) www.localhost:9090/api/carts/{cartId}/products **POST**
7) www.localhost:9090/api/carts/{cartId}/products/{productId **PUT**
8) www.localhost:9090/api/carts/{cartId}/products/{productId} **DELETE**

You can also use the below URLs for **Swagger** **Document** Implementation.
**Docs**: http://localhost:9090/v2/api-docs/
**UI**:   http://localhost:9090/swagger-ui.html#/









