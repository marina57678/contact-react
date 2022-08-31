# Website React Contacts

## Installation

To get the project up and running, and view components in the browser, complete the following steps:

1. Download and install Node
2. Download and install Yarn
3. Clone this repo
4. Install project dependencies: `yarn install`

## Development

Start development

* `yarn dev`

## Production

Build production

* `yarn build`

## Other

### VS Code config

```json
{
  // Format a file on save. A formatter must be available, the file must not be auto-saved, and editor must not be shutting down.
  "editor.formatOnSave": false,
  // Enable/disable default JavaScript formatter (For Prettier)
  "javascript.format.enable": true,
  // Use 'prettier-eslint' instead of 'prettier'. Other settings will only be fallbacks in case they could not be inferred from eslint rules.
  "prettier.eslintIntegration": true,
  "eslint.alwaysShowStatus": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "typescript.preferences.importModuleSpecifier": "non-relative"
}
```

## Stack

- Typescript
- React
- Redux-toolkit
- MUI

## Contacts

1. Данные доступны с сервера [https://randomuser.me/api/?results=200](https://randomuser.me/api/?results=100)

Отображение данных в виде таблицы.
Колонки ряда таблицы:

- Avatar
- Fullname
- Birthday (формат - День недели, mm/dd/yyyy, hh:mm am, кол-во лет)
- Email (должен быть кликабельным с возможностью скопировать)
- Phone (должен быть кликабельным с возможностью скопировать)
- Location (Страна, Город)
- Национальность

2. Должна быть возможность переключения режима просмотра данных:

- табличный вид
- плиточный вид

Выбранное значение должно запоминаться в localStorage и в состоянии приложения.
При обновление страницы илперемонтировании компонента, данные должны
отобразиться в том виде, который выбрал пользователь. Если страница посещается
впервые, то использовать по-умолчанию табличный вид

3. Должна быть возможность фильтровать данные:

- по полному имени;
- по половому признаку;
- по национальности;

Фильтрация должна происходить без ручной отправки формы.

Очистка фильтра возвращает коллекцию к изначальному состоянию.

Фильтровать нужно всю коллекцию, а не только ту часть которая сейчас в таблице
отображается.

4. Вывести пагинацию

- по 10 пользователей на странице
- кол-во страниц зависит от кол-во учитывая фильтр

5. Должна быть возможность сортировать данные по полному имени в трех состояниях:

- отAдоZ
- отZдоA
- изначальный порядок

Сортировать нужно всю коллекцию, а не только ту часть которая сейчас в таблице
отображается

6. Под таблицей необходимо вывести статистику по данным

- размер коллекции
- кол-во мужчин, женщин и неопределившихся
- вывести кого больше
- кол-во контактов по каждой национальности

7. Должна быть возможность обновить данные по клику на кнопку без перезагрузки
страницы

![Task](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F4ef98477-1a45-4014-9abc-510f2c2530e0%2Fscreencapture-inkubator-ks-ua-testing-react-redux-contacts-2020-11-01-10_22_45.png?table=block&id=e25686ce-d609-40d2-bee2-f45d9ba251e6&spaceId=43c7e9f0-3dec-48f3-911f-eac4227e27bb&width=2000&userId=&cache=v2)
