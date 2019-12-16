# graphqldjango
My GraphQL Django project with a simple library CRUD functionality


mutation{
  createUser(username: "sherman",email:"ouko.sherman@fibonacci.systems",password:"sherman")
  {
    user{
      id
      username
      email
      password
    }
  }
}

query{
  users{
    id
    username
    email
  }
}

mutation{
	tokenAuth(username: "sherman",password:"sherman"){
    token
  }
}

mutation{
  createCategory(input: {
  }){
		created
    message
  }
}

query{
  relayCategories(categoryName: "Mathematics"){
    edges{
      node{
        categoryID
    		categoryName
      }
    }
  }
}

query{
  relayCategories{
    edges{
      node{
        categoryID
    		categoryName
      }
    }
  }
}

query{
  relayCategories(categoryID:4){
    categoryName
    message
    code
  }
}

mutation{
  deleteCategory(input: {
    categoryID: 2
  }){
		code
    message
  }
}
