# Ansible-05-testing: Role Vector


## Требования

- Ansible 2.9 или выше
- Поддерживаемые ОС:
  - Ubuntu 22.04 (и выше)
  - CentOS Stream 8
- Python 3.6+ на целевых хостах

## Переменные

| Переменная | Описание | Значение по умолчанию |
|------------|----------|----------------------|
| `vector_version` | Версия Vector | `0.21.1` |
| `vector_config_dir` | Директория конфигурации | `/etc/vector` |
| `vector_data_dir` | Директория данных | `/var/lib/vector` |

## Тестирование
### Molecule
Роль протестирована с использованием Molecule:

molecule test

molecule test -s podman

### Tox
Для запуска тестов через Tox:

tox

## Проверки (Verify)

После применения роли выполняются следующие проверки:

 - Существование бинарного файла /usr/bin/vector

 - Существование конфигурационного файла /etc/vector/vector.yaml

 - Запущен ли процесс Vector

## Лицензия
MIT
