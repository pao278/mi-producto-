---
source: secondary
method: web
date: 2026-10-07
question: ¿Dónde existe una oportunidad suficientemente importante, demandada, financiable y poco resuelta dentro del ecosistema de Cash and Voucher Assistance como para justificar explorar un producto?
---

# Research: oportunidades de mercado en CVA — NexoAid

> Ruta: product/research/cva-market-opportunities.md (antes product/research/market-opportunities.md)
> Estado: VALIDADO — v1.1 (2026-10-07)
> Versión: v1.1 (la v1 sustituyó a los borradores 1 y 2 del 2026-10-07, no validados)
> Etapa: Problem Discovery
> Responsable: Paola Espejo
> Fecha: 2026-10-07
> Base: product/overview.md v1, product/intake.md v1, product/research/market-beliefs.md (v1; trazabilidad actualizada en v1.1)
> Documento derivado: product/research/opportunity-prioritization.md
> Cadena de research: creencias (market-beliefs.md) → exploración del mercado y comparación de oportunidades (este documento) → recomendación para research primario (opportunity-prioritization.md)

## 0. Cómo leer este documento

**Diferencia con market-beliefs.md.**
- `market-beliefs.md` pregunta si las creencias iniciales de NexoAid tienen respaldo.
- Este documento compara **espacios de mercado** y propone cuáles merecen pasar a investigación primaria.

**Qué no es.**
- No valida ninguna oportunidad.
- No elige producto, funcionalidad, MVP, arquitectura ni tecnología.
- La priorización final es **provisional** y se apoya solo en evidencia secundaria.

**Método.**
- Búsqueda web real, en dos rondas, el 2026-10-06 y el 2026-10-07.
- La segunda ronda tuvo seis líneas en paralelo:
  1. conciliación y operación con proveedores financieros (FSP);
  2. interoperabilidad y registro;
  3. monitoreo, reporting y quejas;
  4. fraude y datos;
  5. contextos frágiles, actores locales, comercios y protección social;
  6. demanda, pago, tamaño y América Latina.
- Varias líneas agotaron el cupo de búsquedas antes de terminar. Lo que quedó sin cubrir se marca como **pendiente** o **desconocido**.

**Notación.**
- Cada afirmación remite a un código de fuente entre corchetes, por ejemplo [A01]. La sección 13 da, para cada código, la URL, la organización, la fecha, el tipo de fuente, la oportunidad relacionada y la limitación. Todas las fuentes se consultaron el 2026-10-06 o el 2026-10-07.
- `[conocimiento del modelo — verificar]` marca lo que no se pudo confirmar en ninguna fuente.
- **COMERCIAL** marca lo que afirma un proveedor sobre sí mismo. Esas fuentes se usan para mapear competencia y capacidades, nunca como única prueba de demanda o severidad.
- Las valoraciones usan ALTA / MEDIA / BAJA / DESCONOCIDA. Cada una lleva su evidencia y su confianza (a = alta, m = media, b = baja). **No hay puntuación numérica.**

**Sesgos que el lector debe tener presentes.**
1. **Sesgo de auditoría.** La evidencia más dura sobre problemas operativos viene de auditorías de la ONU: OIOS sobre ACNUR y la Oficina del Inspector General del PMA. Esas agencias publican sus auditorías; las INGO medianas y las ONG locales casi nunca. El cuadro de severidad está inclinado hacia las agencias grandes, que son justo el segmento que menos compra a terceros.
2. **Sesgo de visibilidad del problema.** Que un problema aparezca en una auditoría no prueba que los usuarios lo perciban como prioritario ni que quieran pagar por resolverlo.
3. **Calendario.** El informe CALP *State of the World's Cash 2026* sale el 12-nov-2026 [M16] y probablemente actualizará buena parte de este documento.

---

## 1. Respuesta corta a las cinco preguntas

| Pregunta | Respuesta provisional | Confianza |
|---|---|---|
| 1. ¿Dónde está el problema más doloroso? | En el **ciclo de pago con el FSP**: qué se ordenó pagar, qué se pagó, qué no se cobró y cómo cuadra con la contabilidad (OP3). Y en su causa raíz, la **integridad de la lista y del identificador** (OP2). Hay descuadres de 71 M USD [A02], pagos marcados como exitosos con importe cero [A01], conciliaciones aprobadas 3–6 meses tarde [A06] y 3,6 M USD recuperados de tarjetas inactivas [A02]. Fuera de la operación, el dolor más grave para las personas está en la **liquidez en contextos de conflicto** (OP9), pero ese dolor no se resuelve comprando algo. | Media (casi todo es ONU) |
| 2. ¿Dónde hay demanda observable? | En **contratos FSP + tecnología** de INGO: Prosper Global 2025 [T02], Plan 2025 [T03], PUI 2021 [T11], Solidarités 2026 [T12]. En **plataformas CVA licitadas por separado** por INGO medianas y ONG locales: Diakonie 2024 [T06], Relief International 2026 [T01], SARD 2024 [T07]. En **monitoreo por terceros** (TPM) [T16, T18, T19] y en **centrales de llamadas interagencia** [T15]. No se observó compra específica de "conciliación", "deduplicación" ni "interoperabilidad". | Media |
| 3. ¿Dónde hay un comprador con capacidad plausible de pago? | En las **INGO grandes y medianas**, a través del contrato con el FSP o de licitaciones de plataforma pagadas como coste de proyecto. En **donantes y agencias ONU** para TPM. Las agencias ONU tienen dinero pero construyen sus sistemas (SCOPE, CashAssist, HOPE) [A01, M27]. Las ONG locales tienen necesidad y casi ningún presupuesto [M01, L11]. | Media-baja |
| 4. ¿Dónde dejan las alternativas un gap relevante? | En tres sitios: la **conciliación persona a persona** entre el sistema del programa, el informe del FSP y el ERP [A01, A02, A08]; la **trazabilidad de una queja hasta la corrección del dato o del pago** [A14, A16, A07]; y el **control de cambios de la lista** entre la versión final y el pago [D09, A08, A04]. En los tres casos las causas son en parte de proceso y gobernanza, no solo de herramienta. | Media-baja |
| 5. ¿Qué 2–3 oportunidades justifican research primario? | **OP3** Ciclo de pago con FSP y conciliación. **OP7** Quejas y feedback vinculados a la corrección de datos y pagos. **OP2** Integridad de la lista y del identificador. Ver sección 9. | Provisional |

**Conclusión, en los términos pedidos.** Estas tres oportunidades merecen investigarse primero con usuarios reales. La evidencia secundaria muestra problemas recurrentes y cuantificados en el tramo que va desde la lista de pago hasta el cierre, y señales de compra en INGO. Queda una incertidumbre central: no sabemos si INGO medianas y ONG locales sufren lo mismo que muestran las auditorías de la ONU, ni si alguien pagaría por reducirlo fuera del contrato del FSP.

---

## 2. Cambios en el mapa de oportunidades

El punto de partida eran las áreas O1–O11. La evidencia obliga a reorganizarlas. La lista de trabajo queda en **12 oportunidades (OP1–OP12)**, más **cinco áreas que se eliminan o reclasifican**.

| Área original | Decisión | Resultado | Por qué |
|---|---|---|---|
| "Interoperabilidad" (transversal) | **Se elimina como oportunidad** | Se reparte entre OP1, OP2, OP3 y OP5 | Es sobre todo una **causa** y una **capacidad de solución**, no el problema que viven los usuarios. Lo que se vive es duplicación, conciliación tardía, listas alteradas y reporte que no consolida. Fuentes: [D01, D03, D08]. Detalle en la sección 7. |
| O1 Registro / identidad / deduplicación | **Se divide** | OP1 Deduplicación entre organizaciones · OP2 Integridad de la lista y del identificador dentro de la organización | Tienen causas, decisores y competidores distintos. La deduplicación entre agencias es sobre todo gobernanza y ya tiene herramientas gratuitas [D05, M28]. La calidad del identificador es la causa raíz que OIOS señala en los pagos [A01, A04]. |
| O2 Integración y operación con FSP | **Se divide** | La parte operativa (instrucción de pago, estado, no cobrados) se **fusiona con O3** en OP3 · La contratación y el desempeño de FSP pasan a OP4 | El archivo de instrucción, el informe del FSP y la conciliación son la misma interfaz [A01, F05]. La contratación es un problema de procurement, con otros decisores [A10, F01, F02]. |
| O3 Conciliación | **Se fusiona** con la operación de O2 | OP3 Ciclo de pago con FSP y conciliación | Ver fila anterior. Incluye la conciliación del sistema de programa con el ERP y el cierre financiero [A02]. |
| O4 Monitoreo, reporting y trazabilidad | **Se divide en tres** | OP5 Reporting a donantes y coordinación · OP6 Monitoreo de resultados y verificación · O4c trazabilidad global de volúmenes de CVA, **eliminada** | Cada parte tiene comprador y saturación distintos [R01, T16, R05]. O4c es un problema de bien público (FTS, CALP) sin comprador individual [R05, R06]. |
| O5 Contextos frágiles / baja conectividad | **Se divide** | OP9 Entrega con liquidez o conectividad limitada (parte operativa) · O5b regulación, de-risking y prohibiciones, **eliminada como oportunidad de producto** | La parte sistémica se resuelve con política y regulación, no con una compra [L07, L06]. |
| O6 ONG nacionales y actores locales | **Se reencuadra** | OP10 Carga de cumplimiento y reporte que los intermediarios trasladan a los actores locales | Como "problema de herramientas de la ONG local", la evidencia dice que la barrera principal es la financiación y el poder [M35, L10, L11]. El comprador plausible es el intermediario o el donante, no la ONG local. |
| O7 Gestión de comercios | **Se mantiene, aplazada** | OP11 | Hay poca evidencia reciente y el peso de los vouchers baja [M04, L23]. |
| O8 Humanitario ↔ protección social | **Se divide** | OP12 Alineación de programas humanitarios con sistemas nacionales · O8a sistemas de gobierno (venta a gobiernos), **eliminada** | O8a es un mercado de venta a gobiernos, con préstamos de banca de desarrollo y bienes públicos digitales gratuitos [T23, L24]. Queda fuera del perfil B2B de NexoAid (overview). |
| O9 Quejas, feedback y rendición de cuentas | **Se mantiene, se precisa** | OP7 Quejas y feedback vinculados a la corrección de datos y pagos | La evidencia nueva apunta al tramo que va de la queja a la corrección [A14, A15, A16, A07]. La rendición de cuentas colectiva (percepción, comunicación) queda como contexto. |
| O10 Fraude, anomalías y control | **Se divide** | OP8 Detección tardía de anomalías y colusión en datos transaccionales · El screening de sanciones pasa a **requisito transversal** | El screening es un mercado saturado de proveedores de cumplimiento [X08] y una condición de entrada. La detección de anomalías con datos que nadie analiza es un gap documentado [A07, A10, X03]. |
| O11 Protección y gobernanza de datos | **Se reclasifica como requisito transversal** | Criterio de entrada para cualquier oportunidad | La oferta dominante es gratuita o subsidiada [X11, X13]. Los donantes la exigen [M17]. No hay evidencia de un mercado pagado propio. Un fallo aquí es un riesgo existencial para cualquier producto [X10, X09]. |
| — | **Nueva** | El control de cambios de la lista entre la versión final y el pago se integra en OP2 | Aparece en varias fuentes independientes [D09, A08, A12]. |

**Lista de trabajo final**

| ID | Oportunidad (actor + contexto + problema + consecuencia) |
|---|---|
| OP1 | Los equipos de gestión de información y los coordinadores de cash de organizaciones que asisten a la misma población no pueden saber a tiempo, y sin exponer datos, si un hogar ya recibe asistencia de otra. Resultado: doble asistencia, exclusión y meses de retraso en arrancar. |
| OP2 | Los equipos de programa, gestión de información y finanzas trabajan con listas cuyos identificadores faltan, se repiten o cambian entre el registro, la versión final y el pago. Resultado: pagos a registros inválidos o duplicados, conciliaciones imposibles y cambios no autorizados que nadie detecta. |
| OP3 | Los equipos de Finanzas y de Cash de organizaciones que pagan a través de FSP no logran casar a tiempo, persona a persona, lo ordenado, lo que el FSP reporta como pagado o cobrado y lo registrado en la contabilidad. Resultado: duplicados, pagos marcados como exitosos sin entrega y fondos no cobrados detectados tarde, cierres financieros con descuadres y hallazgos de auditoría. |
| OP4 | Los equipos de Cash, Procurement y Finanzas tardan meses en contratar FSP con procesos pensados para comprar bienes, y apenas evalúan su desempeño. Resultado: asistencia tardía, sobrecostes de comisión y dependencia de un único proveedor. |
| OP5 | Los equipos de MEAL y de grants de ONG con varios donantes reelaboran los mismos datos en formatos y definiciones distintos para cada donante y para la coordinación. Resultado: horas perdidas y reporte incompleto o inconsistente. |
| OP6 | Las oficinas de país en contextos de acceso restringido no alcanzan la cobertura ni la calidad de monitoreo exigidas, y no siguen hasta el cierre lo que encuentran. Resultado: poca evidencia de resultados, riesgo fiduciario y hallazgos de auditoría. |
| OP7 | Los equipos de rendición de cuentas y de programa reciben quejas por canales y sistemas desconectados y no pueden seguirlas hasta que se corrige el dato o el pago. Resultado: errores de pago e inclusión que persisten, fraude y abuso (PSEA) que no se detectan y pérdida de confianza. |
| OP8 | Las áreas de finanzas y cumplimiento detectan tarde la colusión y las anomalías, porque los datos de transacción existen pero nadie los analiza y los incidentes se reportan con semanas de retraso. Resultado: pérdidas y suspensiones de programas. |
| OP9 | Las ONG que entregan efectivo donde faltan liquidez o comunicaciones no logran que el dinero llegue a tiempo y a un coste razonable. Resultado: entre el 20 % y el 60 % del valor perdido en comisiones, o meses de retraso. |
| OP10 | Las ONG nacionales y locales deben cumplir requisitos de due diligence y de reporte que les imponen, por duplicado, varios intermediarios. Resultado: gestionan poco CVA de principio a fin y dependen de las herramientas y los criterios ajenos. |
| OP11 | Las organizaciones con programas de vouchers deben seleccionar, pagar y monitorear comercios. Si el pago se retrasa o fallan los controles, los comercios abandonan y las personas pagan más o esperan. |
| OP12 | Los actores humanitarios no logran alinear registros, valores y pagos con los sistemas nacionales de protección social. Resultado: duplicación, vacíos y transiciones lentas. |

**Requisitos transversales (no son oportunidades, pero condicionan a todas):**
- protección, privacidad y gobernanza de datos (ex O11);
- screening de sanciones y segregación de funciones (parte de ex O10);
- capacidad de operar con varios FSP por país.

---
## 3. Contexto de mercado común a todas las oportunidades

### 3.1 Volumen de CVA: contradicción de cifras

| Fuente | 2023 | 2024 | 2025 | Método / universo |
|---|---|---|---|---|
| CALP/ALNAP, jun-2025 [M04] | 7,8 mil M USD | 6,6 mil M USD | 4,5 mil M USD (proyección, −31 %) | Encuesta a organizaciones que reportan a CALP. Para la proyección de 2025 cita una submuestra de 18 organizaciones [M04]. Datos de 2024 provisionales y parciales. |
| CALP, ene-2026 [M05] | — | — | ~−60 % frente a 2023 (estimación temprana) | Estimación hecha sobre datos de 2023, en el momento de los recortes de EE. UU. (que aportaba el 42 % del CVA). |
| Development Initiatives, GHA 2026 / ALNAP SOHS 2026 [M01, M02] | — | 8,2 mil M USD (serie revisada) | 7,3 mil M USD (−11 %; 21 % de la ayuda humanitaria) | Serie revisada con más fuentes. |

**Qué se puede concluir:**
- El volumen de CVA **cae por tercer año seguido**. Todas las fuentes coinciden en la dirección.
- La caída de 2025 está entre −11 % y −60 % según la fuente.
- La cuota del CVA dentro de la ayuda humanitaria se mantiene o sube un poco (19,6 % → 21 %) [M01].

**Qué no se puede concluir:**
- La magnitud de la caída de 2025.
- Cualquier tamaño de mercado que dependa de esa cifra.

Las series no son comparables entre sí. Siempre que se cite el volumen hay que dar la fuente y el año. Esto afecta a `market-beliefs.md`; ver la propuesta de cambio en la sección 11.

### 3.2 Otros indicadores de contexto (verificados)

- **Ayuda humanitaria internacional:** 47,5 mil M USD (2022) → 33,3 mil M USD (2025). Cerca del 9 % de las organizaciones dejó de operar en 2025, entre ellas unas 500 ONG nacionales [M02].
- **Financiación a actores locales y nacionales en 2025:** 4,3 % directa y 8,7 % sumando la indirecta (~2,4 mil M USD), un 27 % menos que el año anterior [M01].
- **ACNUR (2025):** 450 M USD en efectivo, 100 países, 78 contratos con FSP. CashAssist canaliza el 96 % del volumen [M07].
- **PMA (2025):** 2,2 mil M USD de CVA (67 % efectivo, 33 % vouchers). Alcanzó el 44 % de lo planificado en efectivo [M06].
- **Reserva de EE. UU. (dic-2025):** 1,9 mil M USD, de los que el 34 % (651 M) fue CVA. El PMA ejecuta el 36 % de ese CVA; el 11,9 % llegó a actores locales [M08].
- **INGO de referencia:**
  - DRC entregó 51 M USD de CVA en 2023, en 43 países [T04]. Su convocatoria regional prevé hasta 11 M USD al año con FSP [T05].
  - Mercy Corps, ahora Prosper Global, perdió unos 2/3 de su financiación gubernamental y cerca del 40 % de su personal [M12].
- **Compras totales de la ONU en 2024:** 25,7 mil M USD. El informe no desglosa el gasto en IT o software humanitario [T22].
- **Gasto en IT de las ONG:** "solo el 2 %" [D18]. El 42 % de los profesionales de CVA encuestados cita capacidad limitada de IT y sistemas [M25].

### 3.3 Mercado general frente a mercado direccionable

- **El volumen de CVA (miles de millones de USD) no es el mercado de un producto.** Se paga software y servicio de varias formas:
  - dentro de la comisión o el contrato del FSP [T02, T03, T11];
  - con costes indirectos limitados al 7–8 % [M21];
  - como coste directo de proyecto, en licitaciones puntuales [T01, T06, T07];
  - con desarrollo interno [A01, M27];
  - o con herramientas gratuitas [M26, M28].
- **Ningún documento público revela el monto de la parte tecnológica** de un contrato CVA. La única cifra de inversión en sistemas es interna del PMA: SCOPE costó 47,3 M USD entre 2013 y 2020 [D18], y una nota conceptual de 2019 presupuestó 20 M USD para dos años [T21].
- **Mercado direccionable de cualquier oportunidad:** **no estimable con las fuentes disponibles.** En cada ficha se dan indicadores parciales verificables.

### 3.4 Comportamiento de compra observado (2021–2026)

| Organización | Fecha | Objeto | ¿Incluye FSP? | Monto | Fuente | Oportunidad |
|---|---|---|---|---|---|---|
| Prosper Global (ex Mercy Corps) | oct-2025 | Acuerdo marco global con un "Digital Payment and Technology Service Provider" | **Sí** | No publicado | [T02] | OP3 |
| Plan International | jun-2025 | Acuerdos de largo plazo con FSP globales, con "dashboard for tracking CVA distribution progress"; incluye las Américas | **Sí** | No publicado; 3 años | [T03] | OP3, OP5 |
| DRC (global) | feb-2025 | Convocatoria a plataformas de pago y FSP | Es compra de FSP | Referencia: 51 M USD de CVA/año | [T04] | OP3, OP4 |
| DRC WANALA (incluye América Latina) | may-2024 | FSP: registro y KYC, pago, conciliación, reporting | Es compra de FSP | Hasta 11 M USD/año (volumen transferido) | [T05] | OP3, OP4 |
| Diakonie Katastrophenhilfe | may-2024 | "Technology for Information Management and Delivery", "one single solution" | No consta | No publicado; 2 años | [T06] | OP2, OP3 |
| SARD (ONG local, noroeste de Siria) | jun-2024 | Sistema de e-voucher: registro, pagos, conciliación offline, antifraude, reporting | Sistema propio con tarjetas | Presupuesto "limited", unas 5.520 personas | [T07] | OP3, OP8, OP10 |
| Relief International | feb-2026 | "Cash and voucher digital assistance management platform" | **No leído** | **No leído** | [T01] | Desconocida |
| Solidarités International | jul-2026 | "Plataforma digital integral": pagos, vouchers, datos, reporting | Sí, según el título | No publicado | [T12] | OP3 |
| CRS | jul-2024 | Acuerdos marco de pago con gestión de datos opcional; meta de 1.000 M USD de CVA para 2030 | **Sí** | No publicado | [T13] | OP3 |
| Plan, DRC Afganistán, Save the Children (oPt y Afganistán) | 2025–2026 | Licitaciones de FSP | Es compra de FSP | No publicado | [T14, T08] | OP4 |
| UNICEF Sudán del Sur; FAO Sudán | 2026 | Acuerdos de largo plazo de transferencias | Es compra de FSP | No publicado | [T09, T10] | OP4 |
| ACNUR Pakistán (RFP-3243) | sep-2026 | Línea interagencia nacional con software de helpdesk | — | No publicado | [T15] | OP7 |
| FCDO Siria (Cowater) | feb-2024 | TPM y PEAL | — | **£10 M** en 3 años | [T16] | OP6 |
| PNUD Somalia; UNOPS Yemen | 2024; 2023 | TPM | — | Sin monto; **59.680 USD** | [T18, T19] | OP6 |
| PMA–Palantir | renovación prevista, ago-2026 | Plataforma de datos; renovación por 5 años | — | 2019: 45 M USD; renovación sin monto | [T20] | Contexto (cambio de proveedor) |

**Lectura:**
1. Lo que más se compra es el **servicio del FSP**. La tecnología de gestión suele ir **dentro de ese contrato**.
2. Hay **compras de plataforma por separado**, pero pocas y en INGO medianas y ONG locales.
3. No se observó ninguna compra cuyo objeto sea solo la conciliación, la deduplicación, la interoperabilidad, la detección de fraude o la protección de datos.
4. Los grandes compradores renuevan con los proveedores que ya tienen, aunque una auditoría haya señalado dependencia [T20].

### 3.5 Elegibilidad de costes (lo verificado)

- **ECHO:**
  - Son elegibles los "costs of IT and telecommunication services specifically purchased for the operations of the project office".
  - Los equipos se cargan por depreciación.
  - La subcontratación se acepta solo para "limited parts" de la acción.
  - En la lista de costes no elegibles no aparecen ni software ni licencias [M18].
  - Costes indirectos: máximo 7 % [M21].
  - ECHO no puede financiar la transformación digital de sus socios [M17].
  - La regla concreta sobre licencias (Anexo 5 / AGA): **no leída**.
- **FCDO:** sus costes de apoyo (NPAC) no tienen techo, pero "will need to be absorbed within the overall proposed budget limit" e incluyen "IT maintenance costs" [M19]. La guía de 2020 puede estar desactualizada.
- **EE. UU. (2 CFR 200):** los equipos informáticos pueden ser coste directo si son "essential and allocable". El umbral de "equipment" sube a 10.000 USD desde oct-2024 [M20]. **No se encontró una regla específica para software.**
- **Pendiente:** GFFO, SIDA, PRM tras la desaparición de BHA y las posiciones de NetHope, ICVA y VOICE.
- **Lectura:** comprar tecnología como coste directo de proyecto es **posible pero no está garantizado**. Depende de negociar caso por caso y de justificar el coste-beneficio [M17]. Lo que es infraestructura compartida entre proyectos tiende a ir a costes indirectos, que están limitados.

