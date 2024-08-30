### Установка Clickhouse и Vector инструментом Ansible

---

Установка инфраструктуры в docker контейнерах для сбора и анализа логов на основе Clickhouse и Vector

---


### Installation

Запускаем командой docker compose up файл [docker-compose.yml](https://github.com/smabramov/Ansible-02-hw/blob/b42e046f4445e16b056001c02f90eac9f519acec/playbook/docker-compose.yml)


Для выбора версии и архитектуры замените в файлах group_vars/clickhouse/vars.yml и group_vars/vector/vars.yml соответствующие переменные:

```
clickhouse_version: ""

vector_version: ""

```

Конфигурация для vector содержится в tenplate файле vector.toml.j2

Выполняем следующие команды:

```
ansible-lint site.yml

ansible-playbook -i ./inventory/prod.yml site.yml --check

ansible-playbook -i ./inventory/prod.yml site.yml --diff

ansible-playbook -i ./inventory/prod.yml site.yml --diff

ansible-playbook -i /inventory/prod.yml site.yml

```



