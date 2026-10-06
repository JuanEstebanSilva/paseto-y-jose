# 🔐 Laboratorios de Autenticación y Autorización: PASETO y JOSE

Este repositorio contiene el material formativo y la implementación práctica de tokens de seguridad utilizando **PASETO (Platform-Agnostic Security Tokens)** en **Node.js** y **Express**.

---

## 📂 Estructura del Repositorio

El proyecto está dividido en tres etapas/laboratorios independientes:

```text
.
├── 📁 lab-paseto/             # Versión 1: Autenticación básica con PASETO v4.public
│   ├── src/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── routes/
│   │   └── app.js
│   ├── .env
│   ├── package.json
│   └── README.md
│
├── 📁 lab-paseto-v2/          # Versión 2: Roles (RBAC), Swagger UI y Auditoría SCA
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── data/
│   │   ├── middlewares/
│   │   ├── routes/
│   │   └── app.js
│   ├── .env
│   ├── package.json
│   └── README.md
│
├── 📁 lab-paseto-v3/          # Versión 3: CRUD Completo, Roles, Validaciones (express-validator) y Swagger
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── data/
│   │   ├── middlewares/
│   │   ├── routes/
│   │   ├── validators/
│   │   └── app.js
│   ├── .env
│   ├── package.json
│   └── README.md
│
└── 📄 PASETO y JOSE.pdf       # Diapositivas / presentación teórica del laboratorio
```

---

## 🚀 Proyectos Disponibles

### 1. [Lab PASETO (Versión 1)](./lab-paseto/README.md)
* Flujo de inicio de sesión básico.
* Generación y firma de tokens asimétricos con **PASETO v4.public** (`v4.Sign`).
* Validación mediante middleware y clave pública (`v4.Verify`).
* Acceso a ruta protegida `/api/auth/perfil`.

### 2. [Lab PASETO V2 (Versión 2)](./lab-paseto-v2/README.md)
* Autenticación con datos locales de usuarios.
* **Control de acceso basado en roles (RBAC)**: permisos específicos para `administrador`, `medico` y `paciente`.
* Documentación interactiva de la API con **Swagger / OpenAPI** en `/api-docs`.
* Rutas adicionales para consulta de usuarios (`/api/usuarios`).
* Pruebas y validación de respuestas HTTP (`200`, `401`, `403`, `404`).
* Gestión de dependencias y análisis de vulnerabilidades con `npm audit`.

### 3. [Lab PASETO V3 (Versión 3)](./lab-paseto-v3/README.md)
* **CRUD completo de usuarios**: `GET`, `POST`, `PUT`, `PATCH`, `DELETE`.
* Autenticación con **PASETO v4.public**.
* **Control de acceso basado en roles**: permisos granulares por endpoint (`administrador`, `medico`, `paciente`).
* Validación estricta y sanitización de datos de entrada con **`express-validator`**.
* Filtrado seguro con **`matchedData()`** para evitar asignaciones masivas no autorizadas.
* Protección de contraseñas (exclusión de `password` en todas las respuestas JSON).
* Manejo estandarizado de códigos HTTP (`200`, `201`, `204`, `400`, `401`, `403`, `404`, `409`).
* Documentación interactiva completa con **Swagger / OpenAPI** en `/api-docs`.
* Auditoría de dependencias con `npm audit`.

---

## 🛠️ Cómo Ejecutar Cualquiera de los Laboratorios

1. Entra a la carpeta del laboratorio deseado:
   ```bash
   cd lab-paseto
   # o
   cd lab-paseto-v2
   # o
   cd lab-paseto-v3
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Inicia el servidor de desarrollo:
   ```bash
   npm run dev
   ```
