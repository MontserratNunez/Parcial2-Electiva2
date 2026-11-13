# Laboratorio 2do Parcial - Ansible con Docker

## Objetivo de la práctica
Administrar un entorno de múltiples servidores Linux basados en contenedores Docker utilizando Ansible como herramienta de automatización y configuración.

## Estructura del Laboratorio
ansible-lab/
├── Dockerfile
├── docker-compose.yml
├── inventory.ini
├── playbook.yml
└── README.md

## Comandos
1. Levantar los servidores:
```bash
   docker compose up -d --build
```

2. Instalar Python 3 en los contenedores:
```bash
docker exec -it server1 bash -c "apt update && apt install -y python3"
docker exec -it server2 bash -c "apt update && apt install -y python3"
```

3. Entrar a la terminal del contenedor controlador de Ansible:
```bash
docker exec -it ansible-controller bash

```

4. Navegar a la carpeta de trabajo dentro del contenedor:
```bash
cd /ansible-lab

```

5. Comprobar la conexión mediante un ping de Ansible:
```bash
ansible docker -i inventory.ini -m ping

```

6. Comando para ejecutar el playbook

```bash
ansible-playbook -i inventory.ini playbook.yml

```



## Captura de ejecución exitosa

![Playbook1](https://github.com/user-attachments/assets/0da6a6b9-824f-4601-84b5-2a36dda5d8b8) 
![Playbook2](https://github.com/user-attachments/assets/df8cbb13-4076-4fea-914c-1fea93a79331) 
