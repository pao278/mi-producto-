# Intake — PredictiFlow (nombre provisional)

> Insumo para `/start-product`. Recoge el contexto disponible sin añadir información nueva.
> Foco de esta etapa: **el problema**, no la solución. El concepto de solución existente se registra aparte (sección 9) y no está validado.

**Fuentes usadas**

- [F1] Presentación del equipo `PredictFlow_Final_DM` (resumida por la autora en el chat; el archivo original no está en esta carpeta).
- [F2] Descripción del proyecto "Mi Producto AFPM": producto enfocado en la gestión de devoluciones para marcas pequeñas y medianas.

**Convención:** *Hecho documental* = aparece en una fuente. *Supuesto* = no demostrado. *Pendiente* = decisión o dato que falta.

---

## 1. Identificación básica

| Campo | Valor | Estado |
|---|---|---|
| Nombre provisional | PredictiFlow | Hecho documental [F1] |
| Modo | Producto nuevo (se construye desde cero) | Hecho documental [F2] |
| Tipo | Producto digital B2B para operaciones de e-commerce | Hecho documental [F1] |
| Ámbito | Comercio electrónico | Hecho documental [F1] |
| Segmento declarado | Marcas pequeñas y medianas | Intención declarada [F2]; sin definir con datos |
| Plataformas mencionadas | Shopify, WooCommerce, CSV | Hecho documental [F1]; no validado como segmento |
| Momento de intervención propuesto | Antes del despacho del pedido | Hecho documental [F1]; no validado |

## 2. Propósito preliminar (formulación neutral)

Explorar si existe una oportunidad para ayudar a empresas de comercio electrónico a identificar, antes del despacho, pedidos o condiciones que puedan derivar en devoluciones y reclamos, con el fin de disminuir costes prevenibles, proteger margen y reducir carga operativa.

Esta formulación **no** da por demostrado que:

- las devoluciones puedan anticiparse con precisión suficiente;
- exista una acción útil antes del envío;
- intervenir genere ahorro neto;
- todas las devoluciones sean prevenibles;
- un modelo predictivo sea la respuesta adecuada.

## 3. Resultados de negocio esperados (no demostrados)

1. **Rentabilidad:** menos devoluciones, menos costes logísticos y operativos, margen protegido.
2. **Operación:** menos carga por reclamos y devoluciones; más tiempo disponible del equipo.
3. **Inventario:** menos producto inmovilizado durante la devolución; menos ventas perdidas por falta de stock.

Fuente: [F1]. Son beneficios esperados, no resultados observados.

## 4. El problema tal como se plantea

### 4.1 Hipótesis de contexto

"Vender más no necesariamente significa ganar más." Al crecer las ventas también pueden crecer devoluciones, reclamos, atención, logística inversa e inventario inmovilizado.

Cadena planteada: **más pedidos → más incidencias → más presión sobre el margen.** [F1]

### 4.2 Proceso actual descrito

**Pedido → envío → reclamo → devolución → reembolso**

El problema se detecta **después del envío**. Para entonces ya se comprometieron recursos de transporte, soporte, gestión operativa, inventario y logística inversa. [F1]

> Pendiente: este flujo es una representación del equipo. No se ha observado en ninguna tienda concreta.

### 4.3 Fricciones y consecuencias señaladas

| Grupo | Descripción | Estado |
|---|---|---|
| A. Capacidad operativa | Saturación del equipo por correos, revisiones, seguimiento y coordinación manual de incidencias | Planteado [F1]; sin medición propia |
| B. Inventario / capital de trabajo | El producto deja de estar disponible mientras vuelve; luego requiere revisión, acondicionamiento y reincorporación | Planteado [F1]; sin medición propia |
| C. Repetición de causas | Posibles patrones recurrentes: talla, imágenes, descripción del producto, comportamiento de compra | Planteado [F1]; **sin datos de tiendas que indiquen cuánto pesa cada causa** |

## 5. Evidencia cuantitativa disponible

