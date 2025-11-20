# 🎨 Task Manager Pro - Frontend

## 📋 Descripción

Aplicación web moderna y responsive para gestión de tareas, desarrollada con **HTML5**, **CSS3** y **JavaScript Vanilla**. Interfaz intuitiva y elegante que se comunica con una API RESTful backend, ofreciendo una experiencia de usuario fluida y profesional sin frameworks pesados.

## ✨ Características Principales

### Funcionalidades de Usuario
- ✅ **Creación Rápida de Tareas**: Formulario intuitivo con validación en tiempo real
- 📝 **Edición Inline**: Modal responsive para editar tareas existentes
- 🔍 **Búsqueda Instantánea**: Búsqueda en tiempo real por título y descripción
- 🎯 **Filtros Avanzados**: Filtrado por estado (Pending, In Progress, Completed, Cancelled)
- 📊 **Dashboard de Estadísticas**: 5 tarjetas con métricas en tiempo real
- 🏷️ **Sistema de Etiquetas**: Organización visual mediante tags coloridos
- ⏰ **Fechas de Vencimiento**: Visualización de deadlines
- 🎨 **4 Niveles de Prioridad**: Codificación visual con colores y emojis

### Características Técnicas
- 🚀 **SPA (Single Page Application)**: Sin recargas de página
- 🔄 **Actualizaciones en Tiempo Real**: Sincronización automática con backend
- 💾 **Gestión de Estado**: Estado local sincronizado con API
- 🔐 **Manejo de Sesiones**: Cookies HTTP-only automáticas
- ⚡ **Optimización de Performance**: Debouncing en búsquedas
- 📱 **100% Responsive**: Diseño adaptable a móviles, tablets y desktop
- 🎭 **Animaciones Suaves**: Transiciones CSS3 profesionales
- 🔔 **Sistema de Notificaciones**: Toasts informativos y atractivos

### UX/UI Features
- 🌈 **Diseño Moderno**: Gradientes vibrantes y colores profesionales
- 🎯 **Feedback Visual**: Estados hover, focus y active en todos los elementos
- ⌨️ **Accesibilidad**: Navegación por teclado y labels semánticos
- 🎨 **Código de Colores**: Distinción visual de estados y prioridades
- 📦 **Cards Interactivas**: Hover effects y animaciones de transformación
- 🔄 **Loading States**: Spinners y overlays durante operaciones asíncronas

## 🛠️ Tecnologías Utilizadas

```
HTML5                 # Estructura semántica moderna
CSS3                  # Estilos avanzados (Grid, Flexbox, Animations)
JavaScript ES6+       # Lógica de aplicación (Async/Await, Fetch API)

# No Dependencies      # 100% Vanilla JavaScript
# No Build Process     # Listo para usar sin compilación
# No Frameworks        # Ligero y rápido
```

## 📁 Estructura del Proyecto

```
Frontend/
├── index.html              # Estructura HTML principal
├── styles/
│   └── main.css           # Estilos CSS (incluidos en HTML)
├── scripts/
│   └── app.js             # Lógica JavaScript (incluida en HTML)
├── assets/
│   ├── images/            # Imágenes y recursos
│   └── fonts/             # Fuentes personalizadas (opcional)
├── .gitignore
├── README.md              # Este archivo
└── vercel.json           # Configuración para Vercel
```

## 🚀 Instalación y Configuración

### Prerrequisitos
```
- Navegador web moderno (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+)
- Conexión a internet (para comunicación con API)
- Editor de código (VS Code recomendado)
```

### Instalación Local

#### Opción 1: Servidor Local Simple
```bash
# Clonar repositorio
git clone https://github.com/Erickpe8/Proyecto-caso-testigo-Perez-Carvajal-Frontend.git
cd Proyecto-caso-testigo-Perez-Carvajal-Frontend

# Opción A: Python
python -m http.server 8080
# Abrir: http://localhost:8080

# Opción B: Node.js
npx http-server -p 8080
# Abrir: http://localhost:8080

# Opción C: PHP
php -S localhost:8080
# Abrir: http://localhost:8080
```

#### Opción 2: VS Code Live Server
```bash
1. Instalar extensión "Live Server" en VS Code
2. Click derecho en index.html
3. Seleccionar "Open with Live Server"
4. Abre automáticamente en: http://127.0.0.1:5500
```

