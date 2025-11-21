# 🛍️ Catálogo Digital - Sistema de Productos

![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

## 📖 Descripción

Sistema de catálogo digital profesional para mostrar productos de forma atractiva y facilitar las ventas por WhatsApp. Perfecto para emprendedores, tiendas de ropa, accesorios, y negocios que venden por redes sociales.

## ✨ Características Principales

- 🛒 **Catálogo Completo** - Muestra todos tus productos organizados
- 🔍 **Búsqueda Inteligente** - Los clientes encuentran lo que buscan rápidamente
- 🏷️ **Filtros por Categoría** - Organización clara: ropa, accesorios, tecnología
- 💰 **Precios Destacados** - Con opción de mostrar precio anterior (ofertas)
- 📱 **Botón Directo a WhatsApp** - Cada producto tiene su botón de pedido
- 🎯 **Badges Especiales** - Marca productos nuevos u en oferta
- 📱 **100% Responsive** - Se ve perfecto en celulares y tablets
- ⚡ **Carga Rápida** - Todo en un solo archivo HTML

## 🎯 Ideal Para

- ✅ Tiendas de ropa y moda
- ✅ Accesorios y bisutería
- ✅ Productos de tecnología
- ✅ Emprendimientos en redes sociales
- ✅ Catálogos de productos en general
- ✅ Negocios que venden por WhatsApp

## 🚀 Demo en Vivo

🌐 **[Ver Catálogo en Vivo](https://apgtest.github.io/catalogo-digital/)**


## 💻 Instalación

### Clonar el Repositorio

```bash
git clone https://github.com/apgtest/catalogo-digital.git
cd catalogo-digital
```

### Abrir el Proyecto

Simplemente abre `index.html` en tu navegador o usa Live Server en VS Code.

## 🛠️ Personalización

### 1. Cambiar el Número de WhatsApp

Busca en el código y reemplaza `593999999999` con tu número real:

```javascript
const urlWhatsApp = `https://wa.me/TU_NUMERO?text=${encodeURIComponent(mensajeWhatsApp)}`;
```

### 2. Agregar Tus Productos

En el archivo `index.html`, busca el array `productos` y modifica o agrega nuevos:

```javascript
const productos = [
    {
        id: 1,
        nombre: 'Nombre del Producto',
        categoria: 'ropa', // o 'accesorios' o 'tecnologia'
        descripcion: 'Descripción breve del producto',
        precio: 29.99,
        precioAnterior: 39.99, // null si no hay descuento
        emoji: '👕', // Emoji representativo
        badge: 'oferta' // 'oferta', 'nuevo' o null
    },
    // Agrega más productos aquí
];
```

### 3. Personalizar Categorías

Modifica las categorías en la sección de filtros:

```html
<button class="filter-btn" data-category="tu-categoria">Tu Categoría</button>
```

Y actualiza la lógica de filtrado si agregas nuevas categorías.

### 4. Cambiar Colores

Modifica las variables CSS en el `<style>`:

```css
:root {
    --primary: #667eea;     /* Color principal */
    --secondary: #764ba2;   /* Color secundario */
    --success: #25D366;     /* Color WhatsApp */
}
```

### 5. Cambiar Nombre de la Tienda

Edita el encabezado:

```html
<h1>🛍️ Tu Tienda Online</h1>
<p>Tu eslogan aquí</p>
```

## 📋 Funcionalidades Detalladas

### Filtros por Categoría
- Click en "Todos" muestra todos los productos
- Click en categorías específicas filtra solo esos productos
- Botones con estado activo visual

### Búsqueda en Tiempo Real
- Busca por nombre del producto
- Busca por descripción
- Funciona en combinación con filtros de categoría
- Sin resultados muestra mensaje amigable

### Integración con WhatsApp
- Cada producto genera un mensaje personalizado
- Incluye nombre y precio del producto
- Se abre en WhatsApp Web o app móvil
- Mensaje pre-escrito para el cliente

### Sistema de Badges
- **🔥 OFERTA**: Para productos con descuento
- **⭐ NUEVO**: Para productos recién agregados
- Los badges son opcionales por producto

### Precios con Descuento
- Muestra precio actual en grande
- Precio anterior tachado si existe
- Destaca visualmente las ofertas

## 🎨 Estructura del Código

```
index.html
├── <head>
│   ├── Meta tags (SEO)
│   └── <style> (CSS completo)
│
├── <body>
│   ├── Header (Título de la tienda)
│   ├── Container
│   │   ├── Filtros (Categorías + Búsqueda)
│   │   ├── Grid de productos
│   │   └── Mensaje "sin resultados"
│   ├── Footer
│   └── <script> (JavaScript)
│       ├── Array de productos
│       ├── Función renderizar
│       ├── Event listeners de filtros
│       └── Event listener de búsqueda
```

## 💡 Casos de Uso Reales

### Para Tienda de Ropa:
```javascript
{
    nombre: 'Blusa Elegante',
    categoria: 'ropa',
    descripcion: 'Blusa para toda ocasión, tallas S-XL',
    precio: 25.00,
    emoji: '👚'
}
```

### Para Accesorios:
```javascript
{
    nombre: 'Aretes de Plata',
    categoria: 'accesorios',
    descripcion: 'Aretes artesanales, plata 925',
    precio: 35.00,
    emoji: '💍'
}
```

### Para Productos de Belleza:
```javascript
{
    nombre: 'Set de Maquillaje',
    categoria: 'belleza',
    descripcion: 'Kit completo de maquillaje profesional',
    precio: 45.00,
    emoji: '💄'
}
```

## 📱 Responsive Design

El catálogo se adapta automáticamente a:

- 📱 **Móviles** (< 768px): 1 columna
- 📲 **Tablets** (768px - 1024px): 2-3 columnas
- 💻 **Desktop** (> 1024px): 3-4 columnas

## ⚡ Optimización

- **Sin dependencias externas** - Todo en un archivo
- **Carga instantánea** - No requiere servidor
- **SEO amigable** - Meta tags incluidos
- **Imágenes optimizadas** - Usa emojis (carga cero)

## 🎓 Lo que Demuestra Este Proyecto

- ✅ Manipulación del DOM con JavaScript
- ✅ Event handling (clicks, input)
- ✅ Filtrado y búsqueda de datos
- ✅ Diseño responsive con CSS Grid
- ✅ Integración con APIs externas (WhatsApp)
- ✅ UX/UI profesional
- ✅ Código limpio y organizado

## 🔮 Mejoras Futuras

- [ ] Sistema de carrito de compras
- [ ] Favoritos / Lista de deseos
- [ ] Ordenar por precio (menor/mayor)
- [ ] Vista en cuadrícula o lista
- [ ] Zoom en imágenes de productos
- [ ] Comparador de productos
- [ ] Sistema de valoraciones
- [ ] Modo oscuro

## 🤝 Contribuciones

¿Ideas para mejorar? ¡Son bienvenidas!

1. Fork el proyecto
2. Crea tu branch (`git checkout -b feature/MejoraNueva`)
3. Commit cambios (`git commit -m 'Add: nueva característica'`)
4. Push al branch (`git push origin feature/MejoraNueva`)
5. Abre un Pull Request

## 📄 Licencia

Proyecto bajo Licencia MIT - libre para usar y modificar.


<div align="center">

### ⭐ Si te sirvió este proyecto, dale una estrella ⭐


</div>

---

*Última actualización: Noviembre 2025*