### 3.6 Tendencias transversales

| Tendencia | Dirección | Efecto probable | Fuentes |
|---|---|---|---|
| Recortes de financiación humanitaria | Contracción en 2025–2026; nuevas reservas de EE. UU. concentradas en el PMA | Menos compradores y menos presupuesto; más presión por eficiencia y control | [M01, M02, M05, M08, M12] |
| UN80 / New Humanitarian Compact / servicios comunes | Consolidación: identidad común entre agencias, catálogo de servicios comunes | Las agencias ONU ofrecen más herramientas gratuitas o compartidas; menos espacio para vender a la ONU | [D12, M15] |
| Cash first | Promovido en el reset y en el GHO 2026 | El efectivo multipropósito gana peso; los vouchers pierden peso relativo | [M14, M05, M04] |
| Localización | El discurso sube y el dinero baja (4,3 % directo, −27 %) | Más demanda declarada que capacidad de pago | [M01, M13, L12] |
| Protección social adaptativa | Al alza en el discurso; el traspaso a sistemas nacionales se ve empujado por los recortes | Mercado B2G, fuera del perfil | [L25, L18, L19, L20] |
| Identidad y biometría | Inversión interna de la ONU (EDS del PMA, reconocimiento facial) | Reduce el espacio de OP1 para terceros | [D11, D12] |
| Pagos digitales y rieles nuevos | Crecen el dinero móvil y las stablecoins como "last resort" | Más FSP y más formatos por país, lo que plausiblemente complica OP3 (inferencia) | [M37, M07] |
| Privacidad y regulación | Incidentes graves en 2022–2026; nuevas leyes en América Latina (Ecuador, México) | Más exigencia de entrada para cualquier producto | [X09, X10, X14, X15] |
| IA y automatización | La ONU las usa internamente (EDS del PMA) | No hay evidencia de demanda externa; queda fuera del alcance por instrucción | [D11] |

---
## 4. Fichas por oportunidad

Todas las fichas siguen el mismo esquema:

- **A.** Problema
- **B.** Cadena de actores
- **C.** Demanda observable
- **D.** Capacidad y disposición de pago
- **E.** Alternativas
- **F.** Saturación
- **G.** Estado
- **H.** Tendencia
- **I.** Barreras de entrada
- **J.** Tamaño
- **K.** Segmentos, contextos y geografía
- **L.** Valoración C1–C10
- **M.** Evidencia contraria

En la cadena de actores, "sin evidencia" significa que ninguna fuente describe ese eslabón.

### OP1. Deduplicación y coordinación entre organizaciones

**Enunciado.** Los equipos de gestión de información y los coordinadores de cash de organizaciones que asisten a la misma población no pueden saber a tiempo, y sin exponer datos, si un hogar ya recibe asistencia de otra organización. El resultado es doble asistencia, exclusión y meses de retraso en arrancar.

**A. Problema**
- **Quién lo vive:** equipos de gestión de información de ONG y consorcios, coordinadores de cash, Cash Working Groups (CWG). Las consecuencias recaen en los hogares.
- **Parte del ciclo:** entre el registro y la asignación de la asistencia, y entre las listas de distintas organizaciones.
- **Causas:**
  - No hay identificador común. En Somalia se usan 10 tipos de ID funcional y otros 10–20 de forma ocasional [D03].
  - Los acuerdos de intercambio de datos son lentos [D02].
  - No hay un dueño institucional del proceso [D03].
  - Las reglas de adjudicación se fijan contexto por contexto [D03].
  - En Türkiye 2023 no había base central y había restricciones legales [D13].
- **Qué ocurre hoy:** se cruzan hojas Excel en el clúster [D10], se suben datos a registros centrales (Building Blocks, HotPot) [D05] y se hacen reuniones de adjudicación manual [D03].
- **Si no se resuelve:** doble pago, exclusión de hogares cuando se adjudica mal y riesgos de protección por compartir datos [D15].

| Evidencia | Dato | Fuente |
|---|---|---|
| Tasa de duplicados | ~5 % de media (rango 1–15 %); hay rumores no confirmados del 40–90 % en Yemen y Somalia | [D02] |
| Tiempo para arrancar | Acuerdo de intercambio de datos: "up to three months and more", más ~1 mes para operar; en programas de 12 meses los resultados "may come too late" | [D02] |
| Esfuerzo recurrente | 1–2 días-persona al mes por organización | [D02] |
| Ahorro cuando funciona | Ucrania: 207 M USD evitados en efectivo multipropósito y 23 M USD en otras actividades de CVA, con 63 socios | [D05] |
| Prevalencia de la práctica | Somalia: más del 65 % de las organizaciones no deduplica | [D07] |
| Solapamiento observado | Bangladesh 2020: el 27 % de 88.432 documentos de identidad cruzados figuraba en varios socios | [D10] |

**B. Cadena de actores**

| Rol | Quién | Evidencia |
|---|---|---|
| Afectado | El hogar (doble asistencia o exclusión); el oficial de gestión de información | [D02] |
| Operativo | Gestión de información de la ONG o del consorcio (p. ej. Mercy Corps/CCS, deduplicación semanal) | [D19] |
| Decisor | CWG o equipo de trabajo (TT3 en Ucrania); en Somalia, el equipo humanitario de país (HCT) | [D05, D07] |
| Comprador | La agencia anfitriona o el consorcio. **No se observó compra externa** | — |
| Sponsor | CWG, Donor Cash Forum | [D17] |
| Financiador | ECHO (validación técnica de 2024), donantes noruegos (DIGID) | [D17, D04] |

**C. Demanda observable**
- **Problema mencionado:** mucho. Hay recomendaciones de CWG (Afganistán 2022, Líbano 2024) y principios de donantes [D18].
- **Comportamiento real:**
  - desarrollo interno de la ONU: EDS del PMA en 8 países, HOPE con reconocimiento facial, PING [D11, M27, D06];
  - hoja de ruta del sistema federado de registro de Somalia hasta 2028 [D07];
  - vacantes de gestión de información [D19];
  - **ninguna licitación pública de un servicio de deduplicación independiente.**

**D. Capacidad y disposición de pago**

| Segmento | Situación |
|---|---|
| Agencias ONU | Construyen: EDS, HOPE, PRIMES; identidad común en UN80 [D11, D12] |
| INGO grandes | Usan gratis Building Blocks o HotPot a través del CWG o el consorcio [D05, M28] |
| INGO medianas | Igual, con personal de gestión de información del consorcio |
| ONG locales | El 35 % no tiene política de datos (Somalia) [D07]; un dispositivo biométrico cuesta ~1.000 USD [D07] |

La disposición a pagar por deduplicación aislada es **BAJA o DESCONOCIDA** porque existen alternativas gratuitas.

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Excel del clúster | Cruce de documentos de identidad | Clústeres | Gratis | 0 | Simple | Propenso a errores [A12, D10] |
| Building Blocks (PMA y otras agencias) | Deduplicación entre agencias | Socios de CWG | SaaS gratuito vía CWG | 0 | Escala probada en Ucrania | Gobernanza ligada al PMA [M28] |
| HotPot (CCD), solución del Estonian Refugee Council | Deduplicación ligera | Consorcios | Gratis o desconocido | — | Ligero | Poca documentación [D05] |
| EDS (PMA) | Deduplicación interna con revisión humana | Solo PMA | Interno | — | "De semanas a horas"; 431.000 USD evitados en Malí | No se ofrece a terceros [D11] |
| HOPE, PRIMES/BIMS | Identidad y biometría | Agencia propia y socios | Interno / bien público digital | — | Escala | Interoperabilidad limitada [D01] |
| Consultores de procedimientos | Reglas de adjudicación | CWG | Honorarios | — | Contexto local | No escala |

**F. Saturación**

| Dimensión | Situación |
|---|---|
| Número de actores | Varios, sin dominante |
| Segmentos cubiertos | ONU bien cubierta; ONG locales mal cubiertas |
| Parte del problema resuelta | La técnica (comparar registros) |
| Parte abierta | Gobernanza, adjudicación, consentimiento |
| Coste de cambiar | Alto |
| Opciones gratuitas | Varias |
| Concentración | En la ONU |
| Desarrollo propio | Alto |

**Gap:** la adjudicación y la gobernanza. Las fuentes dicen que **no es técnico**: "Deduplication and adjudication rules are considered as important, if not more important as data standards" [D03].

**G. Estado:** **parcialmente resuelto.**
- Bien resuelto en Ucrania y en curso en Somalia y Tanzania [D05, D07, D06].
- Poco resuelto en Sudán, Haití, Chad y RDC [D08, A11, A08, A12].

**H. Tendencia:** **CRECE** como prioridad, por los recortes y por UN80 [D03, D12]. **DECRECE** como espacio para terceros, porque la ONU consolida y regala herramientas. En Sudán 2026 se concluye que "Household-level interoperability systems are not necessary at current coverage levels" [D08].

**I. Barreras de entrada:** acuerdos de intercambio de datos y leyes nacionales; confianza en quien custodia los datos; asimetría de poder (las ONG pequeñas temen alimentar registros ajenos [D01]); herramientas ONU gratuitas; ausencia de dueño institucional; biometría sensible.

**J. Tamaño:**
- Verificables: 63 socios en Ucrania; 200 o más organizaciones en Somalia [D07]; HOPE en 33 países [M27].
- Valor de mercado: **no estimable con las fuentes disponibles.**

**K. Segmentos, contextos y geografía**
- **Emergencia** (Ucrania): duplicados por autorregistro y altos ahorros cuando hay coordinación [A03, D05].
- **Crisis prolongada** (Somalia, Bangladesh): muchos tipos de identificación y prácticas desiguales [D07, D10].
- **América Latina:**
  - En Colombia (2020), la Coordinadora de Cash compartía "códigos únicos creados por la plataforma, no los datos", con un acuerdo entre 7 organizaciones [D14].
  - El catálogo del GTRM de Perú y Ecuador (2024) no menciona deduplicación.
  - No se encontró una plataforma regional R4V de deduplicación para 2024–2026: **desconocido**.

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | ALTA | 207 M USD evitados en un solo país [D05]; exclusión y riesgos de protección [D15] | m |
| C2 Frecuencia | MEDIA | ~5 % de duplicados de media [D02]; aparece en cada respuesta con varios actores | m |
| C3 Demanda observable | BAJA | Solo desarrollo interno y vacantes; ninguna compra externa [D11, D19] | m |
| C4 No resuelto | MEDIA | Herramientas sí; gobernanza no [D03] | m |
| C5 Pago | BAJA | Herramientas gratuitas, UN80 [M28, D12] | m |
| C6 Competencia | ALTA (ocupado) | Building Blocks, HOPE, EDS, PRIMES, RedRose [M28, M27, D11] | a |
| C7 Diferenciación | BAJA | El gap es de gobernanza, no de producto [D03] | m |
| C8 Tendencia | CRECE la necesidad / DECRECE el espacio para terceros | [D12, D08] | m |
| C9 Barreras | ALTAS | Acuerdos de datos, confianza, gratuidad | m |
| C10 Acceso a usuarios | MEDIO | Las actas de CWG son públicas; hay oficiales de gestión de información en vacantes (inferencia) | b |

**M. Evidencia contraria:** Ucrania y Building Blocks funcionan gratis y a gran escala [D05]. El EDS del PMA reduce el problema dentro del PMA [D11]. En Sudán no se considera necesario a la cobertura actual [D08]. En Somalia hasta el 52 % de los hogares comparte la asistencia, lo que relativiza la noción de "duplicado" [D07].

---

### OP2. Integridad de la lista y del identificador dentro de la organización

**Enunciado.** Los equipos de programa, gestión de información y finanzas trabajan con listas cuyos identificadores faltan, se repiten o cambian entre el registro, la versión final y el pago. El resultado son pagos a registros inválidos o duplicados, conciliaciones que no se pueden hacer y cambios no autorizados que no se detectan.

**A. Problema**
- **Quién lo vive:** gestión de información y MEAL (limpieza y listas), programa (targeting), finanzas (pago y conciliación) y socios ejecutores.
- **Parte del ciclo:** del registro a la lista de pago, y de la lista final al archivo que se envía al FSP.
- **Causas:**
  - registros manuales o en hojas de cálculo [A13];
  - identificadores redondeados o perdidos al migrar de sistema [A01];
  - sincronización lenta entre el sistema de registro y el de pagos [A01];
  - socios que modifican datos después de la lista final [D09];
  - "multiple and rolling spreadsheets" [A12].
- **Qué ocurre hoy:** Excel para construir listas que luego se importan [A01]; limpieza distinta en cada socio [D09]; conciliación agregada en lugar de por persona [A08].
- **Si no se resuelve:** pagos a registros inválidos, duplicados no detectados, conciliación imposible (OP3) y hallazgos de auditoría.

| Evidencia | Dato | Fuente |
|---|---|---|
| Registros sin identificador único | 223.985 en 7 operaciones de ACNUR | [A01] |
| Pagos con ID inválido o repetido | Afganistán: 14,5 M USD a 23.985 hogares con ID inválido, ausente o repetido; IDs redondeados a "140000…" en la migración | [A01] |
| Socios sin conciliación por falta de ID | Afganistán: "Partners did not prepare proper reconciliations since individual transactions did not have unique identifiers" | [A04] |
| Duplicados internos | 249 hogares (93.919 USD) con ID y fecha de nacimiento idénticos | [A01] |
| Desincronización | Jordania: casos sin sincronizar "for months"; 244 nombres y 40 fechas de nacimiento distintos entre sistemas | [A01] |
| Cambios después de la lista final | Yemen (CCY, 6 ONG): los socios "occasionally modified Bio data after the CCY sent the final distribution list" | [D09] (COMERCIAL: caso de proveedor) |
| Calidad del registro | Mozambique: 80 % manual o en hojas de cálculo; posibles errores de inclusión del 30–50 %. RDC: 1,6 M de miembros de hogar sin datos biográficos | [A13, A12] |

**B. Cadena de actores**

| Rol | Quién | Evidencia |
|---|---|---|
| Afectado | Finanzas y programa; la persona receptora (exclusión o error) | [A01] |
| Operativo | Gestión de información y MEAL; socios ejecutores | [D09, A04] |
| Decisor | En la ONU, la sede (soluciones "corporate-approved") [A09]; en las ONG, **sin evidencia** | — |
| Comprador | En la ONU, la sede. En las INGO, procurement global, que licita plataformas CVA donde esto es una función más [T06, T01] | — |
| Sponsor | Auditoría interna (OIOS, Inspector General del PMA) | [A01, A09] |
| Financiador | Donantes, de forma indirecta | — |

**C. Demanda observable**
- **Problema mencionado:** auditorías de OIOS de 2020, 2023 y 2025 y del PMA de 2022–2026 [A01, A04, A05, A08, A12, A13].
- **Comportamiento real:**
  - compromisos con plazo de ACNUR (integración DHOTS e interoperabilidad, dic-2026) y del PMA Zambia (reemplazar procesos manuales, jun/dic-2026) [A01, A09];
  - Diakonie licita "one single solution" de gestión de datos y distribución [T06];
  - ActivityInfo sustituyó R + Excel en el consorcio CCY de Yemen [D09] (COMERCIAL).
- **Matiz:** casi toda la inversión visible es **interna o se compra dentro de una plataforma**. Nadie compra "integridad de lista" por separado.

**D. Capacidad y disposición de pago**

| Segmento | Situación |
|---|---|
| Agencias ONU | Capacidad ALTA, pero desarrollan en casa [A01, A09] |
| INGO grandes | Compran plataformas CVA (RedRose y otras) [M30, M31] |
| INGO medianas | Hay licitaciones de plataforma [T06, T01]; montos desconocidos |
| ONG locales | Licitación pequeña "limited" [T07] o Excel y Kobo |

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Excel + Kobo/ODK | Listas | Todos | Gratis / freemium | Kobo gratis para ONG; Professional 129–159 USD/mes [M26] | Universal | Errores; sin control de versiones [A12] |
| ActivityInfo | Listas y reporte | ONG, clústeres | SaaS | 545 a 3.700 €/año [M26] | Sustituyó R + Excel en CCY | Un solo caso documentado [D09] |
| CashAssist / proGres (ACNUR) | Registro y pago | Solo ACNUR | Interno | — | Corporativo | Desincronización e IDs ausentes [A01] |
| SCOPE (PMA) | Gestión de beneficiarios | PMA y socios | Interno | — | Escala | Haití: "not successful", archivos procesados fuera del sistema [A11] |
| RedRose / HOPE / 121 / Humansis | Gestión del ciclo CVA | INGO, ONU, Cruz Roja | SaaS / bien público digital / open source | No público | Integran registro y pago | No hay evidencia independiente de resultados |

**F. Saturación**
- Muchas plataformas, pero los fallos aparecen **incluso con plataforma corporativa** [A01, A11].
- **Gap:** control de versiones y de cambios de la lista, identificador persistente a lo largo del ciclo, y calidad del dato en el origen.

**G. Estado:** **poco resuelto** en la ONU según las auditorías [A01, A04, A11, A12, A13]. **Desconocido** en ONG medianas y locales.

**H. Tendencia:** **CRECE** como prioridad de control, con recomendaciones de auditoría que vencen en 2026 [A01, A09]. **INCIERTA** como mercado comprable.

**I. Barreras de entrada:** depende de cómo se registra aguas arriba; integración con sistemas de registro ya existentes; obligación de usar herramientas corporativas en la ONU; datos personales.

**J. Tamaño:**
- Verificables: 2,1 M de registros de pago y 2,3 mil M USD de CBI de ACNUR en 2022–24 [A01].
- Número de organizaciones afectadas fuera de la ONU: **desconocido**.
- Valor de mercado: **no estimable**.

**K. Segmentos, contextos y geografía**
- **Crisis prolongada con identificación débil** (Afganistán, Kenia, Haití): IDs ausentes [A01, A11].
- **Consorcios con varios socios** (Yemen): cambios no controlados [D09].
- **América Latina:**
  - auditoría de ACNUR en México: 2 pagos marcados como exitosos con importe cero [A01];
  - Haití: muchos documentos de identidad y poca garantía de unicidad [A11];
  - Colombia: auditoría del PMA AR-26-05 **no leída** [A17].

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | ALTA | 14,5 M USD a IDs inválidos; conciliación imposible [A01, A04] | m |
| C2 Frecuencia | ALTA en la ONU / DESCONOCIDA fuera | 7 de 7 operaciones con registros sin ID [A01]; varias auditorías del PMA | m |
| C3 Demanda observable | MEDIA-BAJA | Compromisos internos y licitaciones de plataforma, no de integridad por separado [A09, T06] | m |
| C4 No resuelto | ALTA | Falla incluso con sistemas corporativos [A01, A11] | m |
| C5 Pago | MEDIA en INGO / BAJA en ONG locales | [T06, T07] | b |
| C6 Competencia | MEDIA | Plataformas generalistas, sin foco específico | b |
| C7 Diferenciación | MEDIA | El gap concreto (cambios de lista, identificador persistente) no aparece como oferta explícita (inferencia) | b |
| C8 Tendencia | CRECE | Plazos de auditoría en 2026 [A01, A09] | m |
| C9 Barreras | MEDIAS-ALTAS | Integración con el registro; herramientas corporativas | m |
| C10 Acceso a usuarios | MEDIO | Finanzas y gestión de información son roles accesibles (inferencia) | b |

**M. Evidencia contraria:**
- La causa puede ser de **proceso y disciplina**, no de herramienta. OIOS atribuye parte del problema a la "maturity of the banking systems" y a restricciones financieras [A01].
- Las ONG con plataformas integradas (RedRose, 121) podrían no sufrirlo. Esto no se pudo verificar.
- Podría ser parte de OP3 y no un problema aparte.

---
### OP3. Ciclo de pago con el FSP y conciliación

*Fusiona la operación de O2 con O3. El análisis en profundidad, con criterio adversarial, está en la sección 6.*

**Enunciado.** Los equipos de Finanzas y de Cash de las organizaciones que pagan a través de FSP no logran casar a tiempo, persona por persona, tres cosas: lo que ordenaron pagar, lo que el FSP reporta como pagado o cobrado y lo que figura en la contabilidad. Por eso detectan tarde los duplicados, los pagos marcados como exitosos que no se entregaron y los fondos no cobrados. Los cierres financieros salen con descuadres y aparecen hallazgos de auditoría.

**A. Problema**
- **Quién lo vive:** Finanzas de país, que valida; Cash/CVA, que aporta la prueba de entrega; Logística, que gestiona el contrato con el FSP [F08]; socios ejecutores [A04].
- **Parte del ciclo:** instrucción de pago → estado de cada transacción → no cobrados y reversiones → conciliación persona a persona → cierre contable → reporte.
- **Causas:**
  - transferencia manual de archivos entre el sistema y el FSP: en 5 de 7 operaciones de ACNUR [A01];
  - formatos distintos según el FSP;
  - falta de identificador común (OP2);
  - conciliación agregada en lugar de por persona [A08];
  - sistemas que no se cruzan con el ERP [A02].
- **Qué ocurre hoy:**
  - Excel y hojas impresas en pagos por ventanilla, que el auditor califica de "error-prone" [A01];
  - tableros propios que fallan, como en Chad, por fechas de ciclo desalineadas con SCOPE [A07];
  - reversión de no cobrados a petición escrita [F05].
- **Si no se resuelve:** desvíos y duplicados no detectados, estados financieros incorrectos, comisiones pagadas sobre efectivo no cobrado [A02] y recomendaciones de auditoría que siguen abiertas.

| Evidencia | Dato | Fuente |
|---|---|---|
| Descuadre sistema de pagos ↔ ERP | 71 M USD sin conciliar entre CashAssist y el ERP (MSRP), contra lo que exigía el procedimiento; bajó a 1 M USD en jul-2023 | [A02] |
| Pagos marcados como exitosos con importe cero | Kenia 5.426, Afganistán 4, México 2, Jordania 1 | [A01] |
| Retraso de la conciliación | Sudán del Sur: aprobada 3–6 meses después; 22 % (5 M USD) entre lo registrado y lo real; más de 100 hojas Excel | [A06] |
| Fondos no cobrados | Moldavia: 3,6 M USD recuperados de 14.432 tarjetas inactivas | [A02] |
| Comisión sobre efectivo no cobrado | 377.813 USD de comisión para desembolsar 8 M USD, de los que 123.639 USD no se cobraron | [A02] |
| Comisiones no registradas | 2,9 M USD sin pagar ni registrar en los estados financieros de 2022 | [A02] |
| Pago duplicado | Polonia: 10.619 personas, 1,5 M USD (jun-2022) | [A02] |
| Papel en lugar de sistema | Haití: anticipos conciliados "months late", en papel, "prone to errors" | [A11] |
| Factura del FSP ≠ informes de ONG | RDC (Fizi, 2022) | [A12] |
| Carga de personal | Oxfam: 5 personas a tiempo completo dedicadas a conciliación manual (piloto de 2019) | [F12] |
| Volumen en papel | Palestina: unas 100.000 transacciones por ciclo en hojas de cálculo | [A18] |

**B. Cadena de actores**

