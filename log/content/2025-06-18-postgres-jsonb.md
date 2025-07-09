+++

title = "Posgres JSONb notes"
date = 2025-07-08

[taxonomies] 

tags = ["Programming"]

[extra]

author = "Rob"
background_media = "https://open.spotify.com/track/3aBgBJnVDjap01AApf7l67?si=d8e412862ea0452f"

+++

# Postgres JSONb notes

I find one of the most annoying parts of working with jsonb columns in postgres
is remembering the syntax. Below are some notes, mostly for myself. (Yes reading the postgres docs
is probably a better call, I'm writing this for me.) `¯\_(ツ)_/¯`

Also how great is Sports, Not Heavy Crime? It's pretty great.

## Field existence in a column

```sql
SELECT * from phlerbs WHERE jsonb_column ? 'field_name'
```

## Retrieving a value

```sql
SELECT * from phlerbs WHERE jsonb_column->'field_name'
```

# Read more

[https://www.postgresql.org/docs/9.5/functions-json.html](https://www.postgresql.org/docs/9.5/functions-json.html)