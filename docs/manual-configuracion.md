# Manual — Configuración

> Corresponde a la versión 1.0.0. Desde el menú lateral: **Configuración**.

Configuración administra el negocio: sus datos, los empleados y sus permisos, y las
opciones del sistema (ticket, impresora, exportaciones, atajos, copias de seguridad).
Tiene cinco tabs: **Negocio**, **Empleados**, **Permisos**, **Sistema** y **Acerca de**.

> Cada tab y cada sección se muestran **según los permisos del usuario**: un empleado
> sin permisos de configuración ve menos (o no ve) estas pantallas.

## Tab Negocio

Los datos que identifican al negocio (aparecen, por ejemplo, en los tickets):

1. Carga **Nombre *** y **Giro *** (obligatorios) y, si quieres, **Dirección**,
   **Teléfono**, **RFC** y **Correo**.
2. Haz clic en **Guardar**.

![Tab Negocio con los datos del negocio y el botón Guardar](imagenes/manual-config-01-negocio.png)

## Tab Empleados

Quienes pueden usar el sistema, cada uno con su alias, código y rol.

- **Nuevo**: carga **Alias *** y **Código *** (lo que se teclea en el login),
  nombre completo, **rol** y **contraseña**, y guarda.
- El ícono de **llave** de cada fila abre los **permisos** de ese empleado.
- **Lápiz** para editar (al editar, la contraseña vacía no se cambia) y
  **papelera** para eliminar, con confirmación.

![Lista de empleados con su rol y las acciones de permisos, editar y eliminar](imagenes/manual-config-04-empleados.png)

## Tab Permisos

**Permisos por rol**: qué puede ver y modificar cada rol. Marca los permisos de cada
rol y haz clic en **Guardar**. Las demás pantallas (y las secciones de Sistema) se muestran
o esconden según estos permisos.

![Matriz de permisos por rol con el rol Cajero seleccionado](imagenes/manual-config-05-permisos.png)

## Tab Sistema

Un listado de secciones; al hacer clic en una, su formulario ocupa la pantalla y
**← Volver** regresa al listado.

![Listado de las secciones de la tab Sistema](imagenes/manual-config-02-sistema.png)

### Configuración de Ticket

**Encabezado** y **pie** del ticket. Haz clic en **Guardar Ticket**.

![Formulario de Configuración de Ticket con encabezado y pie](imagenes/manual-config-06-ticket.png)

### Configuración de Impresora

Para la impresora térmica ESC/POS:

1. Haz clic en **Detectar puertos** y elige el **Puerto** detectado (o escríbelo a mano).
2. Carga **ID Dispositivo** y elige el **Tamaño de Papel** (80 mm o 58 mm).
3. Marca **Imprimir ticket al confirmar la venta** si quieres que salga solo.
4. Haz clic en **Imprimir prueba** para comprobar la conexión, y en **Guardar Impresora**.

![Configuración de Impresora con puerto, dispositivo y tamaño de papel](imagenes/manual-config-03-impresora.png)

### Ruta de exportación de reportes

**Carpeta base** donde quedan los reportes exportados desde Reportes (vacío =
Documentos/MyLittlePOS/reportes). Con **Elegir carpeta…** se elige con el explorador,
y la opción de subcarpeta por período agrupa los archivos por rango de fechas.
Haz clic en **Guardar Ruta de Exportación**.

![Configuración de la ruta de exportación con carpeta base y subcarpeta por período](imagenes/manual-config-07-exportacion.png)

### Atajos de teclado

Teclas que disparan acciones del PV. Haz clic en **Cambiar** en una fila y presiona la tecla
nueva: acepta **F1–F12** o combinaciones con **Ctrl/Alt** (una tecla sola chocaría con
lo que se está tipeando). **Esc** queda libre para cancelar. Si la tecla ya está
usada por otra acción, se avisa. Al terminar, haz clic en **Guardar Atajos**;
**Restaurar por defecto** devuelve las teclas originales.

![Configuración de atajos de teclado con la lista de acciones y sus teclas](imagenes/manual-config-09-atajos.png)

### Eliminar datos del negocio (solo administradores)

Borra **todo**: productos, ventas, compras, empleados, permisos y el resto de la
información del negocio. Pide **confirmar la contraseña**; no se puede deshacer.

![Diálogo de restablecer de fábrica pidiendo confirmar la contraseña](imagenes/manual-config-10-reset.png)

### Copia de seguridad (solo administradores)

Genera una **copia completa** de la base de datos en un archivo `.realm`.

1. Elige la **Carpeta de destino** con **Elegir carpeta…** (vacío =
   Documentos/MyLittlePOS/backups).
2. Haz clic en **Crear copia de seguridad**.

![Configuración de copia de seguridad con carpeta destino y botones de guardar y crear](imagenes/manual-config-08-backup.png)

> Para volver a una copia, el archivo `.realm` se reemplaza a mano con la aplicación
> cerrada; una copia no se "instala" desde la app.

## Tab Acerca de

La versión de MyLittlePOS y los componentes del sistema.

---

**Ver también**: [Manual de Productos](manual-productos.md) ·
[Manual de Reportes](manual-reportes.md) · [Manual de Caja](manual-caja.md)