| Rol | Quién | Evidencia |
|---|---|---|
| Afectado | Finanzas de país y oficiales de Cash | [A01, F09] |
| Operativo | Asistentes de CVA y de Finanzas; vacantes de IFRC que "review and approve the reconciliation" (Colombia, Caracas, Jamaica, 2026) | [F09] |
| Decisor | ONU: sede (soluciones "corporate-approved") [A09]. INGO: **sin evidencia directa** | — |
| Comprador | ONU: sede. INGO: procurement global, que compra el FSP y, a veces, la tecnología en el mismo paquete [T02, T03] | — |
| Sponsor | Auditoría interna (OIOS, Inspector General del PMA) | [A01, A09] |
| Financiador | Donantes: comisión del FSP como coste directo (ECHO pone un tope del 5 % a la comisión de proveedores de remesas) [F07]; la gestión se paga con costes indirectos (inferencia) | — |

**C. Demanda observable**
- **Problema mencionado:** muchas veces, en OIOS 2020/057, 2023/043, 2025/019 y 2025/027 y en auditorías del PMA de 2022–2026.
- **Comportamiento real:**
  - el PMA Zambia se compromete a "assess system integration options to enable automated reconciliations" (plazo 2026) [A09];
  - ACNUR se compromete a integrar DHOTS (dic-2026) [A01];
  - vacantes de IFRC con funciones de conciliación [F09];
  - contratos que combinan FSP y tecnología: Prosper Global, Plan con "dashboard", PUI con conciliación y facturación, DRC WANALA con conciliación como servicio del FSP [T02, T03, T11, T05];
  - la ONG local SARD licita conciliación offline [T07].
- **Lo que falta:** **ningún RFP ni consultoría tiene como objeto específico la conciliación** [búsqueda de la línea O3]. La conciliación se compra **como servicio del FSP o como función de una plataforma**.

**D. Capacidad y disposición de pago**

| Segmento | Capacidad | Cómo se compra | Alternativas | Probabilidad de compra |
|---|---|---|---|---|
| Agencias ONU | ALTA | Desarrollo interno (CashAssist, DHOTS, SCOPE) | Propias | BAJA para un tercero [A01, A09] |
| INGO grandes | MEDIA, con recortes [M12] | Dentro del contrato con el FSP (acuerdos marco de 1 a 3 años) o en una plataforma (RedRose) | Portal del FSP, ERP, Excel | MEDIA [T02, T03, T13] |
| INGO medianas | MEDIA-BAJA | Licitación de plataforma o FSP + plataforma | Excel, portal del FSP | MEDIA [T06, T01, T12] |
| ONG locales | BAJA | Licitación pequeña por proyecto | Excel, papel | BAJA-MEDIA [T07] |

**E. Alternativas.** Ver la tabla completa en la sección 6.

**F. Saturación**
- Hay muchos actores con funciones parciales: herramientas de la ONU, cuatro o más plataformas CVA, portales de FSP, ERP y Excel.
- **Gap documentado:**
  - casar identificadores entre sistemas;
  - conciliar persona a persona y no en agregado;
  - enlazar con el ERP;
  - gestionar los no cobrados.
- **Matiz:** las causas raíz que señala OIOS son la calidad del dato, la sincronización y la madurez de la banca local, no la falta de una herramienta [A01].

**G. Estado:** **poco resuelto** en la ONU según las auditorías. **Parcialmente resuelto** donde hay integración: Etiopía (API) y Rumanía (DHOTS) [A01], o donde el FSP da acceso directo a su plataforma, como en Sierra Leona, que pasó de conciliar a fin de mes a hacerlo a diario [F01]. **Desconocido** en INGO medianas y ONG locales.

**H. Tendencia:**
- **CRECE** como prioridad de control: recomendaciones con plazo en 2026 [A01, A09] y más FSP y rieles por país (78 contratos de ACNUR) [M07].
- **INCIERTA** como mercado comprable: la respuesta que se observa es interna y los presupuestos se contraen [M12].

**I. Barreras de entrada:**
- acceso a sistemas y datos de los FSP, país por país, condicionado por la "maturity of the banking systems" [A01];
- formatos propios de cada FSP;
- datos personales;
- herramientas corporativas obligatorias en la ONU;
- dependencia de la calidad del registro (OP2);
- confianza de auditoría;
- el FSP ya ofrece informes y dashboard dentro de su contrato [T03].

**J. Tamaño:**
- Verificables: el PMA pagó 2,7 mil M USD vía FSP entre ene-2023 y jun-2024 [A10]; ACNUR, 2,3 mil M USD de CBI en 2022–24 [A01]; DRC, 51 M USD/año [T04]; DRC WANALA, hasta 11 M USD/año [T05].
- Número de organizaciones que concilian a mano: **desconocido**.
- Valor de mercado: **no estimable**.

**K. Segmentos, contextos y geografía:** ver la sección 6.6.

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | ALTA | 71 M USD de descuadre; 22 % en Sudán del Sur; 3,6 M USD de no cobrados [A02, A06] | m (solo ONU) |
| C2 Frecuencia | ALTA | En cada ciclo de pago; 5 de 7 operaciones de ACNUR con traspaso manual [A01]; varias auditorías del PMA | m |
| C3 Demanda observable | MEDIA | Contratos FSP + tecnología y licitaciones de plataforma [T02, T03, T06, T07, T11]; ningún RFP solo de conciliación | m |
| C4 No resuelto | ALTA en la ONU / DESCONOCIDO fuera | [A01, A07, A08] | m |
| C5 Pago | MEDIA | INGO compran dentro del contrato con el FSP o de la plataforma; ONU construye | b-m |
| C6 Competencia | MEDIA | Plataformas CVA, portales de FSP, ERP; ningún especialista | m |
| C7 Diferenciación | MEDIA | Conciliación persona a persona entre varios FSP y el ERP no aparece como oferta explícita (inferencia); el FSP puede cubrir parte | b |
| C8 Tendencia | CRECE como necesidad / INCIERTA como mercado | [A01, A09, M12] | m |
| C9 Barreras | ALTAS | Acceso a FSP por país, formatos, datos, confianza | m |
| C10 Acceso a usuarios | MEDIO-ALTO | Las vacantes de Finanzas y CVA son públicas (incluida Colombia); los consorcios publican sus aprendizajes [F09, F06] | m |

**M. Evidencia contraria:**
- Las mayores fallas están en la ONU, que construye sus propios sistemas.
- Los FSP ya dan acceso a su plataforma y conciliación diaria [F01, F06].
- Ya existen integraciones por API [A01].
- La raíz es el dato y la gobernanza [A01].
- No hay ningún RFP específico.
- Que un auditor señale controles insuficientes no prueba que los usuarios perciban el dolor ni que quieran pagar.

---

### OP4. Contratación y gestión del desempeño de FSP

**Enunciado.** Los equipos de Cash, Procurement y Finanzas tardan meses en contratar FSP con procesos pensados para comprar bienes, y apenas evalúan su desempeño. El resultado es asistencia tardía, sobrecostes de comisión y dependencia de un único proveedor.

**A. Problema**
- **Quién lo vive:** Procurement y Logística (licitación), Finanzas (comité de evaluación), Legal y Cash [F02].
- **Parte del ciclo:** preparación de la respuesta, antes de pagar; y seguimiento del contrato.
- **Causas:** procesos de compra genéricos; KYC y regulación; poca oferta de FSP en algunos países; pocas semanas para que los FSP respondan [F02].
- **Qué ocurre hoy:** acuerdos marco globales [T03, T04]; uso de contratos de otra agencia sin due diligence [A05]; pruebas con varios FSP [F06].

| Evidencia | Dato | Fuente |
|---|---|---|
| Duración de la contratación | CICR: 3–4 meses en Nigeria y 5–6 en Etiopía; Cruz Roja de Sierra Leona: ~7 semanas | [F01] |
| Duración de la contratación | IRC Bidi Bidi: 3 meses; IRC Pakistán: 1–2 meses | [F03, F04] |
| Seleccionar un FSP | PMA: hasta un año; aprobación de evaluaciones de desempeño de hasta 678 días; 30 % sin completar | [A10] |
| Contratos irregulares | ACNUR Ucrania: un FSP desembolsó más de 20 M USD antes de tener contrato aprobado | [A02] |
| Diferencia de comisiones | Efecty: 0,9 % a 1,8 % según el socio en el mismo consorcio | [F06] |
| Comisiones en crisis | Proveedores de remesas tipo hawala: 3–4 %; tope ECHO del 5 %; 15–25 % en emergencias agudas | [F07] |
| Fallos del FSP | SIM bloqueadas la noche antes del pago; cancelación por error de tarjetas; plataformas caídas 2 días | [F03, F06] |
| Dependencia | Un solo FSP canaliza el 60 % en Sudán del Sur | [A06] |

**B. Cadena de actores:** Programa (define el alcance) → Procurement/Logística (licita) → Finanzas y Legal (evalúan) → sede (gobernanza del FSP en la ONU [A10]; en IFRC, la oficina regional coordina [F09]) → donante (paga la comisión como coste directo).

**C. Demanda observable**
- **Comportamiento real abundante, pero de compra del FSP:** Plan, DRC, Save the Children ×2, Solidarités, UNICEF, FAO, PRCS [T14, T08, T09, T10, F11].
- **No se observó** ninguna licitación de software ni de servicios para *gestionar* la contratación o el desempeño de FSP.

**D. Capacidad y disposición de pago:** la comisión del FSP es coste directo. La gestión del FSP se absorbe en personal. Hay ahorro posible por negociar en conjunto ("could've negotiated an even lower rate" [F06]; la carta de profesionales de 2025 pide negociar comisiones a escala [F10]). **No hay comprador identificado** para algo distinto del propio servicio del FSP.

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Acuerdos marco globales con FSP | Contratar rápido | ONU, INGO grandes | Contrato | Comisión | Ya existen [T03, T04] | Cobertura por país |
| Contratos de otra agencia | Velocidad | ONU | Gratis | — | Rápido | Sin due diligence [A05] |
| Mapeos de FSP de los CWG; guías ELAN, CaLP, NRC | Información de mercado y bases de licitación | Todos | Gratis | 0 | Bien público | Estático, no ejecuta [F02, F07] |
| Consultores de procurement | Bases y evaluación | INGO | Honorarios | — | — | No escala |

**F. Saturación:** la relación la dominan los propios FSP y los procesos internos. **Gap:** duración y rigidez de la contratación, y evaluación del desempeño. Cambiar de FSP cuesta mucho (hay que repetir registro y KYC).

**G. Estado:** **parcialmente resuelto** en la ONU y las INGO grandes con acuerdos marco. **Poco resuelto** en evaluación de desempeño [A10]. **Desconocido** en ONG locales.

**H. Tendencia:** **ESTABLE.** Siguen las licitaciones y aumenta la exigencia de gobernanza [A10]. La localización empuja a trabajar con instituciones financieras locales [F10].

**I. Barreras de entrada:** KYC/AML y sanciones [F07]; licencias por país; procurement institucional; el decisor es Procurement y no Programas.

**J. Tamaño:** 78 contratos con FSP en ACNUR [M07]. Número de contratos en ONG: **no estimable**.

**K. Segmentos, contextos y geografía:**
- **Emergencias:** contratos retroactivos (Ucrania) [A02] y comisiones del 15–25 % [F07].
- **América Latina:** en el consorcio VenEsperanza (Colombia) cada socio tenía contratos separados con Banco de Occidente, Davivienda y Efecty, con comisiones muy distintas; el KYC de los migrantes se resolvió con flexibilidad del FSP [F06].

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | MEDIA | Retrasos de meses, sobrecostes [F01, A10] | m |
| C2 Frecuencia | MEDIA | Una vez por respuesta o contrato; evaluación periódica | m |
| C3 Demanda observable | ALTA para el servicio del FSP / BAJA para gestionar al FSP | [T14] | m |
| C4 No resuelto | MEDIO | Hay acuerdos marco; la evaluación de desempeño queda abierta [A10] | m |
| C5 Pago | BAJA | No hay comprador fuera de la comisión | m |
| C6 Competencia | ALTA | FSP, guías, consultores | m |
| C7 Diferenciación | BAJA | — | b |
| C8 Tendencia | ESTABLE | [A10, F10] | b |
| C9 Barreras | ALTAS | Procurement, regulación | m |
| C10 Acceso a usuarios | MEDIO | — | b |

**M. Evidencia contraria:** hay casos de contratación ágil (Sierra Leona, ~7 semanas) [F01]. Los FSP mejoran el servicio por su cuenta [F06]. Según profesionales del sector, "it's really about the relationship" [F06].

---
### OP5. Reporting a donantes y a la coordinación

**Enunciado.** Los equipos de MEAL y de grants de ONG con varios donantes vuelven a elaborar los mismos datos en formatos y definiciones distintos para cada donante y para la coordinación (4W/5W). Pierden horas y entregan un reporte incompleto o inconsistente.

**A. Problema**
- **Quién lo vive:** MEAL y grants de INGO y ONG locales que tienen varios donantes (ECHO, FCDO, PRM, GFFO, fondos mancomunados).
- **Causas:**
  - Cada donante usa sus propios formatos.
  - La plantilla común 8+3 solo cubre la narrativa; el reporte financiero y los indicadores no están armonizados [R02, R03].
  - El CVA casi nunca se etiqueta en el FTS [R05, R06].
- **Workaround:** personal interno, Excel, ActivityInfo y Power BI.
- **Si no se resuelve:** tiempo restado a la ejecución y datos de 4W incompletos. En Siria 2023, solo 9 INGO y 13 ONG nacionales reportaban el efectivo multipropósito [D20].

| Evidencia | Dato | Fuente |
|---|---|---|
| Horas | NRC podría ahorrar más de 11.000 h/año solo en reporte financiero. En el sector: unas 283.000 h-persona/año en 27 INGO grandes y unas 898.000 en el resto | [R01] (2016, antigua) |
| Definiciones | Más de 12 donantes con definiciones distintas de costes de apoyo | [R01] |
| Plantilla 8+3 | 9 de 11 donantes la valoran bien. Que ahorre tiempo "imposible" de concluir: solo 17 de 207 reportes recibieron la plantilla de varios donantes | [R02] |
| Adopción de 8+3 | 15 firmantes en 2021; ECHO solo la "consideraba" | [R03] |
| Situación en 2025 | El caucus del Grand Bargain vuelve a comprometerse a usar la 8+3 y a armonizar el reporting y la due diligence en 2026 | [R04] |

**B. Cadena de actores:** el oficial de MEAL o grants es el afectado y quien opera. Deciden la dirección de país y la de programas. Compra la ONG, con costes indirectos o directos. Financia el donante, que es también quien **impone** el formato.

**C. Demanda observable**
- **Lo que se dice:** compromisos de política (Grand Bargain 2016, 2021 y 2025) [R04].
- **Lo que se compra:** licencias de herramientas genéricas (ActivityInfo, Kobo, Power BI). **No se encontró ninguna licitación de "software de reporting".**

**D. Capacidad y disposición de pago:** la licencia genérica cabe en el presupuesto de MEAL. Si el MEAL es coste directo elegible es plausible pero **no está verificado** `[conocimiento del modelo — verificar]`. Hay mucha oferta barata: Kobo gratis, ActivityInfo desde 545 €/año, CommCare desde 100 USD/mes [M26, R18].

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Plantilla 8+3 | Reporte narrativo | Todos | Gratis | 0 | Bien valorada [R02] | No cubre lo financiero ni los indicadores |
| ActivityInfo / 5W de los CWG | Reporte a la coordinación | Socios de CWG | SaaS | 545–3.700 €/año [M26] | Estándar de facto | Subreporte |
| Kobo / SurveyCTO / CommCare | Recogida de datos | Todos | Gratis / SaaS | 0 a 4.000+ USD/mes [M26, R18] | Baratos y adoptados | No consolidan entre donantes |
| Power BI / Tableau | Tableros | Organizaciones grandes | Licencia | No verificado | Flexibles | Necesitan personal técnico |
| Indicadores MPC del Grand Bargain y toolkit de Save the Children | Estandarizar indicadores | INGO | Gratis | 0 | Más de 30 indicadores / 27 indicadores | Menú voluntario [R07, R08] |

**F. Saturación:** **alta** en herramientas, con muchas gratuitas. El **gap** es la armonización financiera y de indicadores entre donantes. Pero lo controla el **donante**, no la ONG: es un problema de estándar, no de producto.

**G. Estado:** **parcialmente resuelto.** La narrativa sí (8+3); lo financiero y los indicadores no [R02, R04].

**H. Tendencia:** **INCIERTA.** Los fondos se concentran en los fondos mancomunados de OCHA, así que hay menos donantes por ONG [M14, M08]. A la vez, hay más presión por demostrar valor y un compromiso de armonización para 2026 [R04].

**I. Barreras de entrada:** los formatos los impone el donante; ya están instalados ActivityInfo y Kobo; hay que integrarse con los sistemas de los donantes.

**J. Tamaño:** solo cifras de horas de 2016 [R01]. Valor de mercado: **no estimable**.

**K. Segmentos y geografía:**
- **Carga más alta:** ONG locales con varios intermediarios (ver OP10).
- **América Latina:** R4V tiene 152 socios en 2026 [M09] y en 2021 eran 53 organizaciones con CVA [M11]; reportan a la plataforma regional. La carga concreta es **desconocida**.

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | MEDIA | Horas perdidas, sin consecuencia crítica documentada [R01] | b (fuente antigua) |
| C2 Frecuencia | ALTA | Cada ciclo de reporte | m |
| C3 Demanda observable | BAJA | Solo compromisos de política y licencias genéricas | m |
| C4 No resuelto | MEDIO | La 8+3 no cubre lo financiero [R02] | m |
| C5 Pago | BAJA-MEDIA | Licencias baratas o gratuitas | m |
| C6 Competencia | ALTA | — | m |
| C7 Diferenciación | BAJA | El estándar lo fija el donante | m |
| C8 Tendencia | INCIERTA | [R04, M08] | b |
| C9 Barreras | MEDIAS | — | b |
| C10 Acceso a usuarios | ALTO | La comunidad de MEAL es amplia (inferencia) | b |

**M. Evidencia contraria:** la 8+3 tiene buena valoración [R02]. Las herramientas genéricas cubren la parte técnica a coste bajo. Según la CHS, "perfect tools don't automatically result in perfect" mecanismos [R11].

---

### OP6. Monitoreo de resultados y verificación

**Enunciado.** Las oficinas de país que operan en contextos con acceso restringido no alcanzan la cobertura ni la calidad de monitoreo exigidas, y no llevan hasta el cierre lo que encuentran. Como resultado hay poca evidencia de resultados, riesgo fiduciario y hallazgos de auditoría.

**A. Problema**

| Evidencia | Dato | Fuente |
|---|---|---|
| Cobertura | Sudán del Sur: 11 % mensual frente a una meta del 20 %; el 55 % de los puntos de distribución en crisis no se visitó | [A06] |
| Seguimiento | Haití: el 50 % de los casos de monitoreo de proceso abiertos, 24 de ellos con más de 60 días; entre el 10 % y el 35 % de los reportes de socios sin cargar | [A15] |
| Requisitos mínimos | Ecuador: no se cumplieron en 2024; una actividad sin monitoreo de registro ni de distribución | [A16] |
| Calidad | Seguimiento posdistribución (PDM) con documentación inadecuada y planes contradictorios | [A24] |
| Estándar | No hay estándar obligatorio de PDM; el menú de indicadores "is still evolving" | [R07] |
| Recortes | Se detuvo el monitoreo de algunos sistemas de seguridad alimentaria | [M05] |

**B. Cadena de actores:** monitores de campo o firma de monitoreo por terceros (TPM) → jefe de MEAL → dirección de programa. **Compran** el donante (FCDO contrata directamente) y las agencias ONU (UNGM).

**C. Demanda observable (compra real, con montos):**
- FCDO Siria (Cowater): **£10 M**, feb-2024 a feb-2027 [T16].
- FCDO Somalia MEL: £13,2 M, licitación retirada [T17].
- PNUD Somalia: TPM sin monto publicado [T18].
- UNOPS Yemen: 59.680 USD [T19].

Es la oportunidad con **más compra observable y montos públicos**, pero lo que se compra es **servicio de campo**, no software.

**D. Capacidad y disposición de pago:** los donantes y las agencias ONU pagan TPM. Las INGO usan su personal de MEAL. Las ONG locales dependen de la línea de MEAL del proyecto.

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Firmas de TPM (Cowater y otras) | Verificación independiente | ONU, donantes | Contrato | £10 M en 3 años [T16] | Acceso a zonas restringidas | Caras; no reducen la carga del socio |
| Kobo / SurveyCTO / CommCare | Recogida de PDM | Todos | Gratis / SaaS | [M26, R18] | Baratos | No comparan resultados entre organizaciones |
| Ground Truth Solutions | Percepción agregada | ONU, donantes | Consultoría | Desconocido | Independiente | No gestiona casos individuales |
| SugarCRM / MoDa (PMA) | Seguimiento de casos | PMA | Interno | — | — | No se comunican entre sí [A07] |

**F. Saturación:** **alta** en servicios de TPM, concentrados en pocas consultoras `[conocimiento del modelo — verificar]`, y en herramientas de recogida. El **gap** es el seguimiento hasta el cierre de lo que se encuentra, que se solapa con OP7.

**G. Estado:** **poco resuelto** según las auditorías [A06, A15, A16].

**H. Tendencia:** **INCIERTA.** Los recortes reducen el monitoreo [M05]. La presión por demostrar valor y el acceso restringido sostienen la demanda de TPM.

**I. Barreras de entrada:** presencia en campo, seguridad, reputación. El modelo es de servicios, no de producto.

**J. Tamaño:** contratos sueltos de £10 M y 59.680 USD [T16, T19]. Mercado total: **no estimable**.

**K. Segmentos y geografía:**
- **Contextos de acceso restringido** (Siria, Somalia, Yemen): la demanda de TPM es alta.
- **América Latina:** auditorías del PMA en Ecuador [A16] y Colombia (no leída) [A17]; PDM de efectivo multipropósito en Colombia en 2020 (consorcio ADN Dignidad) [R19].

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | MEDIA | Riesgo fiduciario y auditorías [A06, A15] | m |
| C2 Frecuencia | ALTA | Continua | m |
| C3 Demanda observable | ALTA (servicio de TPM) | [T16, T18, T19] | a |
| C4 No resuelto | MEDIO | [A15, A16] | m |
| C5 Pago | ALTA para servicios / BAJA para herramientas | [T16] | m |
| C6 Competencia | ALTA | Consultoras de TPM | m |
| C7 Diferenciación | BAJA para un producto | — | b |
| C8 Tendencia | INCIERTA | [M05] | b |
| C9 Barreras | ALTAS (campo, seguridad) | — | m |
| C10 Acceso a usuarios | MEDIO | — | b |

**M. Evidencia contraria:** el TPM ya está resuelto por un mercado de consultoras. El gap de seguimiento es un problema de gestión de casos, que se trata en OP7.

---

### OP7. Quejas y feedback vinculados a la corrección de datos y pagos

**Enunciado.** Los equipos de rendición de cuentas a las poblaciones afectadas (AAP) y de programa reciben quejas por canales y sistemas que no se comunican, y no pueden seguirlas hasta que se corrige el dato o el pago. Por eso persisten los errores de pago y de inclusión, no se detectan el fraude ni la explotación y abuso sexual (PSEA), y se pierde la confianza.

**A. Problema**
- **Quién lo vive:** la persona receptora (afectada); los operadores de la central de llamadas y los equipos de mecanismos de quejas (CFM/FRM), que operan; la jefatura de programa o de AAP, que decide.
- **Parte del ciclo:** después del pago, en el bucle que va de la queja a la corrección del registro o del pago.
- **Causas:**
  - varios canales: línea, mesas de socios, cara a cara;
  - sistemas desconectados (MoDa ↔ SugarCRM; línea 1458 ↔ MoDa);
  - ausencia de protocolos;
  - poca gente: la línea de Sudán del Sur funciona solo en horario laboral, con 2 líneas y 3 personas [A06].
