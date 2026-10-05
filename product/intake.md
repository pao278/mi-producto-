# Intake de producto — PredictiFlow (nombre provisional)

> Estado: VALIDADO — v3 (2026-10-05). v3: actualización de fuentes tras la auditoría de evidencia.
> v2: Reorganización de la v1 validada según la estructura
> de `/prepare-product-context`.
> Insumo para `/start-product`. Foco de esta etapa: el problema, no la solución.

**Fuentes**

- [F1] Presentación `PredictFlow_Final_DM`, elaborada por un equipo original del que formaba parte
  la responsable del proyecto (resumida por ella en la conversación; el archivo original no está
  en esta carpeta).
  **Actualización v3 (2026-10-05):** el archivo original ya está disponible en
  `sources/PredictFlow_Final_DM.pptx` (23 diapositivas con notas del presentador; 4 autores, entre
  ellos la responsable del proyecto, diap. 22).
- [F2] Descripción del proyecto "Mi Producto AFPM".
- [R] Indicaciones de la responsable del proyecto en la conversación del 2026-10-05.

**Estados:** hecho · supuesto · decisión · pregunta abierta · conflicto.
"Hecho documental" = el dato aparece en una fuente; no implica que sea cierto para el segmento.

---

## 1. Solicitud / origen

- El trabajo es el proyecto individual del curso AI-First Product Manager (Alaimo Labs). — hecho [F2]
- Objetivo declarado: construir el producto desde cero, con evidencia y sin asumir funcionalidades
  antes del discovery. — hecho [F2]
- La idea proviene de la presentación PredictFlow_Final_DM, elaborada por un equipo del que formaba
  parte la responsable del proyecto. Ahora ella la retoma y la desarrolla de forma individual
  para el curso. — hecho [R]
- Los roles de PM y especialista Data/ML descritos en [F1] corresponden al equipo original y no
  representan necesariamente el equipo actual del proyecto. — hecho [R]
- Responsable del trabajo: la responsable del proyecto. — hecho [R]
- Sponsor o solicitante distinto de la responsable del proyecto: no identificado. — pregunta abierta

## 2. Propósito preliminar

> Preliminar. No valida la demanda ni define una oportunidad.

Explorar si existe una oportunidad para ayudar a empresas de comercio electrónico a identificar,
antes del despacho, pedidos o condiciones que puedan derivar en devoluciones y reclamos, con el fin
de disminuir costes prevenibles, proteger margen y reducir carga operativa.

Esta formulación **no** da por demostrado que:

- las devoluciones puedan anticiparse con precisión suficiente;
- exista una acción útil antes del envío;
- intervenir genere ahorro neto;
- todas las devoluciones sean prevenibles;
- un modelo predictivo sea la respuesta adecuada.

**Resultados esperados por el equipo original (no demostrados)** [F1]:

1. **Rentabilidad:** menos devoluciones, menos costes logísticos y operativos, margen protegido.
2. **Operación:** menos carga por reclamos y devoluciones; más tiempo disponible del equipo.
3. **Inventario:** menos producto inmovilizado durante la devolución; menos ventas perdidas por falta de stock.

## 3. Contexto del producto o iniciativa

| Campo | Valor | Estado |
|---|---|---|
| Nombre provisional | PredictiFlow | Decisión provisional [F1] |
| Situación | Producto nuevo; no existe ni tiene usuarios | Hecho [F2] |
| Tipo | Producto digital B2B para operaciones de e-commerce | Hecho documental [F1] |
| Ámbito | Comercio electrónico | Hecho documental [F1] |
| Segmento declarado | Marcas pequeñas y medianas | Intención declarada [F2]; sin definir con datos |
| Plataformas mencionadas | Shopify, WooCommerce, CSV | Hecho documental [F1]; no validado como segmento |
| Momento de intervención propuesto | Antes del despacho del pedido | Hecho documental [F1]; no validado |

### 3.1 Planteamiento del equipo original (no es un problema definido)

- Hipótesis de contexto: "vender más no necesariamente significa ganar más". Al crecer las ventas
  pueden crecer devoluciones, reclamos, atención, logística inversa e inventario inmovilizado.
  Cadena planteada: **más pedidos → más incidencias → más presión sobre el margen.** — supuesto [F1]
