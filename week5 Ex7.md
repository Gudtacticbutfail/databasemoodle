Q1
update game
set  location = (select ident from airport where name = "Nottingham Airport"), co2_consumed = co2_consumed+500
where screen_name = "Vesa";

select * from game;


<img width="840" alt="Screenshot 2024-10-08 at 19 56 07" src="https://github.com/user-attachments/assets/5e65e5a4-661c-4987-84ef-eefc5993124f">

Q3
delete from goal_reached;
select * from goal_reached;


<img width="626" alt="Screenshot 2024-10-08 at 19 58 20" src="https://github.com/user-attachments/assets/1610c052-0142-42e4-b482-f63f99bc146c">

Q4
delete from game; select * from game;


<img width="589" alt="Screenshot 2024-10-08 at 19 59 07" src="https://github.com/user-attachments/assets/c34a76b7-46ed-404c-ba63-18f1888d02f7">