- **Workaround:** Excel, SugarCRM y personal con SQL, Python o Power BI. Una vacante del PMA en Kyiv pide esas habilidades para gestionar el mecanismo de quejas de cash [R14].
- **Si no se resuelve:** los errores de OP2 y OP3 no se corrigen; no se detectan fraude ni PSEA (Haití: menos de 10 casos de PSEA, lo que sugiere subreporte [A15]); hallazgos de auditoría.

| Evidencia | Dato | Fuente |
|---|---|---|
| Trazabilidad | Mozambique: sin "traceability from the intake… to their final resolution"; "no tracking of closure time"; duplicados; casos cerrados sin resolución documentada | [A14] |
| Volumen | Mozambique: 340.000 consultas a la línea interagencia en 2023, 32.000 humanitarias. Haití: unos 24.000 mensajes. Ecuador: más de 11.800 casos en SugarCRM (2024–25) | [A14, A15, A16] |
| Integración | Chad: la línea de respuesta automática (IVR) caída, cuando recibía el ~37 % de las quejas; ninguno de 14 casos de la muestra llegó del formulario al CRM | [A07] |
| Priorización | Ecuador: prioridad mal clasificada; el tablero no muestra retrasos ni tiempo de cierre | [A16] |
| Canal | Sudán del Sur: el 85 % del feedback entra por mesas de socios sin protocolo | [A06] |
| Percepción | Somalia: solo el 47 % sabe cómo quejarse (57 % en 2020) | [R09] |
| Sector | En la CHS, el compromiso 5 (quejas) es el más débil | [R11, R12] |
| Datos | Solo el 41 % de las personas receptoras entiende cómo se usan sus datos | [M02] |

**B. Cadena de actores**

| Rol | Quién | Evidencia |
|---|---|---|
| Afectado | La persona receptora | [R09, M02] |
| Operativo | Central de llamadas, asociados de CFM | [R14] |
| Decisor | Jefatura de programa o AAP en la oficina de país | — |
| Comprador | La agencia (ACNUR, PMA) o la agencia que lidera una línea interagencia | [T15] |
| Sponsor | Coordinador humanitario (RC/HC), grupos de AAP | — |
| Financiador | CERF, con una partida de AAP de 3–4 M USD que financia "collective feedback mechanisms" [R13]; donantes del proyecto | [R13] |

**C. Demanda observable**
- **Comportamiento real:**
  - ACNUR RFP-3243 en Pakistán (2026): acuerdo marco para crear y gestionar una línea interagencia con software de helpdesk [T15];
  - vacantes del PMA para mecanismos de quejas y central de llamadas [R14];
  - plataformas propias de la ONU: SugarCRM en el PMA; RapidPro en UNICEF, con 130 oficinas de país [R16];
  - partida específica del CERF [R13].
- **No se encontró** ninguna licitación de software independiente para mecanismos de quejas. Lo que se compra es **servicio de central de llamadas**, y las licencias genéricas se consiguen gratis o donadas.

**D. Capacidad y disposición de pago**

| Segmento | Capacidad | Cómo se compra | Alternativas | Probabilidad de compra |
|---|---|---|---|---|
| Agencias ONU | ALTA | Licitación de servicios; desarrollo interno | SugarCRM, RapidPro | BAJA-MEDIA para un tercero |
| INGO grandes | MEDIA | CRM genérico | Salesforce, Dynamics, Zendesk | DESCONOCIDA |
| INGO medianas | MEDIA-BAJA | Línea del proyecto | Zendesk donado, Kobo | DESCONOCIDA |
| ONG locales | BAJA | Mecanismos colectivos o interagencia (CERF, fondos mancomunados) | Kobo + Excel | BAJA |

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Líneas interagencia (Linha Verde, ACNUR Pakistán) | Recepción colectiva | ONU, sector | Contrato | No publicado | Una sola puerta de entrada | No siguen la queja hasta el cierre; exigen teléfono [A14] |
| SugarCRM / Dynamics / Salesforce | Gestión de casos | ONU, INGO grandes | Licencia | Salesforce: 10 licencias gratis y luego 60–100 USD por usuario/mes [M26] | Flujo de casos | Mal configurados (Ecuador); sin conexión con los datos de pago (Chad) |
| Zendesk Tech for Good | Mesa de ayuda | ONG | Donación | Gratis [R17] | Maduro | Genérico |
| RapidPro / U-Report | Mensajería | UNICEF y socios | Open source | 0 | Escala | Solo es el canal [R16] |
| Kobo + Excel | Registro | ONG locales | Gratis | 0 | Accesible | No permite seguir casos |
| Mesas de ayuda presenciales | Recepción | Todos | Personal | Interno | Las personas las prefieren | Sin protocolo [A06] |

**F. Saturación**
- **Alta** en canales y en CRM genéricos, muchos gratuitos o donados.
- **Baja** en el vínculo entre la queja, el registro de la persona y la corrección del pago, y en medir el tiempo de cierre.
- **Gaps:** ese vínculo; deduplicar las quejas entre canales; canales para personas sin teléfono (en América Latina, ~30 % de los refugiados y migrantes no tenía celular en 2020 [R15]).

**G. Estado:** **poco resuelto** [A14, A15, A16, A06, A07, R11].

**H. Tendencia:** **INCIERTA.** Hay presión creciente: partida del CERF, el reset, auditorías repetidas. Pero los recortes amenazan las líneas: la de Chad estaba caída [A07].

**I. Barreras de entrada:**
- datos sensibles (PSEA) y protección;
- integración con los sistemas de identidad y pago propios de cada agencia (MoDa, SCOPE);
- las personas prefieren el cara a cara;
- RapidPro y Zendesk son gratuitos.

**J. Tamaño:** volúmenes de 340.000, 24.000 y 11.800 contactos por país [A14, A15, A16]; partida del CERF de 3–4 M USD [R13]. Mercado: **no estimable**.

**K. Segmentos, contextos y geografía:**
- **Contextos inseguros:** se prefiere el canal cara a cara [R10].
- **América Latina:** auditoría del PMA en Ecuador (SugarCRM, línea, email, avisos en supermercados) [A16]; encuesta R4V de 2020 (WhatsApp como canal preferido) [R15]; grupo de trabajo de AAP/CwC en R4V.

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | ALTA | Errores sin corregir, PSEA no detectada [A14, A15] | m |
| C2 Frecuencia | ALTA | Volúmenes de decenas o cientos de miles [A14] | m |
| C3 Demanda observable | MEDIA | RFP de ACNUR, partida del CERF, vacantes [T15, R13, R14] | m |
| C4 No resuelto | ALTO | 5 auditorías y la CHS [A06, A07, A14, A15, A16, R11] | m |
| C5 Pago | MEDIA-BAJA | Servicios sí; software gratuito o donado | b |
| C6 Competencia | ALTA en canales / BAJA en el vínculo queja → corrección | — | b |
| C7 Diferenciación | MEDIA | El vínculo con la corrección de datos y pagos no aparece como oferta (inferencia) | b |
| C8 Tendencia | INCIERTA | [R13, A07] | b |
| C9 Barreras | MEDIAS-ALTAS | Datos sensibles, integración | m |
| C10 Acceso a usuarios | MEDIO | Las vacantes de AAP y CFM son públicas | b |

**M. Evidencia contraria:**
- La CHS dice que el fallo es de práctica y compromiso, no de herramienta [R11].
- En Ecuador solo quedaban 4 casos abiertos de más de 11.800: el cierre funciona aunque la priorización falle [A16].
- En Haití el 61 % de los mensajes eran peticiones o problemas técnicos, no quejas [A15].
- Las personas evitan los mecanismos por desconfianza [R10]: puede que el problema sea que no se presentan quejas, más que no poder procesarlas.

---
### OP8. Detección tardía de anomalías y colusión en datos transaccionales

**Enunciado.** Las áreas de finanzas y cumplimiento detectan tarde la colusión interna, la colusión con agentes o comercios y las anomalías de pago. Los datos de transacción existen, pero nadie los analiza, y los incidentes se reportan con semanas de retraso. El resultado son pérdidas y suspensiones de programas enteros.

*El screening de sanciones queda fuera: es un requisito transversal y un mercado saturado de proveedores de cumplimiento [X08]. También queda fuera el desvío por autoridades de facto, que es un problema político [A23].*

**A. Problema**

| Evidencia | Dato | Fuente |
|---|---|---|
| Datos no analizados | Chad: transacciones "within 20 or 30 seconds" en el mismo terminal, y fuera de horario, sin analizar | [A07] |
| Sin análisis corporativo | El PMA no tiene análisis corporativo de casos de fraude | [A10] |
| Detección tardía | GiveDirectly RDC: unos 6 meses en detectarlo; ~1,2 M USD y unas 1.900 familias. El personal registraba SIM a nombre de los receptores | [X03] |
| Reporte lento | PMA Etiopía: 66 días de retraso medio en reportar incidentes | [A21] (ayuda en especie) |
| Volumen de alegaciones | PMA 2025: 2.010 alegaciones (+12 %), el 63 % de fraude o corrupción; 1,90 M USD en juego, 9,94 % recuperado | [A19] |
| Volumen de alegaciones | ACNUR: 2.011 quejas, 18 % por fraude con impacto financiero; 490 implican a personal de socios | [A20] |
| Percepción | La preocupación por fraude en CVA pasó del 36 % (2020) al 42 % (2023) | [X01] |
| Tasa de pérdida | GiveDirectly: 0,27 % global; RDC 2,98 %; Malawi 9,8 % de fraude de inscripción antes de corregirlo | [X02] |

**B. Cadena:** finanzas y cumplimiento en el país (operan) → Head of Compliance/Risk (decide) → Compliance, Finanzas e IT de la sede (compran) → CFO, auditoría interna y junta (sponsors) → donante, a través de costes indirectos (financia).

**C. Demanda observable:**
- Se compra screening de terceros (WeWorld compró Bridger XG) [X08].
- GiveDirectly añadió controles automáticos **después** de la pérdida [X02].
- La Oficina del Inspector General del PMA tiene un presupuesto de 18,83 M USD, con un recorte del 8,6 % [A19].
- **No se encontraron compras de detección de anomalías por parte de ONG medianas o locales.**

**D. Capacidad y disposición de pago:**
- ONU: OIG propias y sistemas internos.
- INGO grandes: licencias de screening.
- INGO medianas y ONG locales: capacidad limitada; asumen el riesgo que les traslada el donante [X01].
- ECHO pide reportar todo caso sustanciado y considera significativo cualquier caso de más de 10.000 EUR [X07]. No queda claro si el gasto en control es elegible.

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| LexisNexis Bridger, World-Check, Dow Jones | Screening de sanciones | INGO | Licencia | No público | Maduros | No detectan colusión [X08] |
| Building Blocks | Deduplicación | ONU, CWG | Gratis | 0 | Escala | No detecta fraude interno |
| TPM, spot-checks, líneas de denuncia | Detección | Todos | Servicio | Variable | En terreno | Lentos |
| Controles internos de las plataformas (121 con registro de cambios; HOPE; RedRose) | Trazas de auditoría | Varios | Varios | — | Privacy-by-design (121) | La detección de fraude no está documentada |

**F. Saturación:**
- **Alta** en screening.
- **Baja** en detección de colusión con datos transaccionales.
- **Gap:** los datos existen pero nadie los analiza [A07, A10].

**G. Estado:** **parcialmente resuelto.** Screening y deduplicación, sí. Colusión y anomalías, poco [A07, X03].

**H. Tendencia:** **CRECE la exigencia** (fraude percibido, alegaciones, OIG de EE. UU. sobre vetting en Gaza [A22]) **con menos recursos** (recorte en la OIG del PMA [A19]).

**I. Barreras de entrada:**
- acceso a datos sensibles;
- confianza institucional;
- un falso positivo puede excluir a una persona;
- competencia de herramientas gratuitas;
- ciclos de compra largos.

**J. Tamaño:** solo hay volúmenes de alegaciones [A19, A20]. Mercado: **no estimable**.

**K. Segmentos y geografía:**
- **Patrones de fraude distintos por región:**
  - Afganistán, Yemen, Sudán: desvío político [A23].
  - Somalia: gatekeepers que se quedan con parte de la ayuda; desvío en 55 de 55 sitios [X16].
  - RDC y Malawi: colusión con agentes y fraude de inscripción [X02].
- **América Latina:** no se encontraron casos públicos de fraude en CVA con cifras. **Desconocido.**

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | MEDIA-ALTA | Pérdidas y suspensiones [X03, A19] | m |
| C2 Frecuencia | MEDIA | Las tasas de pérdida son bajas en promedio, con picos [X02, X04] | m |
| C3 Demanda observable | BAJA (fuera del screening) | [X08] | m |
| C4 No resuelto | MEDIO | [A07, A10] | m |
| C5 Pago | BAJA-DESCONOCIDA | — | b |
| C6 Competencia | ALTA en screening / BAJA en anomalías | — | b |
| C7 Diferenciación | MEDIA | — | b |
| C8 Tendencia | CRECE la exigencia | [X01, A22] | m |
| C9 Barreras | ALTAS | Datos, confianza | m |
| C10 Acceso a usuarios | BAJO | Es un tema sensible | b |

**M. Evidencia contraria:**
- CALP/Key Aid (2026): el CVA "no aumenta inherentemente el riesgo de desvío" [X01].
- Las pérdidas en cash rondan el 2 % [X04]; en GiveDirectly, el 0,27 % [X02].
- El screening de receptores es una herramienta "ineficaz" contra la financiación del terrorismo [X05].
- Los mecanismos actuales sí sustancian casos [A19].
- **Lectura:** puede tratarse mejor como una **parte de OP3** (anomalías visibles al conciliar) que como oportunidad propia.

---

### OP9. Entrega con liquidez o conectividad limitada (parte operativa de O5)

**Enunciado.** Las ONG que entregan efectivo en contextos sin liquidez o con cortes de comunicaciones no consiguen que el dinero llegue a tiempo y a un coste razonable. Como consecuencia, entre el 20 % y el 60 % del valor se pierde en comisiones, o la ayuda llega meses tarde.

**A. Problema**

| Evidencia | Dato | Fuente |
|---|---|---|
| Comisiones en Gaza | Retirar efectivo: 20–40 % (5 % durante la tregua). Cambistas: 50–60 %. Pagar con e-wallet: ~15 % más caro | [L01, L02] |
| Liquidez en Sudán | Los bancos tardan semanas en reunir liquidez; los agentes cobran hasta un 20 % | [L26] |
| Retraso en Myanmar | 5–6 meses después del terremoto, con "cash liquidity constraints" | [L09] |
| Acceso financiero | El 70 % de las ONG tiene dificultades para transferir fondos | [L08] |
| Sahel | Restricciones y prohibiciones del efectivo, con 7 causas identificadas | [L06] |

**B. Cadena:** la responsable de CVA o de finanzas del país opera; la dirección del país o el consorcio decide; la sede de la ONG compra (procurement de FSP); financian ECHO, FCDO y los fondos mancomunados.

**C. Demanda observable:**
- Mercy Corps contrató a Last Mile Technology en Sudán [L03].
- UNCDF y PalPay incorporaron unos 1.000 comercios a pagos digitales en Gaza, con 205.000 USD + 82.000 USD [L02].
- La regulación y el de-risking solo aparecen como **llamados de política** [L07].

**D. Pago:** se paga **comisión** a FSP y a agentes informales. Los montos de los contratos no son públicos.

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Hawala, hundi, cambistas | Liquidez y entrega | Todos | Comisión | 20–60 % [L01, L02] | Funcionan sin bancos | Coste; riesgo de sanciones |
| Bankak, PalPay y e-wallets locales | Transferir sin efectivo | ONG locales, grupos de ayuda mutua | Comisión | Desconocido | ~1 semana en Sudán [L05] | Dependen de la red |
| Last Mile Technology | Entrega donde no hay banca | Consorcios | Contrato | Desconocido | Probado en Sudán [L03] | Sin evaluación independiente |
| Smartcards offline (People in Need), RedRose offline, SCOPE | Funcionar sin conexión | INGO, ONU | Licencia o interno | Desconocido | Offline | Necesitan comercios equipados; sin evaluaciones independientes recientes |
| Satélite | Conectividad | INGO | Suscripción | Desconocido | Inmediato | Legalidad incierta |

**F. Saturación:** los mecanismos locales e informales están muy ocupados. **El cuello de botella es la liquidez y la regulación**, no la herramienta (ver market-beliefs.md, C4).

**G. Estado:** **poco resuelto**, pero sobre todo por causas fuera del alcance de un producto.

**H. Tendencia:** **CRECE.** Sudán, Gaza y Myanmar siguen activos, y aumentan las restricciones en el Sahel [L06, M02].

**I. Barreras de entrada:** licencias financieras, sanciones, seguridad, alianzas con telecomunicaciones y presencia local.

**J. Tamaño:** plan de efectivo multipropósito de Sudán 2025: 201,8 M USD para 1,8 M de personas (necesidades, no gasto) [L04]. Mercado: **no estimable**.

**K. Geografía:**
- Liquidez y comunicaciones: Gaza y Sudán.
- Restricciones políticas: Sahel.
- Liquidez en Haití: no hay evidencia reciente [L23].
- **América Latina:** el problema parece menor, salvo en Haití y Venezuela `[conocimiento del modelo — verificar]`.

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | ALTA | 20–60 % del valor perdido [L01, L02] | a |
| C2 Frecuencia | ALTA en conflictos | [L26, L06] | a |
| C3 Demanda observable | MEDIA (servicios de entrega) | [L03, L02] | m |
| C4 No resuelto | ALTO | — | a |
| C5 Pago | MEDIA (comisión) | — | m |
| C6 Competencia | ALTA (agentes informales, FSP) | — | m |
| C7 Diferenciación | BAJA para un producto que no sea un FSP | — | m |
| C8 Tendencia | CRECE | [L06] | m |
| C9 Barreras | MUY ALTAS (licencia financiera, sanciones) | [L07] | a |
| C10 Acceso a usuarios | BAJO (zonas de conflicto) | — | m |

**M. Evidencia contraria:** las transferencias grupales en Sudán llegaron en ~1 semana vía Bankak [L05]. Los actores locales ya tienen workarounds que funcionan.

---

### OP10. Carga de cumplimiento y reporte que los intermediarios trasladan a los actores locales

**Enunciado.** Las ONG nacionales y locales tienen que cumplir requisitos de due diligence y de reporte que les imponen, cada uno por su lado, varios intermediarios. Por eso gestionan poco CVA de principio a fin y dependen de las herramientas y criterios de otros.

**A. Problema**

| Evidencia | Dato | Fuente |
|---|---|---|
| Financiación directa a ONG locales en Ucrania | Menos del 1 % (80,1 M USD de 9,95 mil M) | [L10] |
| CVA gestionado de principio a fin por ONG locales en Ucrania | 3,4 % de 2,1 mil M USD | [L10] |
| Passporting de due diligence | Solo 8 de 20 INGO lo aceptan | [L10] |
| Corrupción sustanciada | 0 casos confirmados en Ucrania | [L10] |
| Carga documental en Sudán | Algunos donantes exigieron "paper trails" que crearon "significant unexpected burdens" | [L05] |
| Fortalecimiento de capacidades | El 78 % se dedica a sistemas financieros (C4C, n=32) | [L11] |
| Herramientas impuestas | World Vision forma a sus socios en su propia plataforma SMAP | [L14] |
| Retroceso | ACNUR: 0 % de alianzas directas con ONG locales en Cox's Bazar en 2026 | [L12] |

**B. Cadena:** el personal de la ONG local es el afectado. **Decide quien impone el requisito** (la ONU o la INGO intermediaria). Compra el intermediario o el donante, con presupuesto de fortalecimiento de capacidades. Financian donantes, fondos CBPF y Start Network.

**C. Demanda observable:**
- Hay inversión en fortalecimiento de capacidades [L11].
- Alianza Start Network–NetHope para "digital readiness" [L13].
- Una licitación local pequeña (SARD) [T07].
- La armonización de requisitos se plantea como **acuerdo entre actores**, no como compra [L10, L11].

**D. Pago:**
- ONG locales: capacidad muy baja.
- Intermediarios: pagan con costes indirectos (el 70 % de las oficinas de C4C los traslada a la mayoría de sus socios) [L11].
- Herramientas gratuitas: Kobo, 121 [M26, M32].

**E. Alternativas**

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Herramientas del intermediario (LMMS, SMAP, Building Blocks) | Reportar al intermediario | Socios | Impuesta | 0 para el socio | Integración | Dependencia |
| Passporting de due diligence | Evitar evaluaciones duplicadas | Sector | Acuerdo | — | Reduce la carga | Baja adopción [L10] |
| Kobo, Excel, WhatsApp | Todo | ONG locales | Gratis | 0 | Flexibles | No escalan |
| Aidonic, Rahat | CVA para actores locales | ONG locales | SaaS / bien público digital | Desconocido | Foco local | Poca evidencia de uso (COMERCIAL) [M33] |

**F. Saturación:** hay muchas herramientas gratuitas o impuestas. **El gap es la armonización de requisitos, que es política.**

**G. Estado:** **poco resuelto**; la causa es de poder y financiación [M35, L10].

**H. Tendencia:** **INCIERTA.** El discurso sube; los fondos bajan (−27 %) [M01].

**I. Barreras de entrada:** quien paga no es quien sufre el problema; los intermediarios imponen sus sistemas; la capacidad de pago local es casi nula.

**J. Tamaño:** 4,3 % de financiación directa (~2,4 mil M USD con la indirecta) [M01]. Mercado: **no estimable**.

**K. Geografía:**
- Ucrania: hay capacidad local, pero no fondos.
- Sudán: las salas de respuesta de emergencia (ERR) operan fuera del sistema formal.
- **América Latina:** sin datos nuevos. RMRP 2026 tiene 152 socios [M09] y solo un 8,1 % de financiación [M09].

**L. Valoración**

| Criterio | Valor | Evidencia | Confianza |
|---|---|---|---|
| C1 Intensidad | ALTA | [L10, L05] | m |
| C2 Frecuencia | ALTA | En cada acuerdo con un intermediario | m |
| C3 Demanda observable | BAJA-MEDIA | Fortalecimiento de capacidades, no compra de producto [L11] | m |
| C4 No resuelto | ALTO | [L10] | m |
| C5 Pago | BAJA | [M01, L11] | m |
| C6 Competencia | MEDIA | Herramientas impuestas o gratuitas | m |
| C7 Diferenciación | BAJA | El gap es de acuerdos, no de producto | m |
| C8 Tendencia | INCIERTA | [M01, M13] | m |
| C9 Barreras | ALTAS (poder, quién paga) | — | m |
| C10 Acceso a usuarios | MEDIO | Redes como NEAR o C4C (inferencia) | b |

**M. Evidencia contraria:** con 0 casos de corrupción en Ucrania, los requisitos parecen desproporcionados más que faltos de herramientas [L10]. La rendición de cuentas horizontal de las transferencias grupales funciona sin sistemas [L05].

---

### OP11. Gestión de comercios en programas de vouchers

**Enunciado.** Las organizaciones que usan vouchers tienen que seleccionar, pagar y monitorear comercios. Si el pago se retrasa o los controles fallan, los comercios abandonan el programa y las personas pagan más o esperan más.

- **Evidencia:**
  - El PMA tiene más de 4.200 comercios contratados [L16].
  - En Gaza hay unos 1.000 comercios con pagos digitales [L02].
  - World Vision: los retrasos de pago "erode trust and risk disengagement" [L27].
  - La frecuencia de retrasos, sus costes y los errores son **desconocidos**.