- Proceso actual descrito: **pedido → envío → reclamo → devolución → reembolso.** El problema se detecta
  después del envío, cuando ya se comprometieron transporte, soporte, gestión operativa, inventario
  y logística inversa. — supuesto [F1]; no observado en ninguna tienda

### 3.2 Fricciones señaladas

| Grupo | Descripción | Estado |
|---|---|---|
| A. Capacidad operativa | Saturación del equipo por correos, revisiones, seguimiento y coordinación manual de incidencias | Supuesto [F1]; sin medición propia |
| B. Inventario / capital de trabajo | El producto deja de estar disponible mientras vuelve; luego requiere revisión, acondicionamiento y reincorporación | Supuesto [F1]; sin medición propia |
| C. Repetición de causas | Posibles patrones recurrentes: talla, imágenes, descripción del producto, comportamiento de compra | Supuesto [F1]; sin datos sobre el peso de cada causa |

## 4. Actores

| Actor | Rol en el contexto | Qué se sabe | Fuente / estado |
|---|---|---|---|
| Responsable del proyecto | Desarrolla la idea de forma individual; conduce el discovery y valida los artefactos | Formaba parte del equipo original que elaboró [F1] | Hecho [R] |
| Comprador | Tienda u organización de e-commerce (merchant, retailer, responsable de e-commerce) | No se sabe quién tiene presupuesto ni decide | Pregunta abierta [F1] |
| Usuario operativo | Persona o equipo que gestionaría los casos (operaciones, atención al cliente, logística, fulfillment, pedidos) | Rol sin definir | Pregunta abierta [F1] |
| Sponsor operativo (cliente) | Facilita el piloto y los cambios operativos | Mencionado como requisito del piloto | Supuesto [F1] |
| Responsable técnico (cliente) | Acceso a datos, integraciones, seguridad, permisos | Mencionado como requisito del piloto | Supuesto [F1] |
| PM / líder del piloto (equipo original) | Producto, coordinación, contacto con tiendas, UX básica | Rol del equipo original; no representa necesariamente el equipo actual | Hecho documental [F1]; aclarado [R] |
| Especialista Data / ML (equipo original) | Datos, modelo, integración, panel, alertas | Rol del equipo original; no representa necesariamente el equipo actual | Hecho documental [F1]; aclarado [R] |
| Cliente final | Compra y devuelve | No mencionado en [F1] | Pregunta abierta |

### 4.1 Vacío principal: el usuario

No está definido:

- quién sufre hoy más la carga de devoluciones;
- quién detecta y gestiona los reclamos;
- quién mide el coste de una devolución;
- quién es dueño del KPI de devoluciones;
- quién administra la tienda (Shopify/WooCommerce);
- quién es responsable de logística;
- quién tiene autoridad para cambiar, retener o cancelar un pedido;
- quién paga.

En una marca pequeña o mediana varios de estos roles pueden coincidir en una o dos personas. — supuesto

## 5. Sistemas, procesos o trabajo previo existentes

### 5.1 Concepto de solución del equipo original — APARCADO, NO VALIDADO [F1]

Se registra para no perderlo. No es punto de partida ni debe condicionar el discovery del problema.

Idea: analizar con IA patrones de compra y características de pedidos para anticipar el riesgo de
devolución antes del despacho y convertirlo en alertas accionables
("de reaccionar tarde a prevenir antes del despacho").

Componentes imaginados:

1. **Integración pasiva:** Shopify, WooCommerce, CSV.
2. **Modelo predictivo:** score de riesgo y patrones principales.
3. **Panel operativo:** ver, priorizar, filtrar, consultar motivos, revisar estado.
4. **Alertas:** antes del despacho, por correo o Slack, según umbral.

Capacidades propuestas: analítica predictiva de pedidos; detección de patrones de riesgo;
inteligencia operativa preventiva. Ninguna es requisito.

### 5.2 Plan de validación preliminar (planteado por el equipo original, no comprometido) [F1]

- **Datos:** ≈12 meses de histórico de pedidos, devoluciones y motivos, vía API o CSV;
  requieren perfilado, depuración, revisión de cobertura y consistencia de etiquetas.
- **Piloto:** 5–10 tiendas; luego prueba con pedidos reales, alertas y acciones del equipo.
- **Equipo proponente (original):** PM y especialista Data/ML. No representa necesariamente
  el equipo actual del proyecto. [R]
