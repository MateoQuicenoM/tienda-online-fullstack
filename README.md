# 🛒 Tienda Online Full Stack

Aplicación web full stack de comercio electrónico desarrollada con Node.js, Express y MySQL.

El proyecto implementa una arquitectura cliente-servidor con API REST,
gestión de productos, clientes, pedidos y facturas, utilizando una base de datos relacional.

---

## 🚀 Requisitos previos

- [Node.js](https://nodejs.org/) (v16 o superior).
- [XAMPP](https://www.apachefriends.org/) (para MySQL y phpMyAdmin).
- [Git](https://git-scm.com/).
- [Postman](https://www.postman.com/) para probar endpoints.

---

## 📂 Estructura del proyecto

```
Tienda-online-fullstack/
│── css/                # Estilos CSS
│── db/                 # Carpeta con script de base de datos
│   └── tienda_online.sql
│── js/                 # Scripts frontend
│── models/             # Conexión con la base de datos
│   └── db.js
│── pages/              # Páginas HTML
│── public/             # Archivos públicos
│── routes/             # Rutas de la API
│   ├── clientes.js
│   ├── facturas.js
│   ├── pedidos.js
│   └── productos.js
│── .gitignore
│── index.js            # Archivo principal del servidor
│── package.json        # Dependencias del proyecto
│── package-lock.json
```

---

## 🗄️ Base de Datos

1. Abrir **phpMyAdmin** desde XAMPP.  
2. Crear la base de datos:

```sql
CREATE DATABASE tienda_online;
```

3. Importar el script incluido en el proyecto:  

- Ubicación: `db/tienda_online.sql`  
- Opción 1: Importar desde phpMyAdmin → pestaña **Importar**.  
- Opción 2: Desde consola:

```bash
mysql -u root -p tienda_online < db/tienda_online.sql
```

---

## ⚙️ Variables de entorno

Crea en la raíz del proyecto un archivo **.env** con la configuración de la base de datos:

```
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=tienda_online
DB_PORT=3306
PORT=3000
```

*(si tu usuario MySQL tiene contraseña, agrégala en `DB_PASSWORD`).*

---

## 📦 Instalación

1. Clonar el repositorio:

```bash
git clone https://github.com/MateoQuicenoM/Tienda-online-fullstack.git
```

2. Entrar al proyecto:

```bash
cd Proyecto-tienda
```

3. Instalar dependencias:

```bash
npm install
```

---

## ▶️ Inicialización de la aplicación (Backend + Frontend)

Este proyecto **no necesita un servidor separado para el frontend**.  
El mismo servidor Node/Express (`index.js`) se encarga de:

- Exponer la API (rutas de productos, clientes, pedidos, facturas).
- Servir los archivos estáticos de la carpeta `pages/` y `public/`.

### Pasos:

1. Levantar el servidor con:

```bash
nodemon index.js
```

2. Abrir en el navegador:

```
http://localhost:3000/pages/index.html
```

De esta forma ya se cargan las páginas HTML con conexión al backend.

---

## 🧪 Endpoints principales (Postman)

- **GET** → `http://localhost:3000/productos`  
- **POST** → `http://localhost:3000/productos`  
- **PUT** → `http://localhost:3000/productos/:id`  
- **DELETE** → `http://localhost:3000/productos/:id`  

También existen rutas para **clientes**, **pedidos** y **facturas** en la carpeta `routes/`.

---

## ✅ Notas

- Script SQL: `db/tienda_online.sql`  
- Archivo principal: `index.js`  
- Servidor se ejecuta con: `nodemon index.js`  
- Editor recomendado: VS Code