- **Demanda:** se resuelve dentro de las organizaciones (retail engagement del PMA [L16]; módulo de e-voucher en LMMS de World Vision [L15]). **No se encontraron licitaciones externas.**
- **Pago:** se concentra en el PMA (33 % de su CVA son vouchers) [M06], que lo resuelve con medios propios.
- **Alternativas:** el PMA con sus propios medios; LMMS; RedRose; smartcards; PalPay QR (Gaza); vouchers en papel.
- **Estado:** **desconocido**, por falta de datos recientes.
- **Tendencia:** **DECRECE en términos relativos** por el enfoque cash first [M04, M14]. Persiste en contextos sin liquidez.
- **América Latina:** los country briefs del PMA para Haití y Guatemala (2025) solo reportan efectivo [L23]. Es una señal débil de que los vouchers pesan poco en la región; **verificar**.
- **Valoración:**
  - C1 MEDIA (b)
  - C2 DESCONOCIDA
  - C3 BAJA (m)
  - C4 DESCONOCIDO
  - C5 BAJA (m)
  - C6 ALTA en el segmento grande (m)
  - C7 BAJA (b)
  - C8 DECRECE (m)
  - C9 MEDIAS
  - C10 BAJO (b)
- **Evidencia contraria:** los grandes ya tienen capacidad propia, y el universo de compradores se reduce.

---

### OP12. Alineación de programas humanitarios con sistemas nacionales de protección social

**Enunciado.** Los actores humanitarios no logran alinear registros, valores y pagos con los sistemas nacionales de protección social. El resultado es duplicación, vacíos y transiciones lentas.

- **Evidencia:**
  - **Escala:**
    - ESSN Türkiye: 1,5 M de personas, traspasadas al Ministerio y a Kızılay [L18].
    - Baxnaano (Somalia): más de 4 M de personas [L19].
    - Líbano: respuesta ampliada "mostly through" las redes de protección del gobierno [L20].
    - Ucrania 2026: 889 M USD de CVA alineado con el sistema nacional [L21].
  - **Alcance:** la integración sigue siendo "small-scale" [M03].
- **Cadena:** el CWG y el ministerio operan; decide el ministerio. **El comprador es el gobierno**, con préstamos o donaciones del Banco Mundial o del BID (licitación del sistema de información en Irak [T23]).
- **Demanda:** compra real y grande **del lado del gobierno**. Del lado humanitario solo hay **intención** de alinearse.
- **Alternativas:**
  - bienes públicos digitales gratuitos (OpenSPP, OpenG2P) [L24];
  - estándares de la Digital Convergence Initiative;
  - integradores contratados por licitación;
  - sistemas de deduplicación de los grupos de coordinación (ICCG) [L21].
- **Estado:** bien documentado en política; costes **desconocidos**.
- **Tendencia:** **CRECE** en el discurso, empujada por los recortes [L25, L20].
- **Barreras:** compra soberana, exigencia de bienes públicos digitales, soberanía de datos, integradores ya establecidos.
- **América Latina:**
  - Los Estados tienen sistemas fuertes; el comprador es el gobierno.
  - Brasil (2024) pagó el Auxílio Reconstrução sin intervención humanitaria [L22].
  - Guatemala tiene pilotos conjuntos entre PMA, gobierno y OIM [L23].
- **Valoración:**
  - C1 MEDIA (m)
  - C2 MEDIA (m)
  - C3 BAJA en el lado humanitario (m)
  - C4 MEDIO (m)
  - C5 BAJA para una ONG / ALTA para un gobierno (m)
  - C6 ALTA (m)
  - C7 BAJA (b)
  - C8 CRECE (m)
  - C9 MUY ALTAS (m)
  - C10 BAJO (b)
- **Evidencia contraria:**
  - Brasil lo resolvió sin humanitarios [L22].
  - En Sudán, Myanmar o Gaza no hay un sistema estatal con el que alinearse.

---
## 5. Segmentación comparada

**Probabilidad de compra a un tercero por segmento.** Cada valor se apoya en evidencia de la ficha correspondiente.

| Oportunidad | Agencias ONU | INGO grandes | INGO medianas | ONG nacionales/locales | Gobiernos |
|---|---|---|---|---|---|
| OP1 Deduplicación | BAJA: construyen (UN80, EDS) | BAJA: gratis vía CWG | BAJA | BAJA | n/a |
| OP2 Integridad de lista | BAJA: construyen | MEDIA: dentro de una plataforma | MEDIA: licitaciones de plataforma [T06, T01] | BAJA-MEDIA [T07] | n/a |
| OP3 Ciclo de pago y conciliación | BAJA: construyen | MEDIA: FSP + tecnología [T02, T03] | MEDIA [T06, T12] | BAJA-MEDIA [T07] | n/a |
| OP4 Contratación de FSP | BAJA | BAJA (compran el FSP, no la gestión) | BAJA | BAJA | n/a |
| OP5 Reporting a donantes | BAJA | BAJA-MEDIA (licencias genéricas) | BAJA-MEDIA | BAJA | n/a |
| OP6 Monitoreo y verificación | ALTA para servicios de TPM | MEDIA | BAJA | BAJA | n/a |
| OP7 Quejas → corrección | BAJA-MEDIA (servicios de central) | DESCONOCIDA | DESCONOCIDA | BAJA | n/a |
| OP8 Anomalías | BAJA | DESCONOCIDA | DESCONOCIDA | BAJA | n/a |
| OP9 Liquidez y conectividad | Compran FSP | Compran FSP | Compran FSP | Usan agentes informales | n/a |
| OP10 Carga en cascada | n/a | Pagarían como intermediarios: DESCONOCIDA | DESCONOCIDA | BAJA | n/a |
| OP11 Comercios | BAJA (el PMA lo hace con medios propios) | BAJA | BAJA | BAJA | n/a |
| OP12 Protección social | Cofinancian | BAJA | BAJA | BAJA | ALTA (B2G, fuera de perfil) |

**Diferencias por contexto (solo donde hay evidencia)**

| Contexto | Qué cambia | Fuentes |
|---|---|---|
| Emergencia | Duplicados masivos, contratos de FSP retroactivos, comisiones del 15–25 %, retrasos de 3–4 meses | [A02, A03, F07] |
| Crisis prolongada | Identificadores débiles, conciliación agregada, muchas fuentes de identificación | [A01, A04, D07] |
| Baja conectividad o liquidez | Papel, pagos en ventanilla, agentes informales; el cuello de botella es el mercado | [A01, L01, L26] |
| Urbano y digitalizado | Hay integración (Rumanía con DHOTS, Etiopía con API); el FSP ofrece acceso directo | [A01, F01, F06] |
| Protección social | El comprador es el gobierno | [L18, L19, T23] |

## 6. Tratamiento especial: OP3, conciliación

Se aplica el mismo criterio adversarial que al resto de oportunidades. El objetivo es entender el problema, no defenderlo.

### 6.1 Dónde ocurre la conciliación exactamente

| Punto | Qué se compara | Sistemas | Quién | Evidencia |
|---|---|---|---|---|
| Sistema de casos ↔ FSP | Manifiesto de pago frente a la hoja o el informe de distribución del FSP | MIS de beneficiarios (CashAssist, SCOPE, Excel) ↔ portal o archivo del FSP | Cash / Finanzas | 5 de 7 operaciones de ACNUR "manually transferred payment information to and from FSP systems" [A01] |
| Sistema de pagos ↔ ERP | Totales del sistema de pagos frente al libro contable | CashAssist ↔ MSRP (ERP) | Finanzas | 71 M USD sin conciliar [A02] |
| Registro ↔ sistema de pago | Sincronización de datos | proGres ↔ CashAssist | Gestión de información | Casos sin sincronizar "for months" [A01] |
| Socio ejecutor ↔ agencia | Hojas de pago del socio frente al manifiesto | Excel del socio ↔ sistema de la agencia | Socio / programa | "did not have unique identifiers" [A04] |
| Lo financiero ↔ lo programático | Lo distribuido frente a lo previsto, por beneficiario | Sistema de programa ↔ informes | Finanzas / programa | "did not perform reconciliations at the beneficiary level" [A08] |
| Contrato del FSP ↔ cuenta | Saldo, reembolso, factura | Extracto ↔ contrato | Finanzas / Logística | "Final reconciliation of third party / transfer company account"; "a refund may be requested" [F08] |
| ONG ↔ comercio (vouchers) | Canjes frente a facturas | Sistema de vouchers ↔ factura | Finanzas o Logística | Vouchers en papel: 3–4 semanas para pagar al comercio (Yemen, 2016; ver market-beliefs.md, fuente 2.01) |

### 6.2 Actores

- **Programas** aporta la prueba de entrega.
- **Finanzas** valida la conciliación.
- **Logística** gestiona el contrato [F08]. En el CICR, Logística concilia los vouchers (ver market-beliefs.md, fuente 2.03).
- **Roles mixtos:** el "Payment Officer" de Mercy Corps (market-beliefs.md, fuente 2.05) y las vacantes de IFRC de 2026, donde CVA y Finanzas comparten la conciliación [F09].
- **Auditoría interna** actúa como sponsor del cambio [A01, A09].

### 6.3 Errores típicos y excepciones

Todos están documentados en [A01], [A02], [F05] y [A11]:

- pagos marcados como exitosos con importe cero;
- conciliación "amplia" que no detecta compensaciones (unos reciben de menos y otros de más por el mismo importe);
- identificadores ausentes o repetidos;
- pagos duplicados;
- efectivo no cobrado y tarjetas inactivas;
- comisiones cobradas sobre lo no cobrado;
- comisiones no registradas;
- reversión de no cobrados a petición escrita;
- pagos en ventanilla con hojas impresas.

### 6.4 Tiempos, retraso en pagos, cierre financiero y reporting a donantes

**Tiempos:**
- Sudán del Sur: conciliación aprobada a los 3–6 meses [A06].
- Haití: anticipos conciliados "months late" [A11].
- Sierra Leona: pasó de conciliar a fin de mes a hacerlo a diario cuando tuvo acceso directo a la plataforma del FSP [F01].
- Tiempo de personal por ciclo: **desconocido**, salvo el caso de Oxfam (5 personas a tiempo completo) [F12].

**Retraso en pagos:**
- A comercios, con vouchers en papel: 3–4 semanas (market-beliefs.md, fuente 2.01).
- A personas, en Ucrania: 3–4 meses de retraso para 92.947 personas [A02].

**Cierre financiero:** hay comisiones sin registrar en los estados financieros [A02].

**Reporting a donantes:** **no se encontró evidencia directa** de que un retraso de conciliación haya retrasado un informe a un donante. Es un vacío.

### 6.5 Soluciones disponibles y quién las compra

| Solución | Qué resuelve | Segmento | Modelo | Precio | Fortalezas | Limitaciones |
|---|---|---|---|---|---|---|
| Excel / macros | Cruzar listas | Todos | Gratis | 0 | Flexible | Errores; no escala [A18, A06] |
| Hojas impresas (pago en ventanilla) | Prueba de entrega | Contextos sin conectividad | Manual | — | Funciona sin red | "error-prone" [A01] |
| CashAssist + DHOTS (ACNUR) | Manifiesto ↔ FSP ↔ ERP | Solo ACNUR | Interno | n/a | Corporativo | Integrado en 2 de 7 operaciones; 232 M USD de pagos fuera del sistema en 2022–23 [A01] |
| SCOPE (PMA) | Beneficiarios y transferencias | PMA y socios | Interno | n/a | Escala | Tablero de Chad roto; sin conciliación por beneficiario [A07, A08] |
| Portal o informe del FSP | Estado de cada transacción | Clientes del FSP | Incluido en la comisión | Dentro de la comisión | Visibilidad diaria [F01]; Efecty da 3 perfiles de usuario [F06] | Formato propio de cada FSP; informes que pueden ser mensuales [F06] |
| Contrato FSP + dashboard | Seguimiento de la distribución | INGO grandes | Dentro del contrato | No publicado | Un solo proveedor [T03, T02] | Atado al FSP; con varios FSP por país no se sabe qué pasa |
| ERP (MSRP, Dynamics, Unit4) | Cierre contable | Organizaciones grandes | Licencia existente | — | Es el libro oficial | No ve a la persona [A02] |
| RedRose / HOPE / 121 / Humansis | Ciclo CVA con conciliación | INGO, ONU, Cruz Roja | SaaS / bien público digital / open source | No público | Dicen conciliar | Sin evidencia independiente de resultados |
| Consultores o auditores | Conciliación a posteriori | Todos | Servicio | — | — | Llegan tarde |

**Quién compra:**
- En la ONU, la sede construye.
- En las INGO, procurement global compra al FSP y a veces incluye la tecnología.
- En INGO medianas y ONG locales hay licitaciones de plataforma [T06, T01, T07].
- **Nadie compra "conciliación" sola.**

### 6.6 Segmentos y América Latina

- **VenEsperanza (Colombia; Mercy Corps, IRC, World Vision, Save the Children) [F06]:**
  - tres FSP (Banco de Occidente, Davivienda, Efecty);
  - acceso directo a la plataforma de Efecty;
  - informe mensual del banco;
  - plantilla común de incidencias, creada porque cada socio "reported different things in different ways";
  - comisiones de 0,9 % a 1,8 % según el socio;
  - si hay fraude, la responsabilidad "is assumed by the client".
- **Vacantes de IFRC con funciones de conciliación** en Caracas, Colombia y Jamaica (2026) [F09].
- **ACNUR México:** 2 pagos marcados como exitosos con importe cero [A01].
- **PMA Colombia (AR-26-05):** no leída [A17].
- **Plan:** su acuerdo con FSP incluye las Américas [T03].
- **Contexto de la región:** el RMRP 2026 tiene un 8,1 % de financiación [M09] y ACNUR Américas recortó el 42 % de sus programas [M10].

### 6.7 Veredicto adversarial

**A favor:**
- es la oportunidad con evidencia más cuantificada y repetida;
- ocurre en cada ciclo de pago;
- hay señales de compra en INGO (contrato FSP + tecnología, licitaciones de plataforma);
- hay acceso plausible a usuarios en América Latina.

**En contra:**
1. La evidencia dura viene de la ONU, que construye sus propios sistemas.
2. La causa raíz es en buena parte el dato y la gobernanza (OP2), no la falta de herramienta.
3. Los FSP ya ofrecen portales, informes y dashboards dentro de su contrato.
4. No hay ningún RFP específico de conciliación.
5. El comprador más plausible (INGO) prefiere comprar todo en un paquete con el FSP.
6. Los presupuestos se contraen.

**Conclusión:** pasa a investigación primaria **como problema**. **No está demostrado** que sea comprable por separado.

## 7. Tratamiento especial: interoperabilidad

### 7.1 ¿Qué es la interoperabilidad en este mercado?

| Opción | ¿Aplica? | Evidencia |
|---|---|---|
| (a) Problema en sí mismo | **Solo en parte.** El envío de Excel sin cifrar por correo es un riesgo de protección de datos aunque no haya errores | [D01, A08] |
| (b) Causa de otros problemas | **Sí, es su papel principal.** La falta de identificador común, de canales seguros y de formatos compartidos causa duplicación, retrasos, conciliación tardía y reporte que no consolida | [D01, D02, A01] |
| (c) Capacidad de solución | **Sí.** Building Blocks, el sistema federado de Somalia y los estándares de la Digital Convergence Initiative son medios para deduplicar o derivar casos | [D05, D07] |
| **Clasificación** | **(d) Combinación, dominada por (b) y (c)** | "these non-technical aspects are likely more challenging than the technical layer" [D01] |

**Decisión:** no se nombra ninguna oportunidad como "interoperabilidad". Los problemas reales se tratan donde ocurren:
- deduplicación: OP1;
- integridad de la lista: OP2;
- conciliación con el FSP: OP3;
- reporte: OP5.

### 7.2 Traspasos del ciclo y qué información se mueve

| Traspaso | Datos que se mueven | Sistemas | Quién | Cómo | Fallo documentado | Fuente | Problema real (OP) |
|---|---|---|---|---|---|---|---|
| Registro → limpieza y lista maestra | Datos personales del hogar, composición, vulnerabilidad | Kobo/ODK/CommCare → Excel, SCOPE, proGres | Gestión de información / MEAL | Exportación manual a Excel | Datos cambiados después de la lista final; 80 % manual (Mozambique); ~90 % de miembros sin datos biográficos (Chad) | [D09, A13, A08] | OP2 |
| Lista → targeting y asignación | Puntuación, monto, ciclo | Excel/R → SCOPE/HOPE/RedRose | Programa + gestión de información | Hojas que se van actualizando | "multiple and rolling spreadsheets"; listas nunca cotejadas | [A12] | OP2 |
| Lista de una agencia → deduplicación entre agencias | ID o hash, organización, monto | Building Blocks, HotPot, Excel del clúster | Gestión de información + CWG | Carga a un registro central o Excel | Acuerdo de datos de 3 meses o más; Somalia: más del 65 % no deduplica | [D02, D07] | OP1 |
| Derivación entre organizaciones | Datos personales y necesidades, a veces sensibles | Correo → sistema receptor | Gestores de casos | Archivo por correo y doble tecleo | Riesgo de protección de datos | [D01] | Requisito de datos |
| Instrucción al FSP | Nombre, ID, teléfono o cuenta, monto | SCOPE/CashAssist/HOPE/Excel → portal o API del FSP | Finanzas / programa | Excel/CSV por correo o portal; API solo en grandes | 5 de 7 operaciones manuales; Haití: archivos procesados fuera de SCOPE; Chad: "no secured mechanism" | [A01, A11, A08] | OP3 |
| Canje en comercio | Transacción, tarjeta, voucher | Sistema del FSP o tarjeta | FSP / comercio | Sistema cerrado | Doble voucher (Chad); personas atendidas ≠ tarjetas activadas (Mozambique) | [A08, A13] | OP3 / OP11 |
| Conciliación | Pagos acreditados y fallidos, comisiones, facturas | Informe del FSP → ERP / Excel | Finanzas | Manual o en papel | 71 M USD; Haití "months late"; factura del FSP ≠ informes | [A02, A11, A12] | OP3 |
| MEAL / PDM | Muestra tomada de la lista, encuestas | Kobo → Excel / Power BI | MEAL | Muestreo manual | Envíos de PDM no anunciados; sin acceso a datos brutos (CAMEALEON) | [D09, D16] | OP6 |
| Quejas → corrección | Caso, persona, pago | Línea → CRM → sistema de beneficiarios | AAP / programa | Manual o inexistente | Formulario que no llega al CRM; sin trazabilidad | [A07, A14] | OP7 |
| Reporte a donantes y clústeres (4W/5W) | Agregados por lugar y actividad | Excel / ActivityInfo | Gestión de información | Plantilla mensual | Sudán 2026: tablero "confidential" y "no consolidated overview" | [D08] | OP5 |

---
## 8. Matrices comparativas

*Las valoraciones resumen la sección L de cada ficha, donde están la evidencia y la fuente de cada una. La columna de confianza da la confianza global de la fila. Leyenda de confianza: a = alta, m = media, b = baja.*

### 8.1 Matriz de criterios

| Oportunidad | Intensidad | Frecuencia | Demanda | No resuelto | Pago | Competencia (ocupación) | Diferenciación | Tendencia | Barreras | Confianza |
|---|---|---|---|---|---|---|---|---|---|---|
| OP1 Deduplicación entre organizaciones | ALTA | MEDIA | BAJA | MEDIA | BAJA | ALTA | BAJA | Crece la necesidad; decrece el espacio para terceros | ALTAS | m |
| OP2 Integridad de lista e identificador | ALTA | ALTA (ONU) / DESC. | MEDIA-BAJA | ALTA | MEDIA (INGO) | MEDIA | MEDIA | CRECE | MEDIAS-ALTAS | m-b |
| OP3 Ciclo de pago y conciliación | ALTA | ALTA | MEDIA | ALTA (ONU) / DESC. | MEDIA | MEDIA | MEDIA | CRECE (necesidad) / INCIERTA (mercado) | ALTAS | m |
| OP4 Contratación de FSP | MEDIA | MEDIA | BAJA (gestión) | MEDIA | BAJA | ALTA | BAJA | ESTABLE | ALTAS | m-b |
| OP5 Reporting a donantes | MEDIA | ALTA | BAJA | MEDIA | BAJA-MEDIA | ALTA | BAJA | INCIERTA | MEDIAS | b |
| OP6 Monitoreo y verificación | MEDIA | ALTA | ALTA (servicio) | MEDIA | ALTA (servicio) | ALTA | BAJA | INCIERTA | ALTAS | m |
| OP7 Quejas → corrección | ALTA | ALTA | MEDIA | ALTA | MEDIA-BAJA | ALTA en canales / BAJA en el vínculo | MEDIA | INCIERTA | MEDIAS-ALTAS | m-b |
| OP8 Anomalías y colusión | MEDIA-ALTA | MEDIA | BAJA | MEDIA | BAJA-DESC. | BAJA (fuera del screening) | MEDIA | CRECE (exigencia) | ALTAS | b |
| OP9 Liquidez y conectividad | ALTA | ALTA (conflicto) | MEDIA (FSP) | ALTA | MEDIA (comisión) | ALTA | BAJA | CRECE | MUY ALTAS | m-a |
| OP10 Carga en cascada sobre actores locales | ALTA | ALTA | BAJA-MEDIA | ALTA | BAJA | MEDIA | BAJA | INCIERTA | ALTAS | m |
| OP11 Comercios | MEDIA | DESC. | BAJA | DESC. | BAJA | ALTA | BAJA | DECRECE | MEDIAS | b |
| OP12 Protección social | MEDIA | MEDIA | BAJA (lado humanitario) | MEDIA | BAJA (ONG) / ALTA (gobierno) | ALTA | BAJA | CRECE | MUY ALTAS | m |

### 8.2 Matriz actor–comprador

| Oportunidad | Actor con el problema | Comprador potencial | Alternativa actual | Evidencia de compra | Gap principal |
|---|---|---|---|---|---|
| OP1 | Gestión de información, coordinadores de cash, hogares | CWG o consorcio; la ONU, que construye | Building Blocks, HotPot, Excel del clúster | Ninguna externa; solo desarrollo interno [D11] | Gobernanza y adjudicación |
| OP2 | Programa, gestión de información, finanzas | Sede de INGO (dentro de una plataforma) | Excel, Kobo, sistemas corporativos | Licitaciones de plataforma [T06, T01] | Identificador persistente y control de cambios de la lista |
| OP3 | Finanzas y Cash de país | Procurement de INGO (con el FSP o una plataforma) | Portal del FSP, Excel, ERP, plataformas | Contratos FSP + tecnología [T02, T03, T11]; plataformas [T06, T07] | Conciliación persona a persona entre varios FSP y el ERP |
| OP4 | Cash, Procurement, Finanzas | — (el FSP es lo que se compra) | Acuerdos marco | Solo compra del FSP [T14] | Evaluación del desempeño del FSP |
| OP5 | MEAL y grants | ONG (licencia genérica) | 8+3, ActivityInfo, Excel | Ninguna específica | Armonización financiera y de indicadores (la controla el donante) |
| OP6 | Oficina de país, MEAL | Donante y ONU | Firmas de TPM, Kobo | TPM de £10 M [T16] | Seguimiento hasta el cierre de lo encontrado |
| OP7 | Personas receptoras, AAP, programa | Agencia o líder de una línea interagencia; CERF | Líneas de ayuda, CRM genérico, RapidPro | RFP de ACNUR [T15]; partida CERF [R13] | Vincular la queja con la corrección del dato o del pago |
| OP8 | Finanzas y cumplimiento | Compliance de la sede | Screening, TPM, líneas de denuncia | Solo screening [X08] | Análisis de datos de transacción |
| OP9 | ONG y hogares en conflicto | Procurement de FSP | Hawala, Bankak, FSP | Last Mile Technology [L03] | Liquidez y regulación (fuera del alcance de un producto) |
| OP10 | ONG locales | Intermediario o donante | Herramientas impuestas, Kobo | Fortalecimiento de capacidades [L11] | Armonización de requisitos (política) |
| OP11 | Comercios y personas | El PMA, que lo hace con medios propios | LMMS, RedRose, papel | Ninguna externa | Desconocido |
| OP12 | Hogares, CWG, ministerio | Gobierno (con banca de desarrollo) | OpenSPP, integradores | Licitación en Irak [T23] | La interfaz ONG ↔ gobierno |

