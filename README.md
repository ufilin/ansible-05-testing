# ansible-03-yandex
# Ansible Playbook для установки ClickHouse, Vector и Lighthouse

## Описание

Данный playbook автоматизирует установку и настройку трех сервисов на виртуальных машинах в Yandex Cloud:

- **ClickHouse**
- **Vector**
- **Lighthouse**

Playbook написан с учетом требований идемпотентности и прошел проверку `ansible-lint`.

### Целевые хосты
- **Операционная система**: Ubuntu

### Три хоста в Yandex Cloud
| Хост | Назначение | Порт |
|------|------------|------|
| clickhouse-01 | ClickHouse сервер | 8123 (HTTP), 9000 (Native) |
| vector-01 | Vector для сбора логов | - |
| lighthouse-01 | Lighthouse веб-интерфейс | 80 |

### Группа безопасности
Добавлены порты:
- `22` - SSH
- `80` - Lighthouse
- `8123` - ClickHouse HTTP интерфейс
- `9000` - ClickHouse Native протокол