#### Opción 3: Abrir Directamente
```bash
# Simplemente abre index.html en tu navegador
# Nota: CORS puede causar problemas, usar servidor local es recomendado
```

### Configuración de API

Editar la URL del backend en `index.html`:

```javascript
// Buscar esta línea en el <script>
const API_BASE_URL = 'http://localhost:8000';

// Cambiar a tu URL de producción
const API_BASE_URL = 'https://tu-api.onrender.com';
```

## 🎨 Guía de Uso

### Interfaz Principal

#### 1. Header con Estado de Conexión
- **Indicador Visual**: Muestra si está conectado al backend
- **Estados**:
  - 🟢 Verde: Conectado
  - 🔴 Rojo: Desconectado
  - 🟡 Amarillo: Verificando

#### 2. Dashboard de Estadísticas
Cinco tarjetas interactivas con métricas:
- **Total Tareas**: Suma de todas las tareas
- **Pendientes**: Tareas sin iniciar
- **En Progreso**: Tareas en desarrollo
- **Completadas**: Tareas finalizadas
- **Canceladas**: Tareas descartadas

#### 3. Panel de Creación de Tareas
Formulario lateral con campos:
- **Título**: Mínimo 3 caracteres (requerido)
- **Descripción**: Máximo 1000 caracteres (opcional)
- **Prioridad**: 4 niveles con emojis
- **Etiquetas**: Separadas por comas
- **Fecha de Vencimiento**: Selector de fecha

**Validaciones en Tiempo Real**:
- ❌ Título muy corto → Error visual
- ❌ Descripción muy larga → Error visual
- ✅ Validación al escribir

#### 4. Panel de Lista de Tareas
- **Búsqueda**: Filtro instantáneo por texto
- **Filtro de Estado**: Dropdown para filtrar por estado
- **Cards de Tareas**: Información completa y visualmente organizada

Cada tarjeta muestra:
- Título en negrita
- Descripción (si existe)
- Badge de estado (colorizado)
- Badge de prioridad (con emoji)
- Tags personalizados
- Fecha de creación
- Botones de acción

#### 5. Acciones por Tarea
- **✏️ Editar**: Abre modal de edición
- **✅ Completar**: Marca como completada (si está pendiente/en progreso)
- **🗑️ Eliminar**: Elimina la tarea con confirmación

### Operaciones Principales

#### Crear una Tarea
1. Llenar formulario del panel izquierdo
2. Click en "Crear Tarea"
3. Toast de confirmación aparece
4. Tarea aparece automáticamente en la lista
5. Estadísticas se actualizan

#### Editar una Tarea
1. Click en botón "✏️ Editar" en cualquier tarea
2. Se abre modal con datos pre-cargados
3. Modificar campos deseados
4. Click en "Guardar Cambios"
5. Modal se cierra y lista se actualiza

#### Buscar Tareas
1. Escribir en barra de búsqueda
2. Resultados filtran automáticamente
3. Búsqueda en título y descripción

#### Filtrar por Estado
1. Seleccionar estado en dropdown
2. Lista se filtra instantáneamente
3. "Todos los estados" muestra todas

#### Completar Tarea Rápida
1. Click en "✅ Completar"
2. Estado cambia a COMPLETED
3. Visual feedback inmediato

#### Eliminar Tarea
1. Click en "🗑️ Eliminar"
2. Confirmación del navegador
3. Tarea se elimina si se confirma

## 🎨 Sistema de Colores

### Paleta Principal
```css
--primary: #6366f1      /* Índigo principal */
--primary-dark: #4f46e5 /* Índigo oscuro */
--secondary: #8b5cf6    /* Púrpura */
--success: #10b981      /* Verde éxito */
--warning: #f59e0b      /* Ámbar advertencia */
--danger: #ef4444       /* Rojo peligro */
--dark: #1f2937         /* Gris oscuro texto */
--light: #f9fafb        /* Gris claro fondo */
```

### Estados de Tarea
- **Pendiente**: 🟡 Amarillo (`#f59e0b`)
- **En Progreso**: 🔵 Azul (`#3b82f6`)
- **Completada**: 🟢 Verde (`#10b981`)
- **Cancelada**: 🔴 Rojo (`#ef4444`)

