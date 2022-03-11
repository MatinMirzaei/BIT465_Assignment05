BIT 465 – REST API Development 
A Complete Django REST API With GitHub Documentations

Introduction
This assignment is to help you build upon the skills you have acquired from assignment 4 and the first 4 
chapters of Building RESTful Python Web Services. See the submission section for more information 
about what you should submit for this assignment.

Specification
You  should  build  a  new  API  endpoint  that  allows  an  end  user  to  create  a  new Dog model  by  making 
a POST to /api/dogs,  view  current  dogs  that  have  been  saved  to  the  server  before  by  making  a GET to 
/api/dogs,  and  get,  modify,  or  delete  an  existing Dog record  by  making  a GET, PUT,  or DELETE request 
(respectively)  to /api/dogs/<id> where <id> is  the  id  of  the Dog record  to  be  retrieved,  modified,  or 
deleted.  Since  a Dog includes  a  foreign  key  to  the  breed,  you  also  need  to  make  the  same  type  of 
endpoints for dog breed at /api/breeds/ and /api/breeds/<id>.
  
## Dog model
 A dog should contain the following fields:
  1. name (a character string)
  2. age (an integer)
  3. breed (a foreign key to the Breed Model)
  4. gender (a character string)
  5. color (a character string)
  6. favoritefood (a character string)
  7. favoritetoy (a character string)
  
## Breed Model
 A breed should contain the following fields:
  1. name (a character string)
  2. size (a character string) [should accept Tiny, Small, Medium, Large]
  3. friendliness (an integer field) [should accept values from 1-5]
  4. trainability (an integer field) [should accept values from 1-5]
  5. sheddingamount (an integer field) [should accept values from 1-5]
  6. exerciseneeds (an integer field) [should accept values from 1-5]
  
## Todo List
To do this, do the following:
  1. track all your changes using github. 
  2. add a Dog and Breed models to models.py
  3. migrate your database to include tables for Dog and Breed
  4. add two class-based API view controllers for handling Dog REST endpoints to controllers.py
   - call one DogDetail and one DogList to conform to best practice nomenclature
   - The DogDetail class should have three methods named get, put, delete
   - The DogList class should have two methods named get and post
   - refer to Chapter 2 of the recommended text or here for examples
  5. add two class-based API view controllers for handling Breed REST endpoints to controllers.py
   - call one BreedDetail and one BreedList to conform to best practice nomenclature
   - The BreedDetail class should have three methods named get, put, delete
   - The BreedList class should have two methods named get and post
   - refer to Chapter 2 of the recommended text or here for examples
  6. add the appropriate url patterns to the urls.py file to accept all the patterns and map them to the correct controller
  7. test your endpoints with POSTMAN/ web browser (browsable APIs), taking screenshots of each type of request. There should be 5 requests total for each type of model, for a    total of 10 tests and screenshots.
   - GET (list), POST to /api/dogs/
   - GET, PUT, DELETE to /api/dogs/<id>
   - GET (list), POST to /api/breeds/
   - GET, PUT, DELETE to /api/breeds/<id> trainability (an integer field) [should accept values from 1-5]
    
