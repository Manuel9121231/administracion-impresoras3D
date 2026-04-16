# Gestor de Impresoras 3D 🖨️

Sistema integral de gestión y mantenimiento para impresoras 3D y máquinas industriales.

## ✨ Características

- 📋 Gestión de salas y máquinas
- ✅ Checklists personalizados de mantenimiento
- 🔗 Generación automática de códigos QR
- 👷 Sistema de operarios con PIN
- 📊 Dashboard de estadísticas
- 📜 Historial completo de sesiones

## 🚀 Instalación

### Requisitos
- Node.js 14+ instalado

### Pasos

1. **Clona el repositorio**
```bash
git clone https://github.com/Manuel9121231/administracion-impresoras3D.git
cd administracion-impresoras3D
```

2. **Instala las dependencias**
```bash
npm install
```

3. **Inicia el servidor**
```bash
node server.js
```

El servidor estará disponible en: `http://localhost:3000`

## 📱 Uso

### Panel de Administración
Accede a: **http://localhost:3000**

### Para Operarios
Escanea el código QR o accede a: **http://tu-ip:3000/operario.html?id=<ID_MAQUINA>**

## 🔌 API Endpoints

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| GET | /api/salas | Obtener todas las salas |
| GET | /api/maquinas?sala_id=<id> | Máquinas de una sala |
| GET | /api/maquina/:id | Detalles de una máquina |
| GET | /api/maquina/:id/qr | Generar QR para máquina |
| GET | /api/operarios | Listar operarios |
| POST | /api/operarios | Crear nuevo operario |
| GET | /api/dashboard | Estadísticas del sistema |
| GET | /api/historial | Historial de sesiones |

## 📁 Estructura del Proyecto

```
administracion-impresoras3D/
├── server.js              # Servidor principal
├── package.json           # Dependencias
├── database/
│   └── db.js             # Lógica de base de datos
├── public/
│   ├── index.html        # Panel administrativo
│   └── operario.html     # Interfaz de operarios
└── gestion.db            # Base de datos SQLite
```

## 🛠️ Tecnología

- **Backend**: Node.js + Express.js
- **Base de datos**: SQLite
- **Frontend**: HTML5 + JavaScript
- **Generador QR**: qrcode

## 📦 Dependencias principales

- express: Servidor web
- cors: CORS middleware
- qrcode: Generación de códigos QR
- sqlite3: Base de datos SQLite

## 👤 Autor

**Manuel9121231**

---

Nota: La base de datos SQLite (gestion.db) se genera automáticamente al primera ejecución del servidor.