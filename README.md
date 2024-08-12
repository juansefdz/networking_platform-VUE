# networking_platform-VUE

# Proyecto Vue.js

Este proyecto es una aplicación construida con Vue.js que incluye funcionalidades para manejar profile, team, project y connections. Utiliza un enfoque modular con componentes para la interfaz de usuario y datos estáticos para demostrar las funcionalidades, se realizó con el fin de estudiar VUE.

## Estructura del Proyecto

El proyecto está dividido en cuatro secciones principales: **Profile**,**Teams**,**Projects** y **Connections**. Cada sección tiene su propio conjunto de componentes y estilos.


**Datos:**
- Los datos se cargan desde un archivo JSON según la vista.



## Instalación

Para instalar y ejecutar este proyecto localmente, sigue estos pasos:

1. **Clonar el Repositorio**:
    ```bash
    git clone https://github.com/juansefdz/networking_platform-VUE.git
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
