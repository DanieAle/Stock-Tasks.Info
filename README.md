# StockAndTasks - Workshop & Inventory Management System

**StockAndTasks** es una solución de escritorio desarrollada bajo la arquitectura **WPF / MVVM** en **C# / .NET**, orientada a la gestión integral de talleres de reparación electrónica, computación y telefonía. Combina persistencia *offline-first* ultra optimizada con trazabilidad completa de stock, flujo de trabajo para servicio técnico y sistemas remotos de licenciamiento y auto-actualización.

---

## 📸 Módulos e Interfaz

### 📊 Dashboard & Métricas
Visualización centralizada de estado de negocio, alertas de vencimiento de trabajos, stock bajo y resumen financiero interactivo.
![Dashboard Principal](/assets/dashboard.png)

---

### 📦 Gestión de Inventario y Stock
Administración de catálogo con categorización parametrizada, filtros por etiquetas dinámicas (ej. *capacitores, transistores*) y módulo de ingreso rápido de artículos.
| Vista de Inventario | Registro de Productos |
| :---: | :---: |
| ![Inventario](/assets/Inventario.png) | ![Agregar Inventario](/assets/agregarInventario.png) |

**Búsqueda y Filtrado Avanzado:**
![Filtro de Inventario](/assets/filtroinventario.png)

---

### 🛠️ Servicio Técnico y Órdenes de Trabajo
Seguimiento del ciclo de vida de reparaciones (*Pendiente, Activo, Terminado*), asignación de precios, diagnósticos y catálogo de tareas frecuentes preconfiguradas.
| Listado de Trabajos | Alta de Trabajo Técnico |
| :---: | :---: |
| ![Trabajos](/assets/trabajos.png) | ![Agregar Trabajo](/assets/agregar-trabajo.png) |

**Catálogo de Tareas Parametrizadas:**
![Tareas Preconfiguradas](/assets/tareas.png)

---

### 💳 Ventas y Registro Inmutable (Audit Trail)
Carro de ventas directo e historial inmutable de movimientos (*reabastecer, comprar, vender, ajustar precio*) respaldado por un libro mayor de transacciones.
| Carrito de Ventas | Historial de Movimientos |
| :---: | :---: |
| ![Ventas](/assets/ventas.png) | ![Historial](/assets/historial.png) |

---

## ⚡ Arquitectura y Rendimiento

* **Patrón MVVM Estricto:** Desacoplamiento total entre las vistas (XAML) y la lógica de negocio (ViewModels), garantizando mantenibilidad y facilidad para pruebas unitarias.
* **Virtualización de UI y Manejo de Memoria:** Huella de memoria mínima de **~20 MB RAM** testeada con +10,000 elementos. *Scroll infinito* con ventana de renderizado activo (200 a 600 elementos) y reciclado dinámico de componentes en memoria.
* **Persistencia Local:** Almacenamiento directo mediante SQLite para asegurar operatividad offline sin dependencia de red local ni servidores externos.
* **Informes:** Generación automática de reportes detallados y exportación directa de tablas a formato PDF.

---

## 🔐 Licenciamiento y Distribución

* **Validación DRM Remota:** Control de activación y verificación de licencias en línea.
* **Pipeline de Auto-Update:** Integración con **Velopack** para la instalación silenciosa y distribución automatizada de parches y actualizaciones.

---

## 💻 Stack Tecnológico

| Capa | Tecnología |
| :--- | :--- |
| **Arquitectura / GUI** | WPF (Windows Presentation Foundation) / MVVM Pattern |
| **Lenguaje / Runtime** | C# / .NET |
| **Persistencia Local** | SQLite |
| **Despliegue & Updates** | Velopack |
| **Pruebas Unitarias** | xUnit v3 |