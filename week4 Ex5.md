Q1
select name
from country
where iso_country in(
select iso_country
from airport
where name like "Satsuma%"
);


<img width="690" alt="Screenshot 2024-10-08 at 19 29 30" src="https://github.com/user-attachments/assets/2f9401c0-b6ed-4c1b-be3a-296b81b9553f">
 
 Q2
 select name
from airport where
iso_country in(
select iso_country
from country
where name = "Monaco"
);


<img width="690" alt="Screenshot 2024-10-08 at 19 30 53" src="https://github.com/user-attachments/assets/cc50f368-4988-444b-90df-757a546d6e62">

Q3
select screen_name
from game
where id in (
select game_id
from goal_reached
where goal_id in(
select id
from goal
where name = "CLOUDS"
)
);


<img width="690" alt="Screenshot 2024-10-08 at 19 34 12" src="https://github.com/user-attachments/assets/7b21ac6c-8a4e-4f8e-9434-8a260bdcb999">


Q4
select country.name
from country
where iso_country not in
(select airport.iso_country
from airport);


<img width="690" alt="Screenshot 2024-10-08 at 19 34 46" src="https://github.com/user-attachments/assets/f220c136-390c-4964-8efb-1a4022d88378">
Q5
select name
from goal
where id not in(
select goal.id
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini"
);


<img width="690" alt="Screenshot 2024-10-08 at 19 35 12" src="https://github.com/user-attachments/assets/55d405ec-7ea5-4389-bf92-7cecace68ebd">

 