- **Del lado del cliente:** sponsor operativo, responsable técnico, usuarios que actúen.

| Métrica | Fórmula propuesta |
|---|---|
| Coste evitado | Devoluciones prevenidas × coste promedio por devolución |
| Margen protegido | Coste evitado + contribución recuperada − coste del piloto |
| Horas liberadas | Reclamos reducidos × tiempo medio de gestión |

También se plantea comprobar si las alertas son útiles, si el equipo actúa, si bajan las devoluciones
prevenibles y si no se perjudica la conversión. Cadena a distinguir:
**modelo → comportamiento → resultado → impacto económico.**

### 5.3 Riesgos identificados por el equipo original [F1]

| Riesgo | Situación | Consecuencia | Mitigación propuesta | Pregunta abierta |
|---|---|---|---|---|
| Datos | Etiquetas incompletas o motivos inconsistentes | Score poco fiable | Perfilar, depurar, validación temporal | ¿Cobertura/calidad mínima aceptable? |
| Negocio | Falsos positivos | Afecta ventas, conversión, experiencia | Umbral conservador y revisión humana | Coste del error vs. coste de la devolución |
| Adopción | El equipo no actúa | Impacto nulo | Co-diseñar alerta, mostrar motivos, SOP | — |
| Integración y seguridad | Retrasos por acceso, permisos, aprobaciones | Retraso del piloto | Conexión pasiva, mínimo dato, API/CSV | — |
| Línea base económica | La tienda no conoce el coste real de una devolución | ROI no calculable | Definir fórmula y capturar línea base antes del piloto | — |

## 6. Restricciones y dependencias conocidas

> Las restricciones de tiempo y presupuesto proceden de la propuesta del equipo original.
> No se ha confirmado si aplican al proyecto individual actual. — pregunta abierta (§10.1)

- Tiempo: fijo. — declarado [F1]; valor en conflicto (§11.1)
- Presupuesto: máximo 30.000 € como regla de decisión. — declarado [F1]; en conflicto (§11.2)
- Calidad: protegida (utilidad, explicabilidad, seguridad). — declarado [F1]
- Alcance: flexible; primera variable a recortar (menos integraciones, menos funciones). — declarado [F1]
- Dependencia crítica: acceso a los datos y su calidad (histórico completo, consistente,
  con vínculo pedido–devolución y motivos fiables). — declarado [F1]
- Dependencia: acceso técnico, permisos, seguridad y aprobación de integración en cada tienda. — declarado [F1]

## 7. Hechos y evidencia disponibles

### 7.1 Hechos documentales [F1, salvo indicación]

1. Existe una propuesta llamada PredictiFlow.
2. Está orientada al comercio electrónico.
3. La presentación sitúa la intervención antes del despacho.
4. Se propone usar datos históricos y modelos predictivos.
5. Se contempla trabajar con pedidos, devoluciones y motivos.
6. Se plantean ≈12 meses de histórico.
7. Se contemplan API y CSV como acceso.
8. Se mencionan Shopify y WooCommerce.
9. Se propone un panel operativo.
10. Se proponen alertas por correo o Slack.
11. Se prevé revisión humana ante ciertos riesgos.
12. Se propone un piloto de 5–10 tiendas.
13. Se identificaron riesgos de datos, negocio, adopción, integración y medición.
14. Se definieron como métricas económicas coste evitado, margen protegido y horas liberadas.
15. El acceso y la calidad de los datos son una dependencia crítica.
16. Hay inconsistencia documental sobre duración y presupuesto.
17. El producto se construye desde cero y está enfocado en marcas pequeñas y medianas. [F2]
18. No hay datos propios de ninguna tienda del segmento.

### 7.2 Cifras citadas en la presentación

