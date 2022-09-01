# Introduction
Kaggle provides different kinds of data. I would like to play with these data in an easy way. So, I plan to build an infrastructure to query data from Kaggle and visualize data by Superset. The infrastructure will help me analyze data of different types easily.

<br />

# Requirements
## Kaggle
* use Kaggle API to query data

<br />

## Superset
* use Superset to visualize Kaggle data
* connect PostgresSQL with Kaggle data

<br />

## Unit test
* test connection 
* test data can be accessible by Superset

<br />

## Interactive surface
let users only do these things:
  1. see the list of kaggle data
  2. download kaggle data based on the title of data
  3. write sql to create data schema for kaggle data
     1. upload the data to postgresql
  4. visualize data in Superset

<br />

# Current Progress


<details>
<summary> Kaggle </summary>

- [x] Use Kaggle API  <br />
- [x] Kaggle API query data <br />
  - [ ] store csv data in a folder
- [ ] process csv data 
  - [ ] write sql of table creation in a script and execute it
  - [ ] read csv and upload data to PostgreSQL
  - [ ] remove csv

</details>

<br />

<details>
<summary> PostgreSQL </summary>

- [ ] build PostgreSQL
- [ ] Use interactive interface of PostgreSQL to check data

</details>

<br />

<details>
<summary> Superset </summary>

- [x] build Superset
  - [ ] load_example: false => failed
    - [&cross;] SUPERSET_LOAD_EXAMPLES=no or false or comment it
    - [&cross;]  remove containers
    - [ ]  reload remote machine

  - [x] user/password created by myself

      ```bash
        docker exec -it superset_app /bin/bash
        superset fab reset-password --username admin --password <yourpassword>
      
      ```
- [x] Connect PostgreSQL
  - can not connect to my own PostgreSQL 
    - [&check;] try to add network in the docker-compose of superset

- [ ] visualize data

</details>

<br />

<details>
<summary> Unit test </summary>
</details>

<br />

<details>
<summary> Interactive surface </summary>
- [ ] for the first time, Superset will be downloaded from Github
</details>

