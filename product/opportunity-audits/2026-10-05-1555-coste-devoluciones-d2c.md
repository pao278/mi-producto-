# Auditoría de evidencia — Oportunidad: coste de las devoluciones y reclamos en marcas D2C pequeñas y medianas

> Estado: VALIDADO — v1 (2026-10-05)
> Skill: `/audit-opportunity-evidence`
> Oportunidad auditada: [`product/opportunities/2026-10-05-1510-coste-devoluciones-d2c.md`](../opportunities/2026-10-05-1510-coste-devoluciones-d2c.md) (v1 auditada; revisada a v2 tras esta auditoría)
> Cambios aprobados por la responsable del proyecto: P1–P12 (2026-10-05)

## Metadatos

- **Oportunidad:** `product/opportunities/2026-10-05-1510-coste-devoluciones-d2c.md` (v1, `framed`).
- **Fecha:** 2026-10-05.
- **Contexto usado:**
  - [`product/intake.md`](../intake.md) v2 (`/prepare-product-context`);
  - [`product/overview.md`](../overview.md) v2 (`/start-product`);
  - la oportunidad v1 (`/frame-opportunity`);
  - **F1 original:** [`sources/PredictFlow_Final_DM.pptx`](../../sources/PredictFlow_Final_DM.pptx) (23 diapositivas con notas del presentador).
- **Alcance auditado:** marcas D2C pequeñas y medianas con tienda propia, moda y calzado (hipótesis de trabajo).
- **Límite de la auditoría:** las fuentes secundarias se identifican por la cita que da F1. No se
  han consultado los documentos originales de CNMC, INE, NRF & Happy Returns ni Gustafsson et al.

**Fuentes recuperables usadas**

| ID | Fuente | Ubicación |
|---|---|---|
| F1 | Presentación `PredictFlow_Final_DM` (equipo original; 4 autores, entre ellos la responsable del proyecto, diap. 22) | `sources/PredictFlow_Final_DM.pptx` |
| F2 | Descripción del proyecto "Mi Producto AFPM" | Claude Project |
| R | Indicaciones de la responsable del proyecto (2026-10-05) | Registradas en `product/intake.md` |
| CNMC | CNMC, facturación del comercio electrónico en España, Q2 2025 | Citada en F1, diap. 2, "vía informe de investigación"; no consultada |
| INE | INE, 2024, hogares que compran online | Citada en F1, diap. 2, "vía informe de investigación"; no consultada |
| NRF-HR | NRF & Happy Returns (2025) | Citada en F1, diap. 4; no consultada |
| GJH | Gustafsson, Jonsson & Holmström (2021), *International Journal of Physical Distribution & Logistics Management* (IJPDLM) 51(8) | Citada en F1, diap. 4; no consultada |

---

## Hallazgos principales

1. **No hay evidencia del problema en el segmento.** Las cuatro fuentes secundarias describen
   otros contextos. El título de la oportunidad v1 daba por hechas dos afirmaciones que solo hace
   el equipo original: que el coste no está medido (F1, diap. 23) y que las tiendas no saben por
   qué devuelven sus clientes (sin fuente).
2. **Discrepancia de cifras dentro de F1.** Las diap. 4 y 23 muestran 17 % y 72 %. Las notas del
   presentador de las diap. 11 y 23 dicen: *"17,6 % y 65 % aparecen en la presentación de
   referencia, pero la fuente primaria no está visible y debe verificarse antes de uso externo."*
   Queda abierta.
3. **Circularidad en "moda y calzado".** La categoría se eligió por el estudio de Gustafsson et al.,
   y ese mismo estudio aparece como señal de la oportunidad.
4. **Las cifras corresponden a otros contextos:**
   - 19,3 %: retail general de EE. UU. Happy Returns, coautor del informe, ofrece soluciones de
     devolución, lo que exige cautela.
   - 17 % y 72 %: moda y calzado, n = 2.229 devoluciones (no tiendas). País y tipo de empresa
     por verificar.
   - España: todo el e-commerce, incluidos servicios (advertido en F1, diap. 2).