| Dato | Valor | Contexto | Fuente citada en F1 | Estado |
|---|---|---|---|---|
| Facturación e-commerce España, Q2 2025 | 28.346 M€ | Incluye bienes y servicios; indica escala del canal, no volumen devolvible | CNMC (Q2 2025), vía informe de investigación intermedio (diap. 2) | Hecho documental [F1] |
| Crecimiento interanual | +22,6 % | España | CNMC (Q2 2025), vía informe intermedio (diap. 2) | Hecho documental [F1] |
| Hogares que compran online | 56,7 % | España, **2024** | INE (2024), vía informe intermedio (diap. 2) | Hecho documental [F1] |
| Ventas online devueltas | 19,3 % (≈1 de cada 5) | Benchmark retail EE. UU., 2025 | NRF & Happy Returns (2025) (diap. 4) | Hecho documental [F1] |
| Coste de la devolución | ≈17 % del coste primario del producto | Muestra de 2.229 devoluciones, moda y calzado | Gustafsson, Jonsson & Holmström (2021), IJPDLM 51(8) (diap. 4) | Hecho documental [F1]; ver conflicto 9 |
| Composición de ese coste | ≈72 % transporte y manipulación; resto preparación, almacenamiento y capital inmovilizado | Mismo estudio | Gustafsson, Jonsson & Holmström (2021) — misma fuente | Hecho documental [F1]; ver conflicto 9 |

**Límites:**

- Las fuentes están identificadas por la cita de F1, pero no se han consultado los documentos
  originales. Deben verificarse antes de extrapolarlas al segmento objetivo. (v3)

- Los benchmarks vienen de contextos distintos (país, sector, año) y **no deben combinarse**
  en una única estimación económica (advertencia de la propia presentación).
- **No demostrado:** que las tiendas objetivo tengan una tasa del 19,3 %, un coste del 17 %
  o una estructura de costes parecida.
- La evidencia de mercado es de España y EE. UU.; el mercado objetivo no está definido.

## 8. Supuestos no verificados

### 8.1 Hipótesis de oportunidad del equipo original [F1]

> Parte de las devoluciones y reclamos de un e-commerce podría anticiparse con señales disponibles
> antes del despacho, permitiendo acciones preventivas que reduzcan costes y protejan margen.

| # | Subhipótesis | Tipo | Por qué sigue sin verificar |
|---|---|---|---|
| H1 | Devoluciones y reclamos tienen frecuencia y coste suficientes para justificar una intervención | Valor (problema) | No hay datos ni entrevistas con tiendas del segmento |
| H2 | Una parte significativa de las devoluciones es prevenible | Valor (problema) | No se conocen las causas en tiendas del segmento |
| H3 | Los datos previos al despacho contienen señal suficiente para distinguir pedidos de mayor riesgo | Factibilidad | No se ha analizado el histórico de ninguna tienda |
| H4 | Existe una acción útil que cambia el resultado (predicción → acción → cambio) — **crítica** | Valor / uso | No se ha probado ninguna acción |
| H5 | El coste de intervenir es menor que el coste evitado | Viabilidad | No hay línea base de costes |
| H6 | La intervención no deteriora conversión, experiencia, tiempo de preparación, cumplimiento de entrega ni ingresos | Viabilidad | No se ha probado ninguna intervención |

### 8.2 Supuestos que no son hechos

| # | Supuesto | Tipo | Por qué sigue sin verificar |
|---|---|---|---|
| S1 | Las devoluciones son uno de los problemas prioritarios de las tiendas objetivo | Problema | Sin entrevistas ni datos de tiendas |
| S2 | El impacto económico justifica una solución específica | Problema | Sin línea base de costes |
| S3 | Una proporción relevante de devoluciones es prevenible | Problema | Causas desconocidas en el segmento |
| S4 | Las causas pueden detectarse con datos disponibles antes del despacho | Factibilidad | Sin análisis de datos |
| S5 | Un modelo de IA puede lograr precisión suficiente | Factibilidad | Sin datos ni modelo probado |
| S6 | Un score de riesgo cambia decisiones | Uso | Sin usuarios ni prueba de uso |
| S7 | Los equipos operativos quieren recibir alertas | Uso | Sin consulta a usuarios |
| S8 | Los usuarios actuarán sobre ellas | Uso | Sin prueba de uso |
| S9 | Existe una acción preventiva efectiva para un pedido de alto riesgo | Valor | Ninguna acción probada |
| S10 | Esa acción no perjudica conversión ni experiencia | Viabilidad | Ninguna acción probada |
| S11 | Las tiendas tienen histórico suficientemente limpio | Factibilidad | No se han revisado datos de tiendas |
| S12 | Los motivos de devolución se registran de forma consistente | Factibilidad | No se han revisado datos de tiendas |
| S13 | 5–10 tiendas son una muestra adecuada | Validación | Sin justificación documentada |
| S14 | 12 meses de histórico son suficientes | Validación | Sin justificación documentada |
| S15 | Shopify/WooCommerce son el segmento/plataforma inicial adecuado | Segmento | Segmento sin definir |
| S16 | Email o Slack son canales adecuados | Solución | Sin consulta a usuarios |
| S17 | El comprador está dispuesto a pagar por prevenir devoluciones | Viabilidad | Sin conversación con compradores |
| S18 | El ahorro supera el coste del producto y de las acciones preventivas | Viabilidad | Sin línea base ni precio |

