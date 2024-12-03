# Портфолио
Здесь собраны примеры тестовой документации, выполненные во время тестирования ранних сборок проектов "Farming Fever", "Differences"
- [Баг-репорты](#bug-reports)
- [Чек-листы](#checklist)
# <a name="bug-reports"/> Баг-репорты

| ID | Краткое описание (Summary) | Подробное описание (Description) | Шаги и результат (Steps&Result) | Критичность (Severity) | Приоритет (Priority) | Вложения (attachment) |
| ------------- | ------------- | ------------------ | ------ | ------ | ------ | ------ |
| 1  | Игра не заканчивается при окончании таймера | После запуска игры таймер идет, но по его истечению игра не завершается, и проигрыш не засчитывается | 1. Запустить игру и начать уровень <br> 2. Дождаться пока таймер достигнет нуля <br><br> Ожидаемый результат: Игра заканчивается поражением игрока <br><br> Фактический результат: Игра не заканчивается и поражение не засчитывается  | Критический | Высокий  | [Незавершенность игры](https://drive.google.com/file/d/1XtNSI87JXX8FbqHI6HnSae-LTsPk1kVa/view?usp=sharing)  | 
| 2 | Бесконечная загрузка уровня  | При первом запуске игры без подключения к интернету игра застревает на бесконечной загрузке и не переходит к главному экрану. Если же игру сначала запустить с интернетом, а затем отключить его во время игры, через некоторое время снова возникает бесконечная загрузка  | 1. Отключить интернет <br> 2. Запустить игру впервые <br><br> Ожидаемый результат: Игра загружается корректно, и пользователь может войти в офлайн-режим <br><br> Фактический результат: Возникает бесконечная загрузка. <br><br> 3. Подключить интернет <br> 4. Запустить игру снова <br> 5. Отключить интернет во время активного игрового процесса <br> 6. Продолжить играть <br><br> Ожидаемый результат: Игра продолжает работать в офлайн-режиме <br><br> Фактический результат: Игра застревает на бесконечной загрузке после некоторого времени работы без интернета"  | Критический  |  Высокий | [Бесконечная загрузка](https://drive.google.com/file/d/1PpCJ8WEZSYNEF6i06eSZIhkVo9sTB6bp/view?usp=sharing)  | 
| 3 | Завершение уровня без нахождения всех отличий  | Уровень завершается победой игрока, когда он находит только 4 из 5 отличий  | 1. Запустить игру и начать уровень <br> 2. Найти 4 из 5 отличий между двумя картинками <br><br>Ожидаемый результат: Игра продолжается пока не найдены все отличия <br><br> Фактический результат: Игра завершает уровень и позволяет игроку перейти к следующему  | Значительный  | Средний | [Найденные отличия](https://drive.google.com/file/d/1Q7J1yDI7mo0Hj-BY5mrRlDJ0DZwki2xl/view?usp=sharing)  | 
| 4 | Кнопка "продолжить" не переводит на следующий уровень  | После завершения уровня кнопка "Продолжить" не переносит игрока на следующий уровень  | 1. Запустить игру <br> 2. Пройти любой уровень <br> 3. Нажать на кнопку "Продолжить" <br><br> Ожидаемый результат: Игрок переходит на следующий уровень <br><br> Фактический результат: Ничего не происходит, игрок остается на текущем экране завершенного уровня | Значительный | Средний  | [Не работает кнопка продолжить](https://drive.google.com/file/d/1NXTwHZxpC-adlln3JTizRddMNSSU9l0H/view?usp=sharing) | 
| 5 | Отключение вибрации приводит к отключению музыки и наоборот  | В меню настроек, когда игрок отключает вибрацию, неожиданно выключается музыка, а при отключении музыки отключается вибрация | 1. Запустить игру <br> 2. Зайти в меню настроек <br> 3. Выключить вибрацию <br><br> Ожидаемый результат: Вибрация отключается <br><br> Фактический результат: Отключается музыка <br><br> 4. Отключить музыку. <br><br> Ожидаемый результат: Отключается музыка <br><br> Фактический результат: Вибрация отключается | Значительный  | Средний  | [Настройки музыки](https://drive.google.com/file/d/1EIZ1cx4VqO5hhHEBfk2YeKZPyRYaa39C/view?usp=sharing) | 
| 6 | Обводка отличия у другого объекта  | При нахождении отличия обводка иногда отображается смещенной и выделяет неправильный объект вместо того, который действительно отличается  | 1. Запустить игру и начать уровень <br> 2. Найти объект, который отличается на двух изображениях <br> 3. Нажать на этот объект для выделения <br><br> Ожидаемый результат: Обводка точно выделяет объект, который отличается между изображениями <br><br> Фактический результат: Обводка смещена и выделяет неправильный объект | Значительный  | Средний  | [Обводка объекта](https://drive.google.com/file/d/1CT-V4tlgo_zN-B6xHUyVsGqzDTsEWjrj/view?usp=sharing) | 
| 7 | Неправильное отображение найденных отличий  | При нахождении отличия шкала заполняется не с первого элемента. При быстром последовательном нажатии на отличия значения шкалы смещаются вправо, пропуская предыдущие позиции | 1. Запустить игру и начать уровень <br> 2. Найти отличие <br><br> Ожидаемый результат: Отметка о найденном отличии появляется на первой позиции <br><br> Фактический результат: Отметка заполняется со второй позиции <br> 3. Быстро и последовательно найти отличия. <br><br> Ожидаемый результат: Отметка о найденном отличии появляется на соответствующей позиции <br><br> Фактический результат: Отметка смещается вправо, оставляя пропуски на предыдущих позициях | Незначительный  | Низкий  | [Отметки](https://drive.google.com/file/d/1fwjWuc4PEpVwQ8dBZKsAI2g1gxqxTSFa/view?usp=sharing) | 
| 8 | Музыка заканчивается до окончания уровня  | Музыкальный трек, сопровождающий уровень, останавливается, не дойдя до окончания уровня  | 1. Запустить игру и начать уровень <br> 2. Дождаться завершения музыкального трека, не завершая уровень <br><br> Ожидаемый результат: Музыка не останавливается до завершения уровня <br><br> Фактический результат: Музыка завершается раньше уровня  | Незначительный  | Низкий | [Музыкальное сопровождение](https://drive.google.com/file/d/1IJSl99LOsIngPsJxVtX7_AlmgWZAUb8S/view?usp=sharing)  | 
| 9 | Цифры накладываются на таймер  | При быстром нажатии на неправильные отличия цифры таймера накладываются друг на друга  | 1. Запустить игру и начать уровень <br> 2. Быстро и многократно нажимать на неправильные отличия <br><br> Ожидаемый результат: Таймер корректно отображает оставшееся время, независимо от частого снижения <br><br> Фактический результат: Цифры на таймере накладываются друг на друга, что делает время нечитабельным | Незначительный | Низкий | [Таймер](https://drive.google.com/file/d/1X9xxv2fVBPyugL7OV5QMEnd495Is8J_y/view?usp=sharing) | 
| 10 | Промах появляется за границами изображения  | При одновременном нажатии на две картинки метка промахаотображается за границами изображений  | 1. Запустить игру и начать уровень <br> 2. Одновременно нажать на две картинки <br><br> Ожидаемый результат: Метки промаха появляются внутри изображений <br><br> Фактический результат: Метки промаха появляются также за пределами изображений  | Незначительный  | Низкий | [Метки за границей](https://drive.google.com/file/d/1TQhOxdvWsUZUo-wKzBCfmn7Xq2ZEtPWp/view?usp=sharing)  | 
| 11 | Звук предупреждения о завершении уровня не заканчивается  |  Если время истекло, и игрок выходит в меню, а затем возвращается на уровень, звуковое предупреждение продолжает играть  | 1. Запустить игру и начать уровень <br> 2. Подождать окончания таймера <br> 3. Выйти в меню и начать уровень заново <br><br> Ожидаемый результат: При повторном входе в меню и на уровень таймер и звук предупреждения сбрасываются, и звук начинает играть только по окончании нового таймера <br><br> Фактический результат: Звук предупреждения продолжает играть в меню и сразу при входе на уровень | Незначительный  | Низкий  | [Не заканчивающийся звук](https://drive.google.com/file/d/1UdpXEGjiImdFJ6w1PEiTwq-nrziK0pMN/view?usp=sharing)  | 
| 12 | Игра ломается при использовании подсказки за рекламу после нахождения всех 5 отличий  | Если игрок находит все 5 отличий и затем пытается воспользоваться подсказкой, которая требует просмотра рекламы, игра перестает функционировать должным образом  | 1. Запустить игру и начать уровень <br> 2. Найти все отличия <br> 3. Воспользоваться подсказкой на рекламу <br><br> Ожидаемый результат: Игра предлагает просмотреть рекламу, а затем корректно обрабатывает действие, позволяя игроку перейти на следующий уровень <br><br> Фактический результат: Игра ломается, не позволяя завершить текущий уровень  | Критический  | Высокий | [Подсказка и 5 отличий](https://drive.google.com/file/d/1aXvVn6cTRBaXrdKQ_MdTclut3xPRKB8u/view?usp=sharing)  | 
| 13 | Нельзя воспользоваться кнопкной "Восстановить"  | В меню настроек кнопка "Восстановить", предназначенная для восстановления предыдущих настроек или покупок, не реагирует на нажатия  | 1. Запустить игру <br> 2. Зайти в меню настроек <br> 3. Нажать на "Восстановление" <br><br> Ожидаемый результат: Кнопка ""Восстановить"" активируется и выполняет свой функционал <br><br> Фактический результат: Кнопка "Восстановить" не нажимается и не выполняет никаких действий  | Content Cell  | Content Cell  | Content Cell  | 
| 14 | Вылет игры  | Во время игры приложение иногда вылетает, показывая сообщение об ошибке. Это может происходить в произвольные моменты  | 1. Запустить игру и начать уровень <br> 2. Продолжать играть, пока не произойдет вылет <br><br> Ожидаемый результат: Игра продолжает функционировать <br><br> Фактический результат: Игра вылетает с ошибкой, и пользователь возвращается на рабочий стол  | Критический  | Высокий  | [Вылет](https://drive.google.com/file/d/191UtLzo9QI2q6BPE1-Dhhywhjl3CVRFD/view?usp=sharing)  | 
| 15 | Опечатка в слове уровень  | При запуске уровня выше таймера отображается надпись "Уроень"  | 1. Запустить игру и начать уровень <br> 2. Обратить внимание на слово "уровень" <br><br>Ожидаемый результат: Слово написано правильно <br><br> Фактический результат: В слове присутствует опечатка | Тривиальный  | Низкий  | [Опечатка](https://drive.google.com/file/d/1HuAk_ylIIs9D8LjGSFjv3aG8acuinaTn/view?usp=sharing)  | 
| 16 | Отсутствие обучения  | При первом запуске игры для нового игрока инструкция для новичков может не отображаться, хотя должна запускаться автоматически | Предусловие: Игра запущена впервые или с полностью очищенными данными <br> 1. Запустить игру и начать уровень <br><br> Ожидаемый результат: Инструкция для новичков отображается автоматически и пошагово вводит игрока в процесс игры <br><br> Фактический результат: Обучение не появляется  | Значительный | Высокий  | [Отсутствие обучения](https://drive.google.com/file/d/1OEF9BVMPAMD-SyBPs8xiPl5VDG_zeAkh/view?usp=sharing)  | 
# <a name="checklist"/> Чек-листы
| ID  | Название (Title) | Шаги (Steps) | Ожидаемый результат | Статус (Status) |
| ------------- | ------------- | --- | --- | --- | 
| 1  | Запуск уровня | 1. Запустить игру <br> 2. Нажать кнопку запуска уровня | Открывается соответствующий уровень. На экране отображаются все необходимые элементы уровня, такие как таймер, изображения для поиска отличий и интерфейс управления | Пройден |
| 2 | Условие победы  | 1. Запустить игру <br> 2. Начать уровень <br> 3. Найти 5 отличий <br> 4. Убедиться, что таймер еще не закончился| После нахождения всех отличий игра отображает экран пройденного уровня  | Пройден  |
| 3 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 4 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 5 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 6 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 7 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 8 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 9 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 10 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 11 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 12 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 13 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 14 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 15 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 16 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 17 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
| 18 | Content Cell  | Content Cell  | Content Cell  | Content Cell  |