### Prioridades
- **Baja**: 🟢 (`#e0e7ff`)
- **Media**: 🟡 (`#dbeafe`)
- **Alta**: 🟠 (`#fed7aa`)
- **Urgente**: 🔴 (`#fecaca`)

## 📱 Responsive Design

### Breakpoints
```css
Desktop:  > 1024px    /* 3 columnas en stats, layout 2 columnas */
Tablet:   768-1023px  /* 2 columnas en stats, layout 1 columna */
Mobile:   < 767px     /* 2 columnas en stats, todo apilado */
```

### Adaptaciones Móviles
- Formulario de creación no sticky en móvil
- Header con elementos apilados
- Stats en grid 2x2 en móvil
- Búsqueda y filtro en columna
- Cards de tareas con padding reducido
- Modal a 90% de ancho

## 🔄 Flujo de Datos

### Arquitectura de Comunicación

```
┌─────────────┐         ┌──────────────┐         ┌─────────────┐
│   Usuario   │────────▶│   Frontend   │────────▶│   Backend   │
│  (Browser)  │         │  (HTML/JS)   │  HTTP   │  (FastAPI)  │
└─────────────┘         └──────────────┘         └─────────────┘
      │                        │                         │
      │   Toast/Visual         │  JSON Response          │
      │◀───────────────────────┤◀────────────────────────┤
      │                        │                         │
      │   Updated UI           │  Update Local State     │
      └────────────────────────┘                         │
```

### Ciclo de Vida de una Operación

1. **Acción del Usuario** → Click en botón
2. **Validación Frontend** → Verificar datos antes de enviar
3. **Mostrar Loading** → Feedback visual inmediato
4. **Request a API** → `fetch()` con credenciales
5. **Recibir Response** → Parsear JSON
6. **Actualizar Estado** → Modificar `currentTasks[]`
7. **Renderizar UI** → Redibujar lista
8. **Actualizar Stats** → Llamar `/tasks/stats`
9. **Mostrar Toast** → Notificación de éxito/error
10. **Ocultar Loading** → Remover overlay

## ⚡ Optimizaciones de Performance

### Técnicas Implementadas

#### Debouncing en Búsqueda
```javascript
let searchTimeout;
searchInput.addEventListener('input', (e) => {
    clearTimeout(searchTimeout);
    searchTimeout = setTimeout(() => {
        filterTasks();
    }, 300); // 300ms de espera
});
```

#### Renderizado Eficiente
- Solo re-renderizar cuando cambian datos
- Usar `innerHTML` una sola vez por operación
- Evitar reflow innecesarios

#### Gestión de Memoria
- Limpiar event listeners al destruir elementos
- No mantener referencias innecesarias
- Usar event delegation cuando sea posible

#### Cache de Elementos DOM
```javascript
const elements = {
    tasksList: document.getElementById('tasksList'),
    searchInput: document.getElementById('searchInput'),
    // ... más elementos
};
```

## 🧪 Testing Manual

### Checklist de Pruebas

#### Funcionalidad Básica
- [ ] Health check muestra estado conectado
- [ ] Crear tarea con datos válidos
- [ ] Crear tarea muestra en lista
- [ ] Estadísticas se actualizan al crear
- [ ] Editar tarea abre modal correctamente
- [ ] Cambios en edición se guardan
- [ ] Eliminar tarea funciona
- [ ] Estadísticas se actualizan al eliminar

#### Validaciones
- [ ] Título < 3 caracteres muestra error
- [ ] Título > 200 caracteres muestra error
- [ ] Descripción > 1000 caracteres muestra error
- [ ] Formulario no se envía con errores
- [ ] Validación en tiempo real funciona

#### Búsqueda y Filtros
- [ ] Búsqueda por título funciona
- [ ] Búsqueda por descripción funciona
- [ ] Búsqueda es case-insensitive
- [ ] Filtro por PENDING funciona
- [ ] Filtro por IN_PROGRESS funciona
- [ ] Filtro por COMPLETED funciona
- [ ] Filtro por CANCELLED funciona
- [ ] "Todos los estados" muestra todas

