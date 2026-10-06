# Cierre de fase: Market Research

> Estado: **VALIDADO — v1 (2026-10-06).** Decidido por: la responsable del proyecto.
> Ruta: `product/decisions/2026-10-06-cierre-market-research.md`.
> Esta nota no modifica ningún otro artefacto.

## 1. Decisión

La fase de Market Research queda **cerrada** el 2026-10-06.

## 2. Research completados y validados

| Research | Ruta | Validado |
|---|---|---|
| Comparativa general de problemas de pymes de e-commerce | `product/research/2026-10-05-1853-comparativa-problemas-pymes-ecommerce.md` | v1, 2026-10-05 |
| A — Inventario | `product/research/2026-10-05-2320-inventario-pymes-ecommerce.md` | v1, 2026-10-05 |
| C — Conciliación y margen real | `product/research/2026-10-05-2259-margen-real-pymes-ecommerce.md` | v1, 2026-10-05 |
| D — Devoluciones y logística inversa (amplía 1618 y 1735) | `product/research/2026-10-06-0015-devoluciones-pymes-ecommerce.md` | v1, 2026-10-06 |
| E — Fraude, contracargos y abuso de reembolsos | `product/research/2026-10-05-2337-fraude-contracargos-pymes-ecommerce.md` | v1, 2026-10-05 |
| Comparación A vs C vs D vs E (insumo de análisis, no decisión) | `product/research/2026-10-06-0015-comparativa-candidatas-a-c-d-e.md` | v1, 2026-10-06 |

Antecedentes que se conservan sin cambios: research `…-1618-…` y `…-1735-…` de devoluciones, y la
decisión `product/decisions/2026-10-05-reabrir-problema-central.md` (opción B).

Los cuatro research de candidatas siguen la misma estructura (magnitud, prioridad, segmento, quién
lo sufre, comportamiento, coste, tendencias, geografía, competitive scan, evidencia en contra,
calidad de evidencia y conclusión). Por eso **A, C, D y E fueron comparadas con la misma vara**.

## 3. Estado del problema central

- **No se ha seleccionado definitivamente el problema central.** Toda la evidencia es secundaria;
  no se han aplicado K1–K5 ni hay datos primarios.
- **Inventario (A) queda como candidata prioritaria provisional** para el siguiente framing, por
  decisión de la responsable del proyecto. Lo que la sostiene en la comparación:
  - mediciones sobre datos reales de ventas (de proveedores);
  - prioridad intermedia en encuestas de operaciones;
  - pago ya existente por herramientas;
  - datos disponibles en la propia tienda;
  - dolor y compra concentrados en la tienda.

  Sus límites: toda la evidencia del problema es de EE. UU.; no hay ninguna fuente primaria sobre
  la gestión del inventario; y el mercado genérico está saturado.
- C, D y E **siguen siendo candidatas**: no se descartan.

## 4. Siguiente paso

Abrir una **nueva conversación** y ejecutar `/frame-opportunity` para Inventario. El framing se
centrará en los subproblemas donde el research detectó una posibilidad real de producto:

- **E1** — fiabilidad de la sincronización del stock entre canales y sistemas;
- **E3** — sobrestock y stock muerto (qué hacer con él);
- **E6** — planificación entre varias ubicaciones (FBA, AWD, 3PL, almacén propio).

Condiciones que ese framing debe tener en cuenta (implicaciones pendientes del research de A):

- separar el problema de **gestión** del problema de **precio**;
- delimitar el **solapamiento con C** (desajuste inventario–contabilidad, calidad del COGS);
- E1 y E6 dependen de vender en varios canales o ubicaciones: hay que revisar la **exclusión de
  marketplaces** del overview v3.

## 5. Lo que queda pendiente

| Pendiente | Cuándo |
|---|---|
| Actualizar `overview.md`, `intake.md`, F2 y creencias | **Después de cerrar el nuevo framing de Inventario** |
| P1 y P2 (umbrales K1–K5 y pesos C1–C12): propuesta presentada el 2026-10-06, **no validada ni guardada** | Antes del research primario |
| P6 — mercado geográfico | Antes del research primario |
| Briefs de A, C y E: quedaron en borrador y **no se guardaron**. Se reconstruyen a partir de sus research | En sus framings |
| Oportunidad D (`coste-devoluciones-d2c`): revisión a v3 con las correcciones de 1618 | Con la actualización global |
| Regla D/E (provisional): intención de engañar → E; devolución o reclamación legítima → D | Confirmar en el framing de D o E |
| Regla C/D (decidida el 2026-10-06): en D, coste generado por la devolución; en C, partida del margen; una sola pregunta en el research primario | — |
| GitHub: 5 commits locales sin subir (`git push` bloqueado desde la sesión) | Hacer `git push` desde el equipo de la responsable |

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-06 | Versión inicial | Cierre de la fase de Market Research decidido por la responsable del proyecto | Sí |
