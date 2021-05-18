1. Check if logstash_dpp is up
docker exec -it logstash_dpp sh
cd /tmp

2. Once mysql container is ready, create table and DB entries


CREATE TABLE Persons (
    PersonID int,
    LastName varchar(255),
    FirstName varchar(255),
    Address varchar(255),
    City varchar(255)
);

insert into Persons(PersonID,LastName,FirstName,Address,City) values(1, "Howen", "John", "Malaysia", "KL");
insert into Persons(PersonID,LastName,FirstName,Address,City) values(2, "Kenda", "Fathon", "India", "Chennai");

select * from Persons;

drop table Persons;

3. Go back to logstash_dpp to check the logs and /tmp/dpp.data should be created as part of output
