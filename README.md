# tools-packages

## Prettier

```bash
# Установим prettier пакет в проект
npm install --save-dev prettier
```

Чтобы форматтер начал отрабатывать при сохранении файла в VSCode, не забудьте добавить данную настройку в настройки редактора:

```json
{
    "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

Создаем `.prettierignore` файл, чтобы не форматировать не нужные папки и файлы. Пока что игнорим только папку node_modules

Добавим команду в секцию `scripts`, чтобы иметь возможность отформатировать все файлы в проекте разом

```text
"format": "prettier --write ."
```

## ESLint

```bash
# Установим eslint пакет в проект
npm install --save-dev eslint
```

```bash
# Установим дополнительные пакеты, чтобы интегрировать eslint и prettier, чтобы они друг с другом не конфликтовали
npm install --save-dev eslint-plugin-prettier eslint-config-prettier
```

Создаем конфигурационный файл `.eslintrc.json` и добавляем в него необходимые правила. За основу конфига возьмем готовый конфиг от eslint - `eslint:recommended`.

Список всех доступных правил можно посмотреть [тут](https://eslint.org/docs/rules/).

Чтобы исключить из проверки директории/файлы указываем их в виде списка в игнор файле .eslintignore
