# Solución del ejercicio

```diff
# text in gray
```

Practice the following queries:

* Find the restaurant with id 30112340.
```diff
# - db.restaurantes.find({"restaurant_id": "30112340"})
```  
* Find May May Kitchen.
  - db.restaurantes.find({"name": "May May Kitchen"})
  
* Find the restaurants where their cuisine is Tapas.
  - db.restaurantes.find({"cuisine": "Tapas"}).pretty()
  
* Find the restaurants in postal code 11208.
  - db.restaurantes.find({"address.zipcode": "11208"}).pretty()
  
* Find all restaurants that have a score greater or equal than 70.
  - 
* Find all restaurants in Brooklynthat have a score greater than 80
* All restaurants with Chilean or Czech cuisine.
* All restaurants with grade A in second position of the array.
* All restaurants with grades A or B.
* All restaurants that have a review made in 2014-09-16.
* All restaurant their cuisine is Tapas ordered by name in ascending (normal) order.
* How many restaurants have been graded after 2015-01-01.