S1–S3 son los supuestos de problema y deberían atacarse primero.

## 9. Decisiones ya tomadas

- Retomar y desarrollar la idea de forma individual para el curso, partiendo de la presentación
  del equipo original. — Responsable del proyecto [R], 2026-10-05
- Centrar esta etapa en el problema y no en la solución. — Responsable del proyecto [R], 2026-10-05
- Registrar el concepto de solución existente como aparcado y no validado. — Responsable del proyecto [R]
- No usar como contexto el `product/overview.md` actual (caso compartido de Microsoft Teams). — Responsable del proyecto [R].
  **RESUELTO (v3, 2026-10-05):** `product/overview.md` ya contiene PredictiFlow (v1 validada en `/start-product`).
- Nombre provisional: PredictiFlow. — [F1]
- Regla de priorización: tiempo fijo, calidad protegida, alcance flexible. — [F1]; los valores
  de tiempo y presupuesto están en conflicto (§11) y no se ha confirmado si aplican al proyecto actual (§6)

## 10. Preguntas abiertas y decisiones pendientes

### 10.1 Decisiones pendientes — Responsable: responsable del proyecto

- Si las restricciones de tiempo y presupuesto de [F1] aplican al proyecto individual actual (§6).
- Duración vigente del MVP (§11.1).
- Presupuesto aprobado del piloto (§11.2).
- Segmento inicial (§11.3).
- Enfoque: gestión de la devolución o solo prevención (§11.4).

### 10.2 Sobre el problema — Responsable: sin asignar (discovery)

- ¿Cuál es el coste real de una devolución en las empresas objetivo?
- ¿Con qué frecuencia ocurren?
- ¿Cuáles son sus causas principales?
- ¿Qué porcentaje sería realmente prevenible?
- ¿Cuál es el impacto en margen, en horas de trabajo y en inventario?
- ¿Está este problema entre sus prioridades principales?
- ¿Qué hacen hoy para resolverlo?
- ¿Qué herramientas usan?

### 10.3 Sobre el segmento — Responsable: sin asignar

- ¿Segmento inicial: moda, calzado, retail general, D2C, marketplaces?
- ¿Qué tamaño de tienda, qué GMV, qué volumen mensual de pedidos?
- ¿Qué tasa de devoluciones tienen?
- ¿Shopify/WooCommerce es el punto de entrada adecuado?

### 10.4 Sobre el usuario y el comprador — Responsable: sin asignar

- ¿Quién gestionaría el problema a diario (atención al cliente, operaciones, almacén, e-commerce, logística)?
- ¿Quién tiene autoridad para actuar sobre un pedido?
- ¿Quién paga (Head of E-commerce, COO, Operations, CFO, Logística, Customer Experience, el propio fundador)?

### 10.5 Sobre el momento de intervención — Responsable: responsable del proyecto

> Pendiente: el texto original se cortó al inicio de este bloque. Completar con las preguntas
> de la responsable del proyecto.

Preguntas derivadas de H4–H6 (reformulan lo ya dicho, no añaden contenido):

- ¿Cuánto tiempo pasa entre el pedido y el despacho en las tiendas objetivo?
- ¿Qué acciones serían posibles en ese intervalo?
- ¿Qué parte de las causas se origina antes del despacho y qué parte después
  (producto, transporte, expectativa del cliente)?

### 10.6 Sobre el origen del trabajo — Responsable: responsable del proyecto

- ¿Existe un sponsor o solicitante además de la responsable del proyecto?

## 11. Conflictos o incertidumbres en las fuentes

1. **Duración del MVP:** aparecen 10 semanas y 12 semanas. — [F1]
2. **Presupuesto:** aparecen 15–25k €, máximo 30k € y 30–40k €. — [F1]
3. **Segmento:** [F2] habla de marcas pequeñas y medianas; [F1] de e-commerce en general,
   con benchmarks de moda/calzado y retail. — [F1], [F2]
