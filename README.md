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
