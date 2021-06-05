# Django Shopper Challenge

A RESTful django development challenge for shopping in a shop.

## Introduction
In this challenge you are going to develop a small django web application for ordering simple products.

The user must be able to log in to app according to rules explained ahead, and order some of them. Also he/she must be able to see and edit his/her profile.

App parts:
### Entry:
User can login in two ways:
- first, direct and with providing email and password. If a user with this email does not exist, must be created in database, and if it already exists, must be verified with password and in response get the token for steps ahead.
- second, indirect and with third party authentication. The user must be able to enter app with his/her google account, note that if this part needs a client, you must implement the client part too with minimum UI.

### View products:
For simplicity, the user can get the list of all available and not sold products with providing the token for authorization, note that he/she should get a 401 error if the token is expired or wrong.

### Order:
The user can select some products and buy them with a list of product's ids and the number of each product he/she wants to buy. In response he/she must get the result of his/her attempt. Note that he/she must be authorized to do so, also if any of the ids provided by user was wrong, the related error must be returned in response. 

### Profile:
The user must be able to see his/her profile, and also must be able to patch or post an update to edit it. Note that authorization is required.

## Expectations:
We want a clean, readable and maintainable code with meaningful comments and docstrings. Also you need to provide postman API doc for web app. For task managing, you have to break your work to smaller and manageable tasks, and put them on a task managing app, specified by your mentor.

## Estimation
You have to estimate the development time and send us your estimation number and how you obtained it. 

## Tests
You should write unit tests for your code

## Task
1. Fork this repository
2. Estimate the develop
3. break and specify your tasks in project management tool
4. Develop the challenge with Django 2 or higher
5. Push your code to your repository
6. Send us a pull request, we will review and get back to you
7. Enjoy 











## Run project 

docker volume  create shopper_postgresql
docker network  create shopper_network
docker network  create ngnix_network
docker-compose up  -d
docker exec -it shopper_postgresql psql -U nilva -W nilva
CREATE DATABASE shopper_db;


docker exec -it django-shopper_shopper_1  python manage.py migrate



run project in http://127.0.0.1:8000/