# Портфолио
Здесь собраны примеры тестовой документации, выполненные во время тестирования ранних сборок проектов "Farming Fever", "Differences"
- [Баг-репорты](#bug-reports)
- [Тест-кейсы](#test-cases)
- [Чек-лист для регресс-теста](#checklist-regress)
- [Отчет о тестировании](#test-report)
# <a name="bug-reports"/> Баг-репорты

| ID | Краткое описание (Summary) | Подробное описание (Description) | Шаги и результат (Steps&Result) | Критичность (Severity) | Приоритет (Priority) | Вложения (attachment) |
| ------------- | ------------- | ------------------ | ------ | ------ | ------ | ------ |
| 1  | Игра не заканчивается при окончании таймера | После запуска игры таймер идет, но по его истечению игра не завершается, и проигрыш не засчитывается | 1. Запустить игру и начать уровень <br> 2. Дождаться пока таймер достигнет нуля <br><br> Ожидаемый результат: Игра заканчивается поражением игрока <br><br> Фактический результат:  Игра не заканчивается и поражение не засчитывается  | Критический | Высокий  | [Незавершенность игры](https://drive.google.com/file/d/1XtNSI87JXX8FbqHI6HnSae-LTsPk1kVa/view?usp=sharing)  | 
| 2 | Бесконечная загрузка уровня  | При первом запуске игры без подключения к интернету игра застревает на бесконечной загрузке и не переходит к главному экрану. Если же игру сначала запустить с интернетом, а затем отключить его во время игры, через некоторое время снова возникает бесконечная загрузка  | 1. Отключить интернет <br> 2. Запустить игру впервые <br><br> Ожидаемый результат: Игра загружается корректно, и пользователь может войти в офлайн-режим <br><br> Фактический результат: Возникает бесконечная загрузка. <br><br> 3. Подключить интернет <br> 4. Запустить игру снова <br> 5. Отключить интернет во время активного игрового процесса <br> 6. Продолжить играть <br><br> Ожидаемый результат: Игра продолжает работать в офлайн-режиме <br><br> Фактический результат: Игра застревает на бесконечной загрузке после некоторого времени работы без интернета"  | Критический  |  Высокий | [Бесконечная загрузка](https://drive.google.com/file/d/1PpCJ8WEZSYNEF6i06eSZIhkVo9sTB6bp/view?usp=sharing)  | 
| 3 | Завершение уровня без нахождения всех отличий  | Уровень завершается победой игрока, когда он находит только 4 из 5 отличий  | 1. Запустить игру и начать уровень <br> 2. Найти 4 из 5 отличий между двумя картинками <br><br>Ожидаемый результат: Игра продолжается пока не найдены все отличия <br><br> Фактический результат: Игра завершает уровень и позволяет игроку перейти к следующему  | Значительный  | Средний | [Найденные отличия](https://drive.google.com/file/d/1Q7J1yDI7mo0Hj-BY5mrRlDJ0DZwki2xl/view?usp=sharing)  | 
| 4 | Кнопка "продолжить" не переводит на следующий уровень  | После завершения уровня кнопка "Продолжить" не переносит игрока на следующий уровень  | 1. Запустить игру <br> 2. Пройти любой уровень <br> 3. Нажать на кнопку "Продолжить" <br><br> Ожидаемый результат: Игрок переходит на следующий уровень <br><br> Фактический результат: Ничего не происходит, игрок остается на текущем экране завершенного уровня | Значительный | Средний  | [Не работает кнопка продолжить](https://drive.google.com/file/d/1NXTwHZxpC-adlln3JTizRddMNSSU9l0H/view?usp=sharing) | 
| 5 | Отключение вибрации приводит к отключению музыки и наоборот  | В меню настроек, когда игрок отключает вибрацию, неожиданно выключается музыка, а при отключении музыки отключается вибрация | 1. Запустить игру <br> 2. Зайти в меню настроек <br> 3. Выключить вибрацию <br><br> Ожидаемый результат: Вибрация отключается <br><br> Фактический результат: Отключается музыка <br><br> 4. Отключить музыку. <br><br> Ожидаемый результат: Отключается музыка <br><br> Фактический результат: Вибрация отключается | Значительный  | Средний  | [Настройки музыки](https://drive.google.com/file/d/1EIZ1cx4VqO5hhHEBfk2YeKZPyRYaa39C/view?usp=sharing) | 
| 6 | Обводка отличия у другого объекта  | При нахождении отличия обводка иногда отображается смещенной и выделяет неправильный объект вместо того, который действительно отличается  | 1. Запустить игру и начать уровень <br> 2. Найти объект, который отличается на двух изображениях <br> 3. Нажать на этот объект для выделения <br><br> Ожидаемый результат: Обводка точно выделяет объект, который отличается между изображениями <br><br> Фактический результат: Обводка смещена и выделяет неправильный объект | Значительный  | Средний  | [Обводка объекта](https://drive.google.com/file/d/1CT-V4tlgo_zN-B6xHUyVsGqzDTsEWjrj/view?usp=sharing) | 
| 7 | Шкала прогресса уровня заполняется не последовательно  | При нахождении отличия шкала заполняется не с первого элемента. При быстром последовательном нажатии на отличия значения шкалы смещаются вправо, пропуская предыдущие позиции | 1. Запустить игру и начать уровень <br> 2. Найти отличие <br><br> Ожидаемый результат: Отметка о найденном отличии появляется на первой позиции <br><br> Фактический результат: Отметка заполняется со второй позиции <br> 3. Быстро и последовательно найти отличия. <br><br> Ожидаемый результат: Отметка о найденном отличии появляется на соответствующей позиции <br><br> Фактический результат: Отметка смещается вправо, оставляя пропуски на предыдущих позициях | Незначительный  | Низкий  | [Отметки](https://drive.google.com/file/d/1fwjWuc4PEpVwQ8dBZKsAI2g1gxqxTSFa/view?usp=sharing) | 
| 8 | Музыка заканчивается до окончания уровня  | Музыкальный трек, сопровождающий уровень, останавливается, не дойдя до окончания уровня  | 1. Запустить игру и начать уровень <br> 2. Дождаться завершения музыкального трека, не завершая уровень <br><br> Ожидаемый результат: Музыка не останавливается до завершения уровня <br><br> Фактический результат: Музыка завершается раньше уровня  | Незначительный  | Низкий | [Музыкальное сопровождение](https://drive.google.com/file/d/1IJSl99LOsIngPsJxVtX7_AlmgWZAUb8S/view?usp=sharing)  | 
| 9 | Цифры накладываются на таймер  | При быстром нажатии на неправильные отличия цифры таймера накладываются друг на друга  | 1. Запустить игру и начать уровень <br> 2. Быстро и многократно нажимать на неправильные отличия <br><br> Ожидаемый результат: Таймер корректно отображает оставшееся время, независимо от частого снижения <br><br> Фактический результат: Цифры на таймере накладываются друг на друга, что делает время нечитабельным | Незначительный | Низкий | [Таймер](https://drive.google.com/file/d/1X9xxv2fVBPyugL7OV5QMEnd495Is8J_y/view?usp=sharing) | 
| 10 | Промах появляется за границами изображения  | При одновременном нажатии на две картинки метка промахаотображается за границами изображений  | 1. Запустить игру и начать уровень <br> 2. Одновременно нажать на две картинки <br><br> Ожидаемый результат: Метки промаха появляются внутри изображений <br><br> Фактический результат: Метки промаха появляются также за пределами изображений  | Незначительный  | Низкий | [Метки за границей](https://drive.google.com/file/d/1TQhOxdvWsUZUo-wKzBCfmn7Xq2ZEtPWp/view?usp=sharing)  | 
| 11 | Звук предупреждения о завершении уровня не заканчивается  |  Если время истекло, и игрок выходит в меню, а затем возвращается на уровень, звуковое предупреждение продолжает играть  | 1. Запустить игру и начать уровень <br> 2. Подождать окончания таймера <br> 3. Выйти в меню и начать уровень заново <br><br> Ожидаемый результат: При повторном входе в меню и на уровень таймер и звук предупреждения сбрасываются, и звук начинает играть только по окончании нового таймера <br><br> Фактический результат: Звук предупреждения продолжает играть в меню и сразу при входе на уровень | Незначительный  | Низкий  | [Не заканчивающийся звук](https://drive.google.com/file/d/1UdpXEGjiImdFJ6w1PEiTwq-nrziK0pMN/view?usp=sharing)  | 
| 12 | Игра ломается при использовании подсказки за рекламу после нахождения всех 5 отличий  | Если игрок находит все 5 отличий и затем пытается воспользоваться подсказкой, которая требует просмотра рекламы, игра перестает функционировать должным образом  | 1. Запустить игру и начать уровень <br> 2. Найти все отличия <br> 3. Воспользоваться подсказкой на рекламу <br><br> Ожидаемый результат: Игра предлагает просмотреть рекламу, а затем корректно обрабатывает действие, позволяя игроку перейти на следующий уровень <br><br> Фактический результат: Игра ломается, не позволяя завершить текущий уровень  | Критический  | Высокий | [Подсказка и 5 отличий](https://drive.google.com/file/d/1aXvVn6cTRBaXrdKQ_MdTclut3xPRKB8u/view?usp=sharing)  | 
| 13 | Нельзя воспользоваться кнопкной "Восстановить"  | В меню настроек кнопка "Восстановить", предназначенная для восстановления предыдущих настроек или покупок, не реагирует на нажатия  | 1. Запустить игру <br> 2. Зайти в меню настроек <br> 3. Нажать на "Восстановление" <br><br> Ожидаемый результат: Кнопка ""Восстановить"" активируется и выполняет свой функционал <br><br> Фактический результат: Кнопка "Восстановить" не нажимается и не выполняет никаких действий  | Content Cell  | Content Cell  | Content Cell  | 
| 14 | Вылет игры  | Во время игры приложение иногда вылетает, показывая сообщение об ошибке. Это может происходить в произвольные моменты  | 1. Запустить игру и начать уровень <br> 2. Продолжать играть, пока не произойдет вылет <br><br> Ожидаемый результат: Игра продолжает функционировать <br><br> Фактический результат: Игра вылетает с ошибкой, и пользователь возвращается на рабочий стол  | Критический  | Высокий  | [Вылет](https://drive.google.com/file/d/191UtLzo9QI2q6BPE1-Dhhywhjl3CVRFD/view?usp=sharing)  | 
| 15 | Опечатка в слове уровень  | При запуске уровня выше таймера отображается надпись "Уроень"  | 1. Запустить игру и начать уровень <br> 2. Обратить внимание на слово "уровень" <br><br>Ожидаемый результат: Слово написано правильно <br><br> Фактический результат: В слове присутствует опечатка | Тривиальный  | Низкий  | [Опечатка](https://drive.google.com/file/d/1HuAk_ylIIs9D8LjGSFjv3aG8acuinaTn/view?usp=sharing)  | 
| 16 | Отсутствие обучения  | При первом запуске игры для нового игрока инструкция для новичков может не отображаться, хотя должна запускаться автоматически | Предусловие: Игра запущена впервые или с полностью очищенными данными <br> 1. Запустить игру и начать уровень <br><br> Ожидаемый результат: Инструкция для новичков отображается автоматически и пошагово вводит игрока в процесс игры <br><br> Фактический результат: Обучение не появляется  | Значительный | Высокий  | [Отсутствие обучения](https://drive.google.com/file/d/1OEF9BVMPAMD-SyBPs8xiPl5VDG_zeAkh/view?usp=sharing)  | 

# <a name="test-cases"/> Тест-кейсы

| ID  | Название (Title) | Шаги (Steps) | Ожидаемый результат | Статус (Status) |
| ------------- | ------------- | --- | --- | --- | 
| 1  | Запуск уровня | 1. Запустить игру <br> 2. Нажать кнопку запуска уровня | Открывается соответствующий уровень. На экране отображаются все необходимые элементы уровня, такие как таймер, изображения для поиска отличий и интерфейс управления | Пройден |
| 2 | Условие победы  | 1. Запустить игру <br> 2. Начать уровень <br> 3. Найти 5 отличий <br> 4. Убедиться, что таймер еще не закончился| После нахождения всех отличий игра отображает экран пройденного уровня  | Пройден  |
| 3 | Условие поражения  | 1. Запустить игру <br> 2. Начать уровень <br> 3. Убедиться, что таймер работает <br> 4. Подождать пока истечет время или специально ускорить таймер  | После того, как время истекло, игра отображает экран поражения  | Провален  |
| 4 | Выделение отличий  | 1. Запустить игру <br> 2. Начать уровень <br> 3. Найти отличие <br> 4. Нажать на отличие  | Обозначение отличий на двух изображениях в одинаковых местах  | Провален |
| 5 | Отображение найденных отличий  | 1. Запустить игру и начать уровень <br> 2. Найти отличия <br> 3. Наблюдать за шкалой найденных отличий | Отметки заполняются в соответствии с порядком найденных отличий  | Провален  |
| 6 | Проверка работы игры в офлайн-режиме  | 1. Отключить интернет на устройстве <br> 2. Запустить игру и начать игру | Игра корректно запускается в офлайн-режиме  | Провален  |
| 7 | Кнопка "Продолжить"  | 1. Запустить игру и начать уровень <br> 2. Успешно завершить уровень <br> 3. Нажать на кнопку "Продолжить" | Кнопка отобразилась правильно и при нажатии игрок переход на следующий уровень  | Провален  |
| 8 | Возврат на главный экран  | 1. Запустить игру и начать уровень <br> 2. Нажать кнопку выхода <br> 3. Подтвердить выход на главный экран  | Игрок возвращается на главный экран  | Пройден  |
| 9 | Открытие настроек  | 1. Запустить игру <br> 2. Открыть меню настроек  | Все параметры и опции настроек отображаются без ошибок (звуки, музыка, вибрация и т.д.)   | Пройден  |
| 10 | Открытие политики конфиденциальности и правил использования  | 1. Запустить игру <br> 2. Открыть меню настроек <br> 3. Нажать на ссылку "Политика конфиденциальности" <br> 4. Вернуться назад <br> 5. Нажать на ссылку "Правила использования"  | При нажатии на "Политику конфиденциальности" или "Правила использования"  открывается соответствующая страница, текст отображается корректно и полностью | Пройден  |
| 11 | Появление инструкции для новичков  | Предусловие: Игрок запускает игру впервые, прогресс не сохранен <br> 1. Запустить игру и начать уровень <br> 2. Дождаться загрузки уровня | Инструкция с подсказками для новичков отображается автоматически при первом запуске  | Провален  |
| 12 | Включение/ отключение звука, музыки и вибрации в настройках  | 1.Запустить игру <br> 2. Открыть меню настроек <br> 3. Включить или выключить звук/музыку/вибрацию  | Звук/музыка/вибрация включается или выключается соответсвено | Провален  |
| 13 | Проверка звуковых оповещений  | 1. Запустить игру и начать уровень <br> 2. Найти и отметить правильное отличие <br> 3. Найти и отметить неправильное отличие  | При нахождении правильного отличия воспроизводится звук подтверждения. При выборе неправильного отличия воспроизводится звук ошибки  | Пройден |
| 14 | Музыкальное сопровождение  | 1. Запустить игру / начать уровень  | Музыкальный трек играет корректно, без остановки   | Провален  |
| 15 | Автосохранение прогресса  | 1. Запустить игру и начать уровень <br> 2. Пройти успешно уровень <br> 3. Дождаться экрана с результатами уровня <br> 4. Перезапустить игру или вернуться в главное меню  | На главном экране видно, что игрок может пройти следующий уровень  | Пройден |
| 16 | Возможность восстановления игры  | 1. Запустить игру <br> 2. Открыть меню настроек <br> 3. Выбрать пункт "Восстановление"  | Происходит процесс восстановления игры  | Провален  |
| 17 | Возможность отключить рекламу  | 1. Запустить игру. <br> 2. Открыть меню настроек. <br> 3. Выбрать пункт "Убрать рекламу"  | За отдельную плату можно убрать рекламу из игры  | Заблокирован  |
| 18 | Подсказки  | 1. Запустить игру и начать уровень <br> 2. Нажать кнопку подсказки c 0/1/5 найденными отличиями <br> 3. Просмотреть полностью рекламный ролик  | Игрок получает подсказку о не найденном отличии и игра продолжается  | Провален  |

# <a name="checklist-regress"/> Чек-лист для регресс-теста

<table>
  <tr>
    <th rowspan="2">ID</th>
    <th rowspan="2">Функционал</th>
    <th rowspan="2">Тест-кейсы</th>
    <th colspan="3">Результат</th>
    <th rowspan="2">Комментарий</th>
  </tr>
  <tr>
    <th>Версия 0.7.3</th>
    <th>Версия 0.7.2</th>
    <th>Версия 0.7.1</th>
  </tr>
  <tr>
    <td>1</td>
    <td rowspan="6">Игровой процесс (геймплей)</td>
    <td>№1</td>
    <td>Да</td>
    <td>Да</td>
    <td>Да</td>
    <td></td>
  </tr>
  <tr>
    <td>2</td>
    <td>№2</td>
    <td>Да</td>
    <td>Да</td>
    <td>Да</td>
    <td></td>
  </tr>
  <tr>
    <td>3</td>
    <td>№3</td>
    <td>Да</td>
    <td>Да</td>
    <td>Баг</td>
    <td>Баг № 2</td>
  </tr>
   <tr>
    <td>4</td>
    <td>№4</td>
    <td>Да</td>
    <td>Да</td>
    <td>Баг</td>
    <td>Баг № 3</td>
  </tr>
   <tr>
    <td>5</td>
    <td>№5</td>
    <td>Да</td>
    <td>Баг</td>
    <td>Баг</td>
    <td>Баг № 4, 5</td>
  </tr>
  <tr>
    <td>6</td>
    <td>№6</td>
    <td>Да</td>
    <td>Да</td>
    <td>Баг</td>
    <td>Баг № 2</td>
  </tr>
</table>




<br>


# <a name="test-report"/> Отчет о тестировании

## 1. Обзор тестирования
Цель тестирования: <br><br> 
&nbsp;&nbsp;&nbsp;Тестирование функционала игры, чтобы выявить ошибки и проблемы в интерфейсе, игровой механике. <br>
&nbsp;&nbsp;&nbsp;Среда тестирования – Android OC. <br>
&nbsp;&nbsp;&nbsp;Сроки – в период с 31.10 по 14.11. <br>

| ID  | Краткое описание (Summary) | Подробное описание (Description) | Шаги и результат (Steps&Result) | Критичность (Severity) | Приоритет (Priority) | Вложения (attachment) |
| ------------- | ------------- | --- | --- | --- | --- | --- |
| 1 | Неправильный расчет итоговой выручки после выполнения заказа  | После выполнения игроком заказа итоговая выручка складывается неправильно (при суммировании 6$ и 16$ получается 26$, а не 22$)  | 1. Запустить игру и начать уровень <br> 2. Выполнить несколько заказов <br> 3. Обратить внимание на итоговую выручку (например, 16$) <br> 4. Выполнить еще один заказ (например, за 6$) <br><br> Ожидаемый результат: Итоговая выручка увеличивается на сумму выполненного заказа ($16 + $6 = $22). <br><br> Фактический результат: Итоговая выручка складывается неправильно ($16 + $6 = $26) | Значительный  | Высокий  | [Выручка считается неправильно](https://drive.google.com/file/d/1bR5ahhxBUj_pdcdWNSJ7V9bBVKdS64s6/view?usp=sharing)  | 
| 2 | Неправильная стоимость заказа, состоящего из более чем 1 продукта  | При выполнении заказа, состоящего из более чем 1 продукта, сумма заказа не соответствует сумме стоимости продуктов (например, у нас есть заказ, состоящий из молока и яиц, они стоят 7$, но при выполнении заказа отображается 17$)  | 1. Запустить игру и начать уровень <br> 2. Выполнить заказ, состоящий из более чем 1 продукта (например, из молока и яиц) <br> 3. Обратить внимание на выручку от этого заказа <br><br> Ожидаемый результат: Игрок получает выручку согласно сумме стоимости отдельных продуктов (7$ + 7$ = 14$) <br><br> Фактический результат: Выручка не соответствует сумме стоимости отдельный продуктов (7$ + 7$ = 17$) | Значительный | Высокий | [Неправильная стоимость большого заказа](https://drive.google.com/file/d/1nM6D88ZSwsOTrVj9phjjtgdjq1QPne4I/view)  |
| 3 | Непрозрачный фон у бустеров  | При открытии новых бустеров у картинки вместо прозрачного фона присутствует белый фон  | 1. Запустить игру и начать уровень <br> 2. Играть пока не откроется новый бустер <br><br> Ожидаемый результат: Изображение бустера отображается с прозрачным фоном, соответствуя фону игры <br><br> Фактический результат: Изображение бустера отображается с белым фоном, нарушая визуальное оформление игры | Незначительный  | Средний | [Непрозрачный фон](https://drive.google.com/file/d/18d_7vlK9SPX84UCOMgRIxZ5yMPF_bKc2/view) |
| 4 | Кнопка продолжить возвращает на главный экран  | При завершении уровня кнопка продолжить возвращает на главный экран  | 1. Запустить игру и начать уровень <br> 2. Завершить уровень <br> 3. Нажать кнопку продолжить <br><br> Ожидаемый результат: Игрок переходит на следующий уровень после нажатия кнопки <br><br> Фактический результат: Игрок возвращается на главный экран вместо перехода к следующему уровню | Значительный | Высокий | [Кнопка продолжить](https://drive.google.com/file/d/1Ic6clXV1oYG_kuVo5LfS8022ROB3IpWf/view)  |
| 5 | Курица не уходит с места снесения яиц | После того как курицы снесли яйца, одна из них остаётся на месте и визуально сливается с лотком яиц, что нарушает визуальное восприятие  | 1. Запустить игру и начать уровень <br> 2. Дождаться пока курицы снесут яйца <br><br> Ожидаемый результат: Одна из куриц покидает место после снесения яиц, лоток с яйцами остаётся свободным для дальнейшего взаимодействия <br><br> Фактический результат: Одна из куриц остаётся на месте и сливается с лотком яиц, визуально перекрывая его | Незначительный  | Средний  | [Курица на месте](https://drive.google.com/file/d/1GX07lXbEXA-i11LWGhXB_8KzUowJyTjq/view?usp=sharing) |
| 6 | Корова доится сама, а курица требует взаимодействия  | Для получения молока коровы доятся сами по себе, а для сбора яиц от куриц необходимо нажимать на них, что создает несогласованность в игровом процессе  | 1. Запустить игру и начать уровень <br> 2. Обратить внимание, что коровы автоматически дают молоко без нажатия <br> 3. Обратить внимание, что для получения яиц необходимо нажимать на куриц <br><br> Ожидаемый результат: Для получения молока нужно подоить корову и запустить таймер молока, в то время как курицы несутся сами  <br><br> Фактический результат: Коровы доятся автоматически, а курицы требуют нажатия для запуска производства яиц | Незначительный | Низкий | [Курицы и коровы](https://drive.google.com/file/d/1xGKhWPEbB5pbfBdti98iFIhigHUuCW1d/view) |
| 7 | Неправильная стоимость продажи молока, хлеба, сыра и яиц  | Стоимость продажи молока, хлеба, сыра и яиц не соответствует указанной цене (например, улучшенное молоко продается за 8, а не 7) | 1. Запустить игру и начать уровень <br> 2. Продать один из продуктов (молоко, хлеб, сыр или яйца) <br><br> Ожидаемый результат: Выручка за проданный товар соответствует стоимости на экране улучшений  <br><br> Фактический результат: Выручка за проданные продукты отличаются от указанной | Значительный  | Высокий  | [Стоимость продуктов](https://drive.google.com/file/d/1FokQ5S07v806LVhkpf7C3G9BdQQED3f5/view) |
| 8 | Наложение музыки друг на друга при приготовлении сыра  | Если отнести молоко на сыроварню, то происходит наложение музыки друг на друга, создавая неприятный шум и дезориентируя игрока | 1. Запустить игру и начать уровень <br> 2. Собрать молоко и отнести на сыроварню <br><br> Ожидаемый результат: Музыкальное сопровождение воспроизводится правильно и без наложений  <br><br> Фактический результат: Музыка накладывается друг на друга, создавая неприятный шум | Незначительный  | Средний  | [Музыка накладывается](https://drive.google.com/file/d/1busfdNQk2FWSgACt1LjjDQoQz_1zjdqD/view?usp=sharing)  |
| 9 | Перестают появляться покупатели после доп. времени  | При покупке дополнительного времени для завершения уровня происходит сбой, в результате которого покупатели больше не появляются  | 1. Запустить игру и начать уровень с ограничением по времени <br> 2. Дождаться окончания таймера <br> 3. Купить бонусное время <br><br> Ожидаемый результат: Покупатели продолжают появляться после покупки дополнительного времени, позволяя игроку завершить уровень <br><br> Фактический результат: После покупки дополнительного времени покупатели не появляются, блокируя выполнение уровня | Критический  | Высокий  | [Исчезновение покупателей](https://drive.google.com/file/d/1MaRAGH-_P37GhPNtvnQ0Esh8eQP1zh7G/view) |
| 10 | При получении ежедневной награды интерфейсы накладываются  | Когда игрок получает ежедневную награду, элементы интерфейса начинают накладываться друг на друга  | 1. Запустить игру <br> 2. Получить ежедневную награду <br><br> Ожидаемый результат: Интерфейс отображается корректно после получения награды <br><br> Фактический результат: Интерфейсы накладываются друг на друга | Незначительный  | Средний  | [Наложние интерфейсов](https://drive.google.com/file/d/1pF0HqJjybJ941PrvSFWzpLEjjnI2LWW_/view) |
| 11 | Вместо иконки яиц белый квадрат  | После прохождения уровня и появления уведомления об открытии куриц и их продуктов вместо иконки яиц отображается белый квадрат  | 1. Запустить игру <br> 2. Пройти 10 уровень <br><br><br> Ожидаемый результат: Иконка яиц отображается и соответствует дизайну  <br><br> Фактический результат: Иконку яиц невидно из-за белого квадрата | Незначительный  | Средний  |  ![Курица и яйцо](https://github.com/user-attachments/assets/1d0a0b91-70f9-4c5f-ab50-6ebaded2c55e) |
| 12 | Иконка хлеба отличается от модели хлеба  | При улучшении хлеба его иконка не соответствует внешнему виду   | 1. Запустить игру <br> 2. Улучшить качество хлеба <br> 3. Начать уровень <br><br> Ожидаемый результат: Иконка и модель хлеба в игре выглядят одинаково <br><br> Фактический результат: Иконка хлеба не соответствует модели | Незначительный | Средний  | ![Хлеб модель](https://github.com/user-attachments/assets/4c300019-df47-404e-83c9-94a0638985c3) <br> ![Хлеб иконка](https://github.com/user-attachments/assets/71d9ea01-6d17-4457-a141-64272249ebc7) |
| 13 | Отсутствие кнопки рестарт  | Кнопка рестарта отсутствует на уровне, что не позволяет игроку перезапустить его  | 1. Запустить игру и начать уровень <br> 2. Поставить игру на паузу <br><br> Ожидаемый результат: Во время паузы присутствует кнопка рестарта уровня <br><br> Фактический результат: Кнопка отсутствует и невозможно перезапустить уровень | Незначительный  | Средний  | ![Нет рестарта](https://github.com/user-attachments/assets/48be4017-34f2-4006-9c33-76e72da09279) |
| 14 | Комбо ни на что не влияет  | При выполнении нескольких заказов подряд накапливается комбо, однако это не приводит к изменениям в игре — отсутствуют бонусы, увеличение наград или любые другие эффекты | 1. Запустить игру и начать уровень <br> 2. Выполнить последовательно несколько заказов за маленький промежуток времени <br><br> Ожидаемый результат: Накопленное комбо дает бонусы или другие положительные эффекты  <br><br> Фактический результат: Комбо накапливается, но не оказывает никакого влияния на игру | Незначительный | Низкий | [Комбо не влияет ни на что](https://drive.google.com/file/d/1uAosHLMu8qFGNhfxZavIvh0pWuUc23ry/view)|
| 15 | Неправильное начисление денег при 2х бустере  | При активированном 2x бонусе начисленная сумма не соответствует описанию бонуса (например, изначальная стоимость молока – 7$, при использовании 2х бустера, молоко должно продаваться за 14$) | 1. Запустить игру <br> 2. Начать уровень с бонусом 2х <br> 3. Выполнить заказ (например, продать молоко) <br><br> Ожидаемый результат: Сумма выручки удваивается при активированном 2x бонусе (молоко должно продаваться за 14$) <br><br> Фактический результат: Начисленная сумма не соответствует удвоенной стоимости (молоко продается за 16$) | Значительный  | Высокий | [Неправильное начисление денег](https://drive.google.com/file/d/1O-tzsUrUGz1oij52oMURXgylrSEVzzQT/view) |
| 16 | Отсутствие звука завершения уровня | Когда игрок завершает уровень, отсутствует звуковое сопровождение, которое должно сигнализировать об успешном выполнении всех заданий  | 1. Запустить игру и начать уровень <br> 2. Завершить уровень <br><br> Ожидаемый результат: По окончанию уровня воспроизводится звук завершения  <br><br> Фактический результат: Звуковое сопровождение завершения уровня отсутствует | Незначительный | Низкий | [Нет звука завершения](https://drive.google.com/file/d/1AJxAiCua3p_yLWAuw8id3RCv7hB6DKtP/view) |
| 17 | Отсутствие повторного провала  | При повторном выполнении условия проигрыша на уровне игра не завершается  | 1. Запустить игру  <br> 2. Начать уровень с условием проигрыша <br> 3. Провалить уровень по условию <br> 4. Купить попытку <br>5. Провалить уровень по условию еще раз <br><br> Ожидаемый результат: Игра корректно завершается с соответствующим уведомлением о провале <br><br> Фактический результат: Уровень остается активным даже при выполнении условий проигрыша | Значительный | Высокий  | [Отсутсвие повторного провала уровня](https://drive.google.com/file/d/10rNsODTsww_lrNe7D24hp56HY2HsU1wg/view?usp=sharing) |
| 18 | Отсутствие настроек во время паузы  | Когда игрок ставит игру на паузу, меню настроек недоступно, что мешает изменять такие параметры, как громкость звука, музыка  | 1. Запустить игру и начать уровень <br> 2. Поставить игру на паузу <br><br>Ожидаемый результат: В режиме паузы доступно меню настроек <br><br> Фактический результат: Меню настроек отсутствует во время паузы | Незначительный  | Средний | ![image](https://github.com/user-attachments/assets/854fa634-1142-4a12-a7ec-f2dce30e1998) |
| 19 | Отсутствие просмотра рекламы  | На экране, где предусмотрена возможность просмотра рекламы для получения бонусов, реклама не отображается  | 1. Запустить игру <br> 2. Открыть меню с магазином <br> 3. Выбрать получение награды за просмотр рекламы <br><br> Ожидаемый результат: Реклама загружается и доступна для просмотра, а также выдается награда <br><br> Фактический результат: Реклама не отображается, но награда зачисляется | Незначительный  | Низкий  | [Отсутствие рекламы](https://drive.google.com/file/d/1TryxpcGDdjX3WsNOi7tK4J8KtQ_i2xfg/view) |
| 20 | Отсутствие системы оплаты  | Игровая валюта начисляется игроку при попытке покупки за реальные деньги, хотя система оплаты не реализована  | 1. Запустить игру <br> 2. Открыть магазин <br> 3. Попытаться купить внутриигровую валюту <br><br> Ожидаемый результат: Игровая валюта или товар начисляется только после успешного завершения оплаты <br><br>Фактический результат: Игровая валюта или товар начисляется сразу, даже без завершения оплаты | Значительный  | Высокий  | [Отсутствие системы оплаты](https://drive.google.com/file/d/140rcG0v1LRppVNU2A8hhKsxdFWg30XI3/view?usp=sharing) |
| 21 | Подсказка появляется после завершения уровня, а не при приближении к его завершению  | Подсказка появляется только после полного завершения уровня, когда её информация уже не актуальна  | 1. Запустить игру  <br> 2. Начать уровень с условием без потери покупателей <br> 3. Потерять покупателя <br><br> Ожидаемый результат: Подсказка появляется при приближении к проигрышу <br><br> Фактический результат: Подсказка отображается после проигрыша | Незначительный  | Средний | [Подсказка](https://drive.google.com/file/d/16o8A5Q6vlvzTgm9_2s3aOkoJUQ1sbDeg/view?usp=sharing) |
| 22 | Запросы покупателей не меняются обратно после бонуса хлопушки | По окончании действия хлопушки запросы покупателей не возвращаются в обратное состояние  | 1. Запустить игру и начать уровень <br> 2. Использовать бонус «Хлопушка» <br><br> Ожидаемый результат: По окончании действия бонуса иконки запросов покупателей снова отображают конкретные товары <br><br> Фактический результат: Иконки остаются в виде подарков, что не соответствует актуальным запросам покупателей | Значительный  | Средний  | [Запросы покупателей](https://drive.google.com/file/d/16cYTP-X5umRDjfre4vyd5k5ShwLK2YNP/view?usp=sharing) |
| 23 | Уведомление при 0 жизней располагается за интерфейсом  | Когда у игрока 0 жизней уведомление о невозможности начать уровень отображается позади интерфейса уровня при попытке начать уровень  | 1. Запустить игру <br> 2. Начать уровень при 0 жизней <br><br> Ожидаемый результат: При попытке начать уровень с 0 жизней игроку показывается корректное уведомление о нехватке жизней <br><br> Фактический результат: Уведомление о нехватке жизней отображается позади интерфейса уровня | Незначительный  | Средний  |[Уведомление при 0 жизней](https://drive.google.com/file/d/1U3Dbrg5lqFrnug9uy5Dmjd7MtCj7Sgz6/view) |
| 24 | Эмоции покупателей не меняются на нейтральные после бонуса  | После использования бонуса «Карамельное яблоко» на злом покупателе его эмоция не меняется обратно на спокойную  |  1. Запустить игру и начать уровень  <br> 2. Дождаться пока разозлится покупатель <br> 3. Использовать бонус «Карамельное яблоко»  <br> <br> Ожидаемый результат: Эмоция покупателя меняется на спокойную  <br> <br> Фактический результат: Покупатель остается с недовольным лицом  | Незначительный  | Незначительный  | [Эмоции покупателей](https://drive.google.com/file/d/106fbMIwq5x6BhXzP1lcjjOh20tlpsbXH/view?usp=sharing) |
| 25 | Молоко увеличивается в размерах   | После нажатий на пустую сыроварню молоко начинает увеличиваться в размерах  | 1. Запустить игру и начать уровень <br> 2. Нажать несколько раз на пустую сыроварню <br><br> Ожидаемый результат: Молоко начинает мигать в качестве подсказки, не изменяя своего размера <br><br>Фактический результат: С каждым нажатием молоко становится все  | Незначительный  | Средний  | [Большое молоко](https://drive.google.com/file/d/1g4KvO1POFzPLchBiO5chhmKT3ThpHwfh/view?usp=sharing) |
| 26 | Уровень не может быть завершён после активации дополнительной попытки  | На уровне с условием потери покупателей, при покупке дополнительной попытки, уровень не завершается, даже когда все покупатели уже ушли  | 1. Запустить игру <br> 2. Начать уровень с условием без потери покупателей <br> 3. Потерять покупателя <br> 4. Купить дополнительную попытку <br><br>Ожидаемый результат: Уровень продолжается до тех пор, пока не закончатся покупатели <br><br> Фактический результат: Уровень продолжается даже после того, как закончились все покупатели | Критический  | Высокий  | [Уровень не завершается](https://drive.google.com/file/d/1ySU_opNq-8D1J7hfbjXjT0JTiYm9SnqH/view?usp=sharing) |
| 27 | При получении ежедневного бонуса продолжительность бесконечной жизни уменьшается  | Когда игрок открывает ежедневный бонус, который предполагает увеличение количества жизней, вместо добавления жизней их количество уменьшается  | 1. Запустить игру <br> 2. Забрать ежедневный бонус с прибавлением жизней <br><br> Ожидаемый результат: Жизни прибавляются в соответствии с бонусом <br><br> Фактический результат: Жизни уменьшаются вместо того, чтобы увеличиваться | Значительный  | Высокий  | [Жизни уменьшаются](https://drive.google.com/file/d/1mqnF9ZCrA91tqtKBQb77hnErcYz1aEml/view) |
| 28 | Модель молока не соответствует иконке | При улучшении молока, его текущая модель не изменяется, в отличие от иконки | 1. Запустить игру <br> 2. Улучшить молоко <br> 3. Начать уровень <br><br> Ожидаемый результат: Иконка и модель молока в игре выглядят одинаково <br><br> Фактический результат: Модель молока отличается от иконки | Незначительный  | Средний | ![image](https://github.com/user-attachments/assets/78ffa857-163f-4dde-b6a7-8f77a5f8bf23) |
| 29 | Количество галочек на объекте не соответствует возможному взаимодействию с объектом  | При нескольких нажатиях на объект на нём может появиться до 4 галочек, даже если количество доступных объектов (продуктов) меньше, что приводит к наложению звуков  | 1. Запустить игру и начать уровень <br> 2. Многократно выбрать объект, который можно отметить действием <br><br>Ожидаемый результат: Количество галочек на объекте соответствует количеству доступных объектов (продуктов), звуки не накладываются друг на друга  <br><br> Фактический результат: На объекте появляются до 4 галочек независимо от количества доступных объектов (продуктов), происходит наложение звуков | Незначительный  | Средний  | [Много галочек](https://drive.google.com/file/d/1OyBWbc2KG_SUupH_O8cUllXf9jMcLOLO/view) |
| 30 | Шкала уровня заполняется не полностью  | При прохождении уровня на шкале он заполняется на половину, а не полностью  | 1. Запустить игру и начать уровень <br> 2. Успешно завершить уровень <br><br> Ожидаемый результат: Шкала уровней заполнится до следующего уровня <br><br>Фактический результат: Шкала уровней заполняется лишь наполовину | Незначительный  | Низкий  | ![image](https://github.com/user-attachments/assets/e4711ab7-9157-4e8a-b21c-af7d7ddd8fda) |
| 31 | Шкала выполнения целей уровня заполняется быстрее анимации  | При выполнении заказа покупателя шкала целей уровня заполняется быстрее, чем анимация зачисления денег  | 1. Запустить уровень и начать игру <br> 2. Выполнить любой заказ <br><br> Ожидаемый результат: Шкала целей заполняется после того, как анимация достигнет ее. <br><br> Фактический результат: Шкала целей заполняется сразу после выполнения заказа, не дожидаясь анимации | Незначительный  | Низкий  | [Шкала заполняется быстрее анимации](https://drive.google.com/file/d/16s8IKEjz3rSB7fttVaL0vTefsOwg_u6J/view?usp=sharing)|
## Краткий анализ
![image](https://github.com/user-attachments/assets/6fcf9749-ced7-4be7-81f2-ab604f8c0f19) <br>
Наличие критических багов представляет собой наибольшую угрозу для игрового процесса, так как такие ошибки могут приводить к серьезным сбоям или даже к невозможности продолжить игру. Исправление этих 2 критических багов должно стать первоочередной задачей.
