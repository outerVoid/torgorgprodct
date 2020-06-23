1) В корне программы есть файл .gitignore, в нем описаны все файлы, которые игнорируются при экспорте веб-приложения 
2) Для корректной работы, требуется создать бд. 
Таблицы и данные вписывать не нужно, так как в проекте реализованы миграции и сидеры[подробнее можно прочитать тут. https://laravel.com/docs/7.x]
3)некоторая инструкция:
		Установить XAMPP (PHP 7 + MySQL)
		Перейти в папку xampp\htdocs
		клонировать с помощью git проект
		----- (необязательно, но для попадания на сайт потребуется вводить путь к папке public, начиная от папке htdocs не включая её)
		(Для windows) В файле C:\xampp\apache\conf\extra\httpd-vhosts.conf сделать запись
		<VirtualHost *:80>
  		DocumentRoot "C:\xampp\htdocs\platonus\public"
 		 ServerAdmin platonus
  		<Directory "C:\xampp\htdocs\platonus">
    		    Options Indexes FollowSymLinks
     		   AllowOverride All
     		   Require all granted
 		 </Directory>
		</VirtualHost>
		-----
		Установить Composer
		Установить зависимости проекта. Перейти в папку приложения и выполнить команду composer update
		Создать базу данных через phpmyadmin
		Создать файл .env по примеру файла .env.example
		ввести настройки БД в файл .env
p.s. также нужно установить на свой компьютер чистый проект laravel (желательно 7.x) для корректной работы ис;
4) ссылка на проект в гитхабе - https://github.com/outerVoid/torgorgprodct
