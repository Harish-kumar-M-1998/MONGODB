 1. Find all the information about each product

db.users.find()

**2.**Find the product price which is between 400 to 800

db.users.find({product_price:{$gt:400,$lt:800}})

3. Find the product price which is not between 400 to 600

db.users.find({product_price:{$not:{$gte:400,$lte:600}}})

4. List the four products which are greater than 500 in price

db.users.find({product_price:{$gt:500}}).limit(4)

5. Find the product name and product material of each product

db.users.find({},{product_name:1,product_material:1})

6. Find the product with a row id of 10

db.users.find({id:{$eq:"10"}})

7. Find only the product name and product material

db.users.find({},{product_name:1,product_material:1,id:0})

8. Find all products which contain the value 'Soft' in product material

db.users.find({product_material: 'Soft'})

9. Find products which contain product color 'indigo' and product price 492.00

db.users.find({$or:[{product_color:'indigo'},{product_price:'492.00'}]})

10. Delete the products which product price value are 28

db.users.deleteOne({product_price:’28’})
