# Odoo Docker

Purpose of this repository is to provide the dockerized development environment for the odoo developers.

## How to use this repository

To use this repo you need to make sure you have docker & docker-compose install on your machine. 

-  By default this repo use odoo 14 image if you are willing to use different version you can change odoo version in `.env` file by changing the value of `ODOO_VERSION` environment variable
- You can also use `.env` file to setup your default values for `DB_USER` `DB_PASSWORD` and user and password for PgAdmin
-  If you need some external python dependencies you can add those in `service/odoo/requirements.txt` and then you can build/rebuild the odoo image using command `docker-compose build odoo` 
- If you want to install any os package you can add `RUN apt-get update && apt-get install -y <packagename> <packagename2>` line in `service/odoo/Dockerfile`
- Once you are ready with all your configuration you simply run `docker-compose up -d` command it will run your odoo stack along with PgAdmin.
- Odoo is running in watch mode using `--dev=reload` so you don't need to restart odoo after changing python code
- Once stack is running you can access odoo using `localhost:8069` and pgadmin using `localhost:5050`

## Debug

If you want to debug odoo you can follow the steps explain by [Khaled Said](https://dev.to/kerbrose) in his [Dev.to article](https://dev.to/kerbrose/how-to-remote-debugging-odoo-docker-images-python-based-framework-4o2h)

## Note
For any issue please feel free to raise issue here or contact me on
- :email: wagh.aswapnil@gmail.com
- :bird: Follow me on Twitter :point_right: [meswapnilwagh](https://twitter.com/meswapnilwagh)