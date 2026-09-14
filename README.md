

```markdown
# 🎭 Playwright Automation Framework — POM & CI/CD

![Playwright Tests](https://github.com/AaronGalar/playwright-qa-portfolio/actions/workflows/playwright.yml/badge.svg)
![Playwright](https://img.shields.io/badge/Playwright-v1.40+-green?logo=playwright)
![NodeJS](https://img.shields.io/badge/Node.js-LTS-339933?logo=node.js)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript)

Framework de automatización de pruebas E2E desarrollado con **Playwright** y **JavaScript**, aplicando el patrón de diseño **Page Object Model (POM)** y ejecución continua en la nube mediante **GitHub Actions**.

---

## 🎯 Objetivo del Proyecto
Demostrar la implementación de una arquitectura de automatización de pruebas escalable, mantenible y robusta sobre flujos críticos de negocio de una aplicación web (Autenticación, Manejo de Sesiones, Validaciones UI y Control de Excepciones).

---

## 📋 Escenarios de Prueba Cubiertos
| ID | Módulo | Escenario / Caso de Prueba | Tipo de Validación | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- |
| **TC-01** | Auth | Login exitoso con credenciales válidas | Happy Path / Redirección | Redirección a `/inventory.html` |
| **TC-02** | Auth | Intento de Login con usuario bloqueado | Boundary / Error Handling | Visualización del mensaje de error de bloqueo |

---

## 🛠️ Tech Stack & Herramientas
* **Automation Engine:** Playwright
* **Lenguaje:** JavaScript (Node.js)
* **Design Pattern:** Page Object Model (POM)
* **CI/CD Pipeline:** GitHub Actions
* **Reporting & Evidence:** Playwright HTML Reporter / HTML Artifacts

---

## 📁 Estructura del Proyecto
```text
playwright-qa-portfolio/
├── pages/                  # Encapsulación de selectores y acciones (Page Objects)
│   └── LoginPage.js
├── tests/                  # Test Suites y escenarios de prueba
│   └── authAndCheckout.spec.js
├── .github/workflows/      # Pipeline CI/CD automatizado
│   └── playwright.yml
├── playwright.config.js    # Configuración global del runner
└── package.json            # Gestión de dependencias

```

---

## ⚙️ Guía Paso a Paso: Instalación y Configuración Inicial

Si deseas recrear este proyecto o ejecutarlo desde cero en tu máquina local, sigue estos pasos:

### 1. Requisitos Previos

* Tener instalado **Node.js** (versión 18 o superior). Puedes verificarlo en tu terminal con:
```bash
node -v

```



### 2. Inicialización del Proyecto

1. Crea una carpeta local y navega hasta ella:
```bash
mkdir playwright-qa-portfolio
cd playwright-qa-portfolio

```


2. Inicializa el proyecto de Node.js:
```bash
npm init -y

```


3. Instala Playwright y sus navegadores oficiales:
```bash
npm install -D @playwright/test
npx playwright install

```



---

## 🚀 Cómo ejecutar las pruebas localmente

1. **Clonar el repositorio existente:**
```bash
git clone https://github.com/AaronGalar/playwright-qa-portfolio.git
cd playwright-qa-portfolio

```


2. **Instalar dependencias necesarias:**
```bash
npm install
npx playwright install

```


3. **Ejecutar la suite de pruebas (Modo Headless por consola):**
```bash
npx playwright test

```


4. **Ejecutar con interfaz visual (Modo Headed):**
```bash
npx playwright test --headed

```


5. **Generar y abrir el reporte interactivo en el navegador:**
```bash
npx playwright test --reporter=html
npx playwright show-report

```



---

## 🔄 Integración Continua (CI/CD)

Este proyecto cuenta con un workflow en **GitHub Actions** (`.github/workflows/playwright.yml`) que se desencadena automáticamente tras cada `push` o `pull_request` a la rama `main`:

* Instala las dependencias y binarios de los navegadores.
* Ejecutar los tests en entorno aislado Linux (Ubuntu).
* Genera y almacena los reportes y evidencias como artefactos descargables en la pestaña **Actions**.

```

---

### Pasos para actualizarlo en tu terminal:

1. Reemplaza todo el contenido de tu archivo local `README.md` por el código de arriba.
2. Guarda el archivo (`Ctrl + S`).
3. Ejecuta estos tres comandos en la terminal para subirlo:

```powershell
git add README.md
git commit -m "docs: add step-by-step setup and installation guide"
git push

```
