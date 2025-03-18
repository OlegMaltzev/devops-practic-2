# devops-practic-2
Практикум по курсу Kubernetes: мониторинг и логирование


## Описание
Данный репозиторий содержит Ansible роли для автоматизированного развертывания, мониторинга и логирования на CentOS Stream 9. 

Включает:
- Prometheus
- Node Exporter
- OpenSearch + OpenSearch-Dashboard
- FluentBit 


## Роли

- prometheus: установка и настройка Prometheus
- node_exporter: установка и настройка Node Exporter, добавление в конфиг - Prometheus  
- opensearch: установка и настройка OpenSearch + OpenSearch-Dashboard  
- fluentbit: настройка FluentBit для сбора логов в OpenSearch  


## Использование

Запуск VM с CentOS Stream 9

```
vagrant up
```

Запуск плейбука:

```
ansible-playbook playbook.yml
```

Конфигурирование:
/vars/defaults.yml