### 8.3 Matriz de suficiencia de evidencia

| Oportunidad | ¿Evidencia secundaria suficiente? | Qué falta saber | Actor a entrevistar | Prioridad de research primario |
|---|---|---|---|---|
| OP3 | Sí para la ONU; no para INGO | Si INGO medianas y ONG concilian a mano, cuánto tiempo les lleva, si el portal o dashboard del FSP les basta y si pagarían fuera del contrato del FSP | Responsable de Finanzas de país o *Cash/CVA Finance Officer* de una INGO mediana con 2 o más FSP | **ALTA** |
| OP7 | Sí para la ONU; no para INGO | Si el cuello de botella es la herramienta o la práctica; quién paga; cómo se vincula hoy la queja con la corrección | *AAP/CFM Officer* o *Cash Officer* que gestiona quejas de pago | **ALTA** |
| OP2 | Parcial | Si es un problema propio o parte de OP3; frecuencia fuera de la ONU | Oficial de gestión de información o MEAL que prepara listas de pago en un consorcio | **ALTA** (podría fusionarse con OP3) |
| OP10 | Sí sobre el problema; no sobre el comprador | Si los intermediarios pagarían por reducir la carga que trasladan | Director de programas de una ONG nacional; gestor de alianzas de una INGO | MEDIA |
| OP5 | Antigua (2016) | Carga actual en horas; si la 8+3 basta | Grants o MEAL de una INGO con 3 o más donantes | MEDIA-BAJA |
| OP8 | Parcial | Si alguien pagaría por detectar anomalías fuera del screening | Compliance de una INGO | BAJA (revisar dentro de OP3) |
| OP1 | Suficiente para desaconsejar por ahora | — | — | BAJA |
| OP4, OP6, OP9, OP11, OP12 | Suficiente para aplazar o descartar | Ver la sección 10 | — | BAJA |

---

## 9. Shortlist provisional para investigación primaria

**Ninguna de estas oportunidades está validada.** Son las que, con la evidencia secundaria disponible, justifican primero el esfuerzo de hablar con usuarios reales.

### S1 — OP3. Ciclo de pago con el FSP y conciliación

**Por qué entra**
- **Problema:** es el más cuantificado del research. Hay 71 M USD de descuadre, pagos marcados como exitosos con importe cero, conciliaciones aprobadas 3–6 meses tarde y 3,6 M USD en tarjetas inactivas [A01, A02, A06]. Aparece en cada ciclo de pago.
- **Demanda:** varias INGO compran FSP con tecnología en el mismo contrato y otras licitan plataformas con conciliación [T02, T03, T06, T07, T11, T12].
- **Posibilidad económica:** hay un comprador plausible, el procurement de INGO, pagando con coste de proyecto o dentro del contrato del FSP.
- **Gap competitivo:** la conciliación persona a persona entre varios FSP y el ERP no aparece como oferta explícita (inferencia). Los fallos persisten incluso con sistemas corporativos [A01, A07].
- **Tendencia:** hay más FSP y rieles por país [M07] y la presión de auditoría tiene plazos en 2026 [A01, A09].

**Qué la refutaría**
- Que INGO medianas y ONG locales digan que el portal o el dashboard del FSP les basta, o que conciliar no está entre sus 3 problemas principales.
- Que trabajen con un solo FSP por país, lo que reduce la complejidad.
- Que la conciliación siempre se exija y se pague **dentro** del contrato del FSP y nunca por separado.
- Que el tiempo de conciliación por ciclo sea bajo (horas, no días).

**Principal incertidumbre:** si el problema que muestran las auditorías de la ONU existe con la misma intensidad fuera de la ONU, y si alguien pagaría por resolverlo fuera del FSP.

**Primer actor a entrevistar:** responsable de Finanzas de país o *Cash/CVA Finance Officer* de una **INGO mediana que trabaje con dos o más FSP en el mismo país**. Como segundo perfil, el responsable de procurement global que redactó una licitación de FSP + tecnología.

### S2 — OP7. Quejas y feedback vinculados a la corrección de datos y pagos

**Por qué entra**
- **Problema:** cinco auditorías recientes del PMA repiten el mismo patrón: no se puede seguir una queja hasta su cierre ni medir el tiempo de cierre, hay duplicados y los sistemas no se comunican [A06, A07, A14, A15, A16]. La CHS señala las quejas como el compromiso más débil del sector [R11, R12].
- **Demanda:** el RFP de ACNUR para una línea interagencia con software [T15], la partida AAP del CERF de 3–4 M USD [R13] y vacantes específicas [R14].
- **Posibilidad económica:** hay financiación específica (CERF) y presupuesto de proyecto. El software genérico es barato o donado, así que la disposición a pagar dependería de que el gap sea distinto de un CRM.
- **Gap competitivo:** vincular la queja con el registro de la persona y con la corrección del pago no aparece como oferta (inferencia). Abundan los canales y los CRM genéricos.
- **Tendencia:** incierta. Crece la presión normativa, pero los recortes ponen en riesgo las líneas de atención [A07].

**Qué la refutaría**
- Que los equipos atribuyan el fallo a la práctica, al personal o a la desconfianza de la población y no a sistemas que no se comunican [R11, R10].
- Que un CRM genérico bien configurado resuelva el vínculo.
- Que las quejas sobre pagos sean una fracción menor del total. En Haití, el 61 % eran peticiones o problemas técnicos [A15].
- Que nadie tenga presupuesto fuera de la central de llamadas.

**Principal incertidumbre:** si el problema es la herramienta o la práctica, y quién pagaría.

**Primer actor a entrevistar:** *AAP/CFM Officer* o *Cash Officer* que recibe y resuelve quejas de pago en una INGO o en un consorcio. En América Latina hay un punto de partida: la auditoría del PMA en Ecuador documenta este patrón [A16].

### S3 — OP2. Integridad de la lista y del identificador

**Por qué entra**
- **Problema:** OIOS señala la calidad del identificador como causa raíz de los fallos de pago: 223.985 registros sin ID único y 14,5 M USD pagados a identificadores inválidos [A01, A04]. Además, hay cambios no controlados después de la lista final [D09].
- **Demanda:** licitaciones de "one single solution" de gestión de datos y distribución [T06] y compromisos internos con plazo [A09].
- **Posibilidad económica:** media en INGO, dentro de una plataforma.
- **Gap:** el control de versiones y cambios de la lista y el identificador persistente no aparecen como oferta explícita (inferencia).
- **Tendencia:** crece como prioridad de control.

**Qué la refutaría**
- Que en entrevistas resulte indistinguible de OP3. En ese caso se fusiona con S1.
- Que las plataformas integradas (RedRose, 121) ya lo resuelvan para sus usuarios.
- Que la causa sea de disciplina de proceso y no de sistema.

**Principal incertidumbre:** si es un problema separado o la causa raíz de OP3.

**Primer actor a entrevistar:** oficial de gestión de información o MEAL que prepara y entrega listas de pago en un **consorcio con varios socios**. Contraste: un socio ejecutor que recibe la lista.

**Nota sobre la shortlist.** S1 y S3 están muy relacionadas, porque cubren el mismo tramo del ciclo. Conviene investigarlas con el mismo guion de entrevistas y decidir después si se fusionan. Si se fusionan, la tercera plaza la ocupa OP10 (carga en cascada sobre actores locales), cuyo problema está bien documentado pero cuyo comprador sigue sin aclararse.

## 10. Oportunidades que no se priorizan por ahora

| Oportunidad | Decisión | Por qué | Evidencia en contra | ¿Saturada? | ¿Hay comprador claro? | ¿Problema cubierto? | ¿Falta evidencia? |
|---|---|---|---|---|---|---|---|
| OP1 Deduplicación entre organizaciones | **Aplazada** | Problema intenso, pero el gap es de gobernanza y hay herramientas gratuitas de la ONU que se están consolidando (UN80) | [D03, D05, D08, D12, M28] | Sí, en herramientas | No: la ONU construye; las ONG usan herramientas gratis | En parte (Ucrania) | No |
| OP4 Contratación y desempeño de FSP | **Descartada** | Lo que se compra es el servicio del FSP, no su gestión | [T14, F01] | Sí (FSP, acuerdos marco) | No | En parte | No |
| OP5 Reporting a donantes | **Aplazada** | Herramientas genéricas baratas; el gap lo controla el donante; la evidencia de carga es de 2016 | [R01, R02, R04] | Sí | No | En parte (8+3) | Sí (carga actual) |
| OP6 Monitoreo y verificación | **Descartada como producto** | La demanda real es de servicio de campo (TPM), con presencia en zonas inseguras | [T16, T18, T19] | Sí (consultoras) | Sí, para servicios | En parte | No |
| OP8 Anomalías y colusión | **Aplazada; revisar dentro de OP3** | Sin demanda observable fuera del screening; tasas de pérdida bajas en promedio | [X01, X02, X04, X08] | Screening, sí | No | En parte | Sí |
| OP9 Liquidez y conectividad | **Descartada como producto** | El cuello de botella es la liquidez, la regulación y el de-risking; entrar exige licencia financiera | [L01, L07, L26] | Sí (agentes, FSP) | Solo para FSP | No, pero por causas fuera de alcance | No |
| OP10 Carga en cascada sobre actores locales | **Reserva** | Problema real y documentado; comprador poco claro; el gap es de acuerdos | [L10, L11, M01] | Media | No (pagaría el intermediario, sin evidencia) | No | Sí (comprador) |
| OP11 Comercios | **Aplazada** | Poca evidencia; tendencia a la baja; el PMA lo resuelve con medios propios | [L16, M04, L23] | Sí en el segmento grande | No | Desconocido | Sí |
| OP12 Protección social | **Descartada** (fuera del perfil B2B) | El comprador es el gobierno, con bienes públicos digitales gratuitos e integradores | [T23, L24, L22] | Sí | Sí, pero B2G | En parte | No |
| Interoperabilidad | **Eliminada como oportunidad** | Es causa y capacidad, no problema vivido | [D01, D03, D08] | — | — | — | — |
| Trazabilidad global de volúmenes de CVA (O4c) | **Eliminada** | Es un bien público sin comprador individual | [R05, R06] | — | No | No | No |
| Protección y gobernanza de datos (O11) | **Reclasificada como requisito** | La oferta es gratuita o subsidiada; es una condición de entrada | [X11, X12, X13, M17] | Sí (guías) | No | Bien resuelta en normas, poco en práctica | No |
| Screening de sanciones | **Reclasificado como requisito** | Mercado de cumplimiento saturado | [X08, X05] | Sí | Sí, pero saturado | Sí | No |

---
## 11. Contradicciones y propuestas de cambio a artefactos validados

### 11.1 Contradicciones abiertas

| Tema | Fuente A | Fuente B | Explicación posible | Qué se puede concluir |
|---|---|---|---|---|
| Volumen de CVA en 2024 | 6,6 mil M USD (CALP/ALNAP, jun-2025) [M04] | 8,2 mil M USD (GHA 2026, serie revisada) [M01] | Series revisadas, fuentes y métodos distintos | La tendencia es a la baja; la cifra exacta no es fiable |
| Caída del CVA en 2025 | ~−60 % (CALP, ene-2026) y −31 % (CALP, jun-2025) [M05, M04] | −11 % (GHA 2026) [M01] | Las de CALP son estimaciones tempranas o proyecciones con una submuestra; la del GHA es un dato posterior | Hay caída; su magnitud está entre −11 % y −60 % |
| Cuota del CVA en la ayuda humanitaria | 19,6 % en 2024 (CALP) | "23 %" (caucus del Grand Bargain, 2025) [R04] | Bases distintas | No es comparable |
| Ahorro por deduplicación en Ucrania | 207 M USD a fines de 2024 (CWG) [D05] | 270 M USD "through 2025" (Building Blocks) [M28]; 230 M USD (carta de profesionales) [F10] | Periodos y alcances distintos | Ahorros de cientos de millones; la cifra exacta depende del periodo |
| ¿Las INGO grandes ya están integradas? | market-beliefs.md: "las organizaciones grandes ya tienen un MIS integrado internamente" | Auditorías de 2023–2026: fallos de integración dentro de ACNUR y el PMA [A01, A02, A07] | Tener una plataforma corporativa no implica que sus traspasos estén integrados | Los fallos de integración también ocurren dentro de las organizaciones grandes |
| Incidente del PMA en Gaza | "People Portal" (borrador 1, según The New Humanitarian) | "Self-Registration Application" (Access Now) [X09] | Posible diferencia de nombre del mismo sistema | Verificar; la magnitud (≥600.000 hogares) coincide en ambas |
| Fecha del estudio CALP/Key Aid | dic-2025 (borrador 1) | Publicado el 3-mar-2026 [X01] | Fecha de cierre frente a fecha de publicación | Citar el 3-mar-2026 |

### 11.2 Propuesta de cambio a `product/research/market-beliefs.md` (WORKFLOW §3.1)

**Solo se registra. No se aplica.** Requiere validación explícita.

| Campo | Contenido |
|---|---|
| Artefacto | `product/research/market-beliefs.md` (VALIDADO v1, 2026-10-06) |
| Qué cambia | **(1)** Resumen, punto 2, y C3 "Hechos encontrados". *Antes:* "El volumen mundial de CVA cayó en 2024 y se proyectan caídas de entre el 31 % y el 60 % en 2025". *Después:* añadir a continuación: "La serie revisada de Development Initiatives (GHA 2026) da 8,2 mil M USD en 2024 y 7,3 mil M USD en 2025 (−11 %). Las cifras de CALP y del GHA no son comparables entre sí." **(2)** C1, "Evidencia que la contradice o matiza", primer punto. *Antes:* "Las organizaciones grandes ya tienen un sistema integrado internamente (1.01)". *Después:* añadir el matiz: "Auditorías de 2023–2026 muestran que, aun con plataforma corporativa, persisten traspasos manuales y descuadres dentro de ACNUR y el PMA (ver cva-market-opportunities.md)." |
| Por qué cambia | Hay evidencia posterior que actualiza una cifra y matiza una afirmación. No se modifica ningún veredicto. |
| Evidencia | [M01] GHA 2026; [A01] OIOS 2025/019; [A02] OIOS 2023/043; [A07] PMA AR/26/01 |
| Impacto | Ninguno sobre los estados de C1–C4. Sí debería tenerlo en cuenta `/review-evidence` si se revisa `overview.md`. |
| Alternativa | No tocar market-beliefs.md y dejar la actualización solo en este documento. Respeta el principio de no reescribir artefactos para que coincidan con conclusiones posteriores. |

## 12. Impacto en creencias, geografía y agenda de research primario

### 12.1 Impacto en las creencias de overview.md

*Solo vive en este archivo. No se anota overview.md.*

| Creencia | Veredicto de este research | Evidencia |
|---|---|---|
| C1. Sistemas no interoperables y trabajo manual | **Apoya (a) y (b)**, y desplaza el foco: el traspaso manual que más daño causa está en el tramo lista → FSP → conciliación → ERP, y también ocurre dentro de agencias grandes. La interoperabilidad es causa, no problema. Sobre (c), la disposición a cambiar, **no dice nada**. | [A01, A02, A07, D01] |
| C2. Discrepancias entre la ONG y los comercios | **Apoya parcialmente y desplaza:** las discrepancias cuantificadas son sobre todo con el FSP y el ERP, no con comercios. Los vouchers pierden peso. | [A01, A02, A06, M04] |
| C3. Financiación por donantes | **No la apoya.** La compra observada la hacen INGO como coste de proyecto o dentro del contrato del FSP. No se observa compra directa del donante, salvo TPM. | [T02, T03, T06, M17, T16] |
| C4. Conectividad limitada | **Coherente con market-beliefs.md:** el problema es real, pero su núcleo (liquidez, regulación) queda fuera del alcance de un producto. | [L01, L07, L26] |

### 12.2 Geografía

- **Visión global:** la evidencia más densa viene de África Oriental (Somalia, Sudán, Sudán del Sur, Kenia), Oriente Medio (Gaza, Siria, Yemen, Líbano), Ucrania y Afganistán.
- **América Latina, señales encontradas:**
  - consorcio VenEsperanza en Colombia, con tres FSP, comisiones distintas por socio y una plantilla común de incidencias [F06];
  - vacantes de IFRC con funciones de conciliación en Caracas y Colombia [F09];
  - auditoría del PMA en Ecuador sobre quejas y monitoreo [A16];
  - auditoría del PMA en Colombia (no leída) [A17];
  - pagos a importe cero en México [A01];
  - el acuerdo de Plan con FSP cubre las Américas [T03];
  - leyes de datos más exigibles en Ecuador y México [X14, X15];
  - poco peso de los vouchers [L23];
  - gobiernos con sistemas propios, como Brasil [L22];
  - RMRP 2026 financiado al 8,1 % y ACNUR Américas con −42 % de programas [M09, M10];
  - en 2021, 53 organizaciones daban CVA en 17 países [M11].
- **Lectura (inferencia):** las señales de América Latina se alinean más con OP3 y OP7 que con OP9 u OP11. Pero la región está muy desfinanciada. **No se selecciona país.**

### 12.3 Agenda de research primario

**Encuesta (`/design-survey`: cuántos, con qué frecuencia, cuánto):**
- **OP3:** número de FSP por país; frecuencia y tamaño de los descuadres; días de personal por ciclo de conciliación; quién concilia; si el FSP aporta informe o dashboard.
- **OP7:** volumen de quejas sobre pagos; tiempo medio de cierre; sistemas usados.
- **OP2:** porcentaje de registros sin identificador; cambios después de la lista final.
- **Todas:** herramientas usadas, quién las paga y presupuesto tras los recortes de 2025.

**Entrevistas (`/design-interview`: por qué, qué hacen hoy):**
- **OP3:** cómo se concilia paso a paso; qué pasa con una excepción; qué cubre el FSP y qué no; quién decide la compra y cómo se paga.
- **OP7:** recorrido de una queja de pago desde que entra hasta que se corrige; dónde se pierde.
- **OP2:** quién toca la lista entre la versión final y el pago, y por qué.
- **Transversal:** si INGO medianas y ONG locales reconocen los problemas que muestran las auditorías de la ONU.

**Fuentes documentales pendientes:**
- licitación de Relief International IPU2026002;
- auditorías del PMA en Colombia (AR-26-05) y Somalia (AR-26-04);
- Anexo 5 del modelo de acuerdo de ECHO;
- reglas de PRM, GFFO y SIDA;
- informes de Ground Truth Solutions de 2024–2026;
- CALP SOWC 2026 (12-nov-2026).

---
## 13. Fuentes

Todas las fuentes se consultaron entre el 2026-10-06 y el 2026-10-07.

**Tipos:** I = institucional; A = auditoría o evaluación oficial; P = prensa; T = think tank o académica; C = **COMERCIAL** (lo que el proveedor dice de sí mismo); L = licitación o procurement; V = vacante.

**Oportunidad:** la oportunidad (OP) o sección a la que se refiere principalmente.

### A. Auditorías y supervisión

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | OP | Limitación |
|---|---|---|---|---|---|---|---|---|
| A01 | 5 de 7 operaciones transfieren a mano los datos al FSP; pagos marcados como exitosos con importe cero; 223.985 registros sin ID; 14,5 M USD a ID inválidos; 232 M USD fuera de CashAssist | OIOS / ACNUR | Informe 2025/019 CashAssist | 2025-06-27 | https://oios.un.org/system/files/confidential-files/Reports/2025_019_pd.pdf | A | OP2, OP3 | Solo ACNUR; leído a través de un resumen automático |
| A02 | 71 M USD sin conciliar entre CashAssist y MSRP; 3,6 M USD en tarjetas inactivas; comisión sobre efectivo no cobrado; pago duplicado de 1,5 M USD; contratos retroactivos | OIOS / ACNUR | 2023/043 Ucrania CBI | 2023-09-21 | https://oios.un.org/file/9971/download?token=USFilfBC | A | OP3, OP4 | Emergencia excepcional |
| A03 | Duplicados entre agencias por 2,2 M USD | OIOS / ACNUR | 2023/044 Deduplicación Ucrania | 2023-09-21 | https://oios.un.org/system/files/confidential-files/Reports/2023_044_pd.pdf | A | OP1 | — |
| A04 | Socios sin conciliación por falta de ID únicos | OIOS / ACNUR | 2025/027 Afganistán | 2025 | https://oios.un.org/system/files/confidential-files/Reports/2025_027_pd.pdf | A | OP2, OP3 | Fecha exacta no extraída |
| A05 | No se preparaban conciliaciones; Ruanda contrató sin due diligence | OIOS / ACNUR | 2020/057 CBI África | 2020-12-17 | https://oios.un.org/en/node/1363 | A | OP3, OP4 | Antigua |
| A06 | Conciliación aprobada a los 3–6 meses; 22 % de descuadre; más de 100 hojas Excel; 11 % de monitoreo; 85 % de las quejas llega por mesas de socios | PMA, Inspector General | AR/24/25 Sudán del Sur | 2024-12 | https://docs.wfp.org/api/documents/WFP-0000164133/download | A | OP3, OP6, OP7 | — |
| A07 | Tablero de conciliación roto; transacciones sin analizar; IVR caído; quejas que no llegan del formulario al CRM | PMA, Inspector General | AR/26/01 Chad | 2026-04 | https://docs.wfp.org/api/documents/WFP-0000173848/download/ | A | OP3, OP7, OP8 | — |
| A08 | Sin conciliación por beneficiario; dependencia de un FSP; intercambio de datos no seguro; doble voucher | PMA, Inspector General | AR/23/09 Chad | 2023-08 | https://docs.wfp.org/api/documents/WFP-0000152386/download | A | OP2, OP3 | — |
| A09 | Compromiso de automatizar la conciliación (plazo 2026) | PMA | AR/25/18 Zambia | 2025-12 | https://docs.wfp.org/api/documents/WFP-0000171359/download | A | OP2, OP3 | Compromiso, no ejecución |
| A10 | Seleccionar un FSP puede tardar un año; aprobaciones de hasta 678 días; sin análisis corporativo de fraude; 2,7 mil M USD vía FSP | PMA, Inspector General | AR/25/03 Gestión de FSP | 2025-02 | https://docs.wfp.org/api/documents/WFP-0000165178/download | A | OP3, OP4, OP8 | — |
| A11 | Conciliación en papel "months late"; SCOPE "not successful" | PMA, Inspector General | AR/22/12 Haití | 2022-08 | https://docs.wfp.org/api/documents/WFP-0000142543/download | A | OP2, OP3 | — |
| A12 | "multiple and rolling spreadsheets"; factura del FSP ≠ informes | PMA, Inspector General | AR/23/05 RDC | 2023-05 | https://docs.wfp.org/api/documents/WFP-0000150069/download | A | OP2, OP3 | Mayoritariamente ayuda en especie |
| A13 | 80 % del registro manual; posibles errores de inclusión del 30–50 % | PMA, Inspector General | Auditoría Mozambique | 2022-02 | https://docs.wfp.org/api/documents/WFP-0000137461/download | A | OP2 | — |
| A14 | Linha Verde: 340.000 consultas; quejas sin trazabilidad ni medición del tiempo de cierre | PMA, Inspector General | AR/25/02 Mozambique | 2025-02 | https://docs.wfp.org/api/documents/WFP-0000165081/download | A | OP7 | — |
| A15 | Unos 24.000 mensajes; casos de monitoreo abiertos; menos de 10 casos de PSEA | PMA, Inspector General | AR/25/17 Haití | 2025-12 | https://docs.wfp.org/api/documents/WFP-0000171322/download | A | OP6, OP7 | Lectura parcial |
| A16 | Más de 11.800 casos en SugarCRM; monitoreo mínimo no cumplido | PMA, Inspector General | AR/25/16 Ecuador | 2026-01 | https://docs.wfp.org/api/documents/WFP-0000171277/download/ | A | OP6, OP7 | — |
| A17 | Colombia: 94 M USD, 645.000 personas, "some improvement needed" | PMA, Inspector General | AR-26-05 Colombia | 2026-07 | https://www.wfp.org/audit-reports/internal-audit-wfp-operations-colombia-june-2026 | A | OP3, OP7 | **PDF no leído** |
| A18 | Unas 100.000 transacciones por ciclo gestionadas en hojas de cálculo | PMA, Inspector General | AR/22/19 Palestina | 2022-12 | https://docs.wfp.org/api/documents/WFP-0000145990/download/ | A | OP3 | — |
| A19 | 2.010 alegaciones; 1,90 M USD; presupuesto de la OIG de 18,83 M USD (−8,6 %) | PMA, Inspector General | Informe anual 2025 | 2026 | https://executiveboard.wfp.org/document_download/WFP-0000173291 | A | OP8 | Sin desglose por CVA |
| A20 | 2.011 quejas, el 18 % por fraude | ACNUR, Oficina del Inspector General | A/AC.96/76 | 2025-08 | https://www.unhcr.org/sites/default/files/2025-08/a-ac-96-76-8-76-excom-english.pdf | A | OP8 | Sin datos de CBI |
| A21 | 66 días de retraso medio en reportar incidentes | USAID OIG | E-000-25-002-M Etiopía | 2025-02-26 | https://oig.usaid.gov/sites/default/files/2025-02/E-000-25-002-M%20Evaluation%20of%20USAID%20Oversight%20of%20Emergency%20Food%20Assistance%20in%20Ethiopia.pdf | A | OP8 | Ayuda en especie |
| A22 | 1,14 M de receptores sin vetting en Gaza | USAID OIG | 8-294-26-003-P | 2026-05-14 | https://oig.usaid.gov/sites/default/files/2026-05/Final%20Audit%20Report%20-%20West%20Bank%20and%20Gaza%20Partner%20Vetting%20Audit%20%288-294-26-003-P%29.pdf | A | OP8 | Postura de EE. UU. |
| A23 | Al menos 10,9 M USD pagados en tasas a los talibanes | SIGAR | SIGAR-25-29-LL | 2025-08 | https://www.sigar.mil/Portals/147/Files/Reports/lessons-learned/SIGAR-25-29-LL.pdf | A | OP8 | Testimonios |
| A24 | Comisiones fuera de contrato; PDM con documentación inadecuada | PMA, auditor externo | Informe del auditor externo | 2025-11 | https://executiveboard.wfp.org/ar/document_download/WFP-0000169151 | A | OP3, OP6 | — |

