Q1
select country.name as "country name", airport.name as "airport name"
from country inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" and scheduled_service = "yes";

<img width="690" alt="Screenshot 2024-10-08 at 19 15 55" src="https://github.com/user-attachments/assets/a1abdf82-80af-476c-b80b-438d871201fd">

Q2
select screen_name, airport.name
from game inner join airport on location = ident;


<img width="690" alt="Screenshot 2024-10-08 at 19 16 57" src="https://github.com/user-attachments/assets/8ac7e071-356b-42d6-99a6-8d0adc7ae8d7">

Q3
select screen_name, country.name
from game inner join airport on location = ident 
inner join country on airport.iso_country = country.iso_country;


<img width="690" alt="Screenshot 2024-10-08 at 19 17 54" src="https://github.com/user-attachments/assets/4ff7dbbc-7f61-4032-9182-30a5706f69d7">

Q4
select airport.name, screen_name
from airport left join game on ident = location where name like "%Hels%";


<img width="690" alt="Screenshot 2024-10-08 at 19 18 56" src="https://github.com/user-attachments/assets/0686a309-2ddb-423e-86d4-394239a2bd62">

Q5
select name, screen_name
from goal left join goal_reached on goal.id = goal_id  left join game on game.id = game_id;


<img width="690" alt="Screenshot 2024-10-08 at 19 20 04" src="https://github.com/user-attachments/assets/893f601c-34ee-4a8a-807d-a2cc2c7ba535">