| Dato | Valor | Contexto | Estado |
|---|---|---|---|
| Facturación e-commerce España, Q2 2025 | 28.346 M€ | Incluye bienes y servicios; indica escala del canal, no volumen devolvible | Hecho documental [F1] |
| Crecimiento interanual | +22,6 % | España | Hecho documental [F1] |
| Hogares que compran online | 56,7 % | España | Hecho documental [F1] |
| Ventas online devueltas | 19,3 % (≈1 de cada 5) | Benchmark retail EE. UU., 2025 | Hecho documental [F1] |
| Coste de la devolución | ≈17 % del coste primario del producto | Muestra de 2.229 devoluciones, moda y calzado | Hecho documental [F1] |
| Composición de ese coste | ≈72 % transporte y manipulación; resto preparación, almacenamiento y capital inmovilizado | Mismo estudio | Hecho documental [F1] |

**Límites:**

- Los benchmarks vienen de contextos distintos (país, sector, año). La propia presentación advierte que **no deben combinarse** en una única estimación económica.
- **No demostrado:** que las tiendas objetivo tengan una tasa del 19,3 %, un coste del 17 % o una estructura de costes parecida.
- No hay todavía datos propios de ninguna tienda del segmento (pequeña o mediana).
- La evidencia de mercado es de España y EE. UU.; el mercado objetivo no está definido.

## 6. Hipótesis de oportunidad

> Parte de las devoluciones y reclamos de un e-commerce podría anticiparse con señales disponibles antes del despacho, permitiendo acciones preventivas que reduzcan costes y protejan margen.

Es una hipótesis. Se descompone en:

| # | Subhipótesis | Tipo | Comentario |
|---|---|---|---|
| H1 | Devoluciones y reclamos tienen frecuencia y coste suficientes para justificar una intervención | Valor (problema) | Base de todo lo demás |
| H2 | Una parte significativa de las devoluciones es prevenible | Valor (problema) | Sin H2 no hay oportunidad pre-despacho |
| H3 | Los datos previos al despacho contienen señal suficiente para distinguir pedidos de mayor riesgo | Factibilidad | Depende de la calidad del histórico |
| H4 | Existe una acción útil que cambia el resultado (predicción → acción → cambio) | Valor / uso | **Crítica** |
| H5 | El coste de intervenir es menor que el coste evitado | Viabilidad | Revisiones, contactos, retrasos, cancelaciones |
| H6 | La intervención no deteriora conversión, experiencia, tiempo de preparación, cumplimiento de entrega ni ingresos | Viabilidad | Riesgo reconocido en [F1] (falsos positivos) |

En esta etapa, el foco recomendado está en **H1 y H2** (existencia y tamaño del problema) y en **cómo viven hoy el problema** las tiendas, antes de discutir H3–H6.

## 7. Actores identificados

| Actor | Descripción | Grado de definición |
|---|---|---|
| Comprador | Tienda/organización de e-commerce (merchant, retailer, responsable de e-commerce) | Bajo: no se sabe quién tiene presupuesto ni decide |
| Usuario operativo | Persona o equipo que gestionaría los casos (operaciones, atención al cliente, logística, fulfillment, gestión de pedidos) | Bajo |
| Sponsor operativo (cliente) | Facilita el piloto y los cambios operativos | Mencionado como requisito del piloto [F1] |
| Responsable técnico (cliente) | Acceso a datos, integraciones, seguridad, permisos | Mencionado como requisito del piloto [F1] |
| Afectado secundario | Cliente final que compra y devuelve | No mencionado en [F1]; se añade solo como pregunta |

Roles del equipo proponente (PM / líder del piloto; especialista Data/ML) se registran en la sección 10.

### 7.1 Vacío principal: el usuario

No está definido:

- quién sufre hoy más la carga de devoluciones;
- quién detecta y gestiona los reclamos;
- quién mide el coste de una devolución;
- quién es dueño del KPI de devoluciones;
- quién administra la tienda (Shopify/WooCommerce);
- quién es responsable de logística;
- quién tiene autoridad para cambiar, retener o cancelar un pedido;
- quién paga.

En una marca pequeña o mediana varios de estos roles pueden coincidir en una o dos personas. **Pendiente de verificar.**

## 8. Preguntas abiertas (prioridad para `/start-product`)

### 8.1 Sobre el problema