#### UI/UX
- [ ] Toasts aparecen correctamente
- [ ] Loading overlay muestra durante operaciones
- [ ] Hover effects funcionan
- [ ] Animaciones son suaves
- [ ] Colores son consistentes
- [ ] Responsive funciona en móvil
- [ ] Responsive funciona en tablet

#### Casos Edge
- [ ] API desconectada muestra error
- [ ] Lista vacía muestra "empty state"
- [ ] Búsqueda sin resultados muestra mensaje
- [ ] Caracteres especiales en título
- [ ] Múltiples etiquetas se muestran bien
- [ ] Fecha de vencimiento se formatea bien

### Testing en Diferentes Navegadores

| Navegador | Versión Mínima | Estado |
|-----------|---------------|---------|
| Chrome    | 90+           | ✅ OK   |
| Firefox   | 88+           | ✅ OK   |
| Safari    | 14+           | ✅ OK   |
| Edge      | 90+           | ✅ OK   |
| Opera     | 76+           | ✅ OK   |

## 🌐 Despliegue en Vercel

### Configuración de Vercel

#### 1. Preparar Proyecto

Crear archivo `vercel.json` en raíz:
```json
{
  "version": 2,
  "builds": [
    {
      "src": "index.html",
      "use": "@vercel/static"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "/index.html"
    }
  ]
}
```

#### 2. Desplegar desde GitHub

**Opción A: Vercel CLI**
```bash
# Instalar Vercel CLI
npm install -g vercel

# Login
vercel login

# Desplegar
vercel

# Producción
vercel --prod
```

**Opción B: Vercel Dashboard**
1. Ir a https://vercel.com
2. Click en "Import Project"
3. Conectar GitHub repository
4. Seleccionar proyecto frontend
5. Configurar:
   - Framework Preset: `Other`
   - Root Directory: `./`
   - Build Command: (dejar vacío)
   - Output Directory: `./`
6. Click en "Deploy"

#### 3. Variables de Entorno

En Vercel Dashboard → Settings → Environment Variables:

```bash
# Agregar si necesario
API_BASE_URL=https://tu-api.onrender.com
NODE_ENV=production
```

#### 4. Configuración de Dominio

Vercel te asigna automáticamente:
```
https://task-manager-pro.vercel.app
```

**Dominio Personalizado**:
1. Settings → Domains
2. Add Domain
3. Seguir instrucciones DNS

### URL de Producción
```
https://task-manager-pro-tu-usuario.vercel.app
```

### Actualizar URL de API

Editar en `index.html`:
```javascript
// Cambiar de localhost a producción
const API_BASE_URL = 'https://task-management-api.onrender.com';
```

### Verificar Despliegue
```bash
curl https://task-manager-pro.vercel.app
```

### Configuraciones Avanzadas

#### Redirects y Rewrites
```json
{
  "redirects": [
    {
      "source": "/old-path",
      "destination": "/new-path",
      "permanent": true
    }
  ]
}
```

#### Headers de Seguridad
```json
{
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        },
        {
          "key": "X-Frame-Options",
          "value": "DENY"
        }
      ]
    }
  ]
}
```

## 🔧 Personalización

### Cambiar Colores
Editar variables CSS en `<style>`:
```css
:root {
    --primary: #tu-color-primario;
    --success: #tu-color-exito;
    /* ... más variables */
}
```

### Cambiar Logo/Título
```html
<div class="header">
    <h1>Tu Título Personalizado</h1>
    <!-- ... -->
</div>
```

### Agregar Campos Personalizados
1. Agregar input en formulario
2. Recoger valor en `createTask()`
3. Enviar a API
4. Mostrar en `renderTasks()`

## 🐛 Troubleshooting

### Error: CORS Policy
**Problema**: `Access to fetch blocked by CORS policy`

**Solución**:
```javascript
// Verificar que backend tenga CORS habilitado
// Verificar que credentials: 'include' esté presente
```

### Error: Network Request Failed
**Problema**: No se puede conectar a API

**Soluciones**:
1. Verificar URL de API es correcta
2. Verificar que backend esté corriendo
3. Verificar firewall/antivirus
4. Probar con `curl` la API directamente

### Tareas No Aparecen
**Problema**: Lista vacía después de crear

