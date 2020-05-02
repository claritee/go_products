
## ENV vars

```
export APP_DB_USERNAME=postgres
export APP_DB_PASSWORD=
export APP_DB_NAME=products
```

## Creating a DB

Via psql
```
psql
```

Create db
```
create database products;
```

Show databases
```
list
```

Connect to the db
```
\c products
```

Create table

```
CREATE TABLE products
(
    id SERIAL,
    name TEXT NOT NULL,
    price NUMERIC(10,2) NOT NULL DEFAULT 0.00,
    CONSTRAINT products_pkey PRIMARY KEY (id)
);
```

## Running the app

```
go build
```

```
./go_products
```

Routes

```
GET "/products"
POST "/product"
GET "/product/{id}
PUT "/product/{id}
DELETE "/product/{id}
```

Example:

```
http://localhost:8010/products
```