- ¿Cuál es el coste real de una devolución en las empresas objetivo?
- ¿Con qué frecuencia ocurren?
- ¿Cuáles son sus causas principales?
- ¿Qué porcentaje sería realmente prevenible?
- ¿Cuál es el impacto en margen, en horas de trabajo y en inventario?
- ¿Está este problema entre sus prioridades principales?
- ¿Qué hacen hoy para resolverlo?
- ¿Qué herramientas usan?

### 8.2 Sobre el segmento

- ¿Segmento inicial: moda, calzado, retail general, D2C, marketplaces?
- ¿Qué tamaño de tienda, qué GMV, qué volumen mensual de pedidos?
- ¿Qué tasa de devoluciones tienen?
- ¿Shopify/WooCommerce es el punto de entrada adecuado?

### 8.3 Sobre el usuario y el comprador

- ¿Quién gestionaría el problema a diario (atención al cliente, operaciones, almacén, e-commerce, logística)?
- ¿Quién tiene autoridad para actuar sobre un pedido?
- ¿Quién paga (Head of E-commerce, COO, Operations, CFO, Logística, Customer Experience, el propio fundador)?

### 8.4 Sobre el momento de intervención

> **Pendiente:** el mensaje original se cortó al inicio de este bloque ("Este bloque es especialmente crítico."). Completar con las preguntas de la autora.

Preguntas que se derivan directamente de H4–H6 (no son contenido nuevo, solo reformulan lo ya dicho):

- ¿Cuánto tiempo pasa entre el pedido y el despacho en las tiendas objetivo?
- ¿Qué acciones serían posibles en ese intervalo?
- ¿Qué parte de las causas se origina antes del despacho y qué parte después (producto, transporte, expectativa del cliente)?

## 9. Concepto de solución existente — NO VALIDADO

> Se registra para no perderlo, no como punto de partida. No debe condicionar el discovery del problema.

**Idea del equipo [F1]:** analizar con IA patrones de compra y características de pedidos para anticipar el riesgo de devolución antes del despacho y convertirlo en alertas accionables. Lema: pasar de "reaccionar tarde" a "prevenir antes del despacho".

Componentes imaginados:

1. **Integración pasiva:** Shopify, WooCommerce, CSV.
2. **Modelo predictivo:** score de riesgo y patrones principales.
3. **Panel operativo:** ver, priorizar, filtrar, consultar motivos, revisar estado.
4. **Alertas:** antes del despacho, por correo o Slack, según umbral.

Capacidades propuestas: analítica predictiva de pedidos; detección de patrones de riesgo; inteligencia operativa preventiva. Ninguna es requisito.

## 10. Plan de validación preliminar (planteado por el equipo, no comprometido)

- **Datos:** ≈12 meses de histórico de pedidos, devoluciones y motivos, vía API o CSV; requieren perfilado, depuración, revisión de cobertura y consistencia de etiquetas.
- **Dependencia crítica:** calidad y acceso a los datos (histórico completo, consistente, con vínculo pedido–devolución y motivos fiables).
- **Piloto:** 5–10 tiendas; luego prueba con pedidos reales, alertas y acciones del equipo.
- **Equipo proponente:** PM (producto, coordinación, contacto con tiendas, UX básica) y especialista Data/ML (datos, modelo, integración, panel, alertas).
- **Del lado del cliente:** sponsor operativo, responsable técnico, usuarios que actúen.

### 10.1 Métricas propuestas

| Métrica | Fórmula propuesta [F1] |
|---|---|
| Coste evitado | Devoluciones prevenidas × coste promedio por devolución |
| Margen protegido | Coste evitado + contribución recuperada − coste del piloto |
| Horas liberadas | Reclamos reducidos × tiempo medio de gestión |

También se plantea comprobar si las alertas son útiles, si el equipo actúa, si bajan las devoluciones prevenibles y si no se perjudica la conversión. Cadena a distinguir: **modelo → comportamiento → resultado → impacto económico.**

## 11. Riesgos identificados [F1]

