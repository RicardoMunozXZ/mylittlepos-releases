# MyLittlePOS

**Punto de venta (POS) de escritorio** para negocios: punto de venta, productos e
inventario, categorías, impuestos, control de caducidades, clientes, descuentos y
promociones, reportes y tablero de indicadores. Corre en Windows, macOS y Linux.

## Instalación

Descarga el instalador de tu sistema operativo desde la página de
**[Releases](https://github.com/RicardoMunozXZ/mylittlepos-releases/releases)**:

| SO | Instalador | Pasos |
|----|-----------|-------|
| **Windows** | `MyLittlePOS-<versión>.exe` | Ejecutar el `.exe` y seguir el asistente. |
| **Windows 7** | `MyLittlePOS-<versión>-w7.exe` | Instalar [VC++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x64.exe) primero (x64) o [x86](https://aka.ms/vs/17/release/vc_redist.x86.exe) si tu sistema es de 32 bits, y luego ejecutar el `.exe`. |
| **macOS** | `MyLittlePOS-1.0.0.dmg` | Abrir el `.dmg` y arrastrar MyLittlePOS a **Aplicaciones**. |
| **Linux** | `MyLittlePOS-<versión>.deb` | `sudo apt install ./MyLittlePOS-<versión>.deb` o doble clic en el `.deb`. |

Cada versión tiene su release con el instalador y las notas de la versión.

## Actualizaciones

Desde la app: **Acerca de → Buscar actualizaciones**. Si hay una versión nueva,
la app la descarga, verifica el hash y lanza el instalador.

## Documentación

Manuales de usuario en [`docs/`](docs/):

- [Configuración inicial](docs/manual-configuracion-inicial.md) — el asistente de la primera instalación.
- [Inicio de sesión](docs/manual-login.md) — entrar, credenciales y cerrar sesión.
- [Punto de Venta](docs/manual-punto-de-venta.md) — turnos, carrito, cobro, corte de caja y atajos.
- [Caja](docs/manual-caja.md) — turnos, movimientos de caja y corte.
- [Productos](docs/manual-productos.md) — catálogo, precios, stock, lotes y bajas.
- [Categorías](docs/manual-categorias.md) — agrupar productos.
- [Inventario](docs/manual-inventario.md) — las tabs de la sección, incl. Impuestos.
- [Compras](docs/manual-compras.md) — órdenes de compra a proveedores.
- [Clientes y Proveedores](docs/manual-clientes-proveedores.md) — gestión de terceros.
- [Descuentos y Promociones](docs/manual-descuentos-promociones.md) — tipos de promo y vigencias.
- [Reportes](docs/manual-reportes.md) — ventas, compras, productos, stock bajo y clientes.
- [Configuración](docs/manual-configuracion.md) — negocio, empleados, permisos, sistema y respaldos.
