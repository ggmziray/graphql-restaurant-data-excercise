# ExpressGraphQL

The express-graphql module provides a simple way to create an Express server that runs a GraphQL API.

This exercise uses restaurant data created during my fullstack MIT course. 

# GraphQL

## Here are the query and mutation structures based on a GraphQL schema.

mutation editrestaurants($idd: Int = 1, $name: String = "OLDO"){
editrestaurant(id: $idd, name: $name){
name
description
}
}
mutation setrestaurants {
setrestaurant(input: {
name: "Granite",
description: "American"}) {
name
description
}
}
mutation deleterestaurants($idd: Int = 1){
  deleterestaurant(id: $idd){
ok
}
}
query getrestaurants {
restaurants {
name
description
dishes{
name
price
}
}
}
query getrestaurant($iid: Int = 1){
    restaurant(id:$iid){
name
description
}
}
