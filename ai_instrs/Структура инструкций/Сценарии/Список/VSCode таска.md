## VSCode таска

**Входные данные:**
- `scriptPath` - путь к скрипту
- `watchingPath` - путь к файлам для watch-инга

**Инструкции:**

Напиши [](</.vscode/tasks.json>):
- запускает скрипт из `scriptPath`
- запускается при открытии проекта (`runOptions.runOn: "folderOpen"`).
- watch-ит за изменениями `watchingPath`