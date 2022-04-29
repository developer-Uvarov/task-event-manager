# Create empty project and install json-server
https://github.com/typicode/json-server
# 1. add app.js:
```
const jsonServer = require('json-server')
const server = jsonServer.create()
const router = jsonServer.router('db.json')
const middlewares = jsonServer.defaults()

server.use(middlewares)
server.use(router)
server.listen(3000, () => {
    console.log('JSON Server is running')
})
```
# 2. Create db.json file with the following structure:
```
{
  "employees": [
    {
      "id": 1,
      "fls": "Morokhin Sergey Aleksandrovich",
      "photo": "D:/web/json-server.png",
      "login": "SMorokhin"
    },
    {
      "id": 2,
      "fls": "Surakov Andrey Valeryevich",
      "photo": "D:/web/json-server.png",
      "login": "SAndrey"
    },
    {
      "id": 3,
      "fls": "Perebatov Mihail Sergeevich",
      "photo": "D:/web/json-server.png",
      "login": "PMihail"
    }
  ],
  "event-categories": [
    {
      "id": 1,
      "name": "eventSuccess",
      "color": "#3B82F6"
    },
    {
      "id": 2,
      "name": "eventWarning",
      "color": "#FBBF24"
    },
    {
      "id": 3,
      "name": "eventError",
      "color": "#EC4899"
    }
  ],
  "events": [
    {
      "id": 1,
      "name": "Monthly catch-up PRIMARY",
      "description": "Lorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!",
      "begDate": "2021-07-25 09:30",
      "endDate": "2021-07-25 10:00",
      "participant": "SMorokhin",
      "eventTypeId": 3,
      "repeat": true
    },
    {
      "id": 2,
      "name": "Monthly catch-up in ZOOM",
      "description": "You submitted on your Letter of Authorization (LOA) is different from what is on file with your carrier in their Customer Service Record (CSR). A CSR is a copy of how your telephone records appear in the telephone company’s database. Zoom link: https://zoom.com/room?id=1313123213123",
      "begDate": "2021-11-02 14:45",
      "endDate": "2021-11-02 16:00",
      "participant": "SMorokhin",
      "eventTypeId": 1,
      "repeat": true
    },
    {
      "id": 3,
      "name": "Monthly catch-up",
      "description": "You submitted on your Letter of Authorization (LOA) is different from what is on file with your carrier in their Customer Service Record (CSR). A CSR is a copy of how your telephone records appear in the telephone company’s database.",
      "begDate": "2021-11-02 08:30",
      "endDate": "2021-11-02 09:00",
      "participant": "SMorokhin",
      "eventTypeId": 3,
      "repeat": false
    },
    {
      "name": "Новое событие",
      "description": "Ошибочное событие",
      "begDate": "2021-11-03 09:24",
      "endDate": "2021-11-03 09:24",
      "participant": "Perebatov Mihail Sergeevich",
      "eventTypeId": 3,
      "repeat": false,
      "id": 5
    },
    {
      "name": "lkasndlknadlndsnaldsa",
      "description": "некоторое описание для проверки",
      "begDate": "2021-12-07 10:23",
      "endDate": "2021-12-07 10:23",
      "participant": "Morokhin Sergey Aleksandrovich",
      "eventTypeId": 3,
      "repeat": false,
      "id": 6
    },
    {
      "name": "New event",
      "description": "asdsadasdsadasdasdasdasd\n",
      "begDate": "2021-12-26 19:00",
      "endDate": "2021-12-26 19:00",
      "participant": "Surakov Andrey Valeryevich",
      "eventTypeId": 2,
      "repeat": false,
      "id": 8
    },
    {
      "name": "Long event",
      "description": "Lorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequu\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nLorem ipsum dolor <br>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem cupiditate eos fuga, laborum nobis numquam! Aut cumque earum incidunt, natus, odit officia quas quisquam soluta, totam ullam unde voluptas voluptatum? Dolorum quidem rerum voluptatibus. Consequuntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!\nntur doloribus magni quae quas quidem, sit voluptatem. Esse ipsum modi nam quas quidem repellendus! Ipsam!",
      "begDate": "2021-12-28 11:32",
      "endDate": "2021-12-28 11:32",
      "participant": "Perebatov Mihail Sergeevich",
      "eventTypeId": 2,
      "repeat": false,
      "id": 9
    },
    {
      "name": "Some new event",
      "description": "Event for warning withous participants\n",
      "begDate": "2021-12-01 07:00",
      "endDate": "2021-12-01 07:00",
      "participant": "",
      "eventTypeId": 2,
      "repeat": false,
      "id": 10
    },
    {
      "name": "One more event for test scroll-bar",
      "description": "Success event for test scroll-bar.",
      "begDate": "2021-12-01 07:00",
      "endDate": "2021-12-01 07:00",
      "participant": "Surakov Andrey Valeryevich",
      "eventTypeId": 1,
      "repeat": false,
      "id": 11
    },
    {
      "name": "28.12 Test time",
      "description": "Some desc.",
      "begDate": "2021-12-28 10:32",
      "endDate": "2021-12-28 10:32",
      "participant": "",
      "eventTypeId": 2,
      "repeat": false,
      "id": 12
    },
    {
      "name": "New event",
      "description": "New test event. Some description.",
      "begDate": "2021-12-30 14:25",
      "endDate": "2021-12-30 14:35",
      "participant": "Surakov Andrey Valeryevich, Perebatov Mihail Sergeevich",
      "eventTypeId": 1,
      "repeat": false,
      "id": 14
    },
    {
      "name": "123",
      "description": "123",
      "begDate": "2021-12-31 04:25",
      "endDate": "2021-12-31 04:25",
      "participant": "",
      "eventTypeId": 2,
      "repeat": false,
      "id": 15
    },
    {
      "name": "444444",
      "description": "4444444",
      "begDate": "2022-01-01 13:30",
      "endDate": "2022-01-01 14:00",
      "participant": "Morokhin Sergey Aleksandrovich, Surakov Andrey Valeryevich",
      "eventTypeId": 3,
      "repeat": true,
      "id": 16
    },
    {
      "name": "Новое событие",
      "description": "Описание. Описание. Описание. Описание. Описание. Описание. Описание. Описание. Описание. Описание. Описание. Описание. Описание. Описание. Описание.",
      "begDate": "2022-01-18 06:30",
      "endDate": "2022-01-18 06:46",
      "participant": "Morokhin Sergey Aleksandrovich",
      "eventTypeId": 1,
      "repeat": false,
      "id": 17
    }
  ]
}

```

# Install

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
