# 🤝 Guía de Contribución

¡Gracias por tu interés en contribuir a **Clima por Ciudad**! Este documento te ayudará a entender cómo puedes participar en el desarrollo del proyecto.

## 📋 Tabla de Contenidos

- [Cómo Contribuir](#cómo-contribuir)
- [Configuración del Entorno](#configuración-del-entorno)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Convenciones de Código](#convenciones-de-código)
- [Proceso de Pull Request](#proceso-de-pull-request)
- [Reportar Bugs](#reportar-bugs)
- [Solicitar Features](#solicitar-features)

## 🚀 Cómo Contribuir

### Tipos de Contribuciones

Aceptamos diferentes tipos de contribuciones:

- 🐛 **Reportar Bugs**: Encuentra y reporta errores
- 💡 **Solicitar Features**: Sugiere nuevas funcionalidades
- 📝 **Mejorar Documentación**: Ayuda a mejorar la documentación
- 🎨 **Mejorar UI/UX**: Sugiere mejoras en la interfaz
- 🔧 **Optimizaciones**: Mejora el rendimiento del código
- 🌐 **Traducciones**: Agrega soporte para nuevos idiomas

## ⚙️ Configuración del Entorno

### Prerrequisitos

- Git
- Navegador web moderno
- Editor de código (VS Code recomendado)
- API Key de WeatherAPI.com (gratuita)

### Pasos de Configuración

1. **Fork el repositorio**
   ```bash
   # Ve a https://github.com/Xangel0s/Climate-by-city
   # Haz clic en "Fork" en la esquina superior derecha
   ```

2. **Clona tu fork**
   ```bash
   git clone https://github.com/TU_USUARIO/Climate-by-city.git
   cd Climate-by-city
   ```

3. **Configura el upstream**
   ```bash
   git remote add upstream https://github.com/Xangel0s/Climate-by-city.git
   ```

4. **Obtén una API Key**
   - Regístrate en [WeatherAPI.com](https://www.weatherapi.com/)
   - Obtén tu API key gratuita
   - Reemplaza la API key en `index.html` línea ~1000

5. **Prueba la aplicación**
   ```bash
   # Abre index.html en tu navegador
   # O usa un servidor local
   python -m http.server 8000
   ```

## 📁 Estructura del Proyecto

```
Climate-by-city/
├── index.html          # Aplicación principal
├── about.html          # Página "Sobre nosotros"
├── contacto.html       # Página de contacto
├── terminos.html       # Términos y condiciones
├── README.md           # Documentación principal
├── CONTRIBUTING.md     # Esta guía
├── LICENSE             # Licencia MIT
├── .gitignore          # Archivos ignorados por Git
├── .gitattributes      # Configuración de Git
└── .vscode/            # Configuración de VS Code
```

### Archivos Principales

- **`index.html`**: Contiene toda la lógica de la aplicación
  - CSS embebido (líneas 40-600)
  - JavaScript embebido (líneas 1000-1540)
  - HTML semántico y accesible

- **`about.html`**: Información sobre el proyecto
- **`contacto.html`**: Formulario de contacto
- **`terminos.html`**: Términos legales

## 📝 Convenciones de Código

### HTML

- Usa HTML5 semántico
- Incluye atributos `alt` en imágenes
- Mantén la accesibilidad (ARIA labels)
- Usa indentación de 2 espacios

```html
<!-- ✅ Correcto -->
<div class="weather-card">
  <h2>Clima en Madrid</h2>
  <img src="icon.png" alt="Icono de clima soleado">
</div>

<!-- ❌ Incorrecto -->
<div class="weather-card"><h2>Clima en Madrid</h2><img src="icon.png"></div>
```

### CSS

- Usa variables CSS para colores y valores reutilizables
- Organiza las reglas por secciones
- Usa nombres de clases descriptivos
- Mantén la especificidad baja

```css
/* ✅ Correcto */
.weather-card {
  background-color: var(--color-card);
  border-radius: 1.5rem;
  padding: 2rem;
  box-shadow: var(--shadow-lg);
}

/* ❌ Incorrecto */
.weather-card {
  background-color: #ffffff;
  border-radius: 24px;
  padding: 32px;
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}
```

### JavaScript

- Usa ES6+ features
- Mantén funciones pequeñas y enfocadas
- Usa nombres descriptivos para variables
- Comenta código complejo

```javascript
// ✅ Correcto
const fetchWeatherData = async (city) => {
  try {
    const response = await fetch(`${API_URL}?q=${city}`);
    return await response.json();
  } catch (error) {
    console.error('Error fetching weather:', error);
    throw error;
  }
};

// ❌ Incorrecto
const getData = async (c) => {
  const r = await fetch(`${API_URL}?q=${c}`);
  return r.json();
};
```

### Nomenclatura

- **Variables**: camelCase (`weatherData`, `currentTemperature`)
- **Funciones**: camelCase (`fetchWeatherData`, `updateUI`)
- **Clases CSS**: kebab-case (`weather-card`, `search-input`)
- **Constantes**: UPPER_SNAKE_CASE (`API_KEY`, `MAX_TEMPERATURE`)

## 🔄 Proceso de Pull Request

### 1. Crear una Rama

```bash
git checkout -b feature/nombre-de-la-feature
# o
git checkout -b fix/nombre-del-bug
```

### 2. Hacer Cambios

- Escribe código limpio y bien documentado
- Prueba tu código en múltiples navegadores
- Asegúrate de que no rompas funcionalidades existentes

### 3. Commit y Push

```bash
git add .
git commit -m "feat: agregar soporte para nuevos idiomas

- Agregar soporte para francés y alemán
- Actualizar traducciones
- Mejorar selector de idioma"
git push origin feature/nombre-de-la-feature
```

### 4. Crear Pull Request

1. Ve a tu fork en GitHub
2. Haz clic en "Compare & pull request"
3. Completa la plantilla de PR
4. Espera la revisión

### Plantilla de Pull Request

```markdown
## 📝 Descripción
Breve descripción de los cambios realizados.

## 🎯 Tipo de Cambio
- [ ] Bug fix
- [ ] Nueva feature
- [ ] Mejora de documentación
- [ ] Refactorización
- [ ] Otro

## 🧪 Pruebas
- [ ] Probado en Chrome
- [ ] Probado en Firefox
- [ ] Probado en Safari
- [ ] Probado en móvil

## 📸 Capturas de Pantalla
Si aplica, incluye capturas de pantalla de los cambios.

## ✅ Checklist
- [ ] Mi código sigue las convenciones del proyecto
- [ ] He probado mi código
- [ ] He actualizado la documentación si es necesario
- [ ] Mis cambios no generan nuevos warnings
```

## 🐛 Reportar Bugs

### Antes de Reportar

1. Busca en los [issues existentes](https://github.com/Xangel0s/Climate-by-city/issues)
2. Verifica que el bug no haya sido reportado ya
3. Prueba en diferentes navegadores

### Información Requerida

```markdown
## 🐛 Descripción del Bug
Descripción clara y concisa del problema.

## 🔄 Pasos para Reproducir
1. Ve a '...'
2. Haz clic en '...'
3. Escribe '...'
4. Ve el error

## ✅ Comportamiento Esperado
Lo que debería pasar.

## ❌ Comportamiento Actual
Lo que realmente pasa.

## 📱 Información del Sistema
- Navegador: [ej. Chrome 90]
- Sistema Operativo: [ej. Windows 10]
- Versión: [ej. 1.0.0]

## 📸 Capturas de Pantalla
Si aplica, incluye capturas de pantalla.

## 📋 Información Adicional
Cualquier otra información relevante.
```

## 💡 Solicitar Features

### Antes de Solicitar

1. Verifica que la feature no exista ya
2. Busca en los issues si ya se ha solicitado
3. Piensa en el impacto y la implementación

### Plantilla de Feature Request

```markdown
## 💡 Descripción de la Feature
Descripción clara de la funcionalidad deseada.

## 🎯 Problema que Resuelve
Explica qué problema resuelve esta feature.

## 💭 Solución Propuesta
Describe cómo te gustaría que funcione.

## 🔄 Alternativas Consideradas
Otras soluciones que consideraste.

## 📱 Información Adicional
Capturas de pantalla, mockups, etc.
```

## 🌐 Agregar Nuevos Idiomas

Para agregar soporte para un nuevo idioma:

1. **Agregar traducciones**
   ```javascript
   const translations = {
     es: { /* español */ },
     en: { /* inglés */ },
     ja: { /* japonés */ },
     fr: { /* francés - NUEVO */ }
   };
   ```

2. **Agregar opción en el selector**
   ```html
   <div class="language-option" onclick="changeLanguage('fr')">
     <span>🇫🇷</span>
     <span>Français</span>
   </div>
   ```

3. **Probar la traducción**
   - Verifica que todos los textos se traduzcan
   - Prueba el formato de fechas
   - Verifica la dirección del texto (RTL si aplica)

## 🎨 Mejorar la UI/UX

### Principios de Diseño

- **Simplicidad**: Interfaz limpia y fácil de usar
- **Consistencia**: Mantén el mismo estilo en toda la app
- **Accesibilidad**: Asegúrate de que sea usable para todos
- **Responsive**: Funciona bien en todos los dispositivos

### Herramientas Recomendadas

- **Diseño**: Figma, Adobe XD
- **Prototipado**: InVision, Marvel
- **Testing**: BrowserStack, LambdaTest

## 🔧 Optimizaciones

### Rendimiento

- Minimiza las llamadas a la API
- Optimiza imágenes y assets
- Usa lazy loading cuando sea posible
- Minimiza el CSS y JavaScript

### SEO

- Usa meta tags apropiados
- Estructura HTML semántica
- Optimiza para Core Web Vitals
- Incluye datos estructurados

## 📞 Contacto

Si tienes preguntas sobre cómo contribuir:

- 📧 Email: [tu-email@example.com]
- 💬 Discord: [enlace al servidor]
- 🐦 Twitter: [@tu-usuario]

## 🙏 Agradecimientos

Gracias a todos los contribuidores que han ayudado a hacer **Clima por Ciudad** mejor:

- [Lista de contribuidores](https://github.com/Xangel0s/Climate-by-city/graphs/contributors)

---

**¡Gracias por contribuir a Clima por Ciudad! 🌤️** 