1) Посмотреть где я: 
'''bash
pwd
'''
2) Создать папку: mkdir folder
3) Зайти в папку: cd folder
4) Создать 3 папки: mkdir folder{1..3}
5) Зайти в любую папку: cd folder1
6) Создать 5 файлов (3 txt, 2 json): touch file{1..3}.txt file{4..5}.json
7) Создать 3 папки: mkdir folder{4..6}
8) Вывести список содержимого папки: ls -la
9) + Открыть любой txt файл: cat >> file1.txt
10) + Написать туда что-нибудь, любой текст: 123
11) + Сохранить и выйти: ctrl+c
12) Выйти из папки на уровень выше: cd ..
13) Переместить любые 2 файла, которые вы создали, в любую другую папку: mv folder2/{file1.txt,file2.txt} folder3
14) Скопировать любые 2 файла, которые вы создали, в любую другую папку: cp folder3/{file1.txt,file2.txt} folder2
15) Найти файл по имени: find -iname file1.txt
16) Просмотреть содержимое в реальном времени (команда grep) изучите как она работает: tail -f file3.txt | grep 555
17) Вывести несколько первых строк из текстового файла: cat file3.txt | sed -n 1,2p (второй вариант: head -2 file3.txt)
18) Вывести несколько последних строк из текстового файла: tac file3.txt | sed -n 1,2p (второй вариант: tail -2 file3.txt)
19) Просмотреть содержимое длинного файла (команда less) изучите как она работает: less folder3/file2.txt (less +F file3.txt отображать в режиме реального времени)
20) Вывести дату и время: date +%c

Задание *
1) Отправить http запрос на сервер http://162.55.220.72:5005/terminal-hw-request: curl http://162.55.220.72:5005/terminal-hw-request 
										  curl http://162.55.220.72:5005/get_method?name=Dima'&'age=31
2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13: touch script.sh
									       vim script.sh
									       
									      		 #!/bin/bash

									       		 cd folder
									       		 mkdir folder{1..3}
									       		 cd folder1
									       		 touch file{1..3}.txt file{4..5}.json
									       		 mkdir folder{4..6}
									       		 ls -la
									       		 cd ../
									       		 mv folder1/{file1.txt,file2.txt} folder2
									                 
											 :wq
									       chmod +x ./script.sh
									       ./script.sh
