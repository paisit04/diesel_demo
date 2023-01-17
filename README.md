# diesel-demo

Ref: https://diesel.rs/guides/getting-started

## PostgreSQL

Start database

```sh
docker-compose up -d
```

Create a database

```sh
$ docker-compose exec database bash
root@edc769c4f2ab:/# psql -U postgres
postgres=# create database diesel_demo;
CREATE DATABASE
```

## Installing Backend Client Libraries

Option1

```sh
$ brew install postgresql
```

Option2

```sh
$ brew install libpq
$ echo 'export PATH="/usr/local/opt/libpq/bin:$PATH"' >> ~/.zshrc
```

## Troubleshooting

If you see some ld errors, please run cargo clean first.
Then, run cargo run --bin show_posts