5. **F1 contradice la exclusión de marketplaces.** El pitch define el problema para quien "escala
   en Shopify o Marketplaces" (diap. 5). La oportunidad excluye los marketplaces por definición.
6. **Lenguaje de solución en el segmento.** "Shopify/WooCommerce" procede de la integración pasiva
   (diap. 15).
7. **Mezcla de devoluciones y reclamos**, sin evidencia de que ocurran juntos ni de que los
   gestione la misma persona.

---

## Clasificación de la evidencia

| Categoría | Contenido |
|---|---|
| **Evidencia verificada** | Solo sobre el proyecto: es nuevo e individual, no tiene usuarios ni datos de ninguna tienda (F2, R, intake §7.1-18). F1 existe y tiene 4 autores, entre ellos la responsable del proyecto (diap. 22). |
| **Evidencia secundaria (fuente identificada)** | CNMC Q2 2025: 28.346 M€ y +22,6 %. INE 2024: 56,7 % de hogares compra online. NRF & Happy Returns 2025: 19,3 %. Gustafsson, Jonsson & Holmström 2021, IJPDLM 51(8): 17 % y 72 %. **Limitaciones:** contextos distintos; no corresponden necesariamente al segmento D2C pyme; deben verificarse antes de extrapolarlas. CNMC e INE se citan a través de un informe de investigación intermedio que no está en el proyecto. |
| **Señales no verificadas** | Fricciones de F1, diap. 3 (equipo saturado, inventario inmovilizado, "el patrón se repite"). Gráfico ventas vs margen (diap. 1), ilustrativo y sin datos. Discrepancia 17,6 % / 65 % (notas). Ventaja frente a "herramientas tradicionales" (diap. 5). Provenance `stakeholder`. |
| **Supuestos** | Cadena "más pedidos → más incidencias → más presión sobre el margen" (diap. 2). Detección después del envío (diap. 3). Coste no medido (diap. 19 y 23). Causas desconocidas. Devoluciones y reclamos como un mismo problema. H1–H6 y S1–S18. |
| **Inferencias** | Moda y calzado (circular). Roles acumulados en equipos de 1 a 3 personas. Modelo comercial. "Fundadores o responsables de operaciones" como actor. |
| **Decisiones** | Marcas pequeñas y medianas (F2/R). Exclusión de marketplaces (en tensión con F1, diap. 5). Cliente final fuera del segmento. Solución aparcada. Segmento sin plataforma específica (P3, 2026-10-05). |
| **Vacíos** | Quién sufre, gestiona y paga. Frecuencia, coste y causas en el segmento. Mercado geográfico. Prácticas y herramientas actuales. Casos negativos. Intake §10.5 incompleto. Origen de 17,6 % / 65 %. |

---

## Matriz afirmación–fuente

