# StockAndTasks - Workshop & Inventory Management System

**StockAndTasks** es una solución de escritorio optimizada para talleres de reparación de electrónica y computación. El sistema resuelve la gestión integral de inventario y el seguimiento de servicios técnicos mediante una arquitectura *offline-first* eficiente, respaldada por servicios remotos de licenciamiento y despliegue continuo.

---

### 🛠️ Características Principales y Arquitectura

* **Trazabilidad por Libro Mayor (Ledger / Audit Trail):** Cada variación de stock (reabastecimiento, compras, ventas, ajustes) se registra de forma inmutable como un movimiento, permitiendo auditoría histórica y operación mediante carrito de ventas.
* **Categorización por Etiquetado Dinámico:** Filtros avanzados por etiquetas personalizables (ej. *capacitores, transistores*) para la localización rápida de componentes.
* **Gestión del Ciclo de Vida de Servicios (Service Orders):** Catálogo parametrizado de tareas frecuentes (mantenimiento, cambio de módulos) e historial de reparaciones con diagnósticos opcionales, precios y seguimiento de fechas límite[cite: 1].
* **Telemetría e Informes en Dashboard:** Indicadores clave de rendimiento (KPIs) en tiempo real: alertas de bajo stock, trabajos próximos a vencer, gráficos financieros de ingresos/compras y exportación de datos a PDF.

---

### ⚡ Rendimiento y Gestión de Memoria

* **Virtualización de Interfaz y Reciclado de Memoria:** Consumo ultra optimizado de memoria RAM (~20 MB) probado en catálogos de +10,000 elementos. Implementación de *scroll infinito* con una ventana de renderizado activo (200 a 600 elementos) y liberación/reciclado dinámico de objetos según la posición del scroll.
* **Persistencia Local de Alta Eficiencia:** Almacenamiento local mediante SQLite para tiempos de respuesta inmediatos y tolerancia a fallos de red[cite: 1].

---

### 🔐 Licenciamiento y Despliegue

* **Validación de Licencias DRM:** Módulo de verificación en línea para autenticación de licencias activas.
* **Pipeline de Actualización:** Integración con **Velopack** para la distribución e instalación silenciosa de parches y actualizaciones de software (*Auto-updates*).

---

### 💻 Stack Tecnológico

| Componente | Tecnología |
| :--- | :--- |
| **Lenguaje / Framework** | C# / .NET |
| **Base de Datos** | SQLite |
| **Instalador & Updates** | Velopack |
| **Testing** | xUnit v3 |
