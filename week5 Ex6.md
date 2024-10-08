Q1
select max(elevation_ft)
from airport;


<img width="690" alt="Screenshot 2024-10-08 at 19 41 29" src="https://github.com/user-attachments/assets/6d53a080-d581-4650-8b61-cea1645a6a0c">

Q2
select continent, count(*)
from country
group by continent;


<img width="690" alt="Screenshot 2024-10-08 at 19 42 56" src="https://github.com/user-attachments/assets/69bfeaf7-811a-4736-be19-98d556dea0a3">

Q3
select screen_name, count(*)
from game, goal_reached
where id = game_id
group by screen_name;


<img width="690" alt="Screenshot 2024-10-08 at 19 43 44" src="https://github.com/user-attachments/assets/e9e02302-923f-44da-a572-7811aabd0911">

Q4
select screen_name
from game
where co2_consumed in(select min(co2_consumed)from game );


<img width="690" alt="Screenshot 2024-10-08 at 19 45 02" src="https://github.com/user-attachments/assets/cb533fc0-f57d-4b02-9a9c-40265d08fb07">

Q5
select country.name, count(*)
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;

<img width="690" alt="Screenshot 2024-10-08 at 19 45 52" src="https://github.com/user-attachments/assets/f64a5572-5520-43aa-8d3c-f13b3dfc9b6e">

Q6
select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) > 1000;


<img width="690" alt="Screenshot 2024-10-08 at 19 47 37" src="https://github.com/user-attachments/assets/e9257532-1f7a-4df8-bc88-93cc781725d2">

Q7
select name
from airport
where elevation_ft in (select max(elevation_ft) from airport);


<img width="690" alt="Screenshot 2024-10-08 at 19 48 33" src="https://github.com/user-attachments/assets/ff8963b0-84ca-4966-ace7-3a091e5ef66f">

Q8
select name
from country
where iso_country in (select iso_country from airport
where elevation_ft in(select max(elevation_ft)
from airport));


<img width="690" alt="Screenshot 2024-10-08 at 19 49 50" src="https://github.com/user-attachments/assets/19157e27-4003-45ad-a8a2-95d8d0d851f8">

Q9
select count(*)
from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by screen_name;


<img width="690" alt="Screenshot 2024-10-08 at 19 50 40" src="https://github.com/user-attachments/assets/f183a60d-5944-4620-99e0-2d2f3fc89980">



Q10
select name
from airport
where latitude_deg in(
select min(latitude_deg)
from airport
);


<img width="690" alt="Screenshot 2024-10-08 at 19 39 54" src="https://github.com/user-attachments/assets/635c5fc2-cf10-4daa-9a34-b0183ef87b66">


