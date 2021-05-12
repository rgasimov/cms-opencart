# Официальный модуль приема платежей Robokassa для OpenCart
Данный модуль позволяет добавить на сайт способ оплаты через Робокассу. 
Для корректной работы модуля необходима регистрация в сервисе.

Порядок регистрации описан в [документации Robokassa](https://docs.robokassa.ru/#7844)

### Возможности
* Передача состава товаров в заказе для отправки чека клиенту и в налоговую (54-ФЗ);
* Автоматическое формирование итогового чека;
* Приём платежей в тестовом режиме;
* Автоматическая смена статуса заказа;
* Поддержка продажи через iframe
* Поддержка отправки второго чека и маркировки товара
* Поддержка продавцов из Казахстана

### Совместимость
OpenCart v.3.0.0.0 и выше;

### Установка через панель управления

"Меню" -> "Модули/Расширения" -> "Установка расширений" -> "Загрузить".

### Ручная установка

1. Загрузить и разархивировать модуль
2. Переместить папки admin и catalog в корневую директорию OpenCart с заменой

### Настройка модуля

1. Перейти в настройки модуля "Модули/Расширения" -> "Модули/Расширения" -> "Оплата".
Выбрать Robokassa и активировать модуль.
2. Зайти в настройки модуля и указать обязательные данные:
    * Идентификатор магазина
    * Пароль 1
    * Пароль 2
    * Сменить статус на "включено"
    
    Затем сохранить введенные параметры.
    
3. В личном кабинете Robokassa ("мои магазины" - "настройки" - "технические настройки") указать Result URL, Success URL и Fail URL, которые указаны в настройках модуля.

### Фискализация

Для подключения автоматического формирования чеков в соответвии с ФЗ-54 необходимо подключить одну из доступных фискальных схем в Личном кабинете Robokassa ([Раздел "Фискализация"](https://partner.robokassa.ru/Fiscalization){:target="_blank"}) и указать настройки модуля:

* Фискализация - "Да".
* Система налогообложения.
* Налоговая ставка.
* Признак способа расчёта.

### Уведомления об оплате

Уведомление об оплате Robokassa отправляет автоматически, после успешного совершения платежа, на адрес Result URL, который был скопирован из настроек модуля и указан в технических настройках магазина. После получения уведомления, заказ в CMS изменит статус на тот, который указан в поле "Статус заказа после оплаты".
При правильной настройке Robokassa самостоятельно сообщит в модуль статус оплаты, после чего статус заказа изменится согласно настройкам.

### Changelog  


ПОКА ПУСТО