| ID | Afirmación | Tipo | Segmento / contexto | Fuente | Provenance | Fuentes indep. | Contradicciones / límites | Confianza | Acción |
|---|---|---|---|---|---|---:|---|---|---|
| C1 | Marcas D2C pequeñas y medianas | decisión | — | F2, R | stakeholder | 1 | F1 habla de e-commerce en general, incluidos marketplaces (diap. 5) | n/a | keep como decisión |
| C2 | Actor: fundadores o responsables de operaciones | inferencia | D2C pyme | overview | inferred | 0 | Rol sin definir | unsupported | research |
| C3 | Tienda propia Shopify/WooCommerce | supuesto | — | F1 diap. 15 (integración) y diap. 5 ("Shopify o Marketplaces") | stakeholder | 1 | Procede de la integración de la solución | low | rewrite (P3) |
| C4 | Moda y calzado | inferencia | — | Elegida a partir de GJH | inferred | 0 | Circular con C13 | unsupported | keep como hipótesis, marcar circularidad (P6) |
| C5 | Equipos de 1 a 3 personas con roles acumulados | supuesto | — | intake §4.1 | inferred | 0 | — | unsupported | research |
| C6 | Pierden margen | supuesto | D2C pyme | F1 diap. 1, 23 | stakeholder | 1 | Solo contexto secundario de otros segmentos | low | research (creencias 1 y 5) |
| C7 | Pierden tiempo del equipo | supuesto | — | F1 diap. 3 | stakeholder | 1 | Sin medición | unsupported | research |
| C8 | Pierden inventario disponible | supuesto | — | F1 diap. 3 | stakeholder | 1 | Sin medición | unsupported | research |
| C9 | No saben cuánto les cuesta (título v1) | supuesto | — | F1 diap. 19 (riesgo) y 23 | stakeholder | 1 | Tensión con la creencia 1 | unsupported en el segmento | rewrite (P1) |
| C10 | No saben por qué ocurren | supuesto | — | ninguna | unknown | 0 | F1 diap. 3 supone causas repetidas y reconocibles | unsupported | reclasificar (P1) |
| C11 | Más pedidos → más incidencias → más margen perdido | supuesto causal | — | F1 diap. 2 | stakeholder | 1 | CNMC e INE muestran escala del canal, no causalidad | unsupported | keep como supuesto |
| C12 | 19,3 % de ventas online devueltas | dato secundario | Retail EE. UU., 2025 | NRF-HR, vía F1 diap. 4 | secondary | 1 | Otro país y canal; coautor con interés comercial; verificar antes de extrapolar | medium (en su contexto) / unsupported (segmento) | narrow |
| C13 | Devolución ≈ 17 % del coste primario | dato secundario | Moda y calzado, n = 2.229 devoluciones | GJH, vía F1 diap. 4 | secondary (revisada por pares) | 1 | n son devoluciones; país y tipo de empresa por verificar; las notas de F1 citan 17,6 % | medium (en su contexto) / unsupported (segmento) | narrow; resolver la discrepancia |
| C14 | 72 % del coste es transporte y manipulación | dato secundario | Igual que C13 | GJH (misma que C13) | secondary | 0 adicionales | Las notas de F1 citan 65 % | medium (en su contexto) / unsupported (segmento) | fusionar con C13 (P2) |
| C15 | E-commerce España 28.346 M€, +22,6 % | dato secundario | España, Q2 2025, incluye servicios | CNMC, vía informe intermedio (F1 diap. 2) | secondary oficial | 1 | No habla de devoluciones; mercado objetivo sin definir | medium (en su contexto) / unsupported como señal del problema | quitar del "por qué ahora" (P4) |
| C16 | 56,7 % de hogares compra online | dato secundario | España, 2024 | INE, vía informe intermedio | secondary oficial | 1 | Año 2024, no Q2 2025; no habla de devoluciones | medium (en su contexto) / irrelevante como señal | contexto, no señal |
| C17 | Devoluciones y reclamos son un mismo problema | supuesto implícito | — | F1 | stakeholder | 1 | Pueden tener dueños y causas distintos | unsupported | separar (P5) |
| C18 | Modelo comercial: paga la tienda | inferencia | — | F1, S17 | inferred | 0 | — | unsupported | keep (creencia 4) |
| C19 | Se detecta después del envío | supuesto | — | F1 diap. 3 | stakeholder | 1 | — | low | keep como supuesto |
| C20 | Las herramientas actuales no detectan el riesgo a tiempo | supuesto de competencia | — | F1 diap. 5 | stakeholder | 1 | No se nombra ninguna herramienta | unsupported | research (`/research-market`) |

---

## Dependencia entre fuentes

| Fuentes que parecen distintas | Origen común | Consecuencia |
|---|---|---|
| intake, overview y oportunidad | F1 (y R) | 1 intermediario |
| F1 y R | La responsable del proyecto es coautora de F1 (diap. 22) | No son independientes |
| F1 | Sus notas citan "Presentaciones 5, 6 y 7" como fuente | F1 resume material anterior que no está en el proyecto |
| 17 % y 72 % | GJH | 1 fuente |
| CNMC e INE | "Informe de investigación" intermedio | 2 fuentes oficiales citadas de segunda mano |
| CNMC, INE, NRF-HR, GJH | — | 4 fuentes secundarias independientes entre sí; ninguna sobre el segmento |

## Separación por segmento

