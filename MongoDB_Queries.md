####  MongoDB Basic Queries 

##### 1) Find all the information about each products

`db.products.find();`

Example Output:

![alt](./image/Screenshot_29-2-2024_23219_www.mycompiler.io.jpeg)

##### 2)Find the product price which are between 400 to 800

`db.products.find({"product_price":{$gt:400,$lt:800}});`

Example Output:

![alt](./image/Screenshot_29-2-2024_232340_www.mycompiler.io.jpeg)

##### 3)Find the product price which are not between 400 to 600

`db.products.find({"product_price":{$not:{$gt:400,$lt:600}}});`

Example Output:

![alt](./image/Screenshot_29-2-2024_232540_www.mycompiler.io.jpeg)

##### 4)List the four product which are greater than 500 in price

`db.products.find({"product_price":{$gt:500}}).limit(4);`

Example Output:

![alt](./image/Screenshot_29-2-2024_232540_www.mycompiler.io.jpeg)

##### 5)Find the product name and product material of each products

`db.products.find({},{"product_name":1,"product_material":1});`

Example Output:

![alt](./image/Screenshot_29-2-2024_23292_www.mycompiler.io.jpeg)

##### 6)Find the product with a row id of 10

`db.products.findOne({"id":"10"});`

Example Output:

![alt](./image/Screenshot_29-2-2024_233048_www.mycompiler.io.jpeg)

##### 7)Find only the product name and product material

`db.products.find({},{"_id":0,"product_name":1,"product_material":1});`

Example Output:

![alt](./image/Screenshot_29-2-2024_233155_www.mycompiler.io.jpeg)

##### 8)Find all products which contain the value of soft in product material

`db.products.find({"product_material":"Soft"});`

Example Output:

![alt](image/Screenshot_29-2-2024_233317_www.mycompiler.io.jpeg)

##### 9)Find products which contain product color indigo  and product price 492.00

`db.products.find({$and:[{"product_color":"indigo"},{"product_price":492.00}]});`

Example Output:

 ![alt](./image/Screenshot_29-2-2024_233317_www.mycompiler.io.jpeg)

##### 10)Delete the products which product price value are same

`db.products.deleteMany({"product_price":{$eq:400}});`
