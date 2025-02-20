1) Выберите из таблицы orders все заказы
![image](https://github.com/user-attachments/assets/8ada50b3-27cc-4880-8375-b4333ccaac6f)
Ответ: Select * from orders;
2) Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in
   ![image](https://github.com/user-attachments/assets/4fd42d61-dd96-4e4c-be78-ffb7df2c3b9c)
Ответ: Select * from orders where status in ('delivery', 'in_progress', 'cancelled');
3) Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".
   ![image](https://github.com/user-attachments/assets/d2d5896b-9e99-43be-a529-83de1dc5d0dc)
Ответ: Select * from orders where status in ('new', 'cancelled');
4) Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count).
Вывести нужно только номер (id) и сумму (sum) заказа.
![image](https://github.com/user-attachments/assets/5f857bb7-f290-430a-be61-ee01be7d0b3b)
Ответ: Select id, sum from orders where products_count>3;
