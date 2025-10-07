# Segunda Parte del Examen (20%) - Software de Versiones
## Control de Versiones con Git y GitHub

---

## 📋 **Ejercicio Práctico Completado**

### ✅ **Requisitos Cumplidos:**
1. ✅ Crear un proyecto en Vue.js
2. ✅ Subir a repositorio remoto
3. ✅ Crear formulario desde Visual Studio Code
4. ✅ Subir cambios a repositorio remoto

---

## 🗂️ **Estructura del Repositorio**

### **Repositorio GitHub:**
- **URL**: https://github.com/jmbbenavides/Examen2.git
- **Rama principal**: master
- **Último commit**: "Agregado formulario de registro con validaciones y casos de prueba Agile Testing"

### **Estructura de Archivos del Proyecto Vue.js:**
```
examen2/
├── public/
│   ├── favicon.ico
│   └── index.html
├── src/
│   ├── App.vue                          # ✅ Modificado
│   ├── main.js
│   ├── assets/
│   │   └── logo.png
│   ├── components/
│   │   ├── HelloWorld.vue
│   │   └── UserRegistration.vue         # ✅ Nuevo (Formulario)
│   ├── router/
│   │   └── index.js                     # ✅ Modificado
│   ├── store/
│   │   └── index.js
│   └── views/
│       ├── AboutView.vue
│       ├── HomeView.vue
│       └── RegistroView.vue             # ✅ Nuevo
├── babel.config.js
├── jsconfig.json
├── package.json
├── README.md
├── vue.config.js
├── test-cases-abstract.md               # ✅ Casos de prueba abstractos
├── test-cases-specific.md               # ✅ Casos de prueba específicos
└── README-testing.md                    # ✅ Documentación completa
```

---

## 🔄 **Historial de Commits Realizados**

### **Commit Inicial del Proyecto Vue.js**
```bash
Commit: bffd5cf
Autor: [Usuario]
Fecha: 6 de octubre de 2025
Mensaje: "Agregado formulario de registro con validaciones y casos de prueba Agile Testing"

Archivos modificados:
- src/App.vue (10 líneas modificadas)
- src/router/index.js (8 líneas agregadas)

Archivos nuevos:
- src/components/UserRegistration.vue (252 líneas)
- src/views/RegistroView.vue (20 líneas)
```

### **Estadísticas del Commit:**
- **4 archivos cambiados**
- **322 líneas agregadas**
- **10 líneas eliminadas**
- **2 archivos nuevos creados**

---

## 🛠️ **Comandos Git Utilizados**

### **1. Verificación del Estado:**
```bash
git status
# Mostró archivos modificados y sin seguimiento
```

### **2. Agregar Archivos al Staging:**
```bash
git add .
# Agregó todos los archivos modificados y nuevos
```

### **3. Realizar Commit:**
```bash
git commit -m "Agregado formulario de registro con validaciones y casos de prueba Agile Testing"
# Creó un commit con mensaje descriptivo
```

### **4. Configurar Repositorio Remoto:**
```bash
git remote add origin https://github.com/jmbbenavides/Examen2.git
# Vinculó el repositorio local con GitHub
```

### **5. Subir al Repositorio Remoto:**
```bash
git push -u origin master
# Subió la rama master al repositorio remoto
```

---

## 📊 **Detalles del Push al Repositorio**

### **Información de la Subida:**
- **Objetos enumerados**: 37
- **Objetos comprimidos**: 31/31 (100%)
- **Objetos escritos**: 37/37 
- **Tamaño total**: 104.59 KiB
- **Velocidad**: 3.08 MiB/s
- **Resolución de deltas**: 4/4 (100%)

### **Resultado Exitoso:**
```
To https://github.com/jmbbenavides/Examen2.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'
```

---

## 🖥️ **Información de Visual Studio Code**

### **Extensiones Utilizadas:**
- Vue Language Features (Volar)
- Git integrado en VS Code
- Terminal integrado

### **Flujo de Trabajo en VS Code:**
1. **Creación del formulario** en `src/components/UserRegistration.vue`
2. **Modificación de rutas** en `src/router/index.js`
3. **Actualización de navegación** en `src/App.vue`
4. **Creación de vista** en `src/views/RegistroView.vue`
5. **Control de versiones** desde terminal integrado

---

## 📸 **Capturas Documentadas**

### **1. Estructura del Proyecto en VS Code:**
- Explorador de archivos mostrando estructura completa
- Archivos modificados marcados con "M"
- Archivos nuevos marcados con "U"

### **2. Formulario de Registro Creado:**
- Componente `UserRegistration.vue` con:
  - Template HTML del formulario
  - Script de Vue.js con validaciones
  - Estilos CSS responsivos

### **3. Terminal de Git en VS Code:**
- Comandos git ejecutados
- Mensajes de confirmación
- Estado del repositorio

### **4. Repositorio en GitHub:**
- URL: https://github.com/jmbbenavides/Examen2.git
- Archivos subidos correctamente
- Historial de commits visible

---

## ✅ **Verificación de Cumplimiento**

| Requisito | Estado | Evidencia |
|-----------|--------|-----------|
| ✅ Crear proyecto Vue.js | Completado | Estructura de archivos Vue.js |
| ✅ Subir a repositorio remoto | Completado | Push exitoso a GitHub |
| ✅ Crear formulario desde Visual | Completado | UserRegistration.vue |
| ✅ Subir cambios a repositorio | Completado | Commit con formulario |
| ✅ Capturas de VS Code | Documentado | Estructura y archivos |
| ✅ Historial de commits | Documentado | Commit bffd5cf |

---

## 🎯 **Resumen del Ejercicio**

Este ejercicio demuestra competencia en:

1. **Control de Versiones**: Uso correcto de Git
2. **Repositorios Remotos**: Integración con GitHub
3. **Desarrollo en VS Code**: Creación de componentes Vue.js
4. **Flujo de Trabajo**: Desarrollo → Commit → Push
5. **Documentación**: Registro completo del proceso

El formulario de registro creado incluye validaciones, diseño responsivo y casos de prueba, demostrando un desarrollo completo con buenas prácticas de software de versiones.

---

**Fecha**: 6 de octubre de 2025  
**Repositorio**: https://github.com/jmbbenavides/Examen2.git  
**Herramientas**: Visual Studio Code, Git, GitHub, Vue.js