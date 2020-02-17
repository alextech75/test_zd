# test_zd

Ansible playbook: 
1) Разворачивание nginx 
2) Разворачивание postgres в docker  
Проверка ОС установлена на хостовой машине Debian подобная или CentOS подобная. 
Так же база postgres устанавливается локально.

```yaml
---

- hosts: db
  become: true
  vars:
    pip_install_packages:
      - name: docker
  roles:
    - nginx
    - pip
    - docker
    - postgres_docker
```