### D. Datos, registro e interoperabilidad

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | OP | Limitación |
|---|---|---|---|---|---|---|---|---|
| D01 | La hoja de cálculo por correo es lo más común; lo no técnico es más difícil que lo técnico; dependencia del proveedor | IFRC / DIGID | Investigating Safe Data Sharing… | 2023-11 | https://interoperability.ifrc.org/wp-content/uploads/2023/11/DIGIDInteroperability-InvestigatingSafeDataSharingandSystemsInteroperability.pdf | T | OP1, sección 7 | 28 entrevistas |
| D02 | ~5 % de duplicados; acuerdos de datos de 3 meses o más; 1–2 días-persona al mes | IFRC / DIGID | Use case 1: Deduplication | 2023 | https://interoperability.ifrc.org/wp-content/uploads/2023/11/DIGIDInteroperability-Deduplicationofpeoplefamiliesorhouseholds.pdf | T | OP1 | Cifras de fuentes variadas |
| D03 | Sin estándar; 10–20 tipos de ID en Somalia; las reglas importan tanto como los estándares | DIGID / CCD | Deduplication briefing note | 2024-08 | https://interoperability.ifrc.org/wp-content/uploads/2024/10/Deduplication_briefing-note.pdf | T | OP1 | Cualitativa |
| D04 | Financiadores de DIGID; pilotos con 388 hogares | DIGID | Summary Report | 2023 | https://interoperability.ifrc.org/wp-content/uploads/2023/11/DIGID-Summary-Report-Final.pdf | T | OP1 | Pilotos pequeños |
| D05 | 63 socios; 207 M USD evitados; varias plataformas | Ukraine CWG / OCHA | Data Management Assessment | 2025-07 | https://reliefweb.int/report/ukraine/ukraine-cwg-data-management-systems-and-governance-assessment-report-july-2025 | I | OP1 | Un solo contexto |
| D06 | PING automatiza un intercambio que antes era manual | ACNUR / PMA | Collaboration gone right (Tanzania) | 2024-09-16 | https://www.unhcr.org/blogs/collaboration-gone-right-unhcr-and-wfp-take-data-sharing-to-the-next-level-in-tanzania-refugee-camps/ | I | OP1 | Blog institucional |
| D07 | Más del 65 % no deduplica; el 35 % sin política de datos; FRS hasta 2028 | Somalia CWG (alojado por Concern) | Somalia IO Final Report | ~2025-10 | https://admin.concern.net/sites/default/files/documents/2026-07/SOM-IO_Final-281025.pdf | I | OP1 | Muestras pequeñas |
| D08 | "Household-level interoperability systems are not necessary"; tablero confidencial | CALP | Workshop Summary, Sudán | 2026-07 | https://www.calpnetwork.org/wp-content/uploads/2026/07/Workshop-Summary_Cash-Landscape-Review_Sudan.pdf | I | OP1, OP5 | Resumen |
| D09 | Datos personales modificados tras la lista final (CCY Yemen) | ActivityInfo / CCY | Information systems for CBI | 2023-10 | https://www.activityinfo.org/about/assets/pdf/2023-10-11-information-systems-for-cash-based-interventions-drc.pdf | C | OP2 | Caso publicado por el proveedor |
| D10 | Bangladesh: 27 % de solapamiento sobre 88.432 documentos | Food Security Sector | Concept note de deduplicación | 2020 | https://fscluster.org/sites/default/files/documents/fsl_deduplication_exercise_concept_note_v.1_as_of_22_september_1.pdf | I | OP1 | Antigua |
| D11 | EDS: 431.000 USD evitados en Malí; de semanas a horas | PMA | Every meal counts | 2026-05-19 | https://www.wfp.org/stories/every-meal-counts-how-wfp-using-ai-reach-more-people-faster | I | OP1 | Autoinforme |
| D12 | Identidad común y deduplicación entre agencias (UN80) | UNICEF, Junta Ejecutiva | Nota informativa UN80 | 2026-08-12 | https://www.unicef.org/executiveboard/media/40576/file/2026-SRS-UN80-Information-note-EN-2026-08-12.pdf | I | OP1 | — |
| D13 | Sin base central y con restricciones legales (Türkiye) | ReliefWeb / TRC | Fact sheet cross-checking CVA | 2023-07 | https://reliefweb.int/report/turkiye/fact-sheet-situation-cross-checking-and-deduplication-cvas-turkiye-july-2023 | I | OP1 | Extracto |
| D14 | Colombia: códigos únicos compartidos entre 7 organizaciones | CaLP | Informe Venezuela (ESP) | 2020 | https://calpnetwork.org/wp-content/uploads/2020/09/CaLP-Ven-main-report_ESP-FINAL.pdf | T | OP1 | Antigua |
| D15 | Rohingya: 830.000 nombres compartidos; 23 de 24 entrevistados sin saberlo | HRW | UN shared Rohingya data… | 2021-06-15 | https://www.hrw.org/news/2021/06/15/un-shared-rohingya-data-without-informed-consent | T | OP1, requisito de datos | Muestra de 24 |
| D16 | CAMEALEON: acuerdos de datos firmados antes de saber qué datos existían | Evaluación independiente | CAMEALEON | 2022-09 | https://library.alnap.org/system/files/content/resource/files/main/CAMEALEON_Independent%20evaluation_September%202022.pdf | A | OP6 | — |
| D17 | Validación técnica en Uganda y Sudán del Sur, financiada por ECHO | IFRC Cash Hub | Technical validation lessons | 2024 | https://cash-hub.org/resource/data-sharing-in-humanitarian-cva-technical-validation-exercise-lessons-learned/ | I | OP1 | Solo resumen |
| D18 | No hay sistema dominante; 2 % del gasto en IT; SCOPE costó 47,3 M USD | CALP | SOWC 2023, cap. 7 | 2023-11-15 | https://www.calpnetwork.org/web-read/the-state-of-the-worlds-cash-2023-chapter-7-data-and-digitalization/ | I | Contexto | — |
| D19 | Vacante de gestión de información con deduplicación semanal | Mercy Corps / CCS | Vacante | 2025 | https://untalent.org/jobs/cash-consortium-of-sudan-ccs-information-management-coordinator-consultancy | V | OP1 | Cerrada |
| D20 | Subreporte del efectivo multipropósito en la matriz 4W (terremoto de Siria) | CALP | Rapid reflection, Syria earthquake | 2023-11 | https://www.calpnetwork.org/wp-content/uploads/2023/11/Rapid-reflection-on-the-scale-up-of-cash-coordination-for-the-syria-earthquake-response.pdf | I | OP5 | — |

### F. Pagos y FSP

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | OP | Limitación |
|---|---|---|---|---|---|---|---|---|
| F01 | Licitaciones de 3–4 y 5–6 meses; conciliación diaria en Sierra Leona | Cash Hub (Movimiento de la Cruz Roja) | Webinar "Working with FSPs" | 2021-05-19 | https://cash-hub.org/wp-content/uploads/sites/3/2021/06/20210519_WebinarSummaryTakeaways_v2.pdf | I | OP3, OP4 | Testimonios |
| F02 | La contratación lleva meses; los FSP piden 4–6 semanas para responder | ELAN / CaLP | Recommendations for e-transfer procurement | 2017 | https://www.calpnetwork.org/wp-content/uploads/2020/03/elan-recommendations-for-e-transfer-procurement-vfinal-1.pdf | I | OP4 | n pequeño |
| F03 | Contrato en 3 meses; SIM bloqueadas; 0,42 frente a 3,36 USD por transacción | GSMA | Humanitarian Payment Digitisation | 2017 | https://unhcr.org/innovation/wp-content/uploads/2018/11/Humanitarian-Payment-Digitisation.pdf | I | OP4 | Antigua |
| F04 | Contratación en 1–2 meses; formato de archivo de pago; liquidez de agentes | IRC | Improving large-scale mobile money disbursements | 2018-06-14 | https://rescue.org/sites/default/files/document/2853/improvinglargescalemobilemoneydisbursementsvf.pdf | I | OP3, OP4 | Pakistán |
| F05 | Reversión masiva de no cobrados a petición escrita | Cash Hub / PRCS | Cash Case Study Pakistan | 2020-02 | https://cash-hub.org/wp-content/uploads/sites/3/2020/10/CashCaseStudy_Pakistan_Final-26Feb.pdf | I | OP3 | Un caso |
| F06 | Colombia: comisiones de Efecty entre 0,9 % y 1,8 %; plantilla común de incidencias; KYC de migrantes | CaLP / VenEsperanza | Working with FSPs | 2023-10-23 | https://www.calpnetwork.org/wp-content/uploads/2023/10/VenEsperanza_Collaborating-with-FSPs_EN.pdf | I | OP3, OP4 | Un consorcio |
| F07 | Comisiones de proveedores de remesas: 3–4 %; tope ECHO del 5 %; 15–25 % en crisis | NRC | Use of MSPs | 2025 | https://www.nrc.no/globalassets/pdf/reports/humanitarian-organisations-use-of-money-service-providers/2025_nrc-use-of-msps-by-humanitarian-organisations.pdf | I | OP4, OP9 | Solo proveedores de remesas |
| F08 | Reparto de roles: Finanzas, Programas, Logística | IFRC | Secretariat CBP SOPs | 2015-08 | https://cash-hub.org/wp-content/uploads/sites/3/2020/08/IFRC-Secretariat-Cash-Based-Programming-Standard-Operating-Procedures.pdf | I | OP3 | Antigua |
| F09 | Funciones de conciliación en vacantes de CVA y Finanzas | IFRC | Vacantes en Caracas, Colombia y Jamaica | 2026 | https://www.impactpool.org/jobs/1231477 ; https://www.impactpool.org/jobs/1232905 ; https://www.impactpool.org/jobs/1204467 | V | OP3 | Una sola organización |
| F10 | Negociar comisiones a escala; 230 M USD ahorrados por deduplicación | Profesionales de cash (vía CALP) | Letter on the Humanitarian Reset | 2025-06 | https://www.calpnetwork.org/wp-content/uploads/2025/06/Letter-from-Cash-Practitioners-on-the-Humanitarian-Reset-June-2025.pdf | T | OP4 | Opinión |
| F11 | RFP a un FSP con conciliación semanal | PRCS | Scope of Work | 2026 | https://prcs.org.pk/documents/view/MjAyNnxBbm5leCAyIFNjb3BlX29mX1dvcmsucGRm | L | OP3, OP4 | — |
| F12 | 5 personas a tiempo completo dedicadas a conciliación manual (piloto de 2019) | Oxfam Australia | Debrief Project Unblocked Vanuatu | 2024-05 | https://oxfam.org.au/wp-content/uploads/2024/05/Debrief-Report-on-Project-Unblocked-Vanuatu.pdf | I | OP3 | Piloto antiguo |

### T. Licitaciones y compras

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | OP | Limitación |
|---|---|---|---|---|---|---|---|---|
| T01 | Plataforma digital de gestión de CVA | Relief International | ITT IPU2026002 | 2026-02 | https://www.ri.org//content/uploads/2026/02/ITT-IPU2026002-Cash-and-voucher-digital-assistance-management-platform.docx | L | OP2, OP3 | **No leído** |
| T02 | Acuerdo marco global con un proveedor de pago y tecnología | Prosper Global | G 011-2025 | 2025-10 | https://www.prosperglobal.org/tenders/intent-bid-global-master-agreement-digital-payment-and-technology-service-provider-cash-and | L | OP3 | Sin términos de referencia completos |
| T03 | Acuerdos de largo plazo con FSP globales, con dashboard; incluye las Américas | Plan International | ITT FY25-0205 | 2025-06 | https://plan-international.org/uploads/2025/06/ITT-FY25-0205-Invitation-to-Tender.pdf | L | OP3, OP5 | Sin monto |
| T04 | Convocatoria global de FSP; 51 M USD de CVA en 2023 | DRC | EOI (Mercell) | 2025-02 | https://www.mercell.com/en/tender/247017436/call-for-expressions-of-interest-partner-with-the-danish-refugee-council-to-deliver-global-cash-and-voucher-assistance-solutions-tender.aspx | L | OP3, OP4 | Publicado en un agregador |
| T05 | Hasta 11 M USD al año con FSP; incluye conciliación | DRC WANALA | EOI-RO03-2024-001 | 2024-05-31 | https://coordinationsud.org/wp-content/uploads/EOI-RO03-2024-001_Expression-of-Interest.pdf | L | OP3, OP4 | Países africanos |
| T06 | "Technology for Information Management and Delivery", "one single solution" | Diakonie Katastrophenhilfe | Tender | 2024-05 | https://openimis.atlassian.net/wiki/spaces/OP/pages/3808264202/TENDER+Technology+for+Information+Management+and+Delivery+Provider+CVA | L | OP2, OP3 | Copia en otro sitio |
| T07 | e-voucher con conciliación offline en una ONG local | SARD | PECS02-2024 | 2024-06 | https://ab-ilan.com/wp-content/uploads/2024/06/E-CARD-System-PECS02-2024.docx | L | OP3, OP10 | Sin monto |
| T08 | Precalificación de FSP en Gaza y Cisjordania | Save the Children | Vía CALP | 2026-06 | https://www.calpnetwork.org/?p=596822 | L | OP4 | — |
| T09 | Acuerdo de largo plazo de transferencias | UNICEF Sudán del Sur | UNGM 313523 | 2026-09 | https://www.ungm.org/Public/Notice/313523 | L | OP4 | — |
| T10 | Transferencias en efectivo y cupones | FAO Sudán | UNGM 310728 | 2026-08 | https://www.ungm.org/Public/Notice/310728 | L | OP4 | — |
| T11 | FSP más plataforma: registro, pago, conciliación, PDM, quejas | PUI | HQ/STC-01/CASH/2021 | 2021-06 | https://www.coordinationsud.org/wp-content/uploads/Participation-tender-file-HQ-STC-AO-001-cash-2021-FV-002-1.pdf | L | OP3 | Antigua |
| T12 | Plataforma digital integral para CVA | Solidarités International | CFT_PAR-SRV-CVA-001-26 | 2026-07-17 | https://www.solidarites.org/fr/appel-d-offres/call-for-tender-service-provider-for-cash-and-voucher-assistance-cva-programming/ | L | OP3 | Sin monto |
| T13 | Acuerdos marco de pago con gestión de datos opcional | CRS | RFP US8574 | 2024-07-01 | https://www.crs.org/sites/default/files/component_ii_-_scope_of_work_-_crs_rfp_us8574.07.2024.pdf | L | OP3 | Sin monto |
| T14 | Licitaciones de FSP de Plan, DRC, Save the Children y Solidarités | IAPG | Listado "Cash Transfer Solution" | 2025–2026 | https://iapg.org.uk/category/services-cash-transfer-solution/ | L | OP4 | Solo resúmenes |
| T15 | Línea interagencia con software de helpdesk | ACNUR Pakistán | RFP-3243 (UNGM 309770) | 2026-09 | https://www.ungm.org/Public/Notice/309770 | L | OP7 | Sin monto |
| T16 | TPM y PEAL en Siria por £10 M | FCDO / Cowater | Contracts Finder | 2024-02 | https://www.contractsfinder.service.gov.uk/Notice/1eb378a5-b1ae-42e9-b7d5-c16188f088a7 | L | OP6 | No es específico de cash |
| T17 | MEL en Somalia por £13,2 M (retirado) | FCDO | Contracts Finder | 2023–24 | https://www.contractsfinder.service.gov.uk/Notice/32d3efa4-a42d-483c-89ae-73b34c96ccd0 | L | OP6 | Retirado |
| T18 | TPM para el Somalia Joint Fund | PNUD | UNGM 247477 | 2024-09 | https://www.ungm.org/Public/Notice/247477 | L | OP6 | Sin monto |
| T19 | TPM en Yemen por 59.680 USD | UNOPS | UNGM 134561 | 2023-01 | https://www.ungm.org/Public/ContractAward/134561 | L | OP6 | Salud |
| T20 | Renovación prevista de Palantir pese a la dependencia del proveedor | Biometric Update | Artículo | 2026-08 | https://www.biometricupdate.com/202608/un-moves-to-renew-palantir-deal-despite-unresolved-privacy-governance-risks | P | Contexto | Basado en una auditoría filtrada |
| T21 | Plataforma digital del PMA: 20 M USD en 2 años | PMA | Nota conceptual | 2019 | https://executiveboard.wfp.org/document_download/WFP-0000100537 | I | Contexto | Antigua |
| T22 | Compras de la ONU: 25,7 mil M USD, sin desglose de IT | UNOPS | ASR 2024 | 2025 | https://content.unops.org/documents/libraries/executive-board/documents-for-sessions/2025/second-regular-session/item-12-financial-budgetary-and-administrative-matters/en/ASR-EN.pdf | I | Contexto | — |
| T23 | Licitación del sistema de información del programa de transferencias en Irak (donación P178824 del Banco Mundial) | Bidsfactory | Licitación | 2026-04-26 | https://bidsfactory.com/es/tenders/development-of-a-cash-transfer-program-ctp-mis-for-OP00440986 | L | OP12 | Publicado en un agregador |

### R. Reporting, monitoreo y quejas

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | OP | Limitación |
|---|---|---|---|---|---|---|---|---|
| R01 | Más de 11.000 h/año en NRC; 283.000 y 898.000 h-persona en el sector | NRC / BCG | Institutional donor requirements | 2016 | https://www.nrc.no/globalassets/office/whs/institutional-donor-requirements-report-on-sectoral-challenges-21.05.pdf | T | OP5 | Antigua |
| R02 | Plantilla 8+3: ahorro no concluyente; 9 de 11 donantes a favor | GPPi | Final Review | 2019-06 | https://gppi.net/media/Gaus_2019_Harmonizing_Reporting_Pilot_Final_Review.pdf | A | OP5 | Piloto |
| R03 | 15 firmantes; ECHO "considering" | IASC | Signatories using 8+3 | 2021-03 | https://interagencystandingcommittee.org/node/42787 | I | OP5 | Desactualizada |
| R04 | Compromiso 8+3 y armonización en 2026 | Caucus del Grand Bargain | Joint Statement | 2025-06 | https://coastbd.net/wp-content/uploads/2025/08/5.-Joint-Statement-Grand-Bargain-Caucus-on-Efficiency-Measures.pdf | I | OP5 | Copia alojada por terceros |
| R05 | FTS: datos de CVA en ~1/3 de la financiación; 4 publicadores en IATI | Development Initiatives | Tracking CVA | 2022-09 | https://ej.issuelab.org/resources/41062/41062.pdf | T | O4c | 2022 |
| R06 | Etiquetado de CVA "rarely done" | CALP | SOWC 2023, cap. 2 | 2023-11 | https://www.calpnetwork.org/web-read/the-state-of-the-worlds-cash-2023-chapter-2-cva-volume-and-growth/ | I | O4c | — |
| R07 | Indicadores de MPC: menú de más de 30, "still evolving" | Grand Bargain / CALP | MPC Outcome Indicators | 2022 | https://www.calpnetwork.org/wp-content/uploads/2022/05/CALP-MPC-Outcomes-Executive-Summary-EN.pdf | I | OP5, OP6 | — |
| R08 | 27 indicadores para MPCA | Save the Children | MPCA MEAL Toolkit | 2021 | https://fsnnetwork.org/sites/default/files/2022-11/MPCA-MEAL-Toolkit-Guidance-Note.pdf | I | OP5 | — |
| R09 | El 47 % sabe cómo quejarse | Ground Truth Solutions | Cash Barometer Somalia | 2022-02 | https://aap-inclusion-psea.alnap.org/system/files/content/resource/files/main/Cash_barometer_report_Somalia_022022.pdf | T | OP7 | Antigua |
| R10 | Los mecanismos de quejas "often avoided" | GTS / OCHA | Listening is not enough | 2022-11 | https://interagencystandingcommittee.org/ground-truth-solutions-2022-listening-not-enough-global-analysis-report | T | OP7 | — |
| R11 | El compromiso 5 (quejas) es el que menos puntúa | CHS Alliance | Blog de verificación | 2019 | https://chsalliance.org/get-support/article/exploring-the-chs-verification-data-why-commitment-5-is-scoring-low | T | OP7 | Sin cifras |
| R12 | Las quejas son el compromiso más débil | CHS Alliance | HAR 2022 | 2022 | https://www.chsalliance.org/get-support/article/har22_blog/ | T | OP7 | — |
| R13 | Partida de AAP del CERF de 3–4 M USD | CERF | Guía AAP 2024-I | 2024-04 | https://cerf.un.org/sites/default/files/resources/Guidance%20for%20CERF%20AAP%202024-I%20UFE%20envelope_with%20indicators_FINAL_1.pdf | I | OP7 | — |
| R14 | Vacante de mecanismo de quejas que pide SQL, Python y Power BI | PMA | Vacante en Kyiv | 2025-12 | https://www.impactpool.org/jobs/1185376 | V | OP7 | — |
| R15 | La mitad de las personas no se siente informada; ~30 % sin celular | IFRC / ACNUR / UNICEF | Encuesta R4V | 2020-01 | https://www.ifrc.org/es/article/encuesta-revela-que-solo-mitad-las-personas-refugiadas-y-migrantes-venezuela-se-sienten | T | OP7 | Antigua |
| R16 | RapidPro: 130 oficinas de país | UNICEF | rapidpro.io | consultado 2026-10 | https://home.rapidpro.io/ | I | OP7 | — |
| R17 | Zendesk gratis para ONG socias | Zendesk | Tech for Good | consultado 2026-10 | https://www.zendesk.com.mx/techforgood | C | OP7 | Criterios poco claros |
| R18 | CommCare: de 100 USD a más de 4.000 USD al mes | Dimagi | Pricing | consultado 2026-10 | https://commcare.dimagi.com/pricing/ | C | OP5, OP6 | — |
| R19 | PDM de MPC en Colombia (ADN Dignidad) | ACNUR / ADN Dignidad | Infografía | 2020-11 | https://data.unhcr.org/es/documents/details/82767 | I | OP6 | Sin cifras extraídas |

