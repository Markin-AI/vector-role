# Vector Ansible role
=========

Роль для установки [Vector](https://vector.dev/) на Linux rpm.

Requirements
------------

- **Ansible 2.11+**

Role Variables
--------------

| Scope | Variable | Default | Description |
| ---- |---- | ---- | ---- |
| defaults | vector_version | 0.34.1 | Версия дистрибутива |
| defaults | vector_data_dir | /var/lib/vector | Путь к директории с данными |
| defaults | clickhouse_url | http://localhost:8123 | Clickhouse endpoint (http://адрес:порт) |
| defaults | clickhouse_db | logs | Базасв по умолчанию для записи данных |
| defaults | clickhouse_table | logs | Таблица по умолчанию для записи данных |


Dependencies
------------

\-

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- name: Install Vector
  hosts: vector
  become: true
  roles:
    - vector
  tags: vector
```

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).