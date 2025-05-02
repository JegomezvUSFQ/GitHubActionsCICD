## Proyecto CI/CD con GitHub Actions

Este proyecto es una aplicación básica en Node.js que muestra cómo implementar un flujo de trabajo de CI/CD usando GitHub Actions.

---

## Tecnologías utilizadas

- Node.js  
- Express.js  
- GitHub Actions  
- Servidor Ubuntu 22.04  
- SSH + PM2  

---

## ¿Qué hace este proyecto?

Cada vez que se hace un `git push` a la rama `main`, GitHub Actions:

1. Se activa automáticamente.
2. Se conecta por SSH al servidor Ubuntu 22.04.
3. Ejecuta `git pull`, instala dependencias y reinicia la aplicación con PM2.

Este flujo automatizado permite desplegar cambios de forma continua y segura en producción.

---

## Estructura del repositorio

GitHubActionsCICD/
├── app.js
├── package.json
├── .gitignore
├── README.md
└── .github/
└── workflows/
└── deploy.yml

---

## Cómo probarlo localmente

1. Instala las dependencias:
```bash
npm install

2. Ejecuta la aplicación:
node app.js

3. Abre el navegador:
http://localhost:3000
Se deberia ver: ¡Hola desde GitHub Actions!