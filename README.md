# Api Toko Belanja
## Link Railway
https://todeploy-production.up.railway.app/

To run this project, install it locally using npm:

```
npm install
npm run start (for migrate all)
npm run admin (for seeder admin)
```

## Available seed admin:
```json
{
   "email": "admin@gmail.com"
   "password": "123456"
}
```



## Notes
Sesuaikan `config` dengan database postgres device. <br>
Port dapat disesuaikan di `.env`

# User API Testing
run api in `postman` 
### POST /users/register
```
https://todeploy-production.up.railway.app/users/register
```
#### Data Register

```json
{
   "full_name": "andre",
   "email": "andreas@gmail.com",
   "password": "123456",
   "gender": "male"
}
```
![Alt text](images/register_user.png)

<br>
<br>


### POST /users/login
```
https://todeploy-production.up.railway.app/users/login
```

```
pastikan method adalah post
```
#### Data Login   

```json
{
   "email": "andreas@gmail.com",
   "password": "123456",
}
```

![Alt text](images/login.png)

#### Token
* Token akan muncul ketika berhasil login
* Simpan token untuk di gunakan pada feature berikutnya

<br>
<br>


### PUT /users
```
https://todeploy-production.up.railway.app/users/
```
#### Data Edit   
```json
{
   "full_name": "Andreas Nugroho",
   "email": "andreas@gmail.com",
}
```
![Alt text](images/edit_users.png)

#### Header Token
![Alt text](images/edit_header_users.png)

<br>
<br>


### DELETE /users
```
https://todeploy-production.up.railway.app/users/
```
![Alt text](images/delete_users.png)

#### Header Token
![Alt text](images/delete_header_users.png)

<br>
<br>


### PATCH /users/topup
```
https://todeploy-production.up.railway.app/users/topup
```
#### Data Topup   
```json
{
   "balance": 200000,
}
```
![Alt text](images/topup_user.png)

#### Header Token
![Alt text](images/header_topup.png)

<br>
<br>

# Categories API Testing
run api in `postman` 
### POST /categories
```
https://todeploy-production.up.railway.app/categories
```
#### Data category   
```json
{
   "type": "Makanan",
}
```
![Alt text](images/categories_create.png)
```
hanya token admin yang dapat mengakses endpoint categories
header berisi token admin
```
#### Token Admin 
```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJhZG1pbkBnbWFpbC5jb20iLCJyb2xlIjoiYWRtaW4iLCJpYXQiOjE2ODY1NTk4Nzl9.rwa4AhhaUA9UhTUtg2seFmJ6A2vzAGISEzRZOKKGpJk"
}
```
<br>
<br>

### GET /categories
```
https://todeploy-production.up.railway.app/categories
```
![Alt text](images/get_category.png)
```
hanya token admin yang dapat mengakses endpoint categories
header berisi token admin
```
#### Token Admin 
```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJhZG1pbkBnbWFpbC5jb20iLCJyb2xlIjoiYWRtaW4iLCJpYXQiOjE2ODY1NTk4Nzl9.rwa4AhhaUA9UhTUtg2seFmJ6A2vzAGISEzRZOKKGpJk"
}
```
<br>
<br>

### PATCH /categories/:categoryId
```
https://todeploy-production.up.railway.app/categories/4
```
#### Data patch categories   
```json
{
   "type": "Makanan",
}
```
![Alt text](images/patch_category.png)
#### Token Admin 
```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJhZG1pbkBnbWFpbC5jb20iLCJyb2xlIjoiYWRtaW4iLCJpYXQiOjE2ODY1NTk4Nzl9.rwa4AhhaUA9UhTUtg2seFmJ6A2vzAGISEzRZOKKGpJk"
}
```
<br>
<br>

### DELETE /categories/:categoryId
```
https://todeploy-production.up.railway.app/categories/1
```
![Alt text](images/delete_category.png)
#### Token Admin 
```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJhZG1pbkBnbWFpbC5jb20iLCJyb2xlIjoiYWRtaW4iLCJpYXQiOjE2ODY1NTk4Nzl9.rwa4AhhaUA9UhTUtg2seFmJ6A2vzAGISEzRZOKKGpJk"
}
```
<br>
<br>









