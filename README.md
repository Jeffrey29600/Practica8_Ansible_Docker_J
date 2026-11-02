Descripción

En esta práctica utilicé Docker Compose para crear cinco servidores Ubuntu y Ansible para automatizar tareas en todos ellos.

Tecnologías utilizadas

Docker y Docker Compose

Ubuntu 24.04

Ansible

SSH

Archivos del proyecto

Dockerfile: prepara Ubuntu con SSH y el usuario ansible.

docker-compose.yml: crea los cinco servidores.

inventario.ini: contiene las conexiones de los servidores.

ansible.cfg: configura Ansible.

playbook.yml: contiene las tareas de automatización.

Cómo ejecutar la práctica

Se necesita Docker Desktop y Ansible instalados.

Desde la carpeta del proyecto, ejecutar:

docker compose up -d --build
ansible servidores -m ping
ansible-playbook playbook.yml

Tareas automatizadas

Actualizar la caché de APT.

Crear el usuario itla.

Crear la carpeta /home/itla/app.

Crear el archivo hola.txt.

Instalar cowsay y htop.

Resultados obtenidos

La automatización terminó correctamente en los cinco servidores Ubuntu.

Cada servidor mostró ok=6, changed=4, unreachable=0 y failed=0.

También comprobé que los cinco servidores contienen el archivo hola.txt y tienen instalados cowsay y htop.

Autor

Jeffrey Mercado

