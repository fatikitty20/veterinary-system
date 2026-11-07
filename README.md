# 🐾 Veterinary System

Sistema web de gestión para una clínica veterinaria. Permite administrar **clientes, mascotas, servicios y cuentas** desde un panel con inicio de sesión y roles de usuario.

<!-- 🔗 Demo en vivo: https://TU-DEMO.netlify.app -->

![Panel principal](docs/screenshots/panel.png)
<!-- Agrega 2 o 3 capturas: login, listado de mascotas, formulario de cliente -->

---

## ✨ Características

- **Clientes:** alta, edición, búsqueda y eliminación (identificados por teléfono).
- **Mascotas:** registro con raza, especie (perro / gato), observaciones y foto.
- **Servicios:** catálogo de servicios de la clínica.
- **Cuentas:** gestión de cuentas de la clínica.
- **Login con roles** (administrador y recepcionista) y panel de recepción.
- **Solicitud de acceso:** los nuevos usuarios piden acceso y el administrador lo aprueba.
- **Buscador** y tablas dinámicas con datos en tiempo real.

## 🛠️ Stack

| Área | Tecnologías |
|---|---|
| Frontend | HTML5, CSS3, JavaScript (ES Modules) |
| Backend / BD | Supabase (PostgreSQL + API) |
| Arquitectura | Patrón MVC (Vista / Controlador / Modelo) |
| Despliegue | Netlify |

## 📁 Estructura del proyecto

```text
.
├── Vista/          # Páginas HTML, estilos e imágenes
├── controlador/    # Lógica de cada pantalla y conexión con Supabase
└── modelo/         # Operaciones de alta y edición de datos
```

## 🗄️ Modelo de datos

Tablas principales en Supabase: `clientes`, `mascotas`, `razas`, `servicios`, `cuenta`, `usuarios` y `roles`.

## 🚀 Cómo ejecutarlo

1. Clona el repositorio:

   ```bash
   git clone https://github.com/fatikitty20/veterinary-system.git
   cd veterinary-system
   ```

2. Crea un proyecto gratuito en [Supabase](https://supabase.com) y las tablas indicadas arriba.

3. Edita `controlador/config.js` con **tu** URL y tu clave `anon`:

   ```js
   const SUPABASE_URL = "https://TU-PROYECTO.supabase.co";
   const SUPABASE_ANON_KEY = "TU_CLAVE_ANON";
   ```

4. Sirve la carpeta `Vista/` con cualquier servidor estático, por ejemplo:

   ```bash
   npx serve Vista
   ```

   O abre `Vista/index.html` con la extensión **Live Server** de VS Code.

> 🔒 **Seguridad:** activa las políticas **Row Level Security (RLS)** en Supabase para proteger los datos. La clave `anon` es pública por diseño; nunca subas la clave `service_role`.

## ☁️ Despliegue

El proyecto incluye `netlify.toml` con la carpeta `Vista` como directorio de publicación. Conecta el repositorio en Netlify y se despliega automáticamente.

## 🧭 Próximos pasos

- [ ] Agenda de citas y recordatorios
- [ ] Historial clínico por mascota
- [ ] Reportes y facturación
- [ ] Pruebas automáticas

## 👩‍💻 Autora

**fatikitty20** · [GitHub](https://github.com/fatikitty20)
