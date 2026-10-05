---
status: framed
segment: Fundadores o responsables de operaciones de marcas D2C pequeñas y medianas con tienda propia (Shopify/WooCommerce), en moda y calzado — hipótesis de trabajo, no validada
personas: none yet
---

# Oportunidad: coste no medido de las devoluciones y reclamos en marcas D2C pequeñas y medianas

> Estado: VALIDADO — v1 (2026-10-05) · Fuentes: product/intake.md v2, product/overview.md v1

Las marcas D2C pequeñas y medianas podrían estar perdiendo margen, tiempo del equipo e
inventario disponible por las devoluciones y los reclamos, sin saber cuánto les cuesta ni por
qué ocurren. Hoy no tenemos evidencia del segmento de que ese coste exista, de que sea
prioritario ni de cuánto pesa. **Por qué ahora:** no lo sabemos; la única señal (crecimiento del
e-commerce en España) es `unverified` y no habla de devoluciones.

## Qué sabemos hoy

**Evidencia del segmento:** ninguna. No hay datos, encuestas ni entrevistas de tiendas
objetivo (intake §7.1, punto 18).

**Hechos documentales (existen en una fuente, no prueban el problema):**
- Existe una propuesta (PredictiFlow) del equipo original, conocida solo por un resumen (intake §11.6).
- El proyecto se dirige a marcas pequeñas y medianas [F2]: es una intención, no una señal de demanda.

**Supuestos (vienen de F1 y no se han comprobado):**
- La cadena "más pedidos → más incidencias → más presión sobre el margen" (§3.1).
- El problema se detecta después del envío (§3.1).
- Fricciones A (saturación operativa), B (inventario inmovilizado) y C (causas recurrentes) (§3.2).

**Inferencias (las sacamos nosotros, no aparecen en las fuentes):**
- Moda y calzado como categoría: sale de los benchmarks de F1.
- Una misma persona acumula los roles de gestión y decisión en tiendas de 1 a 3 personas (§4.1).
- Modelo comercial (la tienda paga): se infiere de F1 y S17.

**Vacíos:**
- Quién sufre el problema, quién lo gestiona y quién paga (§4.1, §10.4).
- Frecuencia, coste y causas de las devoluciones en el segmento (§10.2).
- Mercado geográfico: las cifras son de España y EE. UU.; el mercado objetivo no está definido.
- Qué hacen hoy las tiendas y con qué herramientas (§10.2).

## Segmento y personas

- **Sin personas todavía.** Faltan al menos dos: la persona que gestiona devoluciones y
  reclamos en el día a día, y la que decide la compra (pueden coincidir; es un supuesto).
  → Cuando haya investigación secundaria, `/generate-personas` puede cubrir este vacío.
  Las personas que salgan de ahí serán **provisionales** (hipótesis de persona) y no personas
  validadas. Para validarlas hará falta después evidencia primaria (encuestas o entrevistas
  con personas reales del segmento).
- **Quién quedaría fuera (por definición, no por evidencia):** marketplaces, grandes retailers
  y tiendas sin tienda propia.
- **Cliente final:** compra y devuelve, pero no forma parte del segmento de esta oportunidad
  (no se menciona en F1).

## Señales

| Señal | Provenance | Fuente |
|---|---|---|
| 19,3 % de las ventas online se devuelven (retail EE. UU., 2025) | unverified | F1 vía intake §7.2; fuente original sin nombrar |
| La devolución cuesta ≈17 % del coste primario del producto (moda y calzado, n = 2.229 devoluciones) | unverified | F1 vía intake §7.2; estudio sin nombrar |
| ≈72 % de ese coste es transporte y manipulación | unverified | F1 vía intake §7.2 |
| E-commerce España Q2 2025: 28.346 M€, +22,6 % interanual | unverified | F1 vía intake §7.2; indica escala del canal, no de devoluciones |
| La saturación operativa, el inventario inmovilizado y las causas recurrentes son fricciones | unverified | Equipo original (F1, §3.2) |

Las cifras vienen de contextos distintos y no deben combinarse ni aplicarse al segmento (§7.2).
No hay ninguna señal `real`, `survey`, `secondary` ni `synthetic`.

