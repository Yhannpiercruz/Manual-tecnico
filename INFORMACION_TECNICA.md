# Información Técnica del Proyecto Renacer

## 🏗️ Arquitectura del Sistema

### Backend
- **Lenguaje**: Java 21 (LTS)
- **Framework**: Spring Boot 3.4.2
- **Arquitectura**: Hexagonal (Puertos y Adaptadores)
- **Build Tool**: Gradle con Wrapper
- **ORM**: Spring Data JPA + Hibernate
- **Librerías**: Lombok 1.18.36

### Frontend
- **Librería UI**: React 18.2.0
- **Bundler**: Vite 5.0.8
- **Enrutamiento**: React Router DOM 6.20.0
- **Estilos**: CSS3 con Variables CSS
- **Notificaciones**: SweetAlert2
- **Iconos**: FontAwesome 6

### Base de Datos
- **Motor**: PostgreSQL 15
- **Puerto**: 5432
- **Persistencia**: Volúmenes Docker

### Infraestructura
- **Contenedores**: Docker & Docker Compose
- **Servidor Web**: Nginx (Alpine)
- **Despliegue**: Railway compatible

## 📦 Módulos del Sistema

### 1. Módulo de Inicio
- Dashboard con resumen de operaciones
- Estadísticas en tiempo real
- Accesos rápidos

### 2. Módulo de Compras
- Registro de compras
- Gestión de proveedores
- Control de inventario entrante

### 3. Módulo de Ventas
- Registro de ventas
- Gestión de clientes
- Control de inventario saliente

### 4. Módulo de Inventario
- Control de stock
- Alertas de inventario bajo
- Movimientos de materiales

### 5. Módulo de Materiales
- Catálogo de materiales
- Categorías y subcategorías
- Precios y unidades de medida

### 6. Módulo de Personas
- Gestión de asociados
- Información de contacto
- Historial de transacciones

### 7. Módulo de Informes
- Reportes de ventas
- Reportes de compras
- Análisis de inventario

### 8. Módulo de Configuración
- Ajustes del sistema
- Gestión de usuarios
- Preferencias de accesibilidad

## 🎨 Sistema de Diseño

### Paleta de Colores

#### Modo Normal
- **Primario**: #2d5a47 (Verde institucional)
- **Primario Hover**: #244a3a
- **Secundario**: #6b7280 (Gris)
- **Peligro**: #dc2626 (Rojo)

#### Modo Daltónico
- **Primario**: #1f6feb (Azul accesible)
- **Primario Hover**: #1158c7
- **Fondo**: #f3f6fb

### Tipografía
- **Familia**: System fonts (-apple-system, BlinkMacSystemFont, Segoe UI, Roboto)
- **Tamaño Base**: 18px (1.125rem)
- **Tamaño Pequeño**: 15px (0.9375rem)
- **Tamaño Grande**: 20px (1.25rem)
- **Títulos**: 28px (1.75rem)

### Espaciado
- **Unidad Base**: 0.5rem (8px)
- **Padding Botones**: 0.4rem 1rem
- **Altura Botones**: 36px (2.25rem)
- **Border Radius**: 6px (0.375rem)

## 🔐 Características de Seguridad

- Autenticación de usuarios
- Recuperación de contraseña con pregunta secreta
- Validación de formularios
- Protección contra inyección SQL (JPA)
- Sanitización de entradas

## ♿ Accesibilidad

### Características Implementadas
1. **Modo Daltónico**: Paleta de colores alternativa
2. **Tamaño de Fuente**: Ajustable (pequeño, mediano, grande)
3. **Contraste**: Alto contraste en modo daltónico
4. **Navegación por Teclado**: Soporte completo
5. **ARIA Labels**: Etiquetas descriptivas
6. **Focus Visible**: Indicadores claros de foco

### Atajos de Teclado
- `Tab`: Navegar entre elementos
- `Enter`: Activar botones y enlaces
- `Esc`: Cerrar modales
- `Ctrl/Cmd + K`: Abrir/cerrar menú (en manual técnico)

## 📱 Responsive Design

### Breakpoints
- **Desktop**: > 1024px
- **Tablet**: 768px - 1024px
- **Mobile**: < 768px
- **Small Mobile**: < 480px

### Adaptaciones
- Menú lateral colapsable
- Tablas con scroll horizontal
- Formularios apilados en móvil
- Botones de ancho completo en móvil

## 🔄 Flujo de Datos

### Arquitectura Frontend
```
Usuario → React Components → Services → API REST → Backend
```

### Arquitectura Backend
```
Controller → Use Cases → Domain → Repository → Database
```

## 📊 Componentes Reutilizables

### Transversales (8)
1. Barra de accesibilidad
2. Barra superior
3. Sistema de colores
4. Cabecera
5. Iconografía
6. Pie de página
7. Tipografía
8. Botón volver arriba

### Generales (19)
1. Acordeón
2. Alerta modal
3. Alerta notificación
4. Área de servicio
5. Botones
6. Buscador
7. Galería de aplicaciones
8. Carrusel
9. Tooltip
10. Etiquetas
11. Spinner
12. Barra de progreso
13. Menú de navegación
14. Breadcrumb
15. Login
16. Paginación
17. Pestañas
18. Tablas
19. Tarjetas

### Formularios (4)
1. Carga de archivos
2. Desplegables
3. Entradas de texto
4. Opciones de selección

## 🚀 Despliegue

### Local
```bash
# Backend
cd Backend
./gradlew bootRun

# Frontend
cd Frontend
npm install
npm run dev
```

### Docker
```bash
docker-compose up -d
```

### Railway
- Push a repositorio Git
- Conectar con Railway
- Variables de entorno configuradas
- Deploy automático

## 📝 Convenciones de Código

### Frontend
- Componentes en PascalCase
- Funciones en camelCase
- Constantes en UPPER_SNAKE_CASE
- CSS con BEM notation

### Backend
- Clases en PascalCase
- Métodos en camelCase
- Paquetes en lowercase
- Interfaces con prefijo "I" opcional

## 🧪 Testing

### Frontend
- Jest para unit tests
- React Testing Library
- Cypress para E2E

### Backend
- JUnit 5 (Jupiter)
- Mockito para mocks
- Spring Boot Test

## 📚 Documentación Adicional

- `ARCHITECTURE.md` - Arquitectura del backend
- `BUSINESS_RULES.md` - Reglas de negocio
- `LEEME-PRIMERO.md` - Guía de inicio rápido
- `RESUMEN_TECNOLOGIAS.md` - Stack tecnológico

## 🔧 Mantenimiento

### Actualizaciones Recomendadas
- Revisar dependencias mensualmente
- Actualizar Spring Boot cada 6 meses
- Actualizar React cada año
- Parches de seguridad inmediatamente

### Backup
- Base de datos: Diario
- Código: Git (continuo)
- Configuración: Semanal

## 📞 Soporte

Para más información sobre el proyecto:
- Revisar documentación en `/Backend/`
- Consultar archivos `.md` en raíz
- Revisar este manual técnico

---

**Última actualización**: 2024  
**Versión del sistema**: 1.0  
**Versión del manual**: 1.0