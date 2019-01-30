# graphql-sandbox
This is an application I developed through the guidance of Stephen Grider on Udemy.  
Check him out here at https://github.com/stephengrider

This application uses GraphQL by way of GraphiQL to hook into a mock JSON REST API that is built using json-server. 

This requires running two server instances in parallel - one for GraphiQL and one for json-server.



### 1) clone this repo then cd into the directory
```cd graphql-sandbox```

### 2) npm install to install dependencies
```npm install```

### 3) open two terminal windows one to run GraphQL, the other to run json-server - see package.json to view the scripts related to each

### 4) run the GraphQL server in one terminal window (this will allow you access to GraphiQL
```npm run dev```

### 5) run json-server in the other terminal window
```npm run json:server```

### 6) to view GraphiQL interface
open URL ```http://localhost:4000/graphql``` in a browser of your choice

### 7) to view json-server (REST API)
open URL ```http://localhost:3000/users``` or ```http://localhost:3000/companies```

### note - this assumes knowledge in how REST API's work
You can view the different REST API URL's based on user id's, company id's, etc using the id's specified in the db.json file

### example of how to access a REST API record in GraphiQL
copy and paste this into the QUERY VARIABLES panel (left hand side) of GraphiQL then press the button with an arrowhead at the top (it looks like a play button) to run the request

```
{
  user(id: "41") {
    firstName
    age
  }  
}
```
### You should see this object result in the right hand panel:
```
{
  "data": {
    "user": {
      "firstName": "Nick",
      "age": 40
    }
  }
}
```
# HOPE THIS HELPS!

