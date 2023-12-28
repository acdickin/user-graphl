# Users
Basic Graphql project



useful queries
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