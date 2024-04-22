git clone https://github.com/laradock/laradock.git
cp .\envlaradock\.env .\laradock\.env
cd .\laradock\
docker-compose up -d nginx postgres pgadmin
docker-compose exec --user=laradock workspace bash
composer i
php artisan key:generate
php artisan optimize