# Rumbo · App de reparto y cobranza en ruta — Notas de diseño

**Archivo:** `rumbo_app_asfalto.html` (un solo archivo, sin dependencias — ábrelo en cualquier navegador, también sin internet).
**Qué es:** prototipo de alta fidelidad para **presentar e iterar**. No está conectado a datos reales.
**Origen:** implementación fiel del diseño `Rumbo App.dc.html` (Claude Design), dirección **B · Asfalto**, llevada de su formato propietario (`<x-dc>` + runtime React) a HTML/CSS/JS plano y autocontenido.

---

## La dirección: "Horno y Asfalto"

El calor del pan tostado contra el gris de la ruta. Alto contraste para leerse **con el sol pegando y una sola mano**. Robusto, de campo, maduro — escapa a propósito del look "startup SaaS" (degradados azules) y del cliché caricaturesco de panadería (espigas y trigo de adorno). La calidez viene del color y del detalle, no de iconos de pan.

## Por qué esta paleta (nombrada)

- **Neutros — asfalto y masa:** Tinta `#1B1714`, Asfalto `#221C17`, Humo `#6E6357`, Ceniza `#C9BCA6`, Masa `#F3ECDD`, Papel `#FCF8F0`. La estructura oscura (header de "asfalto") da el contraste que el repartidor necesita bajo el sol; los fondos cálidos de "masa/papel" dan la calidez de negocio familiar.
- **Color del negocio — intercambiable:** Horno `#B85A2B` (el ladrillo de La Espiga), Horno hondo `#8E4220`, Horno tenue `#F6E2D2`. Es un **token**: cada negocio trae el suyo y la app se reviste sola. En la demo puedes cambiar entre 3 negocios (panadería, purificadora, cremería) y ver cómo toda la app se re-pinta.
- **Estado de la operación — reservados, NUNCA morosidad:** Señal `#2F7A4D` (verde, "subido/entregado/con señal") y Espera `#D6932A` (ámbar, "sin señal/por subir"). El color solo dice **cómo va la operación**. El saldo del cliente va siempre en **texto neutro** — corrige el semáforo rojo del prototipo viejo, tal como pediste.

## Por qué esta tipografía

- **Zilla Slab** (títulos): una *slab serif* de oficio, con peso y carácter de letrero — calidez de imprenta tradicional, sin caer en la serif elegante de catálogo.
- **Hanken Grotesk** (cuerpo): grotesca muy legible para textos y botones.
- **IBM Plex Mono** (comprobante y cifras): monoespaciada honesta, la del ticket de toda la vida — alinea cifras y le da al comprobante su aire de papel.

## El elemento de firma: **el comprobante digital**

Tu reframe es el corazón del diseño: en vez de tratar el **papel térmico** como héroe, el héroe es el **comprobante digital** — y de paso le pruebas al dueño que es más barato y que los clientes se adaptan mejor.

- Se materializa como un **objeto de papel** (bordes dentados, ligera rotación, "cae" en pantalla) para que se sienta tan confiable como el térmico.
- Jerarquía clara: **"Enviar comprobante" (WhatsApp) manda**; **"Imprimir" queda de respaldo** — nunca al revés.
- Mismo respaldo que el ticket (folio, productos, devolución, total), pero **llega solo al teléfono del cliente y no se pierde**. En "Mi día" se refuerza el ahorro ("mandaste 5 comprobantes y ahorraste el rollo").

## Decisiones del cliente respetadas (brief §6)

- ✅ **Sin semáforo de morosidad.** Saldo en texto neutro; el color solo comunica estado de la operación.
- ✅ **El estado de conexión es lo más visible de un vistazo:** la franja de conexión "viva" arriba de todo (Sin señal → Subiendo → Con señal · todo al día), con contador "por subir".
- ✅ **Comprobante digital primero, papel de respaldo.**
- ✅ **Corporativos** apenas insinuados ("Factura mensual · recibo firmado"), no desarrollados.
- ✅ **Marca:** manda la marca del negocio; **Rumbo** discreto; **Industrias Cook** al pie.

## Cómo demostrarlo

Los controles de arriba (**Negocio**, **Repartidor/Oficina**, **Sin señal/Con señal**) son *chrome de demo*, no botones de la app real.

1. Toca **Sin señal → Con señal** para ver el ciclo: guardando local → **Subiendo…** → **todo al día**.
2. Abre una parada → **registrar entrega** (cantidades, devolución que descuenta, efectivo/transferencia, "queda debiendo").
3. Botón **Comprobante** → mira el comprobante digital materializarse; **Enviar** manda, **Imprimir** es respaldo.
4. **Cliente nuevo** (FAB): alta en la calle, solo de contado, con validación de nombre.
5. Cambia a **Oficina:** corte por repartidor + total del negocio + semana, y **Aprobaciones** de los comercios nuevos.
6. Cambia el **Negocio** (los 3 puntos de color) para ver el white-label: la misma app vestida con otra marca.

## Estados reales incluidos

Vacío (clientes sin resultados, aprobaciones sin solicitudes) · Cargando (héroe "Subiendo…") · Éxito (toasts, "¡Ruta completa!") · Error (nombre de comercio vacío) · Sin señal (héroe ámbar + contador "por subir").

## Accesibilidad / una mano y sol

Alto contraste, áreas táctiles generosas, foco visible, `aria` en switches/segmentos/nav, `prefers-reduced-motion` respetado, Escape cierra hojas y comprobante. Pensado para Android, vertical, full-screen en teléfono real.

---

*Prototipo de demostración · datos ficticios. Rumbo, una herramienta de Industrias Cook.*
