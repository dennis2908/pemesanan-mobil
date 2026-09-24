Front End : Next ; Back End : Laravel, MySQL, RabbitMQ ; Docker </br>

copy isi .env.docker ke .env lalu di cmd ketik :

```
docker compose up --build -d
```

Tunggu hingga akhir lalu :

```
docker compose exec app php artisan optimize:clear
```

lalu :


```
docker compose exec app php artisan migrate:fresh --seed
```

lalu :

```
docker compose exec app php artisan schedule:work
```

lalu buka http://localhost:3000 di browser

Untuk pengguna pertama, registrasi dulu di menu registrasi