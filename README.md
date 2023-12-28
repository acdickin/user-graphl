# Users
Basic Graphql project

## Basics 
1. Run json server 
2. new tab Run graphql server


## To run the server 
`yarn dev`

## To run json server db
`yarn json:server`

## accessing graphiql
`http://localhost:4000/graphql`

## json server resources
`http://localhost:3000/users` \n
`http://localhost:3000/companies`

## Useful queries
<pre>
query findCompany{
  apple:company(id:"1"){
    ...companyDetails
    users {
      id,
      firstName
    }
  }
  
  google:company(id:"2"){
   ...companyDetails
    users {
      id,
      firstName
    }
  }
}

fragment companyDetails on Company{
  id
  name
  description
}

query findUser{
   user(id:"48"){
   ...userDetails
    company {
      name
    }
  }
}


fragment userDetails on User{
  id
  firstName
  age
}
</pre>