# 🎬 Proyecto CINE2025

Este proyecto despliega una aplicación web de venta de entradas de cine utilizando **Nginx** en un contenedor **Docker**.  

El flujo consiste en preparar los archivos HTML/CSS/JS, reemplazar el `index.html` por el de la aplicación y luego copiarlos dentro del contenedor.

---


### 1. Copia de los archivos desde el host al contenedor
Luego se copiaron los archivos del proyecto (`CINE2025`) desde Windows al contenedor de Docker en la ruta `/usr/share/nginx/html/`.

![Docker Copy](docs/img/screenshot_1.png)

---

## ⚡ Pasos principales

### 2. Listado de archivos y reemplazo de `index.html`
Primero listamos el contenido de `/usr/share/nginx/html/`.  
Se eliminó el `index.html` por defecto y se reemplazó por el archivo `ventaentradas.html` para que sea la página principal.

![Reemplazo index.html](docs/img/screenshot_2.png)

---


## 🚀 Comandos útiles

- **Eliminar el index por defecto**:
  ```bash
  rm index.html
  ```

- **Renombrar tu archivo principal como index**:
  ```bash
  mv ventaentradas.html index.html
  ```

- **Copiar todo el proyecto desde el host al contenedor**:
  ```powershell
  docker cp "C:\Users\juann\Documents\CINE2025\." affectionate_brattain:/usr/share/nginx/html/
  ```

---

## 🖥️ Acceso al sitio
Una vez que los archivos están en el contenedor, puedes abrir tu navegador en:

```
http://localhost
```

Ahí verás desplegada tu web de **venta de entradas** 🎟️🍿.

---

## 📂 Estructura del proyecto
```
CINE2025/
├── index.html
├── ventaentradas.css
├── ventaEntradas.js
├── ticket.html
├── ticket.css
├── 50x.html
├── img/
└── fonts/
```

---

## ✨ Resultado
Con este proceso ya tienes tu aplicación funcionando en Nginx dentro de Docker, lista para pruebas o despliegue real. 🚀
