# Структура

- Main
	- Dev
		- Feature-123
		- BugFix-123
		- Test
	
	- Release-1.0.0.0
		- HotFix
	- Release-1.0.0.1
	
# Описание веток

Main - основная ветка в которой всегда поддерживается работоспособный билд. Из этой ветки растет Dev ветка и Release ветки.

Dev - ветка разработки. Из которой растут ветки создаваемые для внедрения фичи, исправления бага или создания тестового билда.

Test - ветка создаваяемая девопсом для нужд тестировки.

Release - ветка создаваемая из main с присвоением номера версии. 

HotFix - ветки создаваемые непосредственно в релизной ветке для горячего исправления актуального релиза.


# Пайплайн разработки

1. Тимлид создает репозиторий. Main и Dev ветки. 
2. Команда разработки ведет разработку в подветках Dev, внедряя фичи или исправляя баги. 
3. Изменения в подветках dev мерджатся в dev.
4. Когда требуется тесты, девопс создает ветку Test от Dev с последним коммитом или с коммитом указанным тимлидом. 
5. Когда проект в Dev ветке готов для релиза - тимлид мерджит Dev ветку в Main
6. Девопс создает Release ветку с номером версии от Main.
7. Команда разработки может создавать HotFix ветки в Release ветках для быстрых правок релиза.