| Afirmación | Contexto de la fuente | Segmento objetivo | ¿Combinables? | Motivo |
|---|---|---|---|---|
| Tasa de devolución | Retail EE. UU. 2025 (NRF-HR) | D2C pyme moda | no | País, canal, tamaño y categoría distintos |
| Coste de la devolución | Moda y calzado (GJH) | D2C pyme | unknown | Verificar país, tamaño y canal del estudio |
| Escala del mercado | España (CNMC, INE) | Mercado sin definir | no | Incluye servicios; no mide devoluciones |
| Plataforma | "Shopify o Marketplaces" (F1 diap. 5) | Tienda propia, sin marketplaces | no | Decisión de alcance contraria a F1 |
| Devoluciones vs reclamos | Logística inversa | Atención al cliente | unknown | Pueden ser problemas distintos |

## Contradicciones y casos negativos

- **17 % / 72 % frente a 17,6 % / 65 %** (F1 diap. 4 frente a notas de diap. 11 y 23). Sin resolver;
  comprobar en GJH.
- **Gestión vs prevención:** F1 (notas diap. 22) dice *"el producto no gestiona devoluciones después
  del problema"*; F2 habla de "gestión de devoluciones". Sin resolver (creencia 5).
- **Marketplaces:** F1 los incluye en el problema (diap. 5); la oportunidad los excluye.
- **Tiempo y presupuesto en F1:** 10 semanas y 30–40 k€ (diap. 13–14); 12 semanas y máx. 30 k€
  (diap. 20); 12 semanas y 15–25 k€ (diap. 21). Confirma intake §11.1–11.2; no afecta a la oportunidad.
- **Tensión interna:** "coste no medido" frente a la creencia 1 ("sabe estimar el tiempo").
- **Casos negativos sin buscar:** pymes con tasas bajas, logística externalizada, uso de
  herramientas de devoluciones, coste asumido.
- **Desactualizaciones detectadas:** cabecera de la oportunidad (cita overview v1 pero usa la
  creencia 6 de la v2); intake §9 y §11.8 (overview de Teams); intake §11.6 (fuente original no
  disponible, benchmarks sin nombrar).

## Lenguaje de solución encontrado

| Texto original | Por qué viene de la solución | Problema que se conserva | Hipótesis que se aparca |
|---|---|---|---|
| "Shopify/WooCommerce" en el segmento | Integración pasiva (F1 diap. 15) | Marcas con tienda online propia | Plataforma de integración inicial (S15) |
| Restricción: "acceso al histórico de pedidos" | Dependencia del modelo (F1 diap. 14, 18) | Hacen falta datos para medir el problema | Requisito de datos de una solución basada en datos |
| "Talla, imágenes, descripción y comportamiento" como causa (F1 diap. 3) | "Comportamiento" es una variable de modelo | Causas recurrentes de devolución | Existencia de señales predictivas (S4) |
| "antes del despacho" (creencias 2 y 3) | Momento de intervención del concepto | — | Ya condicionado a la creencia 5; sin cambios |

## Resumen de confianza

- **Alta:** no hay evidencia del segmento; proyecto nuevo e individual; existencia y autoría de F1.
- **Media (solo en su contexto de origen):** C12, C13, C14, C15, C16. Fuentes identificadas pero no
  contrastadas con los originales; C13 y C14 con discrepancia en las notas de F1.
- **Baja o sin respaldo:** todas las afirmaciones sobre problema, actor, categoría, coste, causas y
  competencia en el segmento D2C pyme.

## Vacíos de investigación

- Comprobar en GJH (2021) si las cifras son 17 % / 72 % o 17,6 % / 65 %, y el contexto del estudio
  (país, tamaño, canal). — Discrepancia C13/C14.
- Comprobar en NRF-HR (2025) la definición de "ventas devueltas" y si hay datos por tamaño o
  categoría. — C12 no corresponde al segmento.
- ¿Las tiendas del segmento saben cuánto les cuesta una devolución y por qué devuelven sus
  clientes? — C9, C10.
