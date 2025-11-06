# Ansible Docker Project

Ce projet déploie automatiquement Docker sur une machine distante avec Ansible, puis lance un conteneur Nginx qui sert un site statique personnalisé.

## 📁 Structure du projet

- `inventory/hosts.ini` : fichier d’inventaire Ansible
- `playbooks/install-docker.yml` : installe Docker
- `playbooks/setup-site.yml` : crée un dossier avec un fichier HTML
- `playbooks/run-nginx.yml` : lance un conteneur Nginx avec un volume monté
- `site/index.html` : page HTML servie par Nginx

## 🚀 Utilisation

```bash
ansible-playbook -i inventory/hosts.ini playbooks/install-docker.yml
ansible-playbook -i inventory/hosts.ini playbooks/setup-site.yml
ansible-playbook -i inventory/hosts.ini playbooks/run-nginx.yml
