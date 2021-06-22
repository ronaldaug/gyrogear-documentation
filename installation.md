# Installation

> Before this installation steps, please setup [two domains ]()first.

1. [Clone Repo](installation.md#clone-repo)
2. [Install node dependencies](installation.md#2-install-node-dependencies)
3. [Install composer packages](installation.md#3-install-composer-packages)
4. [Create environment file \(.env\)](installation.md#4-create-environment-file-env)
5. [Add variables to env](installation.md#5-add-variables-to-env)
6. [Generate application key](installation.md#6-generate-application-key)
7. [Migrate database](installation.md#7-migrate-database)
8. [Link media storage](installation.md#8-link-media-storage) 
9. [Create a user via PHP artisan command](installation.md#9-create-a-user-via-php-artisan-command)
10. [Seeding dummy data via PHP artisan command](installation.md#10-seeding-dummy-data-via-php-artisan-command)
11. [Create role and permission via PHP artisan command](installation.md#11-create-role-and-permission-via-php-artisan-command)
12. [Compile scripts and styles with Laravel mix](installation.md#12-compile-scripts-and-styles-with-laravel-mix)

## 1. Clone Repo

```text
git clone https://github.com/joewinn/gyrogear.git
```

After cloning the repo, `cd` into **gyrogear** directory.

```text
cd gyrogear
```

## 2. Install node dependencies

```text
npm install
```

## 3. Install composer packages

```text
composer install
```

## 4. Create environment file \(.env\)

```text
cp .env.example .env
```

## 5. Add variables to env

You'll have to append these below variables in .env file

```text
ADMIN_DOMAIN="http://gyrogear.test"
CLINIC_DOMAIN="http://clinic.gyrogear.test"

# ONLY_SCRIPT=true
# ONLY_STYLE=true
```

## 6. Generate application key

```text
php artisan key:generate
```

## 7. Migrate database

```text
php artisan migrate
```

## 8. Link media storage 

```text
php artisan storage:link
```

## 9. Create a user via PHP artisan command

```text
php artisan up:make_user
```

## 10. Seeding dummy data via PHP artisan command

```text
php artisan up:dummy_data
```

## 11. Create role and permission via PHP artisan command

```text
php artisan up:refresh_role_permission
```

## 12. Compile scripts and styles with laravel mix

```text
npm run prod
```

Usually it takes about **249708ms**

You can compile only style or only script by modifying `ONLY_SCRIPT` and `ONLY_STYLE` variable inside .env file.

