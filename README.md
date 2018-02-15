# Hello!

<a href="https://codeclimate.com/github/codeclimate/codeclimate/maintainability"><img src="https://api.codeclimate.com/v1/badges/a99a88d28ad37a79dbf6/maintainability" /></a>
<a href="https://codeclimate.com/github/codeclimate/codeclimate/test_coverage"><img src="https://api.codeclimate.com/v1/badges/a99a88d28ad37a79dbf6/test_coverage" /></a>
[![Build Status](https://travis-ci.org/Dexter-Freeman/project-lvl1-s224.svg?branch=master)](https://travis-ci.org/Dexter-Freeman/project-lvl1-s224)


Этот проект выполняет Dexter Freeman в рамках прохождения проекта "Brain Games" на Hexlet.

Задачи:
	Инициализация пакета
		1. Проект создан
		2. Файл src/bin/brain-games.js создан. Первой строкой идет шебанг - "#!/usr/bin/env node"
		3. Запуск src/bin/brain-games.js выводит на экран строку: "Welcome to the Brain Games!" (console.log("Welcome to the Brain Games!"))

	Подключение Babel
		1. Файл Makefile создан, в нем прописана команда install
		2. Зависимости в package.json подключены
		3. Запуск make  пока не победил (Windows 7). Инсталл делаю через npm install, .gitignore создан
		4. .babelrc настроен. В package.json прописаны скрипты
		5. В Makefile создана комманда start

	Публикация в npm каталог
		1. Скрипт build не захотел работать. После удаления NODE_ENV=production работает через вот такую комманду - "npm run-script build" (makefile не работает).
		2. Хук prepublish создан
		3. bin добавлен как на сайте. После установки пакета запуск brain-games в консоли выводит то, что нужно - "Welcome to the Brain Games!"

		Пакет опубликовал вчера, но сегодня отредактирвал makefile, сделал unpublish, и теперь нужно ждать 24 часа чтобы заново его опубликовать ((  Но все работало

Шаг 2
	Сторонние библиотеки
		В package.json изменил "main": "dist/index.js",  было вот так: "main": "brain-games.js". Прописал так при инициализации проекта.

		Задачи:
			1. Подключил библиотеку readline-sync в файле package.json : "dependencies": {readline-sync": "*"}
			2. В index.js описал логику, экспортировал функцию, в brain-games.js импортировал эту функцию и вызвал после приветсвия. Все работает. Запуск через комманду npm start.
			3. С публикацией пока не получается, смогу только завтра опубликовать

Шаг 3
	Качество кода
		Задачи:
			1. Установил eslint, eslint-config-airbnb-base, eslint-plugin-import, babel-eslint в devDependencies
			2. В scripts добавил: "eslint": "eslint src/**/*.js"
			3. .eslintrc.yml скопировал из репозитория-образца (мало что понял)
			4. Добавил комманду make lint, запускающую npm run eslint
			5. Подключил eslint к Sublime

			Travis-ci
				1. Зарегистрировался
				2. Подключил репозиторий
				3. В .travis.yml сделал так: script:
                                               - npm run eslint
                4. Бейджи работают

                В файле src/index.js в последней строке оставил export { greeting }; не смотря на то что линтер хотел дефолтный экспорт, но с экспортом по дефолту перестает работать пакет

Шаг 4
	Игра: "Проверка на четность"
		Задачи:
			1. Добавил бинарник brain-even
			2. Реализовал необходимую логику
			3. Опубликовал пакет. Установил, все работает как надо
			4. Аскинема не работает в Windows, поэтому пока не могу сделать запись терминала.

Шаг 5
	Игра: "Калькулятор"
		Задачи:
			1. Добавил bin с названием brain-calc.js
			2. Реализовал небходимый вывод.