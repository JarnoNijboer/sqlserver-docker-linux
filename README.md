# sqlserver-docker-linux
SQL Server Linux hosted on Docker

## Getting started

1. Clone repo
2. Create an folder named `backups` in root of repository
3. Choose a strong password an replace the default password of `SA_PASSWORD` in `docker-compose.yml` file
4. Run `docker-compose up -d` in root of repo
5. When the container is up and running, you can restore your databases by placing the `.bak` files in the `.backups` folder
6. Thats all


## FAQ
### Are files persisted?
Yes, by using docker volumes all the data of sql server is stored outside the container. Deleting and creating a new container doesn't remove the data. The data is lost when the docker volumes are deleted

### Can I restore an existing database?
Yes, you can put the `.bak` in the `backups` folder and they should appear in sql server beneath `data/backups`
