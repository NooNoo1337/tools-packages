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
