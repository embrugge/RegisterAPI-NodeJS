 # Basic description
RESTful API that interacts with a PostgreSQL database. Implemented in NodeJS with typescript, restify, and the sequelize ORM. Edited in Visual Studio Code.  
  
If a "PORT" environment variable has not been defined then the application currently defaults to port 15100 (see ./src/server.ts).  
  
To start via the terminal navigate to the source code directory and run the following commands (after install "rebuild" will be run automatically)...  
`$ npm install`  
`$ npm run (re)build`  
`$ npm run start`  

 # Example HTTP requests via cURL (be sure to update as needed)
 ## Create a product
`curl -i -s -H "Content-Type: application/json" -X POST -d '{"lookupCode":"lookupcode4","count":175}' https://uarkregservnodejsapi.herokuapp.com/api/product/`  
 ## Update an existing product by record ID
`curl -i -s -H "Content-Type: application/json" -X PUT -d '{"id":"bee20aed-5245-46a7-b19c-9ef6abd4ca5c","lookupCode":"lookupcode4","count":200}' https://uarkregservnodejsapi.herokuapp.com/api/product/bee20aed-5245-46a7-b19c-9ef6abd4ca5c`  
 ## Delete an existing product by record ID
`curl -i -s -X DELETE https://uarkregservnodejsapi.herokuapp.com/api/product/bee20aed-5245-46a7-b19c-9ef6abd4ca5c`  