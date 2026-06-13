# Rumbo — Demo

**Rumbo** es el producto **parametrizable** de **Industrias Cook**: una sola app de **reparto y cobranza en ruta** que se *viste* con la marca de cada negocio que la renta. Este repositorio es un **demo de alta fidelidad** (prototipo navegable, sin datos reales) para presentar e iterar.

> ### Proyecto aparte de Cook's Fashion v2 — a propósito
> **Cook's Fashion v2** es la *herramienta interna* del negocio (single-tenant, Flutter). **Rumbo** es la versión **multi-negocio / white-label**, y vive en su **propio repositorio** para poder divergir libremente sin tocar la herramienta real (regla #1 de Cook's: nada de multi-tenant en ese repo). Este demo es el primer paso de esa línea.

## Abrir

Doble clic en **`index.html`** — un solo archivo, sin build ni dependencias. Abre en cualquier navegador (mejor en móvil/vertical, que es donde la usaría el repartidor).

*(Las tipografías cargan de Google Fonts: con internet se ven completas; sin internet usa las del sistema como respaldo.)*

## Qué muestra

Dirección visual **"Horno y Asfalto"** (camino B · Asfalto). Pantallas completas, en estados reales:

- **Repartidor:** Ruta del día con el héroe de conexión *Sin señal → Subiendo → Con señal*, **Registrar entrega** (cantidades, devolución que descuenta, efectivo/transferencia, "queda debiendo"), **Comprobante digital**, Alta de comercio en ruta, Clientes, Mi día.
- **Oficina:** Corte por repartidor + total del negocio + semana, Aprobaciones, Clientes.
- **White-label en vivo:** los 3 puntos de color de arriba cambian el negocio y **toda la app se reviste**.

Los controles de arriba (**Negocio / Repartidor·Oficina / Sin señal·Con señal**) son *chrome de demostración*, no botones de la app real.

## Decisiones del cliente respetadas

- **Saldo en texto neutro** — sin semáforo de morosidad por color. El color solo comunica el estado de la *operación* (pendiente/entregado, sin señal/subido).
- **Comprobante digital primero**, impresión de respaldo.
- La **marca del negocio manda**; *Rumbo* discreto; *Industrias Cook*, al pie.

## Archivos

- `index.html` — el demo completo (un solo archivo, HTML/CSS/JS vanilla).
- `NOTAS_DISENO.md` — por qué esa paleta, esa tipografía y ese elemento de firma.

## Estado

Prototipo de demostración · datos ficticios. Implementado a partir del diseño `Rumbo App.dc.html` (Claude Design), dirección **Asfalto**. No conectado a datos reales.

---

*Rumbo · una herramienta de Industrias Cook.*
