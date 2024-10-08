Q1
select country.name as "country name", airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country and country.name = "Iceland";

<img width="706" alt="Screenshot 2024-10-08 at 18 46 06" src="https://github.com/user-attachments/assets/07a31926-6999-4f68-a253-9005359af8e5">

Q2
select airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country 
and country.name = "France" and 
airport.type = "large_airport";

<img width="632" alt="Screenshot 2024-10-08 at 18 48 35" src="https://github.com/user-attachments/assets/dc6b7a8d-8b9f-4637-ba02-bdf5f4571dba">

Q3
select country.name as country_name, airport.name 
as airport_name
from airport, country
where airport.iso_country = country.iso_country 
and country.continent = "AN";

<img width="966" alt="Screenshot 2024-10-08 at 18 50 18" src="https://github.com/user-attachments/assets/6961377f-938d-439d-aebe-aa53654f5078">

Q4
select elevation_ft
from airport, game
where location = ident and screen_name = "Heini";

<img width="966" alt="Screenshot 2024-10-08 at 18 52 57" src="https://github.com/user-attachments/assets/42b5d6e4-c041-4ef7-a524-9742f742ad45">

Q5
select elevation_ft * 0.3048 as elevation_m
from airport, game
where location = ident and screen_name = "Heini";

<img width="966" alt="Screenshot 2024-10-08 at 18 51 36" src="https://github.com/user-attachments/assets/8a7492b5-b398-448a-9cdd-da381b9205b0">

Q6
select name
from airport, game
where location = ident and screen_name = "Ilkka";

<img width="966" alt="Screenshot 2024-10-08 at 18 54 11" src="https://github.com/user-attachments/assets/dd3e9bb7-6ee4-4543-9206-fed9aa1a36e7">

Q7
select country.name from airport, game, country
where location = ident 
and airport.iso_country = country.iso_country  
and screen_name = "Ilkka";

<img width="690" alt="Screenshot 2024-10-08 at 19 08 49" src="https://github.com/user-attachments/assets/583fa38a-670c-4234-abc4-daf664c47400">

Q8
select name
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id 
and screen_name = "Heini";

<img width="690" alt="Screenshot 2024-10-08 at 19 09 53" src="https://github.com/user-attachments/assets/07fdc4f6-eb9c-4d51-9588-79664e329bdc">

Q9
select airport.name
from airport, game, goal, goal_reached
where ident = location and game.id = game_id and goal.id = goal_id 
and screen_name = "Ilkka" and goal.name = "CLOUDS";

<img width="690" alt="Screenshot 2024-10-08 at 19 11 03" src="https://github.com/user-attachments/assets/fed2b89f-ffd5-4bfc-8373-0fdd1bae031d">

Q10
select country.name
from country, airport, game, goal, goal_reached
where airport.iso_country = country.iso_country 
and ident = location and game.id = game_id 
and goal.id = goal_id and screen_name = "Ilkka" 
and goal.name = "CLOUDS";

<img width="690" alt="Screenshot 2024-10-08 at 19 12 14" src="https://github.com/user-attachments/assets/10fecd80-9dd7-4204-bd47-265fab28fec2">

