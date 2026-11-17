
<div align="center">

# TG-bots-dev

**Объединяющий репозиторий для моих проектов Telegram-ботов, созданных во время изучения Python, асинхронных операций и SQL.**

[![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![aiogram](https://img.shields.io/badge/aiogram-3.x-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://docs.aiogram.dev/)
[![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![python-dotenv](https://img.shields.io/badge/python--dotenv-4B8BBE?style=for-the-badge&logo=python&logoColor=white)](https://pypi.org/project/python-dotenv/)

</div>

---

Каждый бот находится в собственном репозитории и подключается сюда в виде **подмодуля Git**.
Этот репозиторий представляет собой единую точку входа: одна команда `clone` позволит вам получить оба проекта, и
Родительский репозиторий фиксирует точный коммит каждого из них.

Это учебные проекты, а не готовые продукты. Они размещены в открытом доступе.
> Цель — задокументировать мой путь от "привет, мир" до работы с ботами.
> обработчики, конечный автомат, база данных и панель администратора.

## Что внутри

| Бот | Что он делает | Стек | Статус |
| :-- | :-- | :-- | :-- |
| [**Быстрый модуль регистрации пользователей**](https://github.com/WhyCrisis/Simple-start-menu-for-TG-bots) | Telegram-бот с пользовательским кабинетом: регистрация, выбор языка, условия использования, панель администратора | Python · aiogram 3 · aiosqlite (SQLite) · FSM | Архивированно |
| [**Tg-Bot-to-MTG-Mods-With-Scripts**](https://github.com/WhyCrisis/Tg-Bot-to-MTG-Mods-With-Script) | Бот, который предоставляет скрипты автоматизации и конфигурации в виде читаемой библиотеки файлов, а не в виде множества ссылок | Python · aiogram · python-dotenv | MVP, архивировано |

## Структура репозитория

```текст
TG-bots-dev/
├── Simple-start-menu-for-TG-bots/субмодуль → WhyCrisis/Simple-start-menu-for-TG-bots
│ └── src/
│ ├── Начало/ # адаптация, FSM, выбор языка
│ ├── Меню/ # главное меню
│ ├── Администратор/ # панель администратора
│ └── SQL/ # слой aiosqlite
├── Tg-Bot-to-MTG-Mods-With-Scripts/ # submodule → WhyCrisis/Tg-Bot-to-MTG-Mods-With-Scripts
│ ├── composite/ # клавиатуры, текст, общие кнопки
│ └── libs_router/ # раздел routers
└── .gitmodules
```

## Начало работы

Обычная команда `git clone` создаст две **пустые** папки — так работают подмодули.

```bash
git clone --recurse-submodules https://github.com/WhyCrisis/TG-bots-dev.git
cd TG-bots-dev
```

Уже клонировано без флага?

```bash
git submodule update --init --recursive
```

Загрузите последние изменения от обоих ботов:

```bash
git pull --recurse-submodules
```

Что туда помещается:

| Переменная | Значение |
| :-- | :-- |
| `BOT_TOKEN` | токен от [@BotFather](https://t.me/BotFather) |
| `admin` | ваш идентификатор пользователя Telegram — предоставляет доступ к панели администратора |
| `POSTGRES_*` | учетные данные базы данных (`HOST`, `PORT`, `USER`, `PASSWORD`, `DB`) |


Для работы `aiogram 3.x` требуется **Python 3.11+**.


[![Telegram](https://img.shields.io/badge/Telegram-@bartelliada-2CA5E0?style=flat-square&logo=telegram&logoColor=white)](https://t.me/bartelliada)
[![Email](https://img.shields.io/badge/Email-atomicsweetnes@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:atomicsweetnes@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-WhyCrisis-121011?style=flat-square&logo=github&logoColor=white)](https://github.com/WhyCrisis)
