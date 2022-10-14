# RDS

## AWS RDS for the database

- login to the account using your credentials

- from RDS choose databases then click create database button

  ![create database](../../screenshots/RDS/createDB.png)

- choose standard create

  ![standard create](../../screenshots/RDS/RDS1.png)

- choose postgreSQL and version `12.8-R1`

  ![choose postgreSQL](../../screenshots/RDS/RDS2.png)

- choose the free tier

  ![free tier](../../screenshots/RDS/RDS3.png)

- then choose the database name and password

  ![DB name and password](../../screenshots/RDS/RDS4.png)

- then choose the storage to be 20gb and disable the auto scaling

  ![disable auto scaling](../../screenshots/RDS/RDS5.png)

- make sure to choose the puplic access option and click create database

- data base created successfully

  ![database created](../../screenshots/RDS/RDS6.png)

- to be able to connect to the our database we should allow an IP to connect to the database from `Connectivity & Security` tab then select `VPC sercurity groups`

  ![vpc group](../../screenshots/RDS/RDS7.png)

- click `Inbound Rules` Then `Edit Inbound Rules`

  ![edit ibound rules](../../screenshots/RDS/RDS8.png)

- then add `0.0.0.0/0` and hit save

  ![whitelist ip](../../screenshots/RDS/RDS9.png)

- test the connection to our database

  ![test connection](../../screenshots/RDS/db-connected-successfully.png)
