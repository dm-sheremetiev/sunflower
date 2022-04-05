# 1. Цель проекта
Цель проекта - разработать интернет-магазин для киевской студии цветов "SUNFLOWER". Пользователи смогут заказывать цветы онлайн на доставку или самовывоз и мгновенно делать оплату товара или услуг через платежный сервис Приват24. 

# 2. Описание системы
Система будет состоять из следующих функциональных частей:
1. Пользовательский интерфейс заказа.
2. Регистрация, аутентификация и авторизация.
3. Панель администратора для управления магазином.
4. Форма обратной связи.
5. Интеграция с POS системой "Poster".

## 2.1. Пользовательский интерфейс

Пользовательский интерфейс предоставит возможность оформления покупателем заказа на товар или услугу и дальнейшая её
оплата через платёжную систему Приват24. Пользователь сможет добавлять товары в корзину, редактировать их кол-во, а
также удалять их. При оформлении заказа пользователю будет доступна форма, в которой будут указаны контактные данные и возможность привязки своей персональной скидки к заказу. Для клиента будет возможность связи с магазином через форму связи.

## 2.2. Типы пользователей

Всего существуют два вида вторизированых пользователей: администратор и клиент. 

## 2.3. Панель администратора 

Панель администратора будет представлена обычной админ-панелью Django. Возможна кастомизация шаблона, добавление приложений для редактирования текста и инных полей. Также предпочтительным блоком будет создания dashboard, где будут видны наиболее популярные заказы и представление данных в графическом виде для удобства. 

Функционал администратора, в первую очередь, предусматривает:
* Создание товара на главной странице.
* Редактирования имеющихся товаров.

## 2.4. Формы связей
Формы связей с администрацией будут вынесены на отдельную страницу **без** возможности загрузки файлов.

## 2.5. Система регистрации и авторизации
При регистрации пользователя автоматически будут добавлять пользователя к программе лояльности (основная цель регистрации).
Форма для регистрации должна состоять из следующих полей:
1. Полное имя (обязательно).
2. Номер телефона (обязательно).
3. Email (обязательно).
4. Дата рождения родственников: жены, мамы, дочери и т.д (опционально).
5. Возможность напоминания о подарке цветов перед праздником (опционально).
6. Предпочтительный адрес доставки (опционально).

## 2.6. Интеграция с внешними сервисами

Интернет-магазин должен быть интегрирован с сервисами такими как Google Maps, Poster POS и др. Должна быть предусмотрена карта с размещением магазина. С Poster POS должна быть возможность соединения к имеющейся базе данных клиентов в программе лояльности, привязка их процента скидки к выходной цене товара в корзине пользователя, а также добавления суммы заказа с сайта в программу лояльности Poster. Также, при заказе товара от нового покупателя должна быть возможность создания карточки клиента в программе лояльности. Форма для оформления карты лояльности будет на благотворительных основах (клиент имеет право отказаться от оформления).

## 2.7. Аналитика

Автор сможет видеть следующую аналитику:
1. Общее кол-во заказов с сайта и их графическое представление в отдельной HTML странице (доступна только администратору).
2. Популярные товары к заказу и возможно время оформления заказа между первым посещением сайта и оплатой заказа.

## 3. Предполагаемый стек технологий

Фронт:
* HTML, CSS(bootstrap or other), JS(simple animations)

Бэк:
* Python
* Django
* PostgreSQL
* Django REST

Интернет эквайринг: Приват24. Возможность оплаты Google/Apple Pay. Приём иностранных платежей: PayPal и д.р.(опционально).
# 4 Требования к дизайну

Лаконичность, минимализм, мягкие нежные тона с современными цветами (как пример сервисы Apple, Дия).


