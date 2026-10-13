# MyLittlePOS

**Punto de venta (POS) de escritorio** para negocios: punto de venta, productos e
inventario, categorías, impuestos, control de caducidades, clientes, descuentos y
promociones, reportes y tablero de indicadores. Corre en Windows, macOS y Linux.

Este repositorio es **solo de distribución**: acá se publican los instaladores y
el manifiesto que la app consulta para buscar actualizaciones. No hay código
fuente.

## Instalación

Elegí tu sistema operativo, descargá el instalador y ejecutalo:

| SO | Instalador | Pasos |
|----|-----------|-------|
| **Windows** | `releases/MyLittlePOS-1.0.0.exe` | Descargar y ejecutar el `.exe`, seguir el asistente. |
| **macOS** | `releases/MyLittlePOS-1.0.0.dmg` | Abrir el `.dmg` y arrastrar MyLittlePOS a **Aplicaciones**. |
| **Linux** | `releases/MyLittlePOS-1.0.0.deb` | `sudo apt install ./MyLittlePOS-1.0.0.deb` o doble clic en el `.deb`. |

> Los instaladores viven en la carpeta **[`releases/`](releases/)** de este repo,
> uno por versión. El manifest `latest.json` (en la raíz) siempre apunta al más reciente.

## Actualizaciones

Desde la app: **Acerca de → Buscar actualizaciones**. Si hay una versión nueva,
la app la descarga, verifica el hash y lanza el instalador.

## Documentación

- **Manual del usuario**: próximamente en [`docs/`](docs/).
