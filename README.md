# Hard Notes

Генератор статического сайта для ведения базы знаний, написанный на Bash с использованием [`pandoc`](https://pandoc.org/).

## Структура

```text
.
├── hard-notes                              <--- Сгенерированный сайт
│   ├── notes/
│   ├── questions/
│   ├── tasks/
│   ├── index.html
│   └── pygments.css
├── src                                     <--- Исходники с Markdown-файлами
│   ├── notes/
│   ├── questions/
│   └── tasks/
├── web                                     <--- Шаблоны, статика
│   ├── index.template.html
│   ├── notes.template.html
│   ├── pygments.css
│   ├── questions.template.html
│   └── tasks.template.html
└── notes                                   <--- Скрипт-менеджер
```

## Использование

### Добавление заметки, задачи, вопроса

```shell
$ ./notes new note enumerate
$ ./notes new question Порядок init, new и call
$ ./notes new task Сумма от 1 до N
```

Создаст шаблон для Markdown-файла в соответствующей директории в `src/`.

### Сборка

```shell
$ ./notes build
```

Генерирует `html`-страницы из Markdown-файлов и шаблонов.

#### Очистка:

```shell
$ ./notes clean
```

### Запуск

```shell
$ ./notes run
$ ./notes run 8000
```

Запускает локальный сервер с помощью python3-модуля `http.server`. По умолчанию используется адрес `0.0.0.0:4000`