### X. Fraude, control y datos

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | OP | Limitación |
|---|---|---|---|---|---|---|---|---|
| X01 | El CVA no aumenta el riesgo de desvío; la preocupación por fraude pasó del 36 % al 42 % | CALP / Key Aid | Perception vs Reality | 2026-03-03 | https://www.calpnetwork.org/?p=589346 | T | OP8 | Cualitativa |
| X02 | Pérdida del 0,27 %; RDC 2,98 %; Malawi 9,8 % | GiveDirectly | Risk Report 2025 | 2026-06-05 | https://www.givedirectly.org/risk-report-2025 | I | OP8 | Una sola organización |
| X03 | Caso RDC: ~1,2 M USD; detectado en ~6 meses | GiveDirectly | DRC case | 2023 | https://www.givedirectly.org/drc-case-2023/ | I | OP8 | Autoinforme |
| X04 | Pérdidas en cash de ~2 % | CALP | Blog Bumbacher | 2019-03-13 | https://www.calpnetwork.org/blog/cash-is-no-riskier-than-other-forms-of-aid-so-why-do-we-still-treat-in-kind-like-the-safer-option/ | T | OP8 | Antigua |
| X05 | El screening de receptores es ineficaz | CALP / LSE | Newhouse | 2021-07-14 | https://calpnetwork.org/?p=49561 | T | OP8 | Siria |
| X07 | Reportar todo caso sustanciado; significativo a partir de 10.000 EUR | DG ECHO | FAQ fraud & aid diversion | vigente | https://www.dgecho-partners-helpdesk.eu/frequently-asked-questions-ngo/fraud-and-aid-diversion | I | OP8 | — |
| X08 | WeWorld compró Bridger XG para hacer screening | LexisNexis | Case study WeWorld | 2026 | https://risk.lexisnexis.com/global/en/insights-resources/case-study/weworld-sanctions-screening-compliance | C | OP8 | Marketing del proveedor |
| X09 | PMA Gaza (Self-Registration App): al menos 600.000 hogares afectados | Access Now | Comunicado | 2026-06 | https://www.accessnow.org/press-release/wfp-palestinians-data-breach/ | T | Requisito de datos | Parte interesada |
| X10 | Ciberataque al CICR: 515.000 personas | Al Jazeera | Nota | 2022-01-20 | https://www.aljazeera.com/amp/news/2022/1/20/cyberattack-on-icrc-exposes-data-on-515000-vulnerable-people | P | Requisito de datos | — |
| X11 | Guía IASC aplicada en al menos 20 contextos | OCHA Centre for Humanitarian Data | Nota de lanzamiento | 2023-05-01 | https://centre.humdata.org/revised-iasc-operational-guidance-on-data-responsibility-in-humanitarian-action/ | I | Requisito de datos | — |
| X12 | El 53 % de las organizaciones tuvo algún incidente | NetHope (vía commbox.org) | State of Humanitarian Cybersecurity 2025 | 2025 | https://commbox.org/document/2025-state-of-humanitarian-and-development-cybersecurity-report-continued-progress-but-more-is-needed-to-keep-pace-with-rapidly-evolving-threats | T | Requisito de datos | Copia no oficial; 30 organizaciones |
| X13 | 1 de cada 5 ONG tiene un plan de ciberseguridad | CyberPeace Institute | Cyberattacks real threat | sin fecha | https://reliefweb.int/report/world/cyberattacks-real-threat-ngos-and-nonprofits | T | Requisito de datos | Sin metodología |
| X14 | Ecuador: sanciones de la LOPDP desde el 26-may-2023 | NMS Law | Blog | 2023-06-21 | https://nmslaw.com.ec/blog/2023/06/21/regimen-sancionatorio-lopdp/ | T | Requisito de datos | Despacho jurídico |
| X15 | Nueva ley federal de protección de datos de México (2025) | Garrigues | Nota | 2025 | https://www.garrigues.com/es_ES/noticia/mexico-nueva-ley-federal-proteccion-datos-personales-posesion-particulares-introduce | T | Requisito de datos | Despacho jurídico |
| X16 | Somalia: desvío en los 55 sitios estudiados | ONU (vía Reuters / Malaysia Now) | Nota | 2023-09-19 | https://www.malaysianow.com/out-there-now/2023/09/19/eu-temporarily-holds-back-food-aid-in-somalia-after-un-records-widespread-theft | P | OP8 | El informe original no es público |

### L. Contextos frágiles, actores locales, comercios y protección social

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | OP | Limitación |
|---|---|---|---|---|---|---|---|---|
| L01 | Gaza: 20–40 % de comisión; 2 de 94 cajeros automáticos; ~15 % de sobreprecio | The New Humanitarian | Cash became a commodity | 2025-04-17 | https://www.thenewhumanitarian.org/news-feature/2025/04/17/cash-became-commodity-liquidity-crisis-compounding-suffering-gaza | P | OP9 | Testimonios |
| L02 | ~1.000 comercios; cambistas al 50–60 %; 205.000 USD | UNCDF | Amid the chaos… Gaza | 2026-06-04 | https://www.uncdf.org/article/9177/amid-the-chaos-of-conflict-a-long-term-financing-fix-quietly-took-hold-in-gaza | I | OP9, OP11 | Autopromoción |
| L03 | Alianza Mercy Corps–Last Mile Technology por la liquidez | CALP | Partnering to solve cash liquidity crisis | 2025-05 | https://www.calpnetwork.org/publication/partnering-to-solve-cash-liquidity-crisis-mercy-corps-sudan-and-last-mile-technology-lmt/ | I | OP9 | Sin costes |
| L04 | MPCA en Sudán: 201,8 M USD para 1,8 M personas | OCHA | Sudan HNRP 2025 | 2025 | https://humanitarianaction.info/plan/1220/document/sudan-humanitarian-needs-and-response-plan-2025/article/29-multipurpose-cash-section-and-cash-and-voucher-assistance-overview | I | OP9 | Son necesidades, no gasto |
| L05 | Transferencias grupales por Bankak en ~1 semana; carga documental | CALP | Group Cash Transfers in Sudan | 2026-07 | https://www.calpnetwork.org/wp-content/uploads/2026/07/CALP-Network-Report-Group-Cash-Transfers-in-Sudan-July-2026.pdf | T | OP9, OP10 | 5 localidades |
| L06 | Restricciones al CVA en el Sahel | CALP | Mitigating restrictions… Sahel | 2025-03-17 | https://www.calpnetwork.org/publication/mitigating-restrictions-on-cash-and-voucher-assistance-interventions-in-the-sahel-region-and-beyond/ | I | OP9 | Sin cifras |
| L07 | Sanciones mal alineadas; modelo neerlandés | ODI / HPG | Improving financial access for NPOs | 2026-01-13 | https://alnap.org/help-library/resources/improving-financial-access-for-non-profit-organisations/ | T | OP9 | Cualitativa |
| L08 | El 70 % de las ONG tiene dificultades para transferir fondos | ODI / HPG | Financial access challenges | 2025-04 | https://media.odi.org/documents/HPG_financial_access_4_final.pdf | T | OP9 | — |
| L09 | Myanmar: 5–6 meses de retraso; problemas de liquidez | Concern | Myanmar earthquake evaluation | 2025-12 | https://admin.concern.net/sites/default/files/documents/2026-03/Myanmar%20earthquake%20emergency%20response%20evaluation%20December%202025%20Executive%20Summary.pdf | A | OP9 | Un caso |
| L10 | Ucrania: <1 % directo a ONG locales; 3,4 % del CVA gestionado por ellas; 8 de 20 aceptan passporting; 0 casos de corrupción | Refugees International | Ukraine Localization Survey 2024 | 2024-12-19 | https://www.refugeesinternational.org/reports-briefs/annual-ukraine-localization-survey-2024/ | T | OP10 | Datos hasta feb-2024 |
| L11 | El 78 % del fortalecimiento de capacidades va a sistemas financieros; costes indirectos | Charter for Change | Spotlight 2025 | 2026-01 | https://charter4change.org/wp-content/uploads/2026/01/c4c_spotlight_25-1.pdf | T | OP10 | Autorreporte |
| L12 | ACNUR: 0 % de socios locales directos en Cox's Bazar en 2026 | COAST | Position Paper | 2025-11-30 | https://coastbd.net/wp-content/uploads/2025/12/Position-Paper-of-UNHCR-Partnership-and-Undermining-Local-Capacity-30-November-2025.pdf | T | OP10 | Parte interesada |
| L13 | Start Network y NetHope: "digital readiness" | Start Network | Blog | 2025-11-10 | https://startnetwork.org/learn-change/news-and-blogs/start-network-and-nethope-join-forces-advance-nonprofit-digital | I | OP10 | Anuncio |
| L14 | World Vision impone SMAP a sus socios | World Vision | Empowering local responders | ~2025-02 | https://www.wvi.org/sites/default/files/2025-02/Empowering%20local%20responders%20F.pdf | I | OP10 | Autoevaluación |
| L15 | Módulo de e-voucher en LMMS | World Vision | CVA Capacity Statement | 2025-05 | https://www.wvi.org/sites/default/files/2025-05/WV_CVA_Capacity%20Statement%20v2%20web.pdf | I | OP11 | Marketing |
| L16 | Más de 4.200 comercios del PMA | PMA | Supply chain for cash transfers | sin fecha | https://www.wfp.org/supply-chain-for-cash-transfers | I | OP11 | Fecha de corte desconocida |
| L18 | ESSN: 1,5 M de personas, traspasado al gobierno | IFRC | Press release | 2023-12-06 | https://www.ifrc.org/fr/press-release/ifrc-concludes-implementation-essn-programme-turkiye | I | OP12 | — |
| L19 | Baxnaano: más de 4 M de personas | Banco Mundial | Feature story | 2025-12-10 | https://www.worldbank.org/en/news/feature/2025/12/10/turning-hope-into-action-investing-in-resilience-through-somalia-s-national-safety-net | I | OP12 | — |
| L20 | Líbano: respuesta ampliada a través de las redes de protección del gobierno | CAMEALEON / CALP | Safety net and humanitarian cash in Lebanon | 2025-02 | https://www.calpnetwork.org/?p=288380 | T | OP12 | Solo resumen |
| L21 | Ucrania: 889 M USD de CVA alineado con el sistema nacional | OCHA | Ukraine HNRP 2026 | 2026 | https://humanitarianaction.info/plan/1515/document/ukraine-humanitarian-needs-and-response-plan-2026/article/27-cash-voucher-assistance-overview-and-multipurpose-cash-section-3 | I | OP12 | Son necesidades |
| L22 | Brasil: Auxílio Reconstrução pagado sin actores humanitarios | Poder360 | Artículo | 2024-05-29 | https://www.poder360.com.br/brasil/familias-do-rs-comecam-a-receber-o-auxilio-reconstrucao-nesta-semana/ | P | OP12 | — |
| L23 | Haití y Guatemala: solo transferencias en efectivo; piloto conjunto | PMA (ReliefWeb) | Country briefs | 2025-05 / 2025-06 | https://reliefweb.int/report/haiti/wfp-haiti-country-brief-may-2025 ; https://reliefweb.int/report/guatemala/wfp-guatemala-country-brief-june-2025 | I | OP11, OP12 | Mensuales |
| L24 | OpenSPP es un bien público digital | BID | Code catalog | consultado 2026-10 | https://knowledge.iadb.org/en/open-knowledge/code-development/open-source-solution/openspp | I | OP12 | — |
| L25 | 2 mil M de personas sin cobertura adecuada | Banco Mundial | State of Social Protection 2025 | 2025-04-07 | https://www.worldbank.org/en/topic/socialprotectionandjobs/publication/state-of-social-protection-2025-2-billion-person-challenge | I | OP12 | — |
| L26 | Sudán: problemas de liquidez; comisiones de hasta el 20 % | CGAP | Sudan financial system | 2024-12-03 | https://www.cgap.org/blog/can-what-remains-of-sudans-financial-system-be-used-to-fight-famine | T | OP9 | — |
| L27 | Los retrasos de pago a comercios "erode trust and risk disengagement" | World Vision | Blog | 2025-07 | https://www.wvi.org/es/node/142521 | I | OP11 | Blog |

### M. Mercado, tendencias, elegibilidad y competencia

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | OP | Limitación |
|---|---|---|---|---|---|---|---|---|
| M01 | CVA: 8,2 → 7,3 mil M USD; 4,3 % directo a actores locales | Development Initiatives / ALNAP | GHA 2026 | 2026 | https://alnap.org/help-library/resources/global-humanitarian-assistance-gha-report-2026/humanitarian-reform-and-delivery/ | T | Contexto | Serie revisada |
| M02 | 33,3 mil M USD; el 9 % de las organizaciones cerró; el 41 % entiende el uso de sus datos | ALNAP | SOHS 2026 *in brief* | 2026 | https://alnap.org/help-library/resources/sohs-2026/in-brief/ | T | Contexto | — |
| M03 | Integración con sistemas nacionales "small-scale" | ALNAP | SOHS 2026, cap. 2.2 | 2026-09 | https://alnap.org/help-library/resources/sohs-2026/chapter-2-what-works-and-at-what-cost/2-2-cash/ | T | OP12 | — |
| M04 | 6,6 mil M USD (2024); 4,5 mil M USD proyectados para 2025; el efectivo es el 82 % | CALP / ALNAP | How much support is delivered by CVA? | 2025-06-17 | https://www.calpnetwork.org/?p=295310 | I | Contexto | Provisional |
| M05 | EE. UU. aportaba el 42 % del CVA; caída de ~60 % | CALP | One year on from the USG cuts | 2026-01-26 | https://www.calpnetwork.org/?p=588066 | I | Contexto | Estimación temprana |
| M06 | PMA: 2,2 mil M USD; 33 % en vouchers | CALP | Funding Shock Test: WFP | 2026-05 | https://www.calpnetwork.org/?p=595076 | I | Contexto, OP11 | — |
| M07 | ACNUR: 450 M USD; 78 contratos con FSP; CashAssist canaliza el 96 % | ACNUR | 2025 Annual Report on Cash Assistance | 2026-01 | https://www.unhcr.org/us/sites/en-us/files/2026-01/2025-annual-report-on-cash-assistance.pdf | I | OP3, OP4 | — |
| M08 | Reserva de EE. UU.: 651 M USD de CVA; 11,9 % a actores locales | CALP | Blog | 2026-06-17 | https://www.calpnetwork.org/?p=602914 | I | Contexto | Un solo tramo |
| M09 | RMRP 2026: 8,1 % financiado; 152 socios | R4V / OCHA | Plan regional para Venezuela | 2025-11 | https://humanitarianaction.info/plan/1525/article/venezuela-rmrp-3 | I | Geografía | — |
| M10 | ACNUR Américas: 20 % financiado; 42 % de programas recortados | ACNUR | On the brink | 2025-07 | https://www.unhcr.org/sites/default/files/2025-07/on-the-brink-americas-overview.pdf | I | Geografía | — |
| M11 | 53 organizaciones con CVA en 17 países | R4V | CVA 2021 | 2022 | https://www.r4v.info:443/sites/default/files/2022-07/CVA.pdf | I | Geografía | Antigua |
| M12 | Prosper Global perdió ~2/3 de su financiación gubernamental y ~40 % de su personal | Devex | Rebrand | 2026-03-18 | https://www.devex.com/news/mercy-corps-to-become-prosper-global-112100 | P | Contexto | — |
| M13 | El peso del CVA "has plateaued"; prioridad a lo local | CALP | Strategy 2026–2028 | 2025/2026 | https://www.calpnetwork.org/about/strategy/ | I | Contexto, OP10 | — |
| M14 | Cash first; 55 % de los fondos CBPF a actores locales | OCHA | GHO 2026 | 2025-12 | https://humanitarianaction.info/article/2026-global-humanitarian-overview-collective-push-protect-millions-lives | I | Contexto | — |
| M15 | Catálogo de servicios comunes y colaborativo de datos | ONU | UN News, Compact | 2026-02 | https://news.un.org/en/story/2026/02/1167055 | I | Contexto | — |
| M16 | SOWC 2026 se publica el 12-nov-2026 | CALP | Página del informe | 2026 | https://www.calpnetwork.org/?p=592113 | I | Contexto | — |
| M17 | ECHO no puede financiar la transformación digital de sus socios | DG ECHO | Digitalisation Policy Framework | 2023-03 | https://civil-protection-humanitarian-aid.ec.europa.eu/system/files/2023-03/DG%20ECHO%20Policy%20Framework%20on%20Digitalisation%20-%20final_0.pdf | I | Elegibilidad | — |
| M18 | Servicios de IT de la oficina del proyecto elegibles; licencias ausentes de la lista de no elegibles | DG ECHO | Helpdesk, categorías de presupuesto | vigente | https://www.dgecho-partners-helpdesk.eu/ngo/eligibility-of-costs/eligibility-conditions-per-budget-categories | I | Elegibilidad | No incluye el Anexo 5 |
| M19 | NPAC sin techo, absorbido dentro del presupuesto | FCDO | Guía NPAC | 2020-08 | https://www.ukaidmatch.org/wp-content/uploads/2020/05/NPAC-guidance.pdf | I | Elegibilidad | Puede estar desactualizada |
| M20 | Umbral de equipamiento de 10.000 USD (2 CFR 200) | cpcon | Artículo | 2024 | https://cpcongroup.com/insights/article/2-cfr-200-1-equipment-vs-supplies-10000-threshold/ | T | Elegibilidad | No trata software |
| M21 | Costes indirectos del 7–8 % según el donante | IASC / Development Initiatives | Overhead Cost Allocation | 2022-11 | https://library.alnap.org/system/files/content/resource/files/main/IASC%20Research%20report_Overhead%20Cost%20Allocation%20in%20the%20Humanitarian%20Sector.pdf | T | Elegibilidad | No trata IT |
| M23 | Plataforma de transformación digital de IFRC (DTIP): 100 M CHF; ~250.000 CHF por Sociedad Nacional al año | IFRC | Folleto DTIP | 2023 | https://www.ifrc.org/sites/default/files/2023-12/DTIP-brochure-design-pages-v2.pdf | I | Contexto | Vigencia en 2026 sin verificar |
| M25 | El 42 % cita capacidad limitada de IT | CALP | SOWC 2023, cap. 5 | 2023-11 | https://www.calpnetwork.org/wp-content/uploads/2023/11/SOWC_2023_C5-KH-Final.pdf | I | Contexto | — |
| M26 | Precios públicos de Kobo, ODK, SurveyCTO, ActivityInfo y Salesforce (este último según un socio implementador) | Varios | Páginas de precios | consultado 2026-10-07 | https://www.kobotoolbox.org/pricing/ ; https://getodk.org/pricing/ ; https://www.surveycto.com/pricing/ ; https://www.activityinfo.org/about/pricing.html ; https://magicfuse.co/blog/salesforce-nonprofit-cost | C | OP2, OP5, OP7 | — |
| M27 | HOPE: 33 países; 9,3 M de personas; 228 M USD; bien público digital | UNICEF | HOPE Annual Report 2025 | 2026 | https://www.unicef.org/hope-hct/reports/hope-annual-report-2025 | I | OP1, OP2, OP3 | Autoinforme |
| M28 | Building Blocks: SaaS gratuito vía CWG; 6 M de personas | UN Innovation Network | Blog | 2026-02-28 | https://www.uninnovation.network/blog/how-the-building-blocks-blockchain-network-is-transforming-humanitarian-aid | I | OP1 | — |
| M30 | RedRose: 11 agencias usuarias; más de 50 países | CALP (notas de una sesión con RedRose) | RedRose Special Session | 2024-02-13 | https://www.calpnetwork.org/wp-content/uploads/2024/02/RedRose-Special-Session-notes-13th-February-2024.pdf | C | OP2, OP3 | Autodeclarado |
| M31 | RedRose: pago por uso en el Movimiento de la Cruz Roja | IFRC Cash Hub | RedRose introduction | sin fecha | https://cash-hub.org/resources/cash-technology/redrose/redrose-introduction | I | OP2, OP3 | — |
| M32 | 121 adoptada por IFRC | IFRC Cash Hub | IFRC adopts 121 | 2024 | https://cash-hub.org/resource/ifrc-adopts-121-platform-innovative-digital-cash-and-voucher-assistance | I | OP3, OP10 | — |
| M33 | Aidonic: 1,655 M CHF levantados; "120+ small-sized nonprofits" | Venturelab | Perfil | 2022 | https://www.venturelab.swiss/AIDONIC-The-Venture-Leader-Fintech-revolutionizing-payment-infrastructures-for-humanitarian-organizations | C | OP10 | Datos del proveedor |
| M35 | "It's not about tools anymore – it's about political will" | IFRC Cash Hub | Dialogue: Resetting | 2025-05-16 | https://cash-hub.org/wp-content/uploads/sites/3/2025/06/Cash-Hub-Dialogue-Event_Resetting-the-Humanitarian-System-the-role-of-Cash-Assistance_Summary.pdf | I | OP10 | Resumen de evento |
| M37 | Dinero móvil: 2 billones de USD; ~75 % de las cuentas inactivas | GSMA (vía CFOtech) | State of the Industry 2026 | 2026 | https://cfotech.news/story/gsma-says-mobile-money-hits-usd-2-trillion-in-2025 | C | Contexto | Gremio del sector |

---

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| Borrador 1 | 2026-10-07 | Comparación inicial de O1–O11 | /research-market, Research 2 | No |
| Borrador 2 | 2026-10-07 | Ampliación completa: reorganización en OP1–OP12; fichas con criterios C1–C10; tratamiento especial de conciliación e interoperabilidad; matrices; shortlist; áreas no priorizadas; propuesta de cambio según WORKFLOW §3.1 | Instrucciones de la responsable; segunda ronda de búsqueda (6 líneas) | No |
| v1 | 2026-10-07 | Versión validada (= borrador 2). La propuesta de cambio de la sección 11.2 queda registrada, no aplicada | Validación explícita de la responsable | Sí |
| v1.1 | 2026-10-07 | Cambio de ruta: market-opportunities.md → cva-market-opportunities.md; encabezado con fecha, documento derivado y cadena de research; autorreferencia de §11.2 actualizada. Contenido de análisis sin cambios | Reorganización de los documentos de research pedida por la responsable | Sí |
