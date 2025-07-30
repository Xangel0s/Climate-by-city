# 🌤️ Clima por Ciudad

[![GitHub stars](https://img.shields.io/github/stars/Xangel0s/Climate-by-city?style=social)](https://github.com/Xangel0s/Climate-by-city/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Xangel0s/Climate-by-city?style=social)](https://github.com/Xangel0s/Climate-by-city/network/members)
[![GitHub issues](https://img.shields.io/github/issues/Xangel0s/Climate-by-city)](https://github.com/Xangel0s/Climate-by-city/issues)
[![GitHub license](https://img.shields.io/github/license/Xangel0s/Climate-by-city)](https://github.com/Xangel0s/Climate-by-city/blob/main/LICENSE)

Una aplicación web moderna y responsive para consultar el clima y pronóstico del tiempo en cualquier ciudad del mundo. Desarrollada con HTML5, CSS3 y JavaScript vanilla, ofrece una experiencia de usuario intuitiva con soporte multilingüe y modo oscuro.

## ✨ Características

- 🌍 **Cobertura Global**: Consulta el clima en cualquier ciudad del mundo
- 📱 **Diseño Responsive**: Optimizada para dispositivos móviles, tablets y desktop
- 🌙 **Modo Oscuro**: Tema claro/oscuro con persistencia de preferencias
- 🌐 **Multilingüe**: Soporte para Español, Inglés y Japonés
- 🔍 **Búsqueda Inteligente**: Autocompletado con sugerencias de ciudades principales
- 📊 **Pronóstico Extendido**: Pronóstico del tiempo para 7 días
- 💡 **Recomendaciones**: Consejos personalizados según las condiciones climáticas
- ⚡ **Rápida**: Carga instantánea sin dependencias pesadas
- 🎨 **UI Moderna**: Interfaz elegante con animaciones suaves

## 🚀 Demo en Vivo

[Ver Demo](https://tusitio.com) - *Reemplaza con tu URL de producción*

## 📸 Capturas de Pantalla

### Vista Principal
![Vista Principal](https://via.placeholder.com/800x400/3b82f6/ffffff?text=Clima+por+Ciudad+-+Vista+Principal)

### Modo Oscuro
![Modo Oscuro](https://via.placeholder.com/800x400/1e293b/ffffff?text=Modo+Oscuro)

### Vista Móvil
![Vista Móvil](https://via.placeholder.com/400x600/3b82f6/ffffff?text=Vista+Móvil)

## 🛠️ Tecnologías Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **APIs**: WeatherAPI.com para datos meteorológicos
- **Fuentes**: Google Fonts (Inter)
- **Iconos**: Font Awesome 6.4.0
- **Hosting**: GitHub Pages (recomendado)

## 📦 Instalación

### Prerrequisitos
- Navegador web moderno
- Conexión a internet
- API Key de WeatherAPI.com (gratuita)

### Pasos de Instalación

1. **Clona el repositorio**
   ```bash
   git clone https://github.com/Xangel0s/Climate-by-city.git
   cd Climate-by-city
   ```

2. **Obtén tu API Key**
   - Ve a [WeatherAPI.com](https://www.weatherapi.com/)
   - Regístrate para obtener una API key gratuita
   - Reemplaza `YOUR_API_KEY` en `index.html` línea 1000

3. **Configura la API Key**
   ```javascript
   const apiKey = "tu_api_key_aqui";
   ```

4. **Abre el proyecto**
   - Abre `index.html` en tu navegador
   - O usa un servidor local:
   ```bash
   # Con Python
   python -m http.server 8000
   
   # Con Node.js
   npx serve .
   ```

## 🔧 Configuración

### Variables de Entorno
```javascript
// En index.html, línea ~1000
const apiKey = "tu_api_key_de_weatherapi";
```

### Personalización
- **Colores**: Modifica las variables CSS en `:root`
- **Idiomas**: Agrega nuevos idiomas en el objeto `translations`
- **Ciudades**: Edita el objeto `ciudadesPrincipales`

## 📁 Estructura del Proyecto

```
Climate-by-city/
├── index.html          # Página principal de la aplicación
├── about.html          # Página "Sobre nosotros"
├── contacto.html       # Página de contacto
├── terminos.html       # Términos y condiciones
├── README.md           # Este archivo
├── .gitattributes      # Configuración de Git
└── .vscode/            # Configuración de VS Code
```

## 🌐 API Utilizada

### WeatherAPI.com
- **Endpoint**: `https://api.weatherapi.com/v1/forecast.json`
- **Plan Gratuito**: 1,000,000 requests/mes
- **Documentación**: [WeatherAPI Docs](https://www.weatherapi.com/docs/)

### Ejemplo de Respuesta
```json
{
  "location": {
    "name": "Madrid",
    "country": "Spain",
    "localtime": "2024-01-15 14:30"
  },
  "current": {
    "temp_c": 22,
    "condition": {
      "text": "Soleado",
      "icon": "//cdn.weatherapi.com/weather/64x64/day/113.png"
    },
    "wind_kph": 15,
    "humidity": 45,
    "pressure_mb": 1013
  },
  "forecast": {
    "forecastday": [...]
  }
}
```

## 🎨 Características de Diseño

### Sistema de Colores
- **Tema Claro**: Fondo blanco con acentos azules
- **Tema Oscuro**: Fondo azul oscuro con acentos claros
- **Responsive**: Adaptable a todos los tamaños de pantalla

### Animaciones
- Transiciones suaves entre temas
- Animaciones de carga con spinner personalizado
- Efectos hover en botones y tarjetas
- Animaciones de entrada para resultados

## 📱 Compatibilidad

### Navegadores Soportados
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Opera 76+

### Dispositivos
- ✅ Desktop (1920x1080+)
- ✅ Tablet (768x1024)
- ✅ Mobile (375x667)
- ✅ Small Mobile (320x568)

## 🔒 Privacidad y Seguridad

- ✅ No se almacenan datos personales
- ✅ API calls seguros con HTTPS
- ✅ Sin cookies de tracking
- ✅ Cumple con GDPR

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Por favor, sigue estos pasos:

1. **Fork** el proyecto
2. **Crea** una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. **Push** a la rama (`git push origin feature/AmazingFeature`)
5. **Abre** un Pull Request

### Guías de Contribución
- Mantén el código limpio y bien documentado
- Sigue las convenciones de nomenclatura existentes
- Prueba tu código en múltiples navegadores
- Actualiza la documentación si es necesario

## 🐛 Reportar Bugs

Si encuentras un bug, por favor:

1. Revisa los [issues existentes](https://github.com/Xangel0s/Climate-by-city/issues)
2. Crea un nuevo issue con:
   - Descripción detallada del problema
   - Pasos para reproducir
   - Navegador y sistema operativo
   - Captura de pantalla (si aplica)

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo [LICENSE](LICENSE) para más detalles.

## 👨‍💻 Autor

**Xangel0s**
- GitHub: [@Xangel0s](https://github.com/Xangel0s)
- Proyecto: [Climate-by-city](https://github.com/Xangel0s/Climate-by-city)

## 🙏 Agradecimientos

- [WeatherAPI.com](https://www.weatherapi.com/) por proporcionar datos meteorológicos precisos
- [Font Awesome](https://fontawesome.com/) por los iconos
- [Google Fonts](https://fonts.google.com/) por la tipografía Inter
- [GitHub](https://github.com/) por el hosting gratuito

## 📊 Estadísticas del Proyecto

![GitHub stats](https://github-readme-stats.vercel.app/api?username=Xangel0s&show_icons=true&theme=radical)

## ⭐ Si te gusta este proyecto

Si este proyecto te resulta útil, por favor:

- ⭐ Dale una estrella en GitHub
- 🔄 Compártelo con otros desarrolladores
- 💬 Déjanos un comentario
- 🐛 Reporta bugs o sugiere mejoras

---

**¡Gracias por usar Clima por Ciudad! 🌤️**

*Desarrollado con ❤️ por Xangel0s*
