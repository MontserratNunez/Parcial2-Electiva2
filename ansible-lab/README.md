# Laboratorio 2do Parcial - Ansible con Docker

## Objetivo de la práctica
Administrar un entorno de múltiples servidores Linux basados en contenedores Docker utilizando Ansible como herramienta de automatización y configuración.

## Comandos para iniciar los contenedores
1. Levantar los servidores:
   ```bash
   docker compose up -d

```

2. Instalar Python 3 en los contenedores (requisito para Ansible):
```bash
docker exec -it server1 bash -c "apt update && apt install -y python3"
docker exec -it server2 bash -c "apt update && apt install -y python3"

```



## Comando para ejecutar el playbook

```bash
ansible-playbook -i inventory.ini playbook.yml

```

## Captura de ejecución exitosa
