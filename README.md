# Proyecto Final - Despliegue de Servicios con Ansible

## Estructura actual

Este proyecto contiene el despliegue automatizado de un servidor DNS BIND9 en un contenedor LXD, utilizando Ansible.

La estructura actual del proyecto es la siguiente:

- playbooks-proyecto/
- ├── inventory
-├── playbooks/
-│ ├── dns_playbook.yaml
-│ ├── files/
-│ │ ├── db.hospital.local
-│ │ ├── db.soeasy.local
-│ │ └── db.universidad.local
-│ └── templates/
-│ └── named.conf.local.j2


## Descripción de la parte completada

- **dns_playbook.yaml**: Playbook principal para desplegar el servicio DNS en el contenedor `dns-server`.
- **files/**: Contiene los archivos de zona predefinidos para los dominios `hospital.local`, `soeasy.local` y `universidad.local`.
- **templates/**: Contiene el template para generar el fichero `named.conf.local` que define las zonas DNS en el servidor BIND9.
- **inventory**: Archivo de inventario Ansible apuntando al contenedor `dns-server` (`192.168.100.10`).

## Estado actual

- Servidor BIND9 instalado y configurado correctamente.
- Archivos de zona copiados y validados.
- Servicio DNS en funcionamiento y verificable con consultas `dig`.

---

## Próximos pasos (pendiente)

- Configurar el cliente Kali para utilizar `dns-server` como su servidor DNS primario.
- Continuar con la automatización de otros servicios necesarios para el proyecto.

---

> Este `README.md` se actualizará progresivamente a medida que el proyecto avance.
