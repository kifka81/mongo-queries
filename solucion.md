# Solución del ejercicio

Practice the following queries:

* Find the restaurant with id 30112340.
```diff
db.restaurantes.find({"restaurant_id": "30112340"})
```  
* Find May May Kitchen.
```diff
db.restaurantes.find({"name": "May May Kitchen"})
``` 
* Find the restaurants where their cuisine is Tapas.
```diff
db.restaurantes.find({"cuisine": "Tapas"}).pretty()
``` 
* Find the restaurants in postal code 11208.
```diff
db.restaurantes.find({"address.zipcode": "11208"}).pretty()
``` 
* Find all restaurants that have a score greater or equal than 70.
```diff
db.restaurantes.find({"grades.score": {$gte: 70}}).pretty()
``` 
* Find all restaurants in Brooklyn "grades.score that have a score greater than 80
```diff
db.restaurantes.find({$and:[{"borough": "Brooklyn"},{"grades.score": {$gte: 80}}]}).pretty()
``` 
* All restaurants with Chilean or Czech cuisine.
```diff
db.restaurantes.find({$or: [{"cuisine": "Chilean"},{"cuisine": "Czech"}]})
``` 
* All restaurants with grade A in second position of the array.
```diff
-db.restaurantes.find({"grades.1": {"grade": "A"}}).pretty()
``` 
* All restaurants with grades A or B.
```diff
db.restaurantes.find({$or: [{"grades.grade": "A"},{"grades.grade": "B"}]}).pretty()
``` 
* All restaurants that have a review made in 2014-09-16.
```diff
db.restaurantes.find({"grades.date": {$gte: new Date("2014-09-16T00:00:00.000Z")}}).pretty()
``` 
* All restaurant their cuisine is Tapas ordered by name in ascending (normal) order.
```diff
db.restaurantes.find({"cuisine": "Tapas"}).sort({"name": 1}).pretty()
``` 
* How many restaurants have been graded after 2015-01-01.
```diff

``` 
