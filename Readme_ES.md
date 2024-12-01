# Guía para Crear o Actualizar un Superusuario en PocketBase (v0.23.3)

Esta guía explica cómo crear o actualizar un superusuario en PocketBase utilizando la CLI. Este método es útil si el enlace con token que aparece durante la instalación no funciona, como ocurrió en mi caso con la versión `v0.23.3`.

---

## Requisitos Previos
- Tener PocketBase instalado y en funcionamiento.
- Acceso a la CLI de PocketBase.
- Si usas Docker, asegúrate de que el contenedor esté corriendo.

---

## Comando Básico

Utiliza el siguiente comando para crear o actualizar un superusuario:

```
/app/pocketbase superuser upsert <email> <password>
```

### Ejemplo

Para crear un superusuario con el correo `admin@example.com` y la contraseña `strong4a$$w0rd`, utiliza:

```
/app/pocketbase superuser upsert admin@example.com strong4a$$w0rd
```

---

## Notas Clave

1. **Correo Electrónico**:
   - Asegúrate de que la dirección sea válida.

2. **Contraseña Segura**:
   - Usa una contraseña segura (al menos 8 caracteres, mezcla de letras, números y símbolos).

3. **Ubicación de la Base de Datos**:
   - Si tu base de datos no está en la ubicación por defecto, especifica la ruta usando `--dir`:

     ```
     /app/pocketbase superuser upsert admin@example.com strong4a$$w0rd --dir /path/to/pb_data
     ```

4. **Docker**:
   - Si ejecutas PocketBase en Docker, primero accede al contenedor:

     ```
     docker exec -it <nombre_del_contenedor> sh
     ```

     Luego ejecuta el comando dentro del contenedor.

---

## ¿Por Qué Usar Este Comando?

Durante la instalación de PocketBase v0.23.3, se genera un enlace de lanzamiento con un token en la terminal. Sin embargo, este enlace puede no funcionar correctamente (como ocurrió en mi caso), por lo que es necesario utilizar el comando CLI mencionado.

---

## Verificación

Para confirmar que el superusuario se creó o actualizó correctamente, inicia sesión con las credenciales en la interfaz de administración de PocketBase.

---

¡Eso es todo! Ahora tienes un superusuario funcional. 🚀