**Soluciones**:
1. Abrir DevTools → Console buscar errores
2. Verificar que `loadTasks()` se llame después de crear
3. Verificar que response de API sea correcta
4. Verificar cookies en DevTools → Application

### Estilos Rotos en Móvil
**Problema**: Diseño roto en dispositivos pequeños

**Solución**:
```html
<!-- Verificar que esté presente -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Validaciones No Funcionan
**Problema**: Formulario se envía con datos inválidos

**Solución**:
- Verificar event listeners estén vinculados
- Verificar que `validateForm()` retorne boolean
- Agregar `event.preventDefault()` en submit

## 📈 Roadmap Futuro

### Versión 2.0
- [ ] Migrar a React/Vue para mejor gestión de estado
- [ ] TypeScript para type safety
- [ ] Drag & Drop para reordenar tareas
- [ ] Modo oscuro / Temas personalizables
- [ ] Notificaciones Push
- [ ] Offline support con Service Workers
- [ ] Progressive Web App (PWA)
- [ ] Compartir tareas por link

### Versión 1.5 (Próxima)
- [ ] Subtareas anidadas
- [ ] Vista Kanban
- [ ] Vista Calendario
- [ ] Adjuntos de archivos
- [ ] Comentarios en tareas
- [ ] Colaboración en tiempo real
- [ ] Export a PDF/Excel
- [ ] Atajos de teclado

## 🎓 Aprendizajes y Mejores Prácticas

### Lo que Aprendimos
✅ JavaScript Vanilla es poderoso para SPAs pequeños
✅ CSS Grid + Flexbox permite layouts complejos
✅ Fetch API con async/await simplifica llamadas HTTP
✅ Validación en frontend mejora UX significativamente
✅ Feedback visual es crucial para operaciones asíncronas

### Mejores Prácticas Implementadas
✅ Separación de responsabilidades (API, UI, Validación)
✅ Manejo consistente de errores
✅ DRY (Don't Repeat Yourself) en funciones
✅ Nombres descriptivos de variables y funciones
✅ Comentarios donde la lógica es compleja
✅ Mobile-first responsive design

## 👥 Contribución

### Cómo Contribuir
1. Fork el proyecto desde [GitHub](https://github.com/Erickpe8/Proyecto-caso-testigo-Perez-Carvajal-Frontend)
2. Crear feature branch (`git checkout -b feature/NewFeature`)
3. Commit cambios (`git commit -m 'Add NewFeature'`)
4. Push a la rama (`git push origin feature/NewFeature`)
5. Abrir Pull Request

### Estándares de Código
- Usar camelCase para JavaScript
- Usar kebab-case para CSS classes
- Comentar funciones complejas
- Mantener funciones pequeñas y enfocadas
- Probar en múltiples navegadores antes de PR

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 👨‍💻 Autor

**Erick Pérez Carvajal**
- GitHub: [@Erickpe8](https://github.com/Erickpe8)
- Repositorio: [Frontend](https://github.com/Erickpe8/Proyecto-caso-testigo-Perez-Carvajal-Frontend)
- Backend: [API Repository](https://github.com/Erickpe8/Proyecto-caso-testigo-Perez-Carvajal-Backend)

## 📫 Conéctate conmigo

* **Correo electrónico**: ericksperezc@gmail.com
* **Instagram**: [@Erickperez_8](https://instagram.com/Erickperez_8)
* **YouTube**: [ErickPerez_8](https://youtube.com/@ErickPerez_8)

## 🙏 Agradecimientos

- Inspiración de diseño: Dribbble, Behance
- Iconos: Emojis nativos del navegador
- Comunidad de desarrollo web
- Vercel por hosting gratuito

## 📞 Soporte

¿Necesitas ayuda?
- 📧 Email: ericksperezc@gmail.com
- 📸 Instagram: [@Erickperez_8](https://instagram.com/Erickperez_8)
- 🎥 YouTube: [ErickPerez_8](https://youtube.com/@ErickPerez_8)
- 🐛 Issues: [GitHub Issues](https://github.com/Erickpe8/Proyecto-caso-testigo-Perez-Carvajal-Frontend/issues)

---

**⭐ Si te gustó este proyecto, regálale una estrella en GitHub ⭐**

Última actualización: Noviembre 2025
