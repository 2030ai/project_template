# Логирование

Использовать, если скрипт делает сетевые запросы, работает с внешними сервисами или есть риск ошибок.

## Правила
- Использовать минимально необходимый объем данных.
- Логи хранить в `logs/<script>/<timestamp>/`.
- Формат логов: `.md`.
- Одна запись = одно событие; указывать время и уровень (INFO/WARN/ERROR).
- Удалять логи старше одного месяца, если нет иных инструкций.

## Минимальный шаблон лога
```markdown
# Log: <script-name>
Дата: YYYY-MM-DD HH:MM
Запуск: <command/args>

## События
- [HH:MM:SS] [INFO] start - ok
- [HH:MM:SS] [INFO] request <service> <method> <endpoint> - ok
- [HH:MM:SS] [ERROR] <action> - <error>
- [HH:MM:SS] [INFO] finish - ok
```
