# Guía Completa de Git y GitHub

Este repositorio contiene una guía ilustrada (con capturas de pantalla) para aprender los pasos básicos de Git y su integración con GitHub. Cada sección incluye explicaciones y referencias a imágenes (almacenadas en la carpeta `imagenes`), con la intención de cubrir por completo la estructura de la actividad propuesta.

## Tabla de Contenido
- [1. ¿Qué es Git y para qué sirve?](#1-¿qué-es-git-y-para-qué-sirve)
- [2. ¿Qué es GitHub y por qué usarlo?](#2-¿qué-es-github-y-por-qué-usarlo)
- [3. Creación de cuenta en GitHub](#3-creación-de-cuenta-en-github)
- [4. Instalación de Git](#4-instalación-de-git)
- [5. Configuración inicial de Git](#5-configuración-inicial-de-git)
- [6. Creación de un repositorio en GitHub](#6-creación-de-un-repositorio-en-github)
- [7. Apertura del proyecto en Visual Studio Code (opcional)](#7-apertura-del-proyecto-en-visual-studio-code-opcional)
- [8. Creación de un Repositorio Local](#8-creación-de-un-repositorio-local)
- [9. Creación y primer commit del `README.md`](#9-creación-y-primer-commit-del-readmemd)
- [10. Creación de la carpeta `imagenes` y adición de recursos](#10-creación-de-la-carpeta-imagenes-y-adición-de-recursos)
- [11. Trabajo con Ramas (Branching)](#11-trabajo-con-ramas-branching)
  - [11.1 Creación y cambio a una nueva rama](#111-creación-y-cambio-a-una-nueva-rama)
  - [11.2 Realizar cambios y confirmarlos](#112-realizar-cambios-y-confirmarlos)
  - [11.3 Fusión de ramas (Merge)](#113-fusión-de-ramas-merge)
- [12. Vincular el repositorio local con GitHub y hacer `push`](#12-vincular-el-repositorio-local-con-github-y-hacer-push)
- [13. Colaboración y Pull Requests](#13-colaboración-y-pull-requests)
  - [13.1 Fork de un repositorio existente](#131-fork-de-un-repositorio-existente)
  - [13.2 Clonar el repositorio forkeado](#132-clonar-el-repositorio-forkeado)
  - [13.3 Crear una rama, hacer cambios y abrir un Pull Request](#133-crear-una-rama-hacer-cambios-y-abrir-un-pull-request)
- [Contribuciones](#contribuciones)
- [Recursos Adicionales](#recursos-adicionales)
- [Licencia](#licencia)

---

## 1. ¿Qué es Git y para qué sirve?

**Git** es un sistema de control de versiones distribuido que permite a varios desarrolladores trabajar sobre un mismo proyecto sin pisarse los cambios. Con Git, puedes mantener un historial completo de modificaciones, volver a versiones anteriores y fusionar ramas de desarrollo de manera eficiente.

---

## 2. ¿Qué es GitHub y por qué usarlo?

**GitHub** es una plataforma online que aloja repositorios de Git. Ofrece herramientas de colaboración como Pull Requests, gestión de incidencias (Issues) y visibilidad pública o privada de tus proyectos. Es uno de los espacios más populares para compartir y colaborar en proyectos de software de todo tipo y tamaño.

---

## 3. Creación de cuenta en GitHub

1. Ingresa a [github.com](https://github.com/) y haz clic en **Sign up** (o **Regístrate**).  
   ![Creación de cuenta en GitHub](imagenes/1.jpg)

2. Completa el formulario con tus datos (nombre de usuario, correo electrónico y contraseña).  
   ![Formulario de registro](imagenes/2.jpg)

3. Verifica tu correo si así lo requiere GitHub.

4. Una vez creada tu cuenta, podrás iniciar sesión.  
   ![Pantalla final de registro](imagenes/3.jpg)

---

## 4. Instalación de Git

Con tu cuenta de GitHub lista, necesitas **Git** instalado en tu computadora:

- **Windows / macOS**:  
  Descarga el instalador desde [git-scm.com](https://git-scm.com/) y sigue las instrucciones.
- **Linux (Ubuntu)**:
  ```bash
  sudo apt update
  sudo apt install git
  ```

Para verificar la instalación, en la terminal ejecuta:
```bash
git --version
```
![Instalación de Git](imagenes/4.jpg)

---

## 5. Configuración inicial de Git

Para que Git asocie tus commits a tu identidad:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
```
Asegúrate de usar el mismo correo que registraste en GitHub.  
![Configuración inicial de Git](imagenes/8.png)

---

## 6. Creación de un repositorio en GitHub

1. Inicia sesión en GitHub y haz clic en el botón **New** (o **Nuevo repositorio**).  
   ![Crear repositorio desde GitHub](imagenes/5.png)

2. Asigna un nombre a tu repositorio, por ejemplo `Guia_Git_y_Github`, y elige si lo quieres **público** o **privado**.  
   ![Configurando el repositorio](imagenes/repositorio.jpg)

3. Haz clic en **Create repository**.  
   *(De momento, no agregues ningún README para practicar la subida desde local.)*

---

## 7. Apertura del proyecto en Visual Studio Code (opcional)

1. Ubica tu carpeta de proyecto y, en la barra de direcciones (Windows), escribe `cmd` para abrir la terminal.  
   ![Abrir cmd](imagenes/6.png)

2. Ejecuta:
   ```bash
   code .
   ```
   Esto abrirá VS Code en la carpeta actual.  
   ![Abrir Visual Studio Code](imagenes/7.png)

3. Revisa que aparezca la interfaz de VS Code con los archivos de tu carpeta.  
   ![Interfaz de Visual Studio Code](imagenes/9.png)

---

## 8. Creación de un Repositorio Local

1. Elige o crea una carpeta donde estará tu proyecto.
2. Abre la terminal en esa carpeta y ejecuta:
   ```bash
   git init
   ```
   Esto creará la carpeta oculta `.git`, donde Git almacenará todo el historial de versiones.

---

## 9. Creación y primer commit del `README.md`

1. Crea un archivo `README.md` con la descripción o propósito de tu proyecto.  
2. Agrega y confirma los cambios:
   ```bash
   git add README.md
   git commit -m "Primer commit: agrega README"
   ```
   ![Primer commit del README](imagenes/10.png)

---

## 10. Creación de la carpeta `imagenes` y adición de recursos

Para mantener capturas de pantalla u otros recursos gráficos:

1. Crea la carpeta:
   ```bash
   mkdir imagenes
   ```
   ![Carpeta de imágenes en el repositorio](imagenes/11.png)

2. Añade la carpeta y sus contenidos a Git:
   ```bash
   git add imagenes
   git commit -m "Agregar carpeta imagenes con capturas"
   ```
   ![Añadir imágenes al repositorio](imagenes/12.png)

---

## 11. Trabajo con Ramas (Branching)

### 11.1 Creación y cambio a una nueva rama
Para evitar romper la rama principal (`main`), se suele crear una rama para desarrollo:
```bash
git checkout -b desarrollo
```
Esto crea y cambia automáticamente a la nueva rama llamada `desarrollo`.

### 11.2 Realizar cambios y confirmarlos
1. Modifica el `README.md` o agrega nuevos archivos.  
2. Haz `git add .` para incluir todos los cambios en el área de preparación.  
3. Confirma:
   ```bash
   git commit -m "Cambios en la rama desarrollo"
   ```

### 11.3 Fusión de ramas (Merge)
1. Regresa a la rama principal:
   ```bash
   git checkout main
   ```
2. Fusiona la rama `desarrollo` en `main`:
   ```bash
   git merge desarrollo
   ```
3. Si no hay conflictos, se completará exitosamente la fusión.  
4. Para borrar la rama ya fusionada (opcional):
   ```bash
   git branch -d desarrollo
   ```

---

## 12. Vincular el repositorio local con GitHub y hacer `push`

1. En tu proyecto local, agrega la URL de tu nuevo repositorio remoto:
   ```bash
   git remote add origin https://github.com/TU_USUARIO/Guia_Git_y_Github.git
   ```
2. Empuja (push) los cambios de tu rama principal:
   ```bash
   git push -u origin main
   ```
3. Verifica en GitHub que se hayan subido correctamente los archivos y commits.

   ![Cambios en el repositorio local](imagenes/13.png)
   ![Cambios confirmados en GitHub](imagenes/14.png)

---

## 13. Colaboración y Pull Requests

Cuando se trabaja en equipo o se quiere contribuir a un proyecto ajeno, el flujo generalmente consiste en **Fork**, **clonación** y la creación de un **Pull Request** para proponer cambios.

### 13.1 Fork de un repositorio existente
1. En GitHub, visita el repositorio que deseas modificar.  
2. Haz clic en **Fork** para crear tu propia copia en tu cuenta.  
3. Esto genera un repositorio forkeado bajo tu usuario.

### 13.2 Clonar el repositorio forkeado
1. Desde tu repo forkeado, copia la URL (HTTPS o SSH).  
2. En tu local, ejecuta:
   ```bash
   git clone https://github.com/TU_USUARIO/repositorio-forkeado.git
   ```
3. Entra a la carpeta clonada con:
   ```bash
   cd repositorio-forkeado
   ```

### 13.3 Crear una rama, hacer cambios y abrir un Pull Request
1. Crea una rama:
   ```bash
   git checkout -b mi-rama-de-cambios
   ```
2. Realiza las modificaciones en el código o documentación.
3. Haz commit y push de la rama:
   ```bash
   git add .
   git commit -m "Añade o corrige algo"
   git push origin mi-rama-de-cambios
   ```
4. En GitHub, verás la opción de crear un **Pull Request** desde tu rama hacia la rama principal (por ejemplo, `main`) del repositorio original.
5. Espera a que el mantenedor revise e integre (mergee) tus cambios.

---

## Contribuciones

Si alguien desea contribuir a esta guía:
1. Hacer un **Fork** de este repositorio.  
2. Clonar el fork en su máquina local.  
3. Crear una rama nueva para sus cambios.  
4. Subir esa rama a su propio fork y abrir un **Pull Request** hacia este repositorio.

---

## Recursos Adicionales

- [Documentación oficial de Git](https://git-scm.com/doc)  
- [Guía de Git y GitHub para principiantes (freeCodeCamp, español)](https://www.freecodecamp.org/espanol/news/guia-para-principiantes-de-git-y-github/)

---