- ¿Devoluciones y reclamos los gestiona la misma persona? — C17.
- ¿Qué plataforma usa el segmento y deben quedar fuera los marketplaces? — C3, C1.
- ¿Qué herramientas usan hoy? — C20.
- ¿Hay pymes D2C para las que las devoluciones no son un problema? — casos negativos.

---

## Oportunidad corregida

**Segmento / actor:** marcas D2C pequeñas y medianas con tienda online propia. Moda y calzado es
hipótesis de trabajo derivada de GJH (pendiente de la creencia 6). Actor concreto sin definir.

**Contexto:** venta online directa en la que la tienda asume las devoluciones y los reclamos.

**Problema (hipótesis):** las devoluciones, y posiblemente los reclamos como problema aparte,
podrían suponer un coste en margen, tiempo e inventario que la tienda no tiene cuantificado. Lo
afirma el equipo original (F1); no está observado en el segmento.

**Consecuencia:** supuesta pérdida de margen, horas e inventario disponible; no demostrada en el
segmento.

**Señales que se mantienen** (contexto secundario, no evidencia del segmento):

- 19,3 % de ventas online devueltas — NRF & Happy Returns (2025), retail EE. UU.
- Coste ≈ 17 % del coste primario, ≈ 72 % transporte y manipulación — Gustafsson, Jonsson &
  Holmström (2021), IJPDLM 51(8), moda y calzado. Una sola fuente; discrepancia con 17,6 % / 65 %
  pendiente.

**Señales debilitadas, separadas o retiradas:** CNMC e INE pasan a contexto de escala del canal y
salen del "por qué ahora"; fricciones de F1 diap. 3 reclasificadas como `stakeholder`; reclamos
separados de devoluciones.

**Contradicciones abiertas:** gestión vs prevención; marketplaces; 17 % / 72 % frente a 17,6 % / 65 %;
creencia 1 frente a "coste no medido".

**Creencias heredadas sin verificar:** 1–6 de `overview.md`, sin cambios.

**Estado de la auditoría:** `needs more evidence`.

---

## Cambios aprobados y aplicados (2026-10-05)

| # | Artefacto | Cambio | Evidencia |
|---|---|---|---|
| P1 | oportunidad | Título y primera frase: "coste no medido" y "por qué ocurren" pasan a supuestos atribuidos a F1 | F1 diap. 19, 23; C10 sin fuente |
| P2 | oportunidad | Tabla de señales con provenance `secondary` y citas; 17 % y 72 % como una fuente; limitaciones y discrepancia | F1 diap. 2, 4 |
| P3 | oportunidad, overview | Segmento: "tienda online propia"; plataforma aparcada como hipótesis de integración | F1 diap. 15; S15 |
| P4 | oportunidad | CNMC e INE fuera del "por qué ahora" | F1 diap. 2 |
| P5 | oportunidad | Reclamos separados de devoluciones como subproblema | C17 |
| P6 | oportunidad | Nota de circularidad en moda y calzado | C4, C13 |
| P7 | oportunidad | Cabecera aclarada; referencia a overview actualizada | — |
| P8 | overview | "Para quién" en condicional | C5 |
| P9 | intake | §9 y §11.8 marcados como resueltos | overview v2 existe |
| P10 | intake | §11.6 actualizado; §7.2 con citas y año INE 2024; nuevo conflicto 17 %/72 % vs 17,6 %/65 % | F1 diap. 2, 4; notas diap. 11, 23 |
| P11 | oportunidad | Exclusión de marketplaces registrada como contraria a F1 | F1 diap. 5 |
| P12 | proyecto | F1 añadido como fuente en `sources/PredictFlow_Final_DM.pptx` | — |

Las creencias 1–6 no se han marcado como confirmadas ni contradichas.

## Siguiente paso

`/research-market`: verificar las cifras en Gustafsson et al. (2021) y NRF & Happy Returns (2025),
resolver la discrepancia y avanzar con la creencia 6. Después, `/design-interview` para C9, C10,
C17 y C20.

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-05 | Versión inicial | `/audit-opportunity-evidence` sobre la oportunidad v1, con F1 original; aprobación de la responsable del proyecto (P1–P12) | Sí |
