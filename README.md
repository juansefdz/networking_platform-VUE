# networking_platform-VUE

# Proyecto Vue.js

Este proyecto es una aplicación construida con Vue.js que incluye funcionalidades para manejar conexiones y proyectos. Utiliza un enfoque modular con componentes para la interfaz de usuario y datos estáticos para demostrar las funcionalidades.

## Estructura del Proyecto

El proyecto está dividido en dos secciones principales: **Conexiones** y **Proyectos**. Cada sección tiene su propio conjunto de componentes y estilos.

### Conexiones

La sección de **Conexiones** muestra una lista de conexiones con información como avatar, nombre, rol, etiquetas, y estadísticas. Los componentes de esta sección permiten al usuario conectar o enviar mensajes a otros.

**Componentes:**
- `Connections.vue` - Componente principal para mostrar la lista de conexiones.

**Características:**
- **Avatares**: Imágenes de perfil para cada conexión.
- **Etiquetas**: Etiquetas asociadas a cada conexión.
- **Estadísticas**: Información sobre proyectos, tareas y conexiones.
- **Botones**: Botones para conectar o enviar un mensaje.

**Datos:**
- Los datos se cargan desde un archivo JSON estático (`connection.json`) ubicado en `@/assets/data/ConnectionZone/`.

### Proyectos

La sección de **Proyectos** muestra una lista de proyectos con información sobre el cliente, presupuesto, fechas, y progreso. Esta sección permite visualizar detalles del proyecto, como el porcentaje de progreso y el equipo involucrado.

**Componentes:**
- `Projects.vue` - Componente principal para mostrar la lista de proyectos.

**Características:**
- **Iconos de Proyecto**: Iconos representativos de cada proyecto.
- **Detalles del Proyecto**: Información sobre presupuesto, fechas de inicio y vencimiento.
- **Barra de Progreso**: Muestra el progreso del proyecto.
- **Miembros del Equipo**: Imágenes de los miembros del equipo involucrados en el proyecto.

**Datos:**
- Los datos se cargan desde un archivo JSON estático (`project.json`) ubicado en `@/assets/data/ProjectZone/`.

## Instalación

Para instalar y ejecutar este proyecto localmente, sigue estos pasos:

1. **Clonar el Repositorio**:
    ```bash
    git clone https://github.com/tu_usuario/tu_repositorio.git
    ```
2. Debes instalar vue CLI en tu maquina

 ```bash
    npm install -g @vue/cli
   ```
3. Una vez instalada Vue Cli podemos crear nuestro nuevo proyecto de VUE con el siguiente comando:

```bash
    npm create vue@latest
```
4. Instalar Dependencias:
  ```bash
    cd tu_repositorio
    npm install
  ```
5. Si quieres instalar el preprocesador SASS tienes que escribir en consola el siguiente comando:
 ```bash
    npm install -D sass sass-loader
```
6. **Iniciar el Servidor de Desarrollo**:
    ```bash
    npm run dev
    ```

7. Abrir en el Navegador:
    Abre tu navegador y navega a `http://localhost:5173/` para ver la aplicación en acción.


## Estructura del Proyecto

El proyecto sigue una estructura estándar de Vue.js:

- **`src/`**: Carpeta principal que contiene los archivos fuente.
  - **`assets/`**: Contiene los archivos estáticos como imágenes y datos JSON.
  - **`components/`**: Carpeta para los componentes Vue.js.
  - **`App.vue`**: Componente raíz de la aplicación.
  - **`main.js`**: Archivo de entrada que inicializa la aplicación.

- **`public/`**: Contiene el archivo `index.html` y otros recursos públicos.

---

¡Gracias por interesarte en este proyecto! Disfruta explorando y contribuyendo.
