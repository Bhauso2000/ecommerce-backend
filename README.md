Download the zip file and extract it
Zip file contain backend foler that contains
1.Api gateway
2.Customer service
3.order service
4.product service

Prerequisite-
download rabbitmq locally , postgress db
create order-service,customer-service-db, product-service db in postgress sql
Customer service

Folder
Prisma:-
This contains db schema and seed file to insert default data 
src/Common :-
Contains prisma service
src/Customer:-
Contains dto, service and controller

To run customer service
first do 

npm i then run 
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
npx prisma db seed
to insert default record
then npm run start:dev

Product service:-
All the products related operation performed inthis service
Folder structure
Prisma:- contain db connection and seeder file

src/cloidinary
comtains cloudinary service implementation to upload file
src/common/prisma:- contains prisma service

src/product
contains controller ,dto amd services

To run 

first run npm i
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
npx prisma db seed
then npm run start:dev

order service:- 
comtsins all the implementation related customer sction add product to cart,place order,order history
,remove cart,cart list
Folder structure
same as product service

Steps to run
first run npm i
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
then npm run start:dev


Api gateway :-
Api gateway is central point it connected with all microservice
it responsible for emoting event to servoce vwsed on request
it contains middleware login for all authorised request it validate jwt token and add user details in req
steps to run

Steps to run
first run npm i
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
then npm run start:dev
