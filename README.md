# 🏆 WC26 GoodBarber App - 7 Corredores Turísticos CDMX

App web de los 7 corredores turísticos de la Ciudad de México para integración con GoodBarber mediante iframes.

## 🚀 Demo en vivo

[https://wc26-goodbarber-app.onrender.com](https://wc26-goodbarber-app.onrender.com)

## 📱 Estructura de la App

```
├── index.html      # Página principal - 7 Corredores
├── corredor.html   # Vista del corredor con categorías
├── place.html      # Detalle del lugar
├── mapa.html       # Mapa con todos los puntos
└── package.json    # Configuración del proyecto
```

## 🛠️ Tecnologías

- HTML5 + CSS3 + JavaScript Vanilla
- Supabase (Base de datos)
- Leaflet.js (Mapas)
- Render.com (Hosting)
- GoodBarber (App móvil)

## 📦 Instalación Local

1. Clona el repositorio:
```bash
git clone https://github.com/[tu-usuario]/wc26-goodbarber-app.git
cd wc26-goodbarber-app
```

2. Instala dependencias:
```bash
npm install
```

3. Ejecuta el servidor local:
```bash
npm start
```

4. Abre en tu navegador:
```
http://localhost:3000
```

## 🚀 Deploy en Render

### Opción 1: Deploy Automático
1. Conecta tu repo de GitHub en [Render.com](https://render.com)
2. Selecciona "Static Site"
3. Build Command: (dejar vacío)
4. Publish Directory: `.`

### Opción 2: Deploy Manual
1. Sube los archivos a GitHub
2. En Render, crea un nuevo "Static Site"
3. Conecta tu repositorio
4. Render hará deploy automático con cada push

## 📱 Integración con GoodBarber

En cada página HTML de GoodBarber, pega este código:

### Para "7 Corredores":
```html
<iframe 
  src="https://wc26-goodbarber-app.onrender.com/index.html" 
  style="width:100%; height:100vh; border:0; overflow:auto;"
  frameborder="0">
</iframe>
```

### Para "Corredor":
```html
<iframe 
  src="https://wc26-goodbarber-app.onrender.com/corredor.html" 
  style="width:100%; height:100vh; border:0; overflow:auto;"
  frameborder="0">
</iframe>
```

### Para "Place Detail":
```html
<iframe 
  src="https://wc26-goodbarber-app.onrender.com/place.html" 
  style="width:100%; height:100vh; border:0; overflow:auto;"
  frameborder="0">
</iframe>
```

### Para "Mapa":
```html
<iframe 
  src="https://wc26-goodbarber-app.onrender.com/mapa.html" 
  style="width:100%; height:100vh; border:0; overflow:auto;"
  frameborder="0">
</iframe>
```

## 🔄 Navegación

La app maneja la navegación mediante parámetros URL:

- `index.html` → Lista de 7 corredores
- `corredor.html?corredor=zona-rosa` → Vista del corredor
- `place.html?tipo=restaurantes&id=123&corredor=zona-rosa` → Detalle del lugar
- `mapa.html?corredor=zona-rosa` → Mapa del corredor

## 🗄️ Base de Datos

Conectada a Supabase con las siguientes tablas:
- `corredores` - Los 7 corredores turísticos
- `restaurantes` - Restaurantes por corredor
- `hoteles` - Hoteles por corredor
- `imperdibles` - Lugares imperdibles
- `estacionamientos` - Parkings
- `estaciones_ecobici` - Estaciones de bicicletas

## 📊 Datos por Corredor

| Corredor | Restaurantes | Hoteles | Imperdibles | Parking | EcoBici | Total |
|----------|--------------|---------|-------------|---------|---------|-------|
| Zona Rosa | 27 | 21 | 18 | 22 | 22 | 110 |
| Basílica | 28 | 17 | 19 | 16 | 14 | 94 |
| Centro Histórico | - | - | - | - | - | 308* |
| Chapultepec | 38 | 23 | 24 | 18 | 28 | 131 |
| Coyoacán | 31 | 19 | 28 | 17 | 18 | 113 |
| Garibaldi | 22 | 18 | 16 | 14 | 9 | 79 |
| Xochimilco | 28 | 16 | 20 | 15 | 8 | 87 |

*En proceso de geocodificación

## 🎨 Personalización

Los colores principales están definidos en CSS:
- Verde México: `#006847`
- Rojo México: `#CE1126`
- Gris fondo: `#f5f5f5`

## 📝 Notas

- La app es responsive y funciona en móviles y tablets
- Los mapas usan OpenStreetMap (no requiere API key)
- Las imágenes se cargan desde Supabase Storage
- Caché de navegador optimizado para mejor rendimiento

## 🤝 Contribuir

1. Fork el proyecto
2. Crea tu rama (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo Licencia MIT.

## 👨‍💻 Autor

**Tony M** - Mundial México Hub WC2026

---

⚽ Hecho con ❤️ para el Mundial 2026 🇲🇽