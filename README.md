
# Superuser Guide for PocketBase (v0.23.3)

This README contains a guide in both English and Spanish for creating or updating a superuser in PocketBase. 

During the installation of PocketBase v0.23.3, a launch link with a token is provided. However, this link did not work for me, so I had to rely on the CLI. This guide includes the necessary steps to do so.

---

## Table of Contents

- [English Guide](#english-guide)
  - [1. Prerequisites](#1-prerequisites)
  - [2. Basic Command](#2-basic-command)
  - [3. Key Notes](#3-key-notes)
  - [4. Why Use This Command?](#4-why-use-this-command)
- [Guía en Español](#guía-en-español)
  - [1. Requisitos Previos](#1-requisitos-previos)
  - [2. Comando Básico](#2-comando-básico)
  - [3. Notas Clave](#3-notas-clave)
  - [4. ¿Por Qué Usar Este Comando?](#4-¿por-qué-usar-este-comando)

---

## English Guide

### 1. Prerequisites

- PocketBase installed and running.
- Access to PocketBase's CLI.
- If using Docker, ensure the container is running.

### 2. Basic Command

Use the following command to create or update a superuser:

```
/app/pocketbase superuser upsert <email> <password>
```

#### Example

To create a superuser with the email `admin@example.com` and the password `strong4a$$w0rd`:

```
/app/pocketbase superuser upsert admin@example.com strong4a$$w0rd
```

### 3. Key Notes

1. **Email**: Ensure the email address is valid.
2. **Secure Password**: Use a strong password (at least 8 characters, mix of letters, numbers, and symbols).
3. **Database Location**:
   - If your database is not in the default location, specify the path using `--dir`:
     ```
     /app/pocketbase superuser upsert admin@example.com strong4a$$w0rd --dir /path/to/pb_data
     ```
4. **Docker**:
   - If running PocketBase in Docker, first access the container:
     ```
     docker exec -it <container_name> sh
     ```
     Then run the command inside the container.

### 4. Why Use This Command?

In version `v0.23.3`, the token-based link shown during installation might not work properly, as it happened to me. This CLI command provides an alternative method to create or update a superuser.

---

## Guía en Español

### 1. Requisitos Previos

- Tener PocketBase instalado y en funcionamiento.
- Acceso a la CLI de PocketBase.
- Si usas Docker, asegúrate de que el contenedor esté corriendo.

### 2. Comando Básico

Utiliza el siguiente comando para crear o actualizar un superusuario:

```
/app/pocketbase superuser upsert <email> <password>
```

#### Ejemplo

Para crear un superusuario con el correo `admin@example.com` y la contraseña `strong4a$$w0rd`:

```
/app/pocketbase superuser upsert admin@example.com strong4a$$w0rd
```

### 3. Notas Clave

1. **Correo Electrónico**: Asegúrate de que sea válido.
2. **Contraseña Segura**: Usa una contraseña fuerte (mínimo 8 caracteres, mezcla de letras, números y símbolos).
3. **Ubicación de la Base de Datos**:
   - Si tu base de datos no está en la ubicación por defecto, especifica la ruta con `--dir`:
     ```
     /app/pocketbase superuser upsert admin@example.com strong4a$$w0rd --dir /path/to/pb_data
     ```
4. **Docker**:
   - Si ejecutas PocketBase en Docker, primero accede al contenedor:
     ```
     docker exec -it <nombre_del_contenedor> sh
     ```
     Luego ejecuta el comando dentro del contenedor.

### 4. ¿Por Qué Usar Este Comando?

En la versión `v0.23.3`, el enlace con token generado durante la instalación puede no funcionar correctamente, como me pasó a mí. Este comando CLI proporciona un método alternativo para crear o actualizar un superusuario.

---

¡Eso es todo! Si necesitas más ayuda, no dudes en pedirla. 🚀

