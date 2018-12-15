# Adonis API server

This project is a GraphQL server with the concept of a basic blog. The blog will have User and Post entities. We’ll be able to create users and authenticate them using JSON Web Tokens (JWT). Authenticated users will be able to create posts.

## Setup

Use the adonis command to install the blueprint

```bash
adonis new yardstick --api-only
```

or manually clone the repo and then run `npm install`.


### Migrations

Run the following command to run startup migrations.

```js
adonis migration:run
```

## Testing

Use Insomnia as REST client

```
adonis serve --dev
```

### Create a new user
```
POST http://127.0.0.1:3333/graphql
mutation {
    createUser(username: "mezie", email: "mezie@example.com", password: "password") {
        id
        username
        email
    }
}
```

### Login
```
mutation {
    login(email: "mezie@example.com", password: "password")
}
```

### Create a post while logged
```
auth with the JWT returned, selecting Bearer Token and paste the JWT

mutation {
    addPost(title: "Hello Adonis", content: "Adonis is awesome!") {
        id
        title
        slug
        content
        user {
            username
            email
        }
    }
}
```
