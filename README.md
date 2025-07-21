 TeckFlow - Gestor de Correspondencia

TeckFlow es una aplicación web moderna y completa construida con Next.js que te permite gestionar tu correspondencia de manera eficiente y visual. Registra, clasifica y sigue el estado de tus comunicaciones a través de múltiples vistas, incluyendo una tabla detallada, una galería visual y un tablero Kanban interactivo.

![Captura de pantalla de TeckFlow](https://drive.google.com/file/d/1UW8U9v4ai5uHAK8QRvtcEoUdazNzZCxB/view?usp=sharing)

## ✨ Características Principales

- **CRUD Completo:** Crea, lee, actualiza y elimina registros de correspondencia con facilidad.
- **Múltiples Vistas:** Visualiza tus datos en el formato que prefieras:
    - **Vista de Tabla:** Para un análisis detallado con ordenamiento y filtrado.
    - **Vista de Galería:** Para una visualización rápida y atractiva de cada registro.
    - **Vista de Tablero Kanban:** Organiza tu flujo de trabajo arrastrando y soltando tarjetas entre estados (`Borrador`, `Enviado`, `Recibido`).
- **Filtrado y Búsqueda:** Filtra la correspondencia por término de búsqueda y por rango de fechas.
- **Exportación de Datos:** Exporta tus registros a formatos CSV y SQL.
- **Interfaz Multilingüe:** Soporte para Inglés y Español.
- **Tema Claro y Oscuro:** Cambia entre modos de visualización para adaptarse a tus preferencias.
- **Diseño Responsivo:** Totalmente funcional en dispositivos de escritorio y móviles.
- **Backend Serverless:** Utiliza Firebase (Firestore) como base de datos en tiempo real.

## 🚀 Pila Tecnológica

- **Framework:** [Next.js](https://nextjs.org/) (con App Router y Server Actions)
- **Lenguaje:** [TypeScript](https://www.typescriptlang.org/)
- **UI:** [React](https://reactjs.org/)
- **Componentes UI:** [Shadcn/ui](https://ui.shadcn.com/)
- **Estilos:** [Tailwind CSS](https://tailwindcss.com/)
- **Base de Datos:** [Firebase Firestore](https://firebase.google.com/docs/firestore)
- **Formularios:** [React Hook Form](https://react-hook-form.com/) y [Zod](https://zod.dev/) para validación.
- **Arrastrar y Soltar:** [React Beautiful DnD](https://github.com/atlassian/react-beautiful-dnd)
- **Iconos:** [Lucide React](https://lucide.dev/)

## 🛠️ Cómo Empezar

Sigue estos pasos para levantar el proyecto en tu entorno local.

### Prerrequisitos

- [Node.js](https://nodejs.org/en/) (versión 18.x o superior)
- [npm](https://www.npmjs.com/) o [yarn](https://yarnpkg.com/)

### 1. Configuración de Firebase

1.  Ve a la [Consola de Firebase](https://console.firebase.google.com/).
2.  Crea un nuevo proyecto.
3.  Crea una nueva aplicación web y copia las credenciales de configuración.
4.  Ve a **Firestore Database** y crea una base de datos. Comienza en modo de producción.
5.  En la pestaña **Reglas** de Firestore, actualiza las reglas para permitir lecturas y escrituras (para desarrollo):
    ```
    rules_version = '2';
    service cloud.firestore {
      match /databases/{database}/documents {
        match /{document=**} {
          allow read, write: if true; // ¡CUIDADO! Solo para desarrollo.
        }
      }
    }
    ```
6.  Crea una colección llamada `correspondence`.

### 2. Instalación Local

1.  Clona el repositorio:
    ```bash
    git clone https://github.com/tu-usuario/teckflow.git
    cd teckflow
    ```

2.  Crea un archivo `.env.local` en la raíz del proyecto y añade las credenciales de Firebase que copiaste:
    ```env
    NEXT_PUBLIC_FIREBASE_API_KEY=AIza...
    NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=...
    NEXT_PUBLIC_FIREBASE_PROJECT_ID=...
    NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=...
    NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=...
    NEXT_PUBLIC_FIREBASE_APP_ID=...
    ```

3.  Instala las dependencias:
    ```bash
    npm install
    ```

4.  Ejecuta el servidor de desarrollo:
    ```bash
    npm run dev
    ```

¡Abre [http://localhost:3000](http://localhost:3000) en tu navegador para ver la aplicación en funcionamiento!

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Si deseas mejorar el proyecto, por favor haz un fork del repositorio y crea un Pull Request.

## 📄 Licencia

Este proyecto está bajo la Licencia MIT.