| Riesgo | Situación | Consecuencia | Mitigación propuesta | Pregunta abierta |
|---|---|---|---|---|
| Datos | Etiquetas incompletas o motivos inconsistentes | Score poco fiable | Perfilar, depurar, validación temporal | ¿Cobertura/calidad mínima aceptable? |
| Negocio | Falsos positivos | Afecta ventas, conversión, experiencia | Umbral conservador y revisión humana | Coste del error vs. coste de la devolución |
| Adopción | El equipo no actúa | Impacto nulo | Co-diseñar alerta, mostrar motivos, SOP | — |
| Integración y seguridad | Retrasos por acceso, permisos, aprobaciones | Retraso del piloto | Conexión pasiva, mínimo dato, API/CSV | — |
| Línea base económica | La tienda no conoce el coste real de una devolución | ROI no calculable | Definir fórmula y capturar línea base antes del piloto | — |

## 12. Restricciones declaradas

| Variable | Valor | Observación |
|---|---|---|
| Tiempo | Fijo | Ver inconsistencia 1 |
| Presupuesto | Máximo 30.000 € (regla de decisión) | Ver inconsistencia 2 |
| Calidad | Protegida: utilidad, explicabilidad, seguridad | — |
| Alcance | Flexible; primera variable a recortar (menos integraciones, menos funciones) | — |

## 13. Inconsistencias a resolver (no corregidas)

1. **Duración del MVP:** aparecen 10 semanas y 12 semanas. *Pendiente: confirmar cuál es la restricción vigente.*
2. **Presupuesto:** aparecen 15–25k €, máximo 30k € y 30–40k €. *Pendiente: confirmar presupuesto aprobado para el piloto.*
3. **Segmento:** [F2] habla de marcas pequeñas y medianas; [F1] habla de e-commerce en general, con benchmarks de moda/calzado y retail. *Pendiente: confirmar si el foco es pymes y de qué sector.*
4. **Enfoque:** [F2] describe "gestión de devoluciones"; [F1] dice explícitamente que no busca gestionar mejor la devolución, sino prevenirla. *Pendiente: decidir si el problema a explorar es la devolución en sí (antes y después) o solo su prevención. Recomendable no cerrarlo antes del discovery.*

## 14. Hechos documentados

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

## 15. Supuestos que NO son hechos

| # | Supuesto | Tipo |
|---|---|---|
| S1 | Las devoluciones son uno de los problemas prioritarios de las tiendas objetivo | Problema |
| S2 | El impacto económico justifica una solución específica | Problema |
| S3 | Una proporción relevante de devoluciones es prevenible | Problema |
| S4 | Las causas pueden detectarse con datos disponibles antes del despacho | Factibilidad |
| S5 | Un modelo de IA puede lograr precisión suficiente | Factibilidad |
| S6 | Un score de riesgo cambia decisiones | Uso |
| S7 | Los equipos operativos quieren recibir alertas | Uso |
| S8 | Los usuarios actuarán sobre ellas | Uso |
| S9 | Existe una acción preventiva efectiva para un pedido de alto riesgo | Valor |
| S10 | Esa acción no perjudica conversión ni experiencia | Viabilidad |
| S11 | Las tiendas tienen histórico suficientemente limpio | Factibilidad |
| S12 | Los motivos de devolución se registran de forma consistente | Factibilidad |
| S13 | 5–10 tiendas son una muestra adecuada | Validación |
| S14 | 12 meses de histórico son suficientes | Validación |
| S15 | Shopify/WooCommerce son el segmento/plataforma inicial adecuado | Segmento |
| S16 | Email o Slack son canales adecuados | Solución |
| S17 | El comprador está dispuesto a pagar por prevenir devoluciones | Viabilidad |
| S18 | El ahorro supera el coste del producto y de las acciones preventivas | Viabilidad |

S1–S3 son los supuestos de problema y deberían atacarse primero.

## 16. Siguiente paso

Ejecutar `/start-product` con este intake, centrando la conversación en:

1. Segmento inicial (tamaño, sector, plataforma) — inconsistencia 3.
2. Quién vive el problema y quién paga — sección 7.1.
3. Existencia, frecuencia, coste y prevenibilidad del problema — S1–S3.
4. Completar las preguntas sobre el momento de intervención — sección 8.4.