4. **Enfoque:** [F2] describe "gestión de devoluciones"; [F1] dice que no busca gestionar mejor la
   devolución, sino prevenirla. Recomendable no cerrarlo antes del discovery. — [F1], [F2]
5. **Individual o equipo — RESUELTO (2026-10-05):** [F2] define un proyecto individual y [F1]
   describe un equipo (PM y especialista Data/ML). Aclaración: [F1] la elaboró un equipo original
   del que formaba parte la responsable del proyecto; ahora ella desarrolla la idea de forma
   individual, y esos roles no representan necesariamente el equipo actual. — [F1], [F2], [R]
6. **Fuente original no disponible — RESUELTO (v3, 2026-10-05):** la presentación se conocía solo por un resumen
   que no nombraba la fuente de los benchmarks. Ahora el original está en `sources/PredictFlow_Final_DM.pptx`
   y cita CNMC, INE, NRF & Happy Returns (2025) y Gustafsson, Jonsson & Holmström (2021). — [F1]
7. **Texto incompleto:** las preguntas sobre el momento de intervención llegaron cortadas. — [R]
8. **Archivo mal ubicado — RESUELTO (v3, 2026-10-05):** `product/overview.md` contenía el caso compartido de
   Microsoft Teams; ya fue reemplazado por el overview de PredictiFlow. — [R]
9. **Discrepancia de cifras dentro de F1 (nuevo, v3):** las diap. 4 y 23 muestran 17 % del coste primario
   y 72 % transporte y manipulación; las notas del presentador de las diap. 11 y 23 citan 17,6 % y 65 %,
   con "fuente primaria no visible". Sin resolver; verificar en Gustafsson, Jonsson & Holmström (2021). — [F1]

## 12. Traspaso a /start-product

**Contexto reutilizable:**

- Producto nuevo, construido desde cero (§3).
- Proyecto individual a partir de una idea del equipo original (§1).
- Propósito preliminar y resultados esperados (§2).
- Actores conocidos y vacíos sobre el usuario (§4).
- Restricciones y dependencias (§6).
- Hechos documentales y cifras con sus límites (§7).

**Lo que /start-product debe confirmar:**

- Modo: nuevo · comercial (B2B; la tienda pagaría). Comercial se infiere de [F1] y de S17;
  debe confirmarlo la responsable del proyecto.
- Para quién, de forma específica (§4.1) y el segmento inicial (§11.3).
- Enfoque del problema: gestión o prevención (§11.4).
- Quién paga y qué haría que pague (S17, S18).
- Restricciones vigentes del proyecto individual: tiempo y presupuesto (§6, §11.1, §11.2).

**Lo que sigue siendo supuesto y no debe tratarse como evidencia:**

- H1–H6 y S1–S18 (§8).
- El proceso actual y las fricciones descritas por el equipo original (§3.1, §3.2).
- La aplicación de los benchmarks al segmento objetivo (§7.2).
- El concepto de solución y su plan de validación (§5.1, §5.2).

> Esta skill no ha validado la demanda ni ha definido una oportunidad.

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-05 | Versión inicial | Contexto aportado por la responsable del proyecto | Sí |
| v2 | 2026-10-05 | Reorganización según la estructura de `/prepare-product-context`; se añaden §1, §9, §12, motivos de los supuestos, responsables y los conflictos 5–8; se incorpora la aclaración sobre el equipo original (conflicto 5 resuelto) | Ejecución de la skill oficial sobre la v1; aclaración de la responsable del proyecto (2026-10-05) | Sí |
| v3 | 2026-10-05 | §Fuentes: F1 original disponible; §7.2: fuentes citadas por F1 (CNMC, INE 2024, NRF & Happy Returns 2025, Gustafsson, Jonsson & Holmström 2021) y límite de verificación; §9 y conflictos 6 y 8 marcados como resueltos; nuevo conflicto 9 (17 %/72 % vs 17,6 %/65 %) | Auditoría `product/opportunity-audits/2026-10-05-1555-coste-devoluciones-d2c.md` (P9, P10); F1 original diap. 2, 4 y notas diap. 11 y 23 | Sí |
