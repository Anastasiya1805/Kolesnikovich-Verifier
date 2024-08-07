### Kolesnikovich-Verifier
# Описание процесса загрузки кода из репозитория для использования коллекции у вас в Postman.

### Шаг 1: Клонирование репозитория GitHub.

- Скопируйте URL нужного вам репозитория;
- Клонируйте его себе на локальный компьютер(через Visual Code,например,или через терминал используя команду git.clone) либо загрузите ZIP файл

### Шаг 2: Импорт коллекции в Postman
- Откройте Postman.
- Нажмите на кнопку Import в верхнем левом углу.
- В открывшемся окне выберите вкладку Upload Files.
- Найдите и выберите файл коллекции (обычно с расширением .json), который вы клонировали из репозитория.
- Нажмите Open для загрузки файла.
- Нажмите Import, чтобы импортировать коллекцию в Postman.

# Использование переменнных в проекте Verifier
**Переменные могут быть глобальные, переменные окружения,переменные коллекции и локальные переменные.
В проекте Verifier используются 3 вида переменных - это глобальные переменные, пременные окружения и переменные коллекции.**
*Глобальные переменные полезны для хранения значений, которые используются во всех коллекциях и окружениях. Эти переменные доступны везде.В проекте Verifier используется следущая глобальная перменная*:
- Нам необходим один и тот же URL {{url}} для проекта,который будет использоваться в нескольких коллекциях,поэтому удобно хранить его в глобальных переменных. Это позволит вам легко обновлять URL, если он изменится.

*Переменные окружения используются для значений, которые зависят от конкретного окружения.*
-У каждого окружения могут быть свои учетные данные и другие настройки.У нас на одном окружении несколько коллекций, поэтому такие параметры,как usernameVerifierAdmin, passwordVerifierAdmin добавлены в переменные окружения для использования этих данных в коллекциях.

*Переменные коллекции используются для значений, которые специфичны для конкретной коллекции*
- В переменную коллекции добавлен token {{token}}.Вообще токен можно добавть и в переменную окружения.Но удобно работать с одной коллекцией и не искать токен по остальным,а в нужной коллекции его запросить.
- Также в переменную коллекции доббаслена Id задания {{id}}.Id задания передается внутри коллекции в следущие запросы.
