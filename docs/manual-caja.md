# Manual — Caja

> Corresponde a la versión 1.0.0. La caja no es una pantalla propia: se maneja desde el
> **Punto de Venta** (menú lateral → **Punto de Venta**).

La caja es el **turno**: el periodo entre el momento en que abrís la caja con una plata
inicial y el corte final del día. Todo lo que mueve efectivo —ventas en efectivo,
entradas y salidas manuales, compras que afectan caja— se acumula sobre ese turno.

## Abrir la caja

1. Andá al **Punto de Venta**. Si no hay turno abierto, se muestra la pantalla de apertura.
2. Cargá el **saldo inicial**: la plata que dejás en el cajón al empezar (no puede ser negativo).
3. Tocá **Abrir turno**.

Con el turno abierto, la cabecera del PV muestra **Caja: $…** con ese saldo inicial, y
aparecen los botones de **Movimiento** y **Corte**.

> Solo puede haber **un turno abierto a la vez**.

![Pantalla de apertura del turno con el saldo inicial de caja](imagenes/manual-pv-01-apertura-turno.png)

## Movimientos de caja

Los movimientos registran plata que entra o sale del cajón **sin ser una venta**:
un pago a un proveedor suelto, un retiro, un depósito, un ajuste.

1. Tocá **Movimiento** en el PV (con turno abierto).
2. Elegí el tipo: **Salida (gasto)** o **Entrada**.
3. Cargá el **monto** y el **motivo** (ambos obligatorios).
4. Tocá **Registrar**.

El movimiento queda pegado al turno actual y aparece en el corte.

> Los gastos grandes del negocio (alquiler, sueldos, luz) **no** van acá: se cargan en
> **Gastos** y no entran en el corte de caja.

![Diálogo Movimiento de caja con tipo, monto y motivo](imagenes/manual-pv-05-movimiento-caja.png)

## Qué más mueve la caja

- **Ventas en efectivo**: entran por el total de cada venta.
- **Ventas con tarjeta o transferencia**: NO tocan el efectivo del cajón; solo se
  informan en el corte.
- **Compras marcadas "Afecta el movimiento de caja"**: salen como egreso al finalizar
  la compra (ver [Manual de Compras](manual-compras.md)).
- **Devoluciones de esas compras**: vuelven como entrada.
- **Anulación de una venta**: la venta sale del corte y el stock vuelve.

## El corte

El corte cierra el turno y muestra el resumen del día.

1. Tocá **Corte** en el PV y confirmá (así no se cierra por un clic accidental).
2. Se muestra el informe:
   - **Ventas**: cantidad, artículos vendidos y total, desglosado en efectivo, tarjeta
     y transferencia.
   - **Saldo inicial**, **entradas** y **salidas** de caja.
   - **Efectivo que debería haber** (destacado): saldo inicial + ventas en efectivo +
     entradas − salidas. Contá el cajón y compará con ese número.
   - El detalle de **movimientos** y de **artículos vendidos** del turno.
3. Al terminar de revisar, elegí **Iniciar nuevo turno** (sigue cobrando) o
   **Cerrar sesión**.

![Corte de caja con ventas, movimientos y efectivo esperado](imagenes/manual-pv-07-corte.png)

---

**Ver también**: [Manual del Punto de Venta](manual-punto-de-venta.md) ·
[Manual de Compras](manual-compras.md)
