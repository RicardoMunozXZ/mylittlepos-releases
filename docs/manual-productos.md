# Manual — Productos

> Corresponde a la versión 1.0.0. Desde el menú lateral: **Inventario → tab Productos**.

El catálogo de productos es la base de todo el sistema: lo que está acá se puede vender
en el Punto de Venta.

---

## 1. Ver el catálogo

La tab **Productos** muestra la tabla de productos con:

- **Búsqueda**: tipeá parte del código o de la descripción para filtrar.
- **Filtro por categoría**: desplegable que arranca en "Todas".

## 2. Crear un producto

Tocá el botón de **nuevo producto** y completá el formulario:

### Campos básicos

| Campo | Regla |
|-------|-------|
| **Código** | Obligatorio. Es el que lee el escáner de código de barras. |
| **Descripción** | Obligatoria. Nombre del producto tal como se muestra y se imprime. |
| **Costo** | Cuánto te cuesta a vos (solo números). |
| **Precio** | Precio de venta (solo números). |
| **Existencias** | Stock actual (solo números). |
| **Stock mínimo** | Piso de alerta de reposición (solo números). |
| **Tipo de unidad** | Pieza, kilo, etc. Por defecto: Pieza. |
| **Sub-unidad** | Segunda unidad (ej.: caja de 10). Al cambiar el tipo de unidad se limpia, porque pertenece al catálogo anterior. |
| **Categoría** | Se elige del catálogo de categorías. |
| **Imagen** | Seleccioná una foto del producto o quitá la que tenga. |

### Secciones opcionales (checks)

El formulario tiene cuatro interruptores que habilitan secciones adicionales:

- **Impuestos**: marcá las tasas del catálogo (IVA, IEPS, etc.) que aplican al producto.
  Desde ahí mismo también podés **crear una tasa nueva** (nombre + %) y queda aplicada al
  producto automáticamente.
- **Lotes**: para productos con control de vencimiento. Cada lote tiene **número de
  lote**, **fecha de vencimiento** y **existencias** que entran a ese lote.
  - El **día es opcional**: si dejás el día vacío, el sistema toma el **último día del
    mes** (ej.: "vence 03/2026" queda como válido hasta el 31 de marzo de 2026). Esa
    convención se muestra en el propio formulario.
  - Con lotes, en el PV al agregar el producto te pide elegir de qué lote sale.
- **Medicamento**: habilita los **compuestos activos** del producto (nombre, cantidad y
  unidad, ej.: 500 mg).
- **Stock mínimo**: habilita el control de piso de reposición en el producto.

Tocá **Guardar**: el producto se guarda y aparece un aviso de éxito **sin cerrar el
formulario**, por si querés seguir ajustando datos.

## 3. Editar un producto

Hacé clic en el producto de la tabla: se abre el formulario con los datos cargados.
Ajustá lo que haga falta y guardá.

> **Historial de precios**: cada vez que cambia el costo o el precio, el sistema registra
> el valor nuevo con la fecha. Así se puede responder "por qué este producto cuesta lo que
> cuesta". Las compras que finalizan también actualizan el costo y quedan marcadas con su
> origen.

## 4. Dar de baja un producto

Desde el producto en la tabla, pedí **Eliminar** y confirmá. Es una **baja lógica**:

- el producto **sale del catálogo**: ya no aparece en la lista ni se puede vender en el PV;
- **conserva todo**: historial de precios, movimientos y existencias siguen contando en el
  sistema (una compra o devolución posterior no lo "revive" por accidente).

Si necesitás volver a venderlo más adelante, se crea de nuevo con el mismo código.

## 5. Errores comunes

| Aviso | Causa |
|-------|-------|
| Código / descripción marcados en rojo | Faltan los dos campos obligatorios. |
| "Producto sin stock" en el PV | Las existencias llegaron a 0. Cargá stock o registrá la compra que lo repone. |
| El producto no aparece en el PV | Puede estar dado de baja o el filtro de categoría lo está ocultando. |

---

**Ver también**: [Manual de Categorías](manual-categorias.md) ·
[Manual de Inventario](manual-inventario.md) · [Manual del Punto de Venta](manual-punto-de-venta.md)
