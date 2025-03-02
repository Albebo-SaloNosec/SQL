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



1) Выберите из таблицы orders 3 самых дешевых заказа за всё время.
Данные нужно отсортировать в порядке убывания цены.
Отмененные заказы не учитывайте.
![image](https://github.com/user-attachments/assets/5b8d2fdc-2518-4886-801e-e28cc925fab9)
![image](https://github.com/user-attachments/assets/9c3ccef8-ca0f-4c33-a0d9-33b96bcafac1)
Ответ: SELECT * FROM orders WHERE status != 'cancelled' ORDER BY sum ASC LIMIT 3;
2) Выберите из таблицы orders 2 самых дорогих заказов за всё время.
Данные нужно отсортировать в порядке убывания цены.
Отмененные заказы не учитывайте.
![image](https://github.com/user-attachments/assets/8340c706-2791-4084-bc4a-701a1416626f)
![image](https://github.com/user-attachments/assets/cf35d6b9-7ea0-41a8-857c-d7ed46ec49b8)
Ответ: SELECT * FROM orders WHERE status != 'cancelled' ORDER BY sum DESC LIMIT 2;
3) Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).
![image](https://github.com/user-attachments/assets/dfee366e-9f25-4582-a098-424e8bf9bb46)
![image](https://github.com/user-attachments/assets/7dd73fab-618d-4fef-ac54-496b68eab3be)
Ответ: INSERT INTO orders (id, products, sum) VALUES (6, 4, 8000);
4) Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.
![image](https://github.com/user-attachments/assets/5aa26f90-2514-4b8a-b0cd-2b586cb123ee)
![image](https://github.com/user-attachments/assets/5c67f61b-ed24-4027-b5c4-6ac64a682640)
Ответ: INSERT INTO products (id, name, count, price) VALUES (7, 'VR-очки', 2, 70000);
5) В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.
![image](https://github.com/user-attachments/assets/c79e7851-8ce7-4039-9ca0-e4a460492395)
![image](https://github.com/user-attachments/assets/d36dd19a-c7f5-4a63-8a59-c0d785596307)
Ответ: UPDATE products SET name = 'PS5' WHERE name = 'IMAC';

Создайте таблицу users с полем id типа INT и двумя текстовыми полями, которые будут хранить имя (first_name) и фамилию (last_name). Длина имени и фамилии не превышает 50 символов.
Добавьте в таблицу трех пользователей: Дмитрия Иванова, Анатолия Белого и Дениса Давыдова.
![image](https://github.com/user-attachments/assets/856b6562-190f-4631-9f65-88fd9ebdb9ab)
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50)
);
![image](https://github.com/user-attachments/assets/aa82cfe9-7909-4449-a737-a1e568623135)
INSERT INTO users (first_name, last_name)
VALUES
    ('Дмитрий', 'Иванов'),
    ('Анатолий', 'Белый'),
    ('Денис', 'Давыдов');
![image](https://github.com/user-attachments/assets/dbe5ee16-20e4-43cc-851e-7b5f1da2dd52)
