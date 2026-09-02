# 🐾 Patitas con Hogar

Plataforma web para facilitar la adopción responsable de mascotas, conectando refugios con personas interesadas en brindarles un hogar.

La aplicación permite a los usuarios explorar mascotas disponibles, consultar información detallada y enviar solicitudes de adopción. Los refugios pueden publicar y administrar sus mascotas y gestionar las solicitudes recibidas.

---

## 🚀 Tecnologías utilizadas

- **Next.js 14** — Framework principal
- **React 18** — Interfaz de usuario
- **TypeScript** — Tipado estático
- **Tailwind CSS** — Estilos y diseño responsive
- **Supabase** — Base de datos PostgreSQL, autenticación y Row Level Security
- **Dog CEO API** — Consulta de información sobre razas de perros
- **Vercel** — Plataforma prevista para el despliegue

---

## 👥 Roles de usuario

La aplicación cuenta con dos tipos principales de usuarios:

### 🏠 Adoptante

Puede:

- Explorar mascotas disponibles.
- Buscar y filtrar mascotas.
- Consultar información detallada.
- Enviar solicitudes de adopción.
- Consultar el estado de sus solicitudes.

### 🐶 Refugio

Puede:

- Publicar mascotas disponibles para adopción.
- Editar sus publicaciones.
- Eliminar publicaciones.
- Consultar solicitudes de adopción.
- Aprobar o rechazar solicitudes.

Los roles son almacenados en la tabla `profiles` y gestionados mediante Supabase.

---

## ✨ Funcionalidades

- [x] Página de inicio.
- [x] Listado de mascotas.
- [x] Búsqueda y filtrado.
- [x] Página de detalle de cada mascota.
- [x] Registro de usuarios.
- [x] Inicio y cierre de sesión.
- [x] Autenticación mediante Supabase.
- [x] Gestión de roles: adoptante y refugio.
- [x] Panel privado de usuario.
- [x] CRUD de mascotas para refugios.
- [x] Solicitudes de adopción.
- [x] Gestión de solicitudes por parte de refugios.
- [x] Integración con Dog CEO API.
- [x] Protección de datos mediante Row Level Security (RLS).
- [x] TypeScript con tipado estricto.

---

## 🗃️ Modelo de datos

La aplicación utiliza Supabase PostgreSQL para almacenar la información principal.

Las entidades principales son:

- **profiles** — Información y rol de los usuarios.
- **pets** — Mascotas publicadas por los refugios.
- **applications** — Solicitudes de adopción realizadas por los adoptantes.

Relaciones principales:

```text
Usuario (profiles)
      │
      ├───────────────┐
      │               │
      ▼               ▼
   Mascotas       Solicitudes
    (pets)       (applications)
                       │
                       ▼
                    Mascota
