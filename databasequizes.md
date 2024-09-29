# Week [3]

### QUIZ 2

# 1
select * from goal;
![Screenshot 2024-09-29 212141](https://github.com/user-attachments/assets/a0d55b61-f0ff-4e27-a4bc-221406b3e104)

# 2
select name, type from airport where iso_country = "FI";
![Screenshot 2024-09-29 212147](https://github.com/user-attachments/assets/3c99ae14-5aca-4d8a-bb2a-40e5f7471220)

# 3
select name from airport where iso_country = "FI" order by name;
![Screenshot 2024-09-29 212154](https://github.com/user-attachments/assets/f3daa959-6507-4871-9563-3e8d0263b96d)

# 4
select name, type from airport where iso_country = "FI" order by type, name;
![Screenshot 2024-09-29 212203](https://github.com/user-attachments/assets/16beb866-492c-435f-bc4c-dbb9bcd4b34c)

# 5
 select name from country where name like "F%";
![Screenshot 2024-09-29 212210](https://github.com/user-attachments/assets/a8f44461-4e24-4bce-a58d-be293ade2c25)

# 6
 select name from country where name like "%f%";
![Screenshot 2024-09-29 212215](https://github.com/user-attachments/assets/b57f07f0-5253-488d-ad64-9508cc060325)

# 7
select location from game where screen_name = "Vesa";
![Screenshot 2024-09-29 212221](https://github.com/user-attachments/assets/87f8ba8f-b891-4514-b4ed-08571765421a)

# 8
select co2_consumed from game where screen_name = "Ilkka";
![Screenshot 2024-09-29 212225](https://github.com/user-attachments/assets/1bad05c8-a319-46a3-a986-21d396f9e930)

# 9
select co2_budget from game where screen_name = "Ilkka";
![Screenshot 2024-09-29 212228](https://github.com/user-attachments/assets/d4440a5e-ab2b-4397-a74b-13b8b1cf47fd)

# 10
select screen_name, co2_budget, co2_consumed, @co2_left := co2_budget - co2_consumed from game where screen_name = "Ilkka";
![Screenshot 2024-09-29 212235](https://github.com/user-attachments/assets/febb0103-e721-4187-8972-f598144857f0)


### QUIZ 3

# 1
select country.name as "country name", airport.name as "airport name" from country, airport where country.iso_country airport.iso_country and country.name = "Iceland";
![Screenshot 2024-09-29 212454](https://github.com/user-attachments/assets/b7ec578d-bf72-4a42-8dc2-219d0bc7bb78)

# 2
select airport.name as "airport name" from airport, country where country.iso_country = airport.iso_country and country.name = "France" and airport.type = "large_airport";
![Screenshot 2024-09-29 212517](https://github.com/user-attachments/assets/2e23fb6a-2db7-4e64-9876-d3f34182a068)

# 3
select country.name as "country_name", airport.name as "airport_name" from country, airport where country.continent = airport.continent and airport.continent = "an" and country.name = "Antarctica";
![Screenshot 2024-09-29 212536](https://github.com/user-attachments/assets/0174d400-0ab9-4f97-8e0d-5c133d052dd7)

# 4
select elevation_ft from airport, game where airport.ident = game.location and game.screen_name = "Heini";
![Screenshot 2024-09-29 212603](https://github.com/user-attachments/assets/5c9ae1a6-abb2-4ec0-89be-a7df20c6dcc9)

# 5
 select elevation_ft * 0.3048 as "elevation_m" from airport, game where airport.ident = game.location and game.screen_name = "Heini";
 ![Screenshot 2024-09-29 212645](https://github.com/user-attachments/assets/1b475edd-657b-47d8-907e-40a0a97a2e05)

# 6
select name from airport, game where airport.ident = game.location and game.screen_name = "Ilkka";
![Screenshot 2024-09-29 212701](https://github.com/user-attachments/assets/62e53111-a4fe-4bb6-9eb6-04b82e7160b1)

# 7
 select country.name from country, airport, game where game.location = airport.ident and airport.iso_country = country.iso_country and game.screen_name = "Ilkka";
 ![Screenshot 2024-09-29 212725](https://github.com/user-attachments/assets/0e31f3f5-08a3-473e-bbb8-769b42d09fef)

# 8
select goal.name from goal, game, goal_reached where game.id = goal_reached.game_id and goal.id = goal_reached.goal_id and game.screen_name = "Heini";
![Screenshot 2024-09-29 212753](https://github.com/user-attachments/assets/4d798660-f25d-4610-8ed4-77296b075569)

# 9
select airport.name from airport, goal, game, goal_reached where airport.ident = game.location and game.id = goal_reached.game_id and goal.id = goal_reached.goal_id and game.screen_name = "Ilkka" and goal.name = "CLOUDS";
![Screenshot 2024-09-29 212821](https://github.com/user-attachments/assets/522ad41c-f7cd-4231-b132-ca3bd5026eda)

# 10
select country.name from country, airport, goal, game, goal_reached where country.iso_country = airport.iso_country and airport.ident = game.location and game.id = goal_reached.game_id and goal.id = goal_reached.goal_id and game.screen_name = "Ilkka" and goal.name = "CLOUDS";
![Screenshot 2024-09-29 212842](https://github.com/user-attachments/assets/b75c80fa-1d28-4ad3-804b-f4ffd6f930c1)



# Week [4]

### QUIZ 4

# 1
 select country.name as "country name", airport.name as "airport name" from country
    -> inner join airport where airport.iso_country = country.iso_country
    -> and country.iso_country = "FI";
![Screenshot 2024-09-29 213004](https://github.com/user-attachments/assets/c2d28f78-4c20-4f39-bd8c-c50e32621d70)

# 2
select game.screen_name, airport.name from game
right join airport where airport.ident = game.location;

//

select screen_name, airport.name from game inner join airport on location = ident;
![Screenshot 2024-09-29 213447](https://github.com/user-attachments/assets/57868a07-2713-4a52-9b1c-53a709e09c2a)
![Screenshot 2024-09-29 213501](https://github.com/user-attachments/assets/f1ee3084-e685-484c-ad36-d09759ee302e)

# 3
 select game.screen_name, country.name from game
    -> left join airport on airport.ident = game.location
    -> left join country on airport.iso_country = country.iso_country;
 ![Screenshot 2024-09-29 213518](https://github.com/user-attachments/assets/a2660cd2-3fcd-424f-80fd-e826398a7e9b)

# 4
select airport.name, game.screen_name from airport
    -> left join game on game.location = airport.ident
    -> where airport.name like "%Hels%";
![Screenshot 2024-09-29 213549](https://github.com/user-attachments/assets/9c4e02fc-967c-4576-99d3-69ffc5b730e1)

# 5 
 select goal.name, game.screen_name from goal
    -> left join goal_reached on goal_reached.goal_id = goal.id
    -> left join game on goal_reached.game_id = game.id;
![Screenshot 2024-09-29 213613](https://github.com/user-attachments/assets/f32777de-b3b0-4889-a989-6dff716a44f7)


### QUIZ 5

# 1
select name from country where iso_country in( select iso_country from airport where name like "Satsuma%");
![Screenshot 2024-09-29 213902](https://github.com/user-attachments/assets/a7f3abba-1f53-4601-af42-cfc0981515d1)

# 2
 select name from airport where iso_country in(select iso_country from country where name = "Monaco");
 ![Screenshot 2024-09-29 213920](https://github.com/user-attachments/assets/1103a8f0-e400-49a5-a257-e264bc1dac82)

# 3
select screen_name from game
    -> where id in(select game_id from goal_reached where goal_id
    -> in(select goal.id from goal where goal.name = "clouds"));
![Screenshot 2024-09-29 213939](https://github.com/user-attachments/assets/09b63385-03d3-4bd0-b8f4-67969e680423)

# 4
 select name from country where iso_country
    -> not in(select iso_country from airport);
![Screenshot 2024-09-29 213955](https://github.com/user-attachments/assets/2067597a-4737-43cc-9d8f-f5a38b253948)

# 5
select name from goal where id
    -> not in(select goal_id from goal_reached where game_id
    -> in(select game.id from game where screen_name = "Heini"));
![Screenshot 2024-09-29 214011](https://github.com/user-attachments/assets/dc92c55c-6423-4c7f-97fe-2b39b70dd253)



# Week [5]

### QUIZ 6

# 1
 select max(elevation_ft) from airport;
 ![Screenshot 2024-09-29 214059](https://github.com/user-attachments/assets/0de19b13-3d5c-4486-9e6f-884ae697dffa)

# 2
select continent, count(*)
    -> from country
    -> group by continent;
![Screenshot 2024-09-29 214114](https://github.com/user-attachments/assets/80f6cdf5-95df-4dd1-9e7a-0a101e309e6a)

# 3
select screen_name, count(*)
    -> from game, goal_reached
    -> where id = game_id
    -> group by screen_name;
![Screenshot 2024-09-29 214132](https://github.com/user-attachments/assets/8346bc3d-89e9-4dfd-878e-ab24f9096e23)

# 4
select screen_name from game
    -> where co2_consumed in(select min(co2_consumed) from game);
![Screenshot 2024-09-29 214146](https://github.com/user-attachments/assets/0fa37af8-0658-4520-9470-7817e1893b9e)

# 5 
 select country.name, count(*) from airport, country
    -> where airport.iso_country = country.iso_country
    -> group by country.iso_country
    -> order by count(*) desc
    -> limit 50;
![Screenshot 2024-09-29 214203](https://github.com/user-attachments/assets/207a7ebb-a840-4ed3-a116-bbd9b4edaa12)

# 6
 select country.name from airport, country
    -> where airport.iso_country = country.iso_country
    -> group by country.iso_country
    -> having count(*) >= 1000;
![Screenshot 2024-09-29 214222](https://github.com/user-attachments/assets/7e7186d2-d772-400f-8553-11f7e408925c)

# 7
 select name from airport where elevation_ft in(select max(elevation_ft) from airport);
 ![Screenshot 2024-09-29 214238](https://github.com/user-attachments/assets/a0f69b74-f934-4ccf-92b7-8b336cd3a27e)

# 8
 select name from country
    -> where iso_country in(select iso_country from airport
    -> where elevation_ft in(select max(elevation_ft) from airport));
    ![Screenshot 2024-09-29 214253](https://github.com/user-attachments/assets/a98cc501-937d-426d-89bd-bca261e10464)

# 9
 select count(*) from goal
    -> where id in(select goal_id from goal_reached
    -> where game_id in(select game.id from game
    -> where screen_name = "Vesa"));
![Screenshot 2024-09-29 214317](https://github.com/user-attachments/assets/47f25311-d5db-4a06-8ed1-a97a9cd60bdc)

# 10
 select name from airport
    -> where latitude_deg in(select min(latitude_deg) from airport);
![Screenshot 2024-09-29 214342](https://github.com/user-attachments/assets/a296048d-b8d8-41f9-9403-a64143d134c1)

