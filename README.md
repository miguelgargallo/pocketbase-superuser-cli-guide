# Superuser Guide for PocketBase (v0.23.3)

<p align="center">
    <a href="https://pocketbase.io" target="_blank" rel="noopener">
        <img src="https://i.imgur.com/5qimnm5.png" alt="PocketBase - open source backend in 1 file" />
    </a>
</p>
<div align="center">
  <a href="#english">English</a> | <a href="#spanish">Español</a>
</div>

---

## <a id="english">English Guide</a>

### 1. Prerequisites
- PocketBase installed and running.
- Access to PocketBase's CLI.
- If using Docker, ensure the container is running.

---

### 2. Basic Command
Use the following command to create or update a superuser:

<pre style="background:#282c34;color:#61dafb;padding:10px;border-radius:5px;overflow:auto;">
/app/pocketbase superuser upsert &lt;email&gt; &lt;password&gt;
</pre>

#### Example
To create a superuser with the email `admin@example.com` and the password `strong4a$$w0rd`:


<pre style="background:#282c34;color:#61dafb;padding:10px;border-radius:5px;overflow:auto;">
/app/pocketbase superuser upsert admin@example.com strong4a$$w0rd
</pre>

---

### 3. Key Notes
1. **Email**:
   - Ensure the email address is valid.
2. **Secure Password**:
   - Use a strong password (at least 8 characters, mix of letters, numbers, and symbols).
3. **Database Location**:
   - If your database is not in the default location, specify the path using `--dir`:
     ```bash
     /app/pocketbase superuser upsert admin@example.com strong4a$$w0rd --dir /path/to/pb_data
     ```

---

### 4. Why Use This Command?
During the installation of PocketBase `v0.23.3`, a launch link with a token is generated in the terminal. However, this link may not work properly (as it happened for me). Using the above command allows you to bypass this issue.

---

## <a id="spanish">Guía en Español</a>

### 1. Requisitos Previos
- Tener PocketBase instalado y en funcionamiento.
- Acceso a la CLI de PocketBase.
- Si usas Docker, asegúrate de que el contenedor esté corriendo.

---

### 2. Comando Básico
Utiliza el siguiente comando para crear o actualizar un superusuario:


<pre style="background:#282c34;color:#61dafb;padding:10px;border-radius:5px;overflow:auto;">
/app/pocketbase superuser upsert &lt;email&gt; &lt;password&gt;
</pre>

#### Ejemplo
Para crear un superusuario con el correo `admin@example.com` y la contraseña `strong4a$$w0rd`:


<pre style="background:#282c34;color:#61dafb;padding:10px;border-radius:5px;overflow:auto;">
/app/pocketbase superuser upsert admin@example.com strong4a$$w0rd
</pre>

---

### 3. Notas Clave
1. **Correo Electrónico**:
   - Asegúrate de que sea válido.
2. **Contraseña Segura**:
   - Usa una contraseña fuerte.
3. **Ubicación de la Base de Datos**:
   - Si tu base de datos no está en la ubicación por defecto, especifica la ruta con `--dir`:
     ```bash
     /app/pocketbase superuser upsert admin@example.com strong4a$$w0rd --dir /path/to/pb_data
     ```

---

### 4. ¿Por Qué Usar Este Comando?
Durante la instalación de PocketBase `v0.23.3`, se genera un enlace con token en la terminal. Sin embargo, este enlace puede no funcionar correctamente (como ocurrió en mi caso). Usar este comando permite solucionar este problema.

---

<div align="center">
  <strong>That's all! 🚀 ¡Eso es todo!</strong>
</div>
