
# Práctica 8 - Automatización de Servidores con Ansible y Docker

## Descripción

En esta práctica creé cinco servidores Ubuntu utilizando Docker Compose y automaticé su configuración mediante Ansible.

El proyecto se llama **ITLA DevOps Lab** e incluye una identificación personalizada para cada servidor.

## Tecnologías utilizadas

- Docker y Docker Compose
- Ubuntu 24.04
- Ansible
- SSH

## Archivos del proyecto

- `Dockerfile`: configuración de Ubuntu con SSH.
- `docker-compose.yml`: creación de los cinco servidores.
- `inventario.ini`: información de conexión de los servidores.
- `ansible.cfg`: configuración de Ansible.
- `playbook.yml`: tareas de automatización.

## Tareas realizadas

- Actualizar la caché de APT.
- Crear el usuario `itla`.
- Crear la carpeta `app`.
- Crear el archivo `hola.txt`.
- Instalar `cowsay` y `htop`.

## Personalización

Agregué el archivo `identidad.txt`, que identifica cada servidor con el nombre del proyecto, mi nombre y matrícula.

También configuré un mensaje de bienvenida para los servidores.

## Ejecución

Para iniciar los servidores y ejecutar la automatización:

```bash
docker compose up -d --build
ansible servidores -m ping
ansible-playbook playbook.yml
```

## Resultado

La automatización se completó correctamente en los cinco servidores Ubuntu.

**Resultado final:** 8 tareas correctas por servidor, 0 errores y 0 servidores inaccesibles.

Jeffrey Mercado

