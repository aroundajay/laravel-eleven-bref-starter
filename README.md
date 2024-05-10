## About Laravel Bref App

Laravel Bref App is a serverless web application built with laravel 10.X and bref 2.X.

## Documentation

- [Laravel Documentation](https://laravel.com/docs/10.x)
- [Bref Documentation](https://bref.sh/docs/)

## Database

- Create MySql database with publicly accessible url using AWS RDS
- serverless bref:cli --args="migrate --seed"

## Generate key

- php artisan key:generate

## Config cache

- php artisan config:cache

- php artisan config:clear

## AWS SSM

- aws ssm put-parameter --region ap-south-1 --name '/bref-app/dev/LaravelElevenBrefStarterDatabaseUrl' --type String --value 'database connection url' --profile aws-profilename

## Variable changes

- serverless.yml: provider > profile

## Deployment

- npm run build
- php artisan optimize && php artisan config:cache && php artisan config:clear && serverless deploy --verbose

## Remove stack

- serverless remove
