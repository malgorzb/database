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
# 2
# 3
# 4
# 5 
# 6
# 7
# 8
# 9
# 10
