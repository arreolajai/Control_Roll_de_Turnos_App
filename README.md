# Control de Roll de Turnos

Aplicación web (PWA) para llevar el control del roll de turnos de personal **Sindicalizado** y **Empleado**, con los campos Área, Cuadrilla, Ficha, Nombre, Tipo de empleado, Nota y los 7 días de la semana (nombre + fecha día/mes/año).

## Contenido del paquete
- `index.html` – Aplicación completa (interfaz + lógica).
- `manifest.json` – Metadatos para instalación como app (PWA).
- `service-worker.js` – Habilita el funcionamiento sin conexión a Internet.
- `seed.json` – Datos iniciales (roster) tomados de tu archivo `ROLL DE TURNOS 2026 SEMANA 43.xlsx` (solo Área, Cuadrilla, Ficha, Nombre y Tipo; los turnos se capturan vacíos para que tú los llenes).
- `icons/` – Íconos de la aplicación.

## Cómo usarla
1. **Opción rápida (sin instalar nada):** abre `index.html` con doble clic; funciona en el navegador (Chrome, Edge) de tu PC.
2. **Para instalarla en celular, tablet o laptop (recomendado):**
   - Sube esta carpeta completa a un hosting simple (SharePoint con "Abrir como sitio", Netlify, GitHub Pages, o un servidor interno con HTTPS).
   - Entra a la URL desde Chrome/Edge en tu celular, tablet o PC.
   - Aparecerá el botón **"⬇ Instalar app"** en la parte superior (o la opción "Agregar a pantalla de inicio" / "Instalar aplicación" del navegador).
   - Una vez instalada, funciona como una app normal, incluso sin Internet.
3. Los datos (empleados y turnos capturados) se guardan automáticamente en el dispositivo (localStorage), no requieren servidor ni base de datos.

## Funcionalidades incluidas
- Alta, edición y eliminación de empleados (Área, Cuadrilla, Ficha, Nombre, Tipo, Nota).
- Captura de turno por día con un selector de códigos (1, 2, 3, E2, D, F, V, G) + opción de código personalizado.
- Edición de la leyenda de códigos (agregar/quitar/cambiar color y descripción).
- Filtro por tipo de empleado, área, cuadrilla y búsqueda por nombre/ficha.
- Navegación por semana (anterior/siguiente/hoy), con encabezados que muestran nombre del día y fecha dd/mm/aaaa.
- Exportar a Excel (.xlsx) y a PDF la vista filtrada de la semana en turno.
- Instalable como PWA en celular, tablet y computadora; funciona offline.

## Notas
- El roster inicial (91 personas) se cargó únicamente con los datos maestros confiables del archivo (área, cuadrilla, ficha, nombre, tipo); las celdas de turno se dejaron en blanco para que captures la información vigente directamente en la app, evitando traspasar posibles desalineaciones del archivo original.
- Puedes editar o eliminar cualquier registro desde la propia tabla (íconos ✎ y 🗑).