## Resultado de negocio

Modo comercial (inferido, no validado): ingreso recurrente que pagan marcas del segmento.
Para la tienda, el resultado esperado sería margen protegido, horas liberadas o inventario
disponible (F1, no demostrado). Cuál de los tres pesa más está sin resolver (creencia 5).

## Restricciones

- Proyecto individual del curso AFPM, construido desde cero [F2].
- Dependencia: cualquier análisis del problema con datos reales necesita acceso al histórico de
  pedidos y devoluciones de tiendas, y ese histórico debe tener calidad suficiente (§6).
- Tiempo y presupuesto: los valores de F1 están en conflicto y no se ha confirmado que apliquen
  al proyecto actual (§6, §11.1, §11.2). **No se registran como restricción hasta confirmarlos.**

## Creencias

Referencias a `product/overview.md`, el único registro de creencias:

- [product] [value] **1** — Las devoluciones y los reclamos están entre los 3 problemas principales
  y alguien dedica un tiempo semanal que sabe estimar. → *Creencia de valor de esta oportunidad.*
- [product] [viability] **4** — La persona que decide pagaría una cuota si ve el ahorro con sus
  propias cifras; hoy no conoce el coste real. → *Creencia de viabilidad de esta oportunidad.*
- [product] [value] **5** — El dolor está en el coste (margen, inventario) y no solo en la carga
  operativa. → *Decide si la oportunidad se orienta a gestión o a prevención.*
- [product] [value] **2** y **3** — Causas identificables antes del despacho y acción posible en ese
  intervalo. → *Solo son relevantes si la creencia 5 apunta a prevención.*
- [opportunity: coste-devoluciones-d2c] [value] **6** — En las marcas D2C pequeñas y medianas de
  moda y calzado, la tasa de devolución supera el 15 % de los pedidos enviados. *(15 % es un
  umbral de trabajo provisional para poder refutar la creencia, no una cifra con respaldo.)*

## Agenda de investigación

| Creencia | Instrumento (de menor a mayor coste) | Decisión que desbloquea | Cuándo |
|---|---|---|---|
| 6 | `/research-market`: tasas de devolución por categoría y tamaño de tienda; mercado geográfico. Pregunta abierta: ¿la tasa de moda y calzado es más alta que la de otras categorías del mismo tamaño? | Mantener moda y calzado o cambiar de categoría; fijar el mercado | Primero; fecha pendiente |
| 1 | `/research-market` (prioridades de merchants en informes del sector) → `/design-survey` (ranking de problemas y horas semanales) | Seguir con la oportunidad, reformularla o descartarla | Después de la 6 |
| 5 | `/design-survey` (dónde duele: coste o carga) → `/design-interview` (por qué) | Resolver el conflicto §11.4: gestión o prevención | Con la encuesta de la 1 |
| 4 | `/research-market` (precios de herramientas de devoluciones existentes) → `/design-interview` con quien decide | Si el modelo comercial es plausible y quién es el comprador | Después de que la 1 se sostenga |
| 2 | `/research-market` (motivos de devolución por categoría) → entrevistas o datos de una tienda | Si vale la pena explorar la dirección de prevención | Solo si la 5 apunta a prevención |
| 3 | `/design-interview` (qué ocurre entre el pedido y el despacho) | Si existe una acción previa al envío | Solo si la 2 se sostiene |

## Ideas candidatas (no evaluadas)

- Modelo predictivo con score de riesgo y alertas antes del despacho (correo o Slack) — F1, intake §5.1.
- Integración pasiva con Shopify, WooCommerce o CSV — F1.
- Acciones antes del despacho: contactar al cliente, confirmar la talla, retener el pedido — overview, creencia 3.
- Herramienta para gestionar mejor la devolución una vez ocurre — enfoque de F2 ("gestión de devoluciones").

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-05 | Versión inicial | intake v2, overview v1; ajustes de la responsable del proyecto (creencia 6 sin comparación entre categorías; personas de `/generate-personas` como provisionales) | Sí |
