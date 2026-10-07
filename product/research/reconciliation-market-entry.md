---
source: secondary
method: web + artefactos validados
date: 2026-10-07
question: ¿Cómo está resuelto hoy el problema de conciliación en CVA, quién compite directa e indirectamente, qué gaps permanecen abiertos y cuál sería una estrategia plausible de entrada al mercado para NexoAid?
---

# Análisis competitivo y entrada al mercado: conciliación CVA — NexoAid

> Ruta: product/research/reconciliation-market-entry.md
> Estado: VALIDADO — v1 (2026-10-07)
> Versión: v1 (corresponde al borrador 2, reescritura narrativa del borrador 1 con el mismo contenido, evidencia y fuentes)
> Etapa: Problem Discovery
> Fecha: 2026-10-07
> Responsable: Paola Espejo
> Origen: product/research/market-beliefs.md v1.1 · product/research/cva-market-opportunities.md v1.1 · product/research/opportunity-prioritization.md v1
> Cadena de research: creencias → exploración del mercado → priorización (OP3, conciliación) → **análisis competitivo y entrada (este documento)**

## 0. Alcance, método y límites

Este documento examina un solo problema: la conciliación dentro del ciclo de pago de Cash and Voucher Assistance (CVA). Corresponde a OP3 y a su causa raíz, OP2, en `cva-market-opportunities.md`. El análisis busca explicar cómo se resuelve hoy ese problema, quién compite, qué hueco queda abierto y qué vía de entrada sería plausible para NexoAid.

**Fuentes y notación.**

- La base son los tres research validados. Sus fuentes se citan con el prefijo `[CVA-xx]`.
- Se añadieron tres líneas de búsqueda web realizadas el 2026-10-07:
  - plataformas CVA y RedRose;
  - proveedores financieros (FSP), ERP y sustitutos;
  - capas de integración y evidencia de compra.
- Las fuentes nuevas llevan los códigos [R], [P], [F], [E], [I] y [D]. Todas figuran en la sección 14.
- Etiquetas: **COMERCIAL** indica que la afirmación procede del propio proveedor; **Inferencia**, que se deduce de los hechos sin aparecer en ninguna fuente; `[conocimiento del modelo — verificar]`, que no pudo comprobarse.

**Límites de la búsqueda.**

- Varias búsquedas agotaron su cupo y algunas páginas estaban bloqueadas.
- No se pudieron leer:
  - la licitación de Relief International (IPU2026002);
  - el código de HOPE;
  - las cuentas de RedRose;
  - el documento CALP/CGAP sobre stablecoins (sep-2026).
- La evidencia más sólida procede de auditorías de ACNUR y del PMA. Fuera de la ONU, lo que se sabe es sobre todo cualitativo.

**Lo que el documento no hace.** No define MVP, roadmap, arquitectura, precios ni tamaño de mercado. Cuando menciona capacidades, lo hace para comparar competidores, no para diseñar un producto.

---

## 1. El problema de conciliación dentro del ciclo CVA

### 1.1 Del registro al cierre

Un programa de efectivo empieza mucho antes del pago.

**Registro y programación.** La organización registra a cada participante en Kobo, ODK o CommCare, o directamente en un sistema de gestión de beneficiarios: HOPE, SCOPE, CashAssist, RedRose o 121. Con frecuencia usa también Excel. A partir de ese registro, el equipo de Programa define el derecho de cada persona en cada ciclo: quién recibe, cuánto y cuándo.

Los problemas ya pueden empezar aquí:
- identificadores ausentes, repetidos o redondeados al migrar de sistema;
- datos que alguien modifica después de cerrar la lista [CVA-A01, CVA-D09];
- listas que se rehacen varias veces ("rolling spreadsheets") hasta que nadie sabe cuál es la versión válida [CVA-A12].

**Instrucción de pago.** Con la lista aprobada, Finanzas y Programa emiten la instrucción de pago al FSP, respetando la segregación de funciones. En la mayoría de los casos la instrucción es un archivo, no una llamada a una API. En cinco de las siete operaciones de ACNUR auditadas en 2025, los datos se transfieren a mano hacia y desde los sistemas del FSP [E8]. Cada FSP exige su propio formato.

**Ejecución en el FSP.** El FSP valida cada pago (identidad, cuenta registrada, saldo disponible) y lo ejecuta mediante un abono, un código de retiro, una carga de tarjeta o un voucher. Aquí aparecen las primeras desviaciones:
- pagos parciales cuando falta saldo;
- rechazos a personas no registradas [F3, F4];
- agentes sin liquidez;
- dispositivos que no sincronizan [CVA-F04, R6].

**Respuesta del FSP.** El FSP devuelve el resultado por callback, archivo o portal. Pero usa sus propios identificadores. Los callbacks de M-Pesa se pierden si fallan, porque no hay reintento automático [F1]. Y algunos reportes llegan con meses de retraso: en Nigeria, el PMA pasó seis meses sin recibirlos, por un total de 800.000 USD [F15].

### 1.2 Cuando empieza la conciliación

El problema rara vez aparece al enviar el pago. Aparece después, cuando la organización tiene que responder preguntas como estas:
- ¿Quién recibió y quién no?
- ¿Cuánto se pagó realmente?
- ¿Qué falló y debe reintentarse?
- ¿Qué no se cobró y debe reintegrarse?
- ¿Cuánto queda por liquidar del anticipo entregado al FSP?
- ¿Qué tiene que registrar Finanzas para cerrar el ciclo?

Responderlas exige cruzar tres planos que viven en sistemas distintos:
1. **Programático:** la lista aprobada frente al resultado por persona.
2. **Financiero:** el anticipo o débito frente a lo pagado, más comisiones y reintegros, frente al ERP y el extracto bancario.
3. **Comercial** (solo en programas de vouchers): los canjes frente a la factura del comercio y el pago al comercio.

En cada plano interviene un actor distinto [D13, D14]:
- **Programa** aporta la prueba de entrega y decide si se reintenta o se recoloca un pago.
- **Finanzas** valida, liquida el anticipo, registra comisiones, gestiona reintegros y cierra en el ERP.
- **Logística o Procurement** vela por el cumplimiento del contrato con el FSP.
- **El FSP** informa, revierte o reintegra cuando se le pide. En algunos contratos entrega además un informe de conciliación; UNICEF Bangladesh, por ejemplo, lo exige en 10 días hábiles [D5].
- **El comercio**, en programas de vouchers, espera su pago. Si se retrasa, puede abandonar el programa [CVA-L27].

En la práctica, varias de estas funciones las comparten roles mixtos: el "Payment Officer" de Mercy Corps y las vacantes de IFRC y de UNICEF Sudán combinan tareas de Cash y de Finanzas [D8, D12].

### 1.3 Qué pasa cuando la conciliación llega tarde

La evidencia muestra consecuencias concretas, todas documentadas en auditorías de la ONU:

- **Diferencias entre sistemas.** En ACNUR se acumularon 71 M USD de diferencia entre CashAssist y el ERP [E7]. En el PMA de Sudán del Sur, las conciliaciones se aprobaban tres a seis meses después del pago y se gestionaban en más de 100 hojas de Excel [CVA-A06].
- **Fondos no cobrados.** ACNUR recuperó 3,6 M USD de 14.432 tarjetas inactivas. Además, un FSP cobraba comisión por cada código emitido, se cobrara o no [E7].
- **Comisiones sin registrar.** Quedaron 2,9 M USD en comisiones fuera de los estados financieros [E7].
- **Duplicados.** En Polonia se pagaron dos veces 1,5 M USD [E7].
- **Pagos marcados como exitosos con importe cero** [E8].
- **Anticipos al FSP que siguen abiertos** [E5].
- **Recomendaciones de auditoría con plazo en 2026** [E8, E9].

Hay también consecuencias para las personas y los comercios: quien no cobró puede quedarse sin reintento a tiempo [P2], y los comercios cobran tarde. La literatura no muestra de forma directa que un informe a un donante se haya retrasado por esta causa. Es un vacío de evidencia, no una refutación.

**Idea central de esta sección.** La conciliación no es un único cruce de datos. Es un workflow de cierre y de resolución de excepciones que empieza cuando el FSP devuelve el resultado y termina cuando Finanzas cierra el ciclo y Programa sabe a quién le falta recibir.

---

## 2. Dónde se concentra realmente el dolor

Los quince subproblemas identificados en el borrador anterior pueden agruparse en cuatro bloques. Su grado de cobertura no es uniforme, y esa diferencia es la que orienta el resto del análisis.

### 2.1 Diferencias entre lo instruido y lo ejecutado

El primer bloque reúne lo que ocurre entre la instrucción y el primer resultado: pagos fallidos, parciales o duplicados, montos incorrectos y personas que no aparecen en el reporte del FSP.

**Causas:**
- formatos e identificadores distintos entre la organización y el FSP;
- problemas de KYC, cuentas no registradas, saldo insuficiente o SIM bloqueadas [F3, CVA-F03];
- listas con la misma persona dos veces.

**Cómo se resuelve hoy.** Las plataformas CVA resuelven razonablemente el **estado por persona**:
- 121 importa un CSV de éxito o error, o recibe callbacks por API, y desde la misma interfaz permite reintentar los pagos fallidos [P1, P2]. En Sudáfrica, los rechazos bajaron de 100–150 a cinco [P4].
- HOPE y RedRose comparan lo ordenado con lo pagado a partir del archivo de retorno [P5, R1].

**Dónde se queda corto:**
- En 121 el estado es binario. El cruce se hace por una sola columna configurable, sin validar que exista. Si hay duplicados, se toma el primer registro o el archivo sobrescribe sin avisar [P1].
- No hay evidencia de que alguna plataforma controle duplicados en el momento de conciliar. La deduplicación se hace antes, con Building Blocks o EDS, y aun así ocurrieron pérdidas como la de Polonia [E7, P10].
- Los montos parciales no aparecen tratados en ninguna documentación (inferencia sobre [F3, P1]).
- Cuando un identificador del FSP no casa con el de la organización, el cruce se hace a mano por nombre o teléfono [CVA-A04].
- En algunas operaciones ni siquiera se concilia por persona: el PMA en Chad solo revisaba diferencias agregadas [CVA-A08].

**Cobertura: media.** Es buena con API e insuficiente sin ella.

### 2.2 Excepciones posteriores al primer resultado

El segundo bloque empieza cuando el estado ya se conoce y hay que actuar sobre él: pagos no cobrados, reversos, vencimientos, reintegros y reintentos.

La evidencia muestra que este bloque se gestiona por petición y a mano:
- En Pakistán, el FSP JazzCash revertía de forma masiva los no cobrados solo tras una petición escrita [F20].
- En Kenia, los reversos de M-Pesa son manuales y dependen de roles del portal [F3].
- En Colombia, los giros de Efecty vencen a los 30 días y hay que solicitar su recolocación [F13].
- El CICR registra los no cobrados como prepago hasta que vencen [D13].
- En un programa del gobierno colombiano, la Contraloría señaló "dificultades para conciliar": de 246.668 giros, 21.907 se reintegraron y 26.173 seguían pendientes a mitad de 2026 [F14]. No es un caso de ONG, pero ilustra el mismo mecanismo.

**Cobertura: baja.** Ninguna plataforma documenta públicamente un ciclo de vida completo para estas excepciones. Hoy se siguen en Excel y por correo electrónico.

### 2.3 Conciliación financiera

El tercer bloque es el paso de la persona a la contabilidad: liquidar el anticipo entregado al FSP, registrar comisiones y reintegros, y cerrar en el ERP. Es el tramo más débil.

**Por qué el ERP no basta.** El ERP concilia el extracto bancario con el libro mayor, pero solo ve uno o pocos movimientos por ciclo. No ve las decenas de miles de pagos individuales [E1, E2, E6]. Las comisiones se calculan a mano y en ocasiones se pagan fuera de contrato [E7, CVA-A24]. El cierre depende de reportes del FSP que pueden tardar meses [F15].

**El caso más avanzado.** HOPE lee los compromisos financieros de SAP VISION y liquida el anticipo frente a la conciliación individual. Pero no escribe de vuelta en el ERP [P6, P8].

**Cobertura: baja o media.** La consecuencia es la que muestran las auditorías: anticipos abiertos y diferencias de decenas de millones entre el sistema de programa y la contabilidad.

### 2.4 Coordinación entre actores

El cuarto bloque no es un dato que falte, sino una conversación que se rompe:
- Programa decide reintentar o recolocar.
- Finanzas reintegra y cierra.
- El FSP ejecuta, pero responde con su propio ritmo y formato.
- El comercio necesita cobrar.

Las guías de IFRC y del CICR reparten estos papeles con claridad [D13, D14, D15]. En la práctica, sin embargo, los roles se mezclan, y los consorcios terminan creando sus propias herramientas para coordinarse: en Colombia, el consorcio VenEsperanza diseñó una plantilla común de incidencias porque cada socio "reported different things in different ways" [F18].

**Comercios.** En los programas de vouchers la cobertura es algo mejor. RedRose y Building Blocks concilian canjes de comercios, con POS o con un libro de transacciones [R5, P12]. Aun así, el papel sigue presente: en Siria, RedRose verificaba el 30 % de los recibos; en Nigeria, CRS recomendó llevar registros en papel por los fallos de sincronización [R5, R6].

### 2.5 Lectura de conjunto

La cobertura disminuye a medida que se avanza en el ciclo:
- El **primer resultado** está razonablemente cubierto.
- Lo que viene **después** está cubierto de forma débil: excepciones con ciclo de vida, comisiones, anticipo, cierre y coordinación entre áreas.

Sobre el reporting a donantes con cifras conciliadas no hay evidencia suficiente para valorarlo.

---

## 3. Cómo se resuelve hoy

El mercado no está vacío. Hay cinco familias de soluciones, y cada una ocupa un lugar distinto en el ciclo.

### 3.1 Plataformas CVA: cubren el estado por persona

Las plataformas CVA ocupan el centro operativo.

**RedRose, 121 y HOPE** cruzan, persona por persona, lo ordenado con lo informado por el FSP, ya sea por archivo de retorno o por API [R1, P1, P5]. Sus diferencias:
- **HOPE** añade la liquidación del anticipo. En 2025 automatizó la conciliación con Western Union y MoneyGram [P8].
- **121** trabaja con nueve o más FSP documentados (MTN, Airtel, Nedbank, Intersolve Visa, Commercial Bank of Ethiopia, entre otros), bajo licencia Apache 2.0 [P3].
- **Humansis** declara conciliación, pero no la documenta, y sus repositorios no tienen actividad desde 2023 [P13].
- **Aidonic, OmniAid, ESTHER–Visa, Stellar Aid Assist, IrisGuard y Mastercard Community Pass** prometen seguimiento o reporting, sin evidencia operativa de conciliación [P14, P16] (COMERCIAL).

**Herramientas internas de la ONU.** Las agencias grandes construyeron las suyas:
- El PMA tiene **SCOPE**. Sus controles pueden desactivarse [P9], y en Burkina Faso la conciliación tripartita se incumplía y había IDs duplicados [P10]. En Chad, el tablero de conciliación no funcionaba porque sus fechas de ciclo no coincidían con las de SCOPE [CVA-A07]. Además desarrolló **DARTs**, una herramienta de aseguramiento y conciliación que opera en 14 países, con planes de llegar a unos 40, y que declara 3.000 horas ahorradas; sus cifras publicadas son inconsistentes [P15].
- ACNUR usa **CashAssist** y avanza en su integración con FSP mediante DHOTS, con plazo a diciembre de 2026 [E8].
- **Building Blocks** es gratuito vía los grupos de coordinación de cash (CWG) y lo usan unas 30 organizaciones. Funciona sobre todo para coordinar y deduplicar; solo en Jordania concilia canjes de comercios [P11, P12, CVA-D05].

**Lo que ninguna plataforma documenta.** No hay documentación pública de un motor de conciliación con normalización entre FSP, reglas configurables, clasificación de excepciones o colas de trabajo, ni de conciliación de comisiones o asiento en el ERP. Su conciliación es parte central del producto, pero se detiene en el primer resultado.

### 3.2 FSP: cubren su propio canal

Los FSP entregan bien lo que ocurre dentro de su canal.

**Dinero móvil.**
- M-Pesa ofrece estado por transacción, extractos de seis meses y un portal masivo de hasta 20.000 filas. Promete "real-time automated reconciliation" por API (COMERCIAL) [F2]. En la práctica, los pagos parciales quedan como "failed" y los reversos son manuales [F3].
- MTN advierte a sus propios clientes que no confíen solo en los callbacks y que concilien a diario [F4].

**Agregadores.** Flutterwave, dLocal, Onafriq, Thunes e IntaSend envían notificaciones por transacción con entre cuatro y siete estados. Onafriq promete "real-time reconciliation" e IntaSend ofrece reportes para donantes (COMERCIAL) [F6, F7, F9, F10, F11].

**Remesadoras.** Western Union y MoneyGram ya están integradas con HOPE y RedRose [P8, R9].

**Bancos y pagadores en América Latina.** Davivienda y Daviplata entregan informes acordados por un portal seguro [F12]. Efecty trabaja con ventanilla y vencimientos [F13].

**Plataformas de pago masivo.** Wise acepta lotes de hasta 1.000 pagos [F21]. Stripe lo dice sin rodeos: "You're responsible for reconciling" [F8].

**Lo que el FSP no cubre:**
- el cruce con la lista de la organización;
- la vista conjunta de varios FSP;
- el ciclo de vida de las excepciones;
- la liquidación del anticipo frente al ERP;
- la tolerancia a reportes tardíos o en formatos difíciles de procesar. En Colombia, el PMA recibía reportes de comercios por correo en hojas de cálculo y tenía 2 M USD sin conciliar [F16].

### 3.3 ERP: recibe el cierre, pero no concilia

El ERP es el destino del cierre, no el lugar donde se concilia.

Dynamics 365 o NetSuite concilian el extracto bancario con el libro mayor [E1, E2]. Las organizaciones grandes usan ERP corporativos:
- ACNUR migró a Oracle Fusion Cloud en 2023 [E3];
- el PMA usa WINGS (SAP);
- UNICEF usa VISION (SAP);
- NRC lleva casi 25 años con Unit4 [E4].

**¿Podría el ERP absorber la conciliación?** Técnicamente sí, con desarrollo a medida. En la práctica hay cuatro fricciones:
1. Por cada ciclo el ERP registra uno o pocos movimientos, no las ~100.000 líneas individuales [E6].
2. Los datos personales viven fuera del ERP, y las políticas de datos desaconsejan meterlos.
3. Los anticipos al FSP se liquidan más tarde [E5].
4. Las comisiones y los reintegros llegan por otros canales [E7].

El caso de UNICEF lo confirma: aun teniendo SAP, situó la conciliación con el FSP en HOPE y no en VISION [P8].

### 3.4 Excel, procesos manuales y personal: el sustituto dominante

Excel, junto con los procesos manuales y el conocimiento interno, es el competidor dominante.

**La evidencia de su peso:**
- En Palestina, el PMA conciliaba unas 100.000 transacciones por ciclo en hojas de cálculo, un proceso que la auditoría calificó de "inherently prone to errors" [E6].
- Una vacante de UNICEF Sudán (2026) pide Excel avanzado para conciliar listas contra reportes del FSP y extractos bancarios [D8].
- El propio PMA creó DARTs porque su personal buscaba datos a mano en Excel y en papel [P15].

**Por qué resiste:** no cuesta nada, es flexible y se apoya en conocimiento local.

**Por qué falla:** produce errores, no escala, no deja rastro de auditoría y depende de personas que rotan [R1].

**Variantes y alternativas genéricas:**
- Power Query, Power BI, SQL, scripts y RPA son el "hazlo tú mismo" de las organizaciones con capacidad técnica. No se encontraron casos publicados de conciliación CVA con estas herramientas. El PMA usa UiPath, pero para anticipos de viaje [E10]. OCHA usa Power Apps para conciliar facturación entre agencias, no pagos CVA [I12].
- Las herramientas genéricas de conciliación financiera no tienen evidencia de uso humanitario. BlackLine tiene una mediana estimada de 40.125 USD al año y una implementación costosa [E11]. Simetrik, en América Latina, procesa más de 1.000 millones de transacciones diarias [E13].
- Xero solo concilia a nivel bancario, entre 27 y 97 USD al mes [E12].
- Los consultores hacen conciliaciones a posteriori. No se encontraron términos de referencia específicos.

**Dónde está el gasto real hoy.** En personal dedicado: las vacantes de UNICEF, DRC, PMA e IFRC incluyen la conciliación entre sus funciones [D8–D12].

### 3.5 Plataformas de integración: conectan, pero sin lógica de negocio

Las plataformas de integración pueden conectar sistemas, pero no traen la lógica de negocio de la conciliación.

**OpenFn** es la más legítima del sector:
- es un bien público digital (DPG) de código abierto, con versión SaaS;
- sus precios van de 0 a 499 USD al mes, con soporte desde 75 USD por hora [I1];
- tiene adaptadores de M-Pesa y MTN MoMo desde 2025 [I6, I7];
- vende a través de socios integradores [I5];
- promete "automatically reconcile records" (COMERCIAL) [I2], pero no tiene ningún caso publicado de conciliación CVA. Sus clientes nombrados (UNICEF, IRC, Mercy Corps, NRC) no indican qué uso le dan, y sus socios no se especializan en cash [I3, I4].

**Otras herramientas:**
- MuleSoft, Boomi y Workato son caras para una ONG mediana y no tienen presencia en CVA.
- Zapier, Make y n8n no están pensadas para lotes de miles de filas con datos sensibles [I10, I11].
- Mojaloop, G2P Connect y Mifos Payment Hub pertenecen a otra capa, la de los pagos públicos de gobierno a personas (G2P). Aun así, G2P Connect podría llegar a ser el estándar de datos de pago [I8, I9].

**Dónde está la competencia, entonces.** Hoy está en las plataformas CVA y en Excel. A medio plazo, OpenFn con un integrador es la amenaza más plausible para organizaciones con capacidad técnica (inferencia).

### 3.6 Mapa de capacidades

La siguiente matriz resume qué hace cada familia. **S** = sí documentado; **P** = parcial; **N** = no; **D** = desconocido.

| Capacidad | RedRose | 121 | HOPE | SCOPE/DARTs | Portal FSP / agregador | ERP | Excel/BI | OpenFn |
|---|---|---|---|---|---|---|---|---|
| Ingesta de datos del FSP | S | S | S | S | No aplica | N (solo banco) | S (manual) | S |
| Normalización entre FSP | D | N | D | D | N | N | Manual | P (a medida) |
| Matching por persona | P | P (una columna) | P | P | N | N | Manual | A medida |
| Reglas configurables | D | N | D | P | N | S (banco) | Manual | A medida |
| Gestión de excepciones por tipo | P (papel) | P (fallo + reintento) | D | N | P (reversos manuales) | P (banco) | Manual | A medida |
| Alertas | P | P | D | D | P | P | N | P |
| Auditoría / audit trail | S | D | P | P | P | S | N | P |
| Trazabilidad por persona | S | S | S | S | N (IDs propios) | N | P | N |
| APIs | P | S | S | D | S | S | N | S |
| Integración con FSP | P | S | S | S | No aplica | N | N | S (conectores) |
| Integración con ERP | D | N | P (lectura) | P (WINGS) | N | No aplica | Manual | P |
| Comisiones y anticipos | D | N | P (anticipo) | D | P (su canal) | P | Manual | N |
| Reporting | S | D | S | D | P | S | P | N |
| Multi-país / multi-FSP | S / S | S / S | S / S | S / S | Su red | S / No aplica | — | S |
| Seguridad / privacidad | P (incidente en 2017) | D | P | P | S | S | N | P (autoalojable) |
| Soporte | S (helpdesk) | D | S | No aplica | S | S | — | P (de pago) |

**Capacidades que ya son estándar:**
- estado por transacción;
- ingesta del archivo o la API del FSP;
- trazabilidad por persona;
- envío multi-país y multi-FSP;
- reporting;
- audit trail básico.

**Capacidades poco cubiertas:**
- normalización entre FSP con formatos distintos;
- matching robusto (más de una clave, detección de duplicados y montos parciales);
- ciclo de vida de las excepciones;
- comisiones;
- liquidación del anticipo;
- puente hacia el ERP;
- tolerancia a reportes tardíos.

Hay además capacidades que parecen diferenciadoras pero ya son comunes: "trazabilidad end-to-end", "dashboards en tiempo real", integración con dinero móvil, audit trail y operación offline. Casi todos los actores las prometen.

**Conclusión de la sección.** El mercado tiene soluciones parciales, pero ninguna capa domina claramente el cierre del ciclo entre Programa, FSP y Finanzas.

---

## 4. RedRose como referencia competitiva principal

RedRose merece un análisis propio. Es la plataforma comercial más extendida entre las INGO y la que más se acerca al espacio de la conciliación.

### 4.1 Lo que se sabe

**La empresa.**
- Red Rose CPS Ltd se constituyó en Londres el 30 de enero de 2015 y sigue activa. Está registrada con actividades de consultoría TI y hosting [R8].
- Presenta cuentas abreviadas auditadas, que no publican ingresos [R8].
- Se describe como autofinanciada y rentable, con un crecimiento del 20–30 % (COMERCIAL) [R4].

**Clientes.**
- En la sesión de CALP de 2024 declaró 11 agencias y más de 50 países. Entre ellas: Concern, IFRC, CRS, UNICEF, OIM, PMA, Save the Children, GiveDirectly, NRC, IRC y CARE [R4].
- Según MoneyGram, ambas empresas distribuyeron juntas más de 350 M USD (COMERCIAL, sin fecha) [R9].

**Producto.**
- Cubre registro, monitoreo de precios, seguimiento posdistribución (PDM), distribución de efectivo y en especie, vouchers y reporting. Incluye una app para comercios (ONEapp), tarjetas (ONEcard) e integración con Kobo y ODK [R3, R5, R6].
- El IFRC la describe con la frase "automated reconciliation in a secured and auditable manner", que reproduce el posicionamiento del propio proveedor [R3].

**Cómo concilia en la práctica.**
- **Pilotos del IFRC.** La mayoría trabajó de forma semiintegrada. Se descargaba el archivo de pago, el FSP lo cargaba y devolvía un archivo de conciliación, y RedRose comparaba "who should be paid" con "who was paid" [R1]. En Ruanda hubo integración completa con MTN, pero exigió una cuenta intermedia [R1]. En Kenia, en 2018, la conciliación con M-Pesa fue en tiempo real [R2].
- **Con comercios (Siria, 2016).** Cada semana se recibía un informe con recibos escaneados, se verificaba el 30 % en el back end y se reembolsaba al comercio en menos de una semana [R5].
- **CRS en Nigeria.** Los fallos de sincronización llevaron a recomendar "keep meticulous paper records… triangulate" [R6].
- **Controles.** El IFRC documenta segregación de funciones [R1]. La versión de CRS, CAT, añade auditoría de usuarios y alertas de fraude [R7].

**Implementación.**
- La formación estándar son cinco días presenciales con dos consultores, o dos a tres días en remoto. Resultó estrecha: dejó fuera vouchers, comercios y tramos múltiples [R1].
- El helpdesk se describe como un factor decisivo.
- Se recomienda usar la configuración estándar [R1].

**Modelo de negocio.**
- Pago por uso: "service fee… percentage of the total cash disbursed", con descuentos dentro del acuerdo marco del IFRC. Si no hay distribución, no hay coste [R2, R3].
- En Siria, en 2016, la tarifa fue del 4 % por transacción, más un 1 % de hawala [R5].

**Limitaciones documentadas.**
- Costes operativos "less well understood".
- Gestión de datos que no suele presupuestarse.
- Rotación de personal.
- Gambia pedía "complete control" de la plataforma.
- Tanzania volvió a Kobo y Excel por problemas de conectividad [R1].
- Incidente de seguridad en 2017 [R10].

### 4.2 Lo que se infiere

**Por qué es difícil desplazarla.** Controla buena parte del flujo de sus clientes:
- un ecosistema cerrado de tarjetas, app de comercios y marca blanca (CRS CAT);
- un acuerdo marco con el IFRC;
- experiencia probada en operación offline.

**Dónde parecen estar sus límites.** Su conciliación es sólida en el estado por persona y en el canje de comercios. Pero no hay evidencia pública de:
- gestión de excepciones por tipo y con ciclo de vida;
- conciliación de comisiones;
- liquidación del anticipo;
- puente al ERP;
- normalización de FSP no integrados más allá del archivo de retorno.

**Sus debilidades estratégicas.**
- Un precio proporcional al desembolso puede encarecerse con volúmenes altos.
- Sus costes son poco claros.
- Es una empresa de tamaño desconocido que intenta cubrir todo el ciclo.

### 4.3 ¿Competidor directo, incumbente adyacente o socio potencial?

El argumento apunta a que RedRose es un **incumbente adyacente con potencial de socio**.

- **Por qué es incumbente.** Ya ocupa el lugar donde sus clientes concilian, y su fuerza en ese espacio es media-alta.
- **Por qué es adyacente y no rival directo.** Su producto se centra en el ciclo completo de distribución, no en el cierre financiero.
- **Por qué podría ser socio.** Si NexoAid compitiera como plataforma CVA completa, se enfrentaría a un ecosistema consolidado sin una ventaja clara. Si, en cambio, resultara útil también a los usuarios de RedRose, 121, HOPE o Excel en el tramo posterior al primer resultado, RedRose pasaría a ser un socio o canal potencial.

**La condición.** Una propuesta que solo sirviera a quien no tiene plataforma reduciría el mercado. Una que sirviera a todos lo ampliaría. Esto es una hipótesis, no una conclusión.

---

## 5. El resto del mapa competitivo

El resto de alternativas se ordena mejor por el tipo de amenaza que representan que por nombre de producto.

### 5.1 Competidores que ya tienen los datos: RedRose, HOPE y 121

Estas plataformas ya tienen la lista, el resultado del pago y, en algunos casos, el canje de comercios.

**HOPE** es la amenaza más directa dentro de su ecosistema:
- es gratuita;
- ya liquida anticipos y lee de SAP;
- en 2025 automatizó la conciliación con Western Union y MoneyGram [P8].

Una ONG la elegiría por su coste y su conexión con UNICEF. La descartaría por su complejidad y porque exige alojarla por cuenta propia.

**121** es gratuita y tiene el respaldo del IFRC. Su lógica de cruce, sin embargo, es frágil [P1]. Ampliar su producto es técnicamente sencillo; lo limitan la capacidad de su equipo y su foco en el Movimiento de la Cruz Roja.

En los tres casos la conciliación es parte central del producto, y poco les impediría añadir capacidades nuevas.

### 5.2 Competidores que ya tienen el canal de pago: FSP y agregadores

Los FSP vienen incluidos en la comisión y son una ventanilla única, así que su reemplazo cuesta poco. Su límite es estructural:
- su incentivo comercial es su propio volumen;
- no tienen la lista ni los criterios de elegibilidad de la organización;
- la protección de datos restringe que los reciban.

Por eso no se espera que concilien entre varios FSP. Los agregadores como Onafriq o Thunes ya unen varios canales y podrían ampliar sus reportes. Son una amenaza media.

### 5.3 Competidores que ya tienen el cierre financiero: el ERP

El ERP ya existe y es el libro oficial, de modo que reemplazarlo es muy difícil. Pero su modelo de datos es contable, los datos personales viven fuera y el segmento ONG es un nicho para los grandes proveedores. Es improbable que lo cubra sin desarrollo a medida. La amenaza es baja.

### 5.4 El sustituto dominante: Excel y personal

Excel y el personal dedicado no cuestan dinero y sí costumbre. Fallan por errores, falta de trazabilidad y rotación. Son el competidor que más se repite en las fuentes, porque es lo que hoy se paga.

### 5.5 La amenaza futura: OpenFn con un integrador

OpenFn tiene la legitimidad de un bien público digital, es barato y se puede autoalojar. Exige un integrador y no trae lógica de dominio. Aun así, es la vía más rápida para que un tercero replique la conciliación a medida para un cliente concreto.

### 5.6 Las agencias de la ONU y las herramientas genéricas

**ONU.** SCOPE, DARTs y CashAssist no están a la venta, pero retiran a las agencias de la ONU como compradoras: concilian con sus propias herramientas.

**Herramientas genéricas.** BlackLine y Simetrik son robustas y técnicamente podrían cubrir el problema. Comercialmente es improbable: son caras, no tienen contexto humanitario y el nicho es pequeño.

### 5.7 Síntesis comparativa

| Alternativa | Para quién | Conciliación core | Dificultad de reemplazo | ¿Puede cubrir el gap? |
|---|---|---|---|---|
| RedRose | INGO, IFRC | Sí (estado y comercios) | Alta | Técnicamente sí |
| 121 | Cruz Roja | Sí (binaria) | Media | Sí, con facilidad técnica |
| HOPE | UNICEF y socios, gobiernos | Sí | Alta en su ecosistema | Sí, ya avanza |
| SCOPE / DARTs / CashAssist | PMA / ACNUR | Sí | No está a la venta | Sí, para sí mismos |
| FSP / agregadores | Clientes del FSP | Secundaria | Baja | Poco incentivo para cubrir varios FSP |
| ERP | Finanzas | No | Alta | Improbable sin desarrollo a medida |
| Excel + personal | Todos | Sí | Baja en coste, alta en costumbre | No aplica |
| OpenFn + integrador | Organizaciones con capacidad técnica | No | Media | Sí, a medida |
| BlackLine / Simetrik | Corporativo, fintech | Sí | Alta | Técnicamente sí; comercialmente improbable |

---

## 6. El gap que realmente queda abierto

### 6.1 Lo que el gap no es

Antes de formular el gap conviene descartar tres lecturas fáciles:

- **No es que "falte conciliación".** Las plataformas CVA ya concilian el estado de cada persona.
- **No es que "falte interoperabilidad".** Las fuentes sectoriales describen la interoperabilidad como un problema "not primarily technical but systemic" [D16] y constatan que la hoja de cálculo enviada por correo sigue siendo la norma [D18]. La interoperabilidad es una causa, no el hueco.
- **No es que "falte un dashboard".** Casi todos los actores prometen visibilidad en tiempo real.

### 6.2 Lo que sí aparece

El gap aparece después del primer resultado. Formulado como actor, situación, limitación y consecuencia:

> *Los equipos de Finanzas y de Cash de INGO medianas y consorcios que pagan a través de dos o más FSP —con al menos uno sin integración por API, como un banco, una remesadora o el pago por ventanilla— **no pueden** cruzar, persona por persona y ciclo por ciclo, la lista aprobada con los reportes heterogéneos de cada FSP. Tampoco pueden dar seguimiento a las excepciones (fallidos, no cobrados, vencidos, reintegros, comisiones) hasta su cierre, ni liquidar el anticipo contra lo realmente pagado. Hoy lo resuelven con Excel y personal dedicado, o con plataformas que solo devuelven éxito o error. **En consecuencia**, detectan tarde los duplicados y los no cobrados, cierran ciclos con semanas o meses de retraso y llegan a auditoría con diferencias sin explicar.*

En concreto, el hueco está en cuatro puntos:
1. la gestión de excepciones después del primer resultado;
2. la normalización entre varios FSP;
3. la liquidación financiera del anticipo y las comisiones;
4. la coordinación entre Programa, que decide reintentar o recolocar, y Finanzas, que reintegra y cierra.

### 6.3 Nivel de confianza

El gap está **inferido**: se deduce de que no hay documentación pública que lo cubra. No está demostrado. Hay dos razones para la cautela:
- RedRose o HOPE podrían cubrirlo sin publicarlo.
- La severidad documentada procede de la ONU, que construye sus propias herramientas (DARTs, DHOTS).

Por eso el gap debe validarse con usuarios antes de considerarse firme.

---

## 7. ¿Existe una oportunidad de negocio?

### 7.1 Problema real frente a mercado comprable

El problema está documentado. Lo que no está claro es la **unidad de compra**.

**Lo que sí se observa (interés o problema mencionado):**
- auditorías con plazos [E8, E9];
- un discurso sectorial sobre interoperabilidad [D16, D17];
- promesas comerciales de OpenFn, RedRose y Onafriq [I2, R3, F10].

**El comportamiento real de compra es distinto. La conciliación se compra dentro de un contrato mayor o se resuelve con desarrollo interno:**
- **Dentro de plataformas.** La licitación de Solidarités (2026) es la única que menciona expresamente la conciliación, y la incluye en una plataforma integral: "Comprehensive reporting and reconciliation capabilities" [D1]. Relief International (2026) y Diakonie (2024) también licitaron plataformas. La primera no pudo leerse; la segunda buscaba "one single solution" de gestión de datos y entrega [D2, CVA-T06].
- **Dentro de contratos con FSP.**
  - UNICEF Bangladesh exige al FSP un informe de conciliación mensual en 10 días hábiles [D5].
  - ACNUR Europa fija un formato de datos de pago [D6].
  - Prosper Global (2025), Plan (2025) y CRS (2024) contratan FSP con dashboard o con gestión de datos [CVA-T02, D4, CVA-T13].
  - En el registro de licitaciones IAPG aparecen 14 avisos entre 2024 y 2026: 2 de plataforma y el resto de FSP, entre ellos un contrato de e-card de DRC en Turquía por 3.262.500 EUR. Ninguno compra la conciliación por separado [D7].
- **Desarrollo interno.** DARTs, DHOTS, HOPE y la decisión del PMA en Zambia de automatizar la conciliación antes de junio de 2026 [P15, E8, P8, E9].
- **Personal.** Las vacantes con funciones de conciliación son el gasto más visible [D8–D12].
- **Alianzas de pago.** RedRose–MoneyGram, 121–Intersolve/Africa's Talking, HOPE–Western Union/MoneyGram y ESTHER–Visa [R9, P2, P8, P16].

En América Latina no se pudieron verificar vacantes de 2025–2026 con conciliación explícita. Es un hueco de la búsqueda, no prueba de que no existan.

**La tensión central.** Hay dolor, pero no se observa ninguna compra de conciliación como producto o servicio separado.

### 7.2 Por qué una organización compraría, construiría o seguiría igual

Esa tensión se entiende mejor al ver las opciones de cada organización:

- **Comprar** tendría sentido ante hallazgos de auditoría con plazo, varios FSP, poco personal tras los recortes y exigencias de trazabilidad de los donantes [D1, E8, E9].
- **Construir** es lo que hacen las agencias de la ONU, que tienen escala, presupuesto central e interés en controlar sus datos [P15, E8, P8].
- **Seguir con Excel** es la opción por defecto: no cuesta nada, es flexible y responde a la idea de "ya sabemos hacerlo" [D8, E6].
- **Contratar consultores** serviría para problemas puntuales o revisiones de procesos, pero no se encontraron términos de referencia específicos.
- **Pedírselo al FSP** permite pagarlo dentro de la comisión y tener una sola ventanilla [D4, D5, D6].

La tendencia observada en las INGO es pedírselo al FSP o a la plataforma dentro de un contrato mayor y cubrir el resto con Excel. Comprar algo aparte solo tiene sentido si cubre lo que ni el FSP ni la plataforma resuelven, sobre todo cuando hay varios FSP (inferencia).

### 7.3 Quién podría comprar

| Segmento | Tiene el problema | Decide / compra | Financia | Alternativa actual | Probabilidad de compra |
|---|---|---|---|---|---|
| Agencias de la ONU | Finanzas y CBT de país | Sede, con soluciones "corporate-approved" [E9] | Recursos propios | DARTs, DHOTS, HOPE, SCOPE | No plausible: construyen |
| INGO grandes | Finanzas de país y Cash | Responsable global de Cash con Finanzas; compra Procurement global con acuerdos marco | Donantes, como coste directo o dentro de la comisión del FSP | RedRose, plataforma propia, FSP, Excel | Media, pero compran en paquete [D4, CVA-T02] |
| INGO medianas y consorcios | Finanzas de país y oficiales de CVA, a menudo en roles mixtos | Director de país o coordinador del consorcio con Finanzas; compra Procurement mediante licitación de plataforma | Coste directo de proyecto (ECHO admite IT de proyecto, con costes indirectos limitados al 7 %) [CVA-M18, CVA-M21] | Excel, portales de FSP, a veces RedRose | La mayor de los segmentos analizados [D1, D2, CVA-T06] |
| ONG nacionales | Finanzas, con personal mínimo | Dirección, por proyecto | Donante o intermediario, con presupuestos muy limitados [CVA-L11] | Excel o la herramienta que impone el intermediario | Baja como compradoras directas |
| Gobiernos y protección social | Ministerio y pagador | Ministerio, por licitación pública | Banca de desarrollo (Banco Mundial, BID) | Integradores y bienes públicos digitales | Fuera del perfil B2B inicial, aunque la Contraloría de Colombia muestra que el problema existe [F14] |

**Por qué las INGO medianas y los consorcios son el comprador más plausible.** Por exclusión:
- Las agencias de la ONU construyen sus propias herramientas.
- Las INGO grandes prefieren paquetes con el FSP o con su plataforma.
- Las ONG nacionales no tienen presupuesto propio.
- Los gobiernos son otro tipo de mercado.

Queda un segmento que concilia en Excel, que suele trabajar con varios FSP y que ya licita plataformas como coste de proyecto. No se mencionan precios ni montos porque no hay datos públicos sobre la parte de conciliación.

---

## 8. Cómo podría entrarse al mercado

### 8.1 Las barreras

Cualquier vía de entrada se enfrenta a barreras de cuatro tipos.

**Técnicas:**
- acceso a los datos y a las API de cada FSP, país por país, condicionado por "the maturity of the banking systems" [E8, R1];
- formatos heterogéneos y con identificadores propios [F1, F4, P1];
- integración con el ERP (Unit4, SAP, Oracle) [E1–E4];
- calidad del registro aguas arriba, la causa raíz identificada como OP2 [E8, CVA-A04].

**Comerciales:**
- compras en paquete con el FSP o la plataforma, mediante acuerdos marco de uno a tres años [D1, D4, D7];
- ciclos de venta largos y atados a proyectos y donantes [CVA-F01, CVA-F02];
- necesidad de un historial: los incumbentes tienen acuerdos marco [R4];
- alternativas gratuitas como HOPE, 121, Building Blocks u OpenFn [P3, P6, P11, I1];
- costes de cambio ligados al ecosistema RedRose o a los hábitos de Excel [R6, R7];
- contracción del sector, con menos compradores y menos personal [CVA-M12, CVA-M01].

**Regulatorias:**
- protección de datos personales: un nuevo proveedor es un tercero más con datos sensibles, como mostró el caso del CICR en 2022 [CVA-X10, CVA-X09];
- KYC/AML y sanciones, de forma indirecta a través del FSP [CVA-F07];
- leyes nacionales de datos en Ecuador, México o Colombia [CVA-X14, CVA-X15].

**Organizacionales:**
- reparto distinto de roles entre Programa y Finanzas en cada organización [D14, D15];
- implementación, soporte y rotación de personal, señalados como cuellos de botella en RedRose y 121 [R1].

### 8.2 Las vías posibles

**Producto independiente de conciliación.** Su atractivo es el foco: serviría a usuarios de cualquier plataforma o de Excel. Pero choca con un dato central de este análisis: hoy nadie compra la conciliación por separado. Exigiría integrarse con FSP y ERP desde el inicio y vender a procurement de INGO, que tiende a comprar en paquete. Su diferenciación sería media (el flujo de excepciones), su velocidad baja y su riesgo alto, aunque no dependería de terceros.

**Módulo complementario de plataformas CVA.** Llegaría donde ya están los datos y se sumaría sin reemplazar nada. Atendería a usuarios de RedRose, 121 o HOPE. Su punto débil es la dependencia: cada plataforma controla el acceso a sus API y podría absorber la funcionalidad. Velocidad y riesgo medios; dependencia alta.

**Middleware entre plataforma, FSP y ERP.** Atacaría justo el tramo menos cubierto: varios FSP y el puente al ERP. Es la vía más técnica. Compite con OpenFn y con integradores, y obliga a construir integraciones país por país. Su diferenciación podría ser media-alta si acumula formatos de FSP, pero su entrada es lenta y su coste de integración elevado. La dependencia de los FSP es media.

**Conciliación como servicio.** Un equipo propio que usa tecnología propia. Encaja con lo que hoy se paga, que es personal, cabe como coste de proyecto y permite aprender el flujo real. Es la vía más rápida y la que menos depende de terceros. Sus límites son el margen y la escalabilidad bajos, el riesgo de quedarse en consultoría y el reto de confianza de manejar datos personales como tercero. Exige un comprador con poder de decisión local: el director de país o el coordinador del consorcio.

**Alianza con una plataforma (RedRose, Humansis u otra).** Daría distribución y legitimidad inmediatas. Pero el socio decidiría, la diferenciación quedaría en manos de otro y el riesgo de ser absorbido sería alto. La dependencia sería muy alta.

**Entrada a través de un FSP o agregador.** Aprovecharía que el FSP ya está en el contrato. El problema es de incentivos: el FSP no tiene interés en cubrir a otros FSP, y el precio quedaría ligado a la comisión. Diferenciación baja, riesgo alto y dependencia muy alta.

### 8.3 Síntesis

Las vías de servicio y de middleware responden mejor al gap formulado: varios FSP, excepciones, anticipo y ERP. Además, la conciliación como servicio aprovecha el patrón de gasto actual. Las alianzas y la entrada vía FSP dan velocidad, pero ceden el control. El producto independiente es la vía más expuesta, porque no hay demanda observada de conciliación aislada.

**La combinación más plausible es una inferencia:** empezar por servicio y aprendizaje, con la ambición de evolucionar hacia una capa entre plataforma, FSP y ERP, y usar las alianzas para distribuir, no para depender. La elección final depende de la evidencia primaria descrita en la sección 11.

---

## 9. Beachhead y wedge

### 9.1 El segmento de entrada (beachhead)

El perfil de entrada se define así:

> *INGO medianas y consorcios de cash que ejecutan efectivo multipropósito recurrente (ciclos mensuales o periódicos) en uno a tres países, pagan a través de dos o más FSP —al menos uno sin integración por API, como un banco, una remesadora o el pago por ventanilla— y concilian hoy con Excel y personal dedicado, sin plataforma CVA corporativa o con una que solo devuelve éxito o error.*

**Por qué este perfil:**
- **Dolor.** Sus organizaciones viven justo el tramo menos cubierto: excepciones, varios FSP y anticipo [E6, F15, F16]. La confianza es media-baja porque la severidad está documentada sobre todo en la ONU.
- **Frecuencia.** El problema se repite en cada ciclo de pago [D14, D15].
- **Capacidad de pago.** Pueden financiarlo como coste directo de proyecto o del consorcio, y ya licitan plataformas [D1, CVA-T06]. Confianza baja-media.
- **Acceso.** Los consorcios publican sus aprendizajes y las vacantes son públicas. VenEsperanza, en Colombia, trabaja con tres FSP, cobro por ventanilla en Efecty, informe mensual del banco y una plantilla común de incidencias [F18, D12].
- **Competencia.** El segmento está menos ocupado que el de la ONU o el de los usuarios de RedRose; aquí el rival real es Excel.
- **Urgencia.** La empujan los recortes de personal y las exigencias de donantes y auditores [CVA-M12]. Confianza media-baja.
- **Replicabilidad.** El patrón de varios FSP con formatos distintos se repite entre países, y una biblioteca de formatos podría acumularse con el uso (inferencia, confianza baja).

**Geografía.** No se selecciona ningún país. Colombia y la región andina ofrecen señales útiles para el research primario: varios FSP, cobro por ventanilla, giros que vencen y se recolocan [F13, F18]. Al mismo tiempo, su financiación es muy baja: el plan de respuesta regional RMRP 2026 está financiado al 8,1 % [CVA-M09].

### 9.2 El punto de entrada (wedge)

> *Al cerrar cada ciclo de pago, el oficial de Finanzas o de Cash de una INGO mediana recibe los reportes de resultado de cada FSP. En ese momento necesita saber, en horas y no en semanas, qué personas cobraron, cuáles fallaron o no cobraron y qué importe debe reintentarse, reintegrarse o liquidarse del anticipo, para cerrar el ciclo y decidir con Programa qué hacer con cada excepción.*

**Por qué este momento y no todo el ciclo CVA:**
- evita competir con las plataformas que ya cubren el registro y el envío (RedRose, 121, HOPE);
- se concentra en el tramo con menor cobertura;
- tiene resultados observables: días hasta el cierre, excepciones abiertas y anticipo pendiente;
- sirve tanto a quien usa una plataforma como a quien usa Excel, lo que amplía el mercado posible;
- no obliga a cambiar cómo se registra ni cómo se paga.

**Su riesgo:** si el FSP o la plataforma ya entregan esta información a la mayoría del segmento, el wedge desaparece.

---

## 10. Qué podría ser defendible

El análisis de copia es poco favorable para cualquier propuesta basada en funcionalidades. Matching, dashboards, alertas, APIs, reglas configurables, normalización e importación de CSV son fáciles de copiar.

**Quién podría copiar y qué le frenaría:**
- **RedRose:** casi nada técnico se lo impide, porque ya tiene los datos de pago y de canje. Le frenan su foco en el ciclo completo y una capacidad limitada.
- **HOPE:** puede hacerlo gratis en su ecosistema y ya avanza en esa dirección.
- **121:** podría ampliar su producto con facilidad técnica.
- **Humansis:** su mantenimiento es bajo, así que la amenaza también lo es.
- **OpenFn:** puede replicar un flujo por cliente, no un producto, porque le falta la lógica de dominio.
- **Los FSP:** no tienen incentivo para cubrir a otros FSP.
- **Los agregadores:** ya unen canales y podrían ampliar sus reportes.
- **El ERP:** su modelo de datos es contable y el segmento ONG es un nicho.
- **Los equipos internos:** son una amenaza alta en la ONU y baja en las INGO medianas.

Si la propuesta de NexoAid fuera una funcionalidad, la respuesta honesta sería que muy poco impediría que otros la añadieran.

**Distintos tipos de ventaja, ordenados por solidez:**

- **Workflow difícil de replicar.** Un ciclo completo de excepciones, con decisiones compartidas entre Programa y Finanzas y cierre del anticipo. Requiere conocer los procedimientos operativos estándar (SOP) del CICR e IFRC y los contratos con FSP. Es moderadamente defendible.
- **Integración.** Una biblioteca de formatos de FSP por país (bancos, remesadoras, ventanilla en América Latina y África) se acumula y cuesta replicar. OpenFn, sin embargo, compite en este terreno.
- **Datos.** Es una ventaja débil: los datos pertenecen a cada cliente y la protección de datos limita reutilizarlos.
- **Conocimiento del sector.** Es real, pero se puede copiar contratando personas.
- **Implementación ligera.** Podría ser la ventaja más fuerte al inicio, porque la implementación es el cuello de botella documentado de los incumbentes [R1, P2].
- **Alianzas.** Pueden acelerar la entrada, pero generan dependencia.

**Hipótesis de defensibilidad.** Ninguna funcionalidad aislada es defendible. Lo que podría defenderse es la combinación de cinco elementos: un flujo de excepciones bien resuelto, conocimiento operativo del sector, una biblioteca de formatos de FSP que crece con el uso, una implementación ligera y la coordinación entre Programa y Finanzas. Esto es una hipótesis, no un hecho probado.

---

## 11. Riesgos que pueden invalidar la oportunidad

La oportunidad no está validada. Hay seis hallazgos que, si el research primario los confirmara, harían recomendable abandonarla o cambiar de vía.

1. **Un solo FSP por país.** Si la mayoría del segmento trabaja con un único FSP, o si el portal o la plataforma del FSP le basta, el problema de normalizar y cruzar entre varios proveedores pierde peso.
2. **Esfuerzo bajo.** Si conciliar y gestionar excepciones lleva horas y no días por ciclo, el dolor no justifica una compra.
3. **Cobertura no publicada.** Si RedRose, 121 o HOPE ya cubren excepciones y anticipo aunque no lo documenten, el gap desaparece para sus usuarios.
4. **Sin compra separada.** Si procurement solo pagaría la conciliación dentro del contrato del FSP o de la plataforma, el problema puede investigarse pero no monetizarse por separado.
5. **Integraciones caras.** Si acceder a los datos de cada FSP exige integraciones a medida, país por país, sin que nadie las pague, el modelo no se sostiene.
6. **Recortes.** Si la contracción del sector elimina el presupuesto de proyecto para herramientas, desaparece el comprador.

**Evidencia primaria necesaria antes de avanzar:**
- **Del segmento de entrada:** número de FSP por país, proporción de FSP sin API, días-persona dedicados por ciclo, tipos y volumen de excepciones, tiempo hasta el cierre y anticipos abiertos.
- **De los usuarios de RedRose, 121 o HOPE:** qué parte de la conciliación hacen fuera de la plataforma.
- **De procurement y de la dirección de país o del consorcio:** cómo se compraría, con qué línea presupuestaria y si comprarían algo fuera del contrato del FSP.
- **De dos o tres FSP (un banco, una remesadora y un operador de dinero móvil):** qué entregan y en qué formato.

---

## 12. Conclusión gerencial

La conciliación en CVA es un problema real, recurrente y cuantificado. Las auditorías de ACNUR y del PMA documentan diferencias de decenas de millones entre los sistemas de programa y la contabilidad, millones en fondos no cobrados y en comisiones sin registrar, duplicados y cierres aprobados meses después del pago. Esos hallazgos muestran que el problema no está en enviar el pago, sino en todo lo que ocurre después: saber quién recibió, qué falló, qué debe reintentarse o reintegrarse, cuánto queda del anticipo y qué debe registrar Finanzas. La conciliación es, en la práctica, un workflow de cierre y de resolución de excepciones.

Ese workflow no está vacío de soluciones. Las plataformas CVA, con RedRose, HOPE y 121 a la cabeza, resuelven bien el estado de pago de cada persona. Los FSP informan sobre su propio canal y el ERP recibe el cierre contable. Las agencias de la ONU han construido herramientas propias, como DARTs y DHOTS. Lo que ninguna de estas piezas documenta es el tramo que las une: las excepciones con ciclo de vida, varios FSP con formatos distintos, la liquidación del anticipo, las comisiones y el puente hacia el ERP. Hoy ese tramo se cubre con Excel y personal dedicado, el competidor más extendido y también el gasto más visible del sector.

En ese contexto, RedRose es un incumbente adyacente más que un rival directo. Es fuerte dentro de sus clientes gracias a su ecosistema, su acuerdo marco con el IFRC y su experiencia offline. Pero no hay evidencia pública de que cubra el tramo posterior al primer resultado, y su modelo de precio proporcional al desembolso, con costes poco claros, deja margen para propuestas complementarias. Competir con RedRose como plataforma completa sería una mala apuesta. Ser útil también a sus usuarios podría convertirla en socio o canal. La amenaza a medio plazo procede de OpenFn con un integrador y de las propias plataformas, que tienen los datos y pocas barreras técnicas para ampliar su oferta.

La gran incógnita es comercial, no técnica. No se ha observado ninguna compra de conciliación como producto o servicio separado. Las organizaciones la compran dentro de un contrato de plataforma o de FSP, la construyen si son agencias de la ONU o la pagan con personal. El comprador más plausible son las INGO medianas y los consorcios con varios FSP y conciliación en Excel, porque ya licitan plataformas como coste de proyecto y no tienen herramientas corporativas. Aun así, su capacidad y su disposición de pago siguen sin demostrarse, y la contracción del sector reduce su margen.

Por eso la entrada más razonable es prudente: empezar por un servicio que permita aprender el flujo real en el momento del cierre de cada ciclo, con la ambición de convertirse después en una capa entre plataforma, FSP y ERP, y usar las alianzas para distribuir sin depender de ellas. El segmento de entrada serían las INGO medianas y los consorcios con efectivo multipropósito recurrente, dos o más FSP y al menos uno sin API. El punto de entrada sería el momento inmediatamente posterior al resultado del pago. Esta combinación evita competir de frente con las plataformas y se concentra donde la cobertura es más baja.

Lo que puede invalidar esta lectura está identificado: un solo FSP por país, un esfuerzo de horas y no de días, plataformas que ya cubren el tramo sin publicarlo, compradores que solo pagan dentro del contrato del FSP, integraciones demasiado caras o presupuestos que desaparecen con los recortes. Cualquiera de esos hallazgos en el research primario cambiaría la decisión.

**Recomendación: ENTRAR SOLO BAJO DETERMINADAS CONDICIONES.**

El problema parece real y poco resuelto en el tramo posterior al pago. Pero la oportunidad comercial depende de demostrar que existe un comprador dispuesto a pagar por resolverlo fuera del contrato actual del FSP o de la plataforma.

La entrada sería plausible si el research primario confirma tres cosas:
1. que el segmento de entrada trabaja habitualmente con dos o más FSP por país, al menos uno sin API;
2. que la conciliación y las excepciones le cuestan varios días por ciclo, con anticipos o no cobrados sin cerrar;
3. que existe un responsable de presupuesto dispuesto a financiarlo como coste de proyecto o de consorcio.

Hacen falta también otras dos condiciones:
- que las plataformas que ya usan no cubran ese tramo;
- que los datos de los FSP se puedan obtener por archivo, sin integraciones a medida en cada país.

Si falla la condición del comprador, el problema seguirá siendo valioso para investigar, pero no monetizable por separado. En ese caso, la vía pasaría a ser una alianza o un rol de proveedor dentro de una plataforma existente.

---

## 13. Límites del documento

- No define MVP, roadmap, arquitectura, precios ni tamaño de mercado.
- El gap se infiere de la ausencia de documentación pública, y puede existir cobertura no publicada.
- No se pudieron leer cinco fuentes: la licitación de Relief International, el código de HOPE, las cuentas de RedRose, el documento CALP/CGAP sobre stablecoins (sep-2026) y la auditoría del PMA en Colombia (AR-26-05).
- Varias afirmaciones de proveedores son comerciales: Onafriq, M-Pesa, OpenFn, RedRose e IntaSend.
- No se proponen cambios a los tres research validados. Los hallazgos son coherentes con ellos y precisan OP3, por lo que no se activa WORKFLOW §3.1.

---

## 14. Fuentes


Consultadas el 2026-10-07. Las referencias `[CVA-xx]` remiten a las fuentes de `cva-market-opportunities.md`.

**Tipos:** T = técnica, I = institucional, A = auditoría, L = procurement/licitación, V = vacante, P = prensa, C = **COMERCIAL**.

### R. RedRose

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | Limitación |
|---|---|---|---|---|---|---|---|
| R1 | Archivo de pago y de retorno; conciliación en RedRose; Ruanda con integración completa; formación; costes poco claros | IFRC | Red Rose Learning Review | 2022-12-15 | https://cash-hub.org/wp-content/uploads/sites/3/2023/06/IFRC-Red-Rose-Learning-Review.pdf | A | 5 pilotos pequeños |
| R2 | Pricing en % del desembolso; conciliación diaria (Filipinas); M-Pesa en tiempo real; offline | IFRC | Learning Review RedRose Pilots 2018 | 2018 | https://cash-hub.org/wp-content/uploads/sites/3/2020/10/Learning-Review-RedRose-Cash-Data-Management-Pilots-2018.pdf | A | Tono favorable |
| R3 | "Automated reconciliation"; pago por uso | IFRC Cash Hub | RedRose Introduction | s.f. | https://cash-hub.org/resources/redrose/redrose-introduction/ | I (reproduce al proveedor) | — |
| R4 | 11 agencias, más de 50 países, rentable; "manages all of the transactional flows, reconciliations and audit logs" | CALP | RedRose Special Session notes | 2024-02-13 | https://www.calpnetwork.org/wp-content/uploads/2024/02/RedRose-Special-Session-notes-13th-February-2024.pdf | C | Autodeclarado |
| R5 | 4 % de fee; reembolso semanal a comercios; verificación del 30 % | Relief International / CALP | E-Transfers… N. Syria | 2016 | https://www.calpnetwork.org/wp-content/uploads/2020/01/relief-internationale-transfers-for-hygiene-through-red-rose-in-syria-2.pdf | I | Un proyecto |
| R6 | Recibos en papel; fallos de sincronización | CRS | E-vouchers in conflict situations, Nigeria | 2016–17 | https://www.crs.org/sites/default/files/tools-research/e-vouchers_in_conflict_situations_crs_nigeria_case_study_0.pdf | I | Antiguo |
| R7 | CAT sobre OneSystem; auditoría de usuarios; alertas | CRS | CAT brochure | 2018-09-26 | https://www.crs.org/sites/default/files/crs_cat_brochure_20180926.pdf | I / C | Folleto |
| R8 | Datos registrales de Red Rose CPS Ltd | Companies House | Ficha 09415212 | consultada 2026-10-07 | https://find-and-update.company-information.service.gov.uk/company/09415212 | I | PDF de cuentas no leído |
| R9 | RedRose–MoneyGram: más de 350 M USD | MoneyGram | Blog | s.f. | https://blog.moneygram.com/world-humanitarian-day.html | C | Sin fecha |
| R10 | Vulnerabilidad de seguridad en 2017 | Devex vía ALNAP | Nota | 2017-11-28 | https://alnap.org/help-library/resources/new-security-concerns-raised-for-redrose-digital-payment-systems/ | P | Antigua |

### P. Otras plataformas

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | Limitación |
|---|---|---|---|---|---|---|---|
| P1 | Excel FSP: CSV éxito/error, `columnToMatch`, 10.000 filas, duplicados sobrescritos | 121 | Wiki "Excel payment instructions FSP" | s.f. | https://github-wiki-see.page/m/global-121/121-platform/wiki/Excel-payment-instructions-FSP | T | Espejo de la wiki |
| P2 | Callbacks de error y reintento; involucrar a Finanzas | NLRC / IFRC Cash Hub | Next Level Integration with FSPs | 2021-12 | https://cash-hub.org/wp-content/uploads/sites/3/2021/12/Next-Level-Integration-with-Financial-Service-Providers-in-Kenya-and-The-Netherlands.pdf | T | Piloto de 350 hogares |
| P3 | Licencia Apache 2.0; lista de FSP | 121 | Repositorio en GitHub | 2026 | https://github.com/global-121/121-platform | T | Que aparezca un FSP no implica que esté en producción |
| P4 | Rechazos de 100–150 a 5 | 121 / IFRC | 121 SA case study | 2024-09 | https://cash-hub.org/wp-content/uploads/sites/3/2024/09/121-SA-case-study-design.pdf | I | Autoinforme |
| P5 | Rol de Reconciler; SFTP/API | UNICEF | HOPE 1.0 Introduction | s.f. | https://www.unicef.org/hope-hct/10-introduction | T | Alto nivel |
| P6 | Conciliación individual para liquidar el anticipo; AGPL | UNICEF | Repositorio unicef/hct-mis | 2026 | https://github.com/unicef/hct-mis | T | Código no leído |
| P7 | Verificación de pagos por muestreo | UNICEF | Payment Verification | s.f. | https://www.unicef.org/hope-hct/payment-verification | I | — |
| P8 | WU/MoneyGram; automatización de la conciliación; SAP VISION; 228 M USD | UNICEF | HOPE Annual Report 2025 | 2026 | https://www.unicef.org/hope-hct/reports/hope-annual-report-2025 | I | Autoinforme |
| P9 | Controles de SCOPE desactivables; integración con WINGS | Inspector General del PMA | AR/21/08 SCOPE | 2021-05 | https://docs.wfp.org/api/documents/WFP-0000128891/download | A | 2021 |
| P10 | IDs duplicados en conciliación de dinero móvil; tripartita incumplida | Inspector General del PMA | AR/21/06 Burkina Faso | 2021-04 | https://docs.wfp.org/api/documents/WFP-0000128117/download | A | Una operación |
| P11 | Building Blocks: 30 organizaciones, gratuito | PMA | Building Blocks | s.f. | https://www.wfp.org/building-blocks | I | Autoinforme |
| P12 | Jordania: conciliación de comercios sin bancos | VMware | Blog | ~2018 | https://blogs.vmware.com/tanzu/can-blockchain-help-feed-the-hungry/ | C | Proveedor |
| P13 | Humansis: repositorios GPL, actividad hasta 2023 | People in Need | GitHub / web | 2023–25 | https://github.com/humansis | T / C | Sin documentación de conciliación |
| P14 | Aidonic: offline, clientes | research.swiss | Perfil | s.f. | https://research.swiss/aidonic/ | C | — |
| P15 | DARTs: 14 países, 3.000 h ahorradas | PMA | Innovation | 2025 | https://innovation.wfp.org/node/494 | I | Cifra inconsistente |
| P16 | ESTHER–Visa: pilotos | BusinessWire | Nota | 2025-02-04 | https://www.businesswire.com/news/home/20250204746940/en/ESTHER-International-and-Visa-to-collaborate-on-payments-solutions-for-humanitarian-aid | C | — |

### F. Proveedores financieros

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | Limitación |
|---|---|---|---|---|---|---|---|
| F1 | B2C asíncrono; "no automatic retries" de callbacks | Safaricom Daraja (copia) | AccountBalance docs | s.f. | https://glama.ai/mcp/servers/@JacksCodeVault/mpesa-daraja-mcp/blob/e875f3b350a0119c928c623c4e0cdd8999a5d329/daraja_docs_v3/docs/AccountBalance.md | T | Copia no oficial |
| F2 | Portal masivo de 20.000 filas; "real-time automated reconciliation" | Safaricom | M-PESA Bulk Payment B2C | s.f. | https://www.safaricom.co.ke/images/Downloads/M-PESA-bulk-payment-b2c.pdf | C | Folleto |
| F3 | Pagos parciales "failed"; reversos manuales | Safaricom | FAQ B2C | s.f. | https://safaricom.co.ke/media-center-landing/frequently-asked-questions/m-pesa-bulk-payment-b2c | C | — |
| F4 | "Do not rely solely on callbacks"; "reconciliation daily" | MTN | MoMo Open API Best Practices (Ruanda) | s.f. | https://momoapi.mtn.co.rw/content/html_widgets/rxugb.html | T | Un solo país |
| F5 | Listas en Excel cargadas al portal masivo | GSMA | Mobile Money CVA Operational Handbook | 2019-04 | https://www.gsma.com/mobilefordevelopment/wp-content/uploads/2019/04/Mobile_Money_CVA_Operational-Handbook.pdf | I | Antiguo |
| F6 | Webhooks por transferencia con 4 estados | Flutterwave | Bulk transfers docs | actual | https://developer.flutterwave.com/docs/making-payments/transfers/bulk-transfers | T | — |
| F7 | 7 estados de pago | dLocal | Payout status | actual | https://docs.dlocal.com/reference/payout-status-v3 | T | — |
| F8 | "You're responsible for reconciling" | Stripe | Payouts reconciliation | actual | https://docs.stripe.com/payouts/reconciliation | T | No humanitario |
| F9 | 95 % de transacciones en 30 segundos | CaLP / Thunes | Notas de sesión especial | 2024-04-24 | https://calpnetwork.org/wp-content/uploads/2024/05/Thunes-Special-Session-notes-24-April-2024-1.pdf | C | — |
| F10 | "Real-time reconciliation", "360 view" | Onafriq | Disbursements | actual | https://onafriq.com/services/disbursements | C | — |
| F11 | Pagos masivos para ONG con reportes para donantes | IntaSend | NGO payments | actual | https://intasend.com/products/intasend-ngo-payments | C | — |
| F12 | Informes acordados y portal seguro | Davivienda | Oferta a Colombia Compra Eficiente | 2023 | https://www.colombiacompra.gov.co/sites/cce_public/files/documentos_adicionales_oc/oferta_davivienda_jea._evento_144209_2023.pdf | C (licitación pública) | Programa de gobierno |
| F13 | Giros que vencen a los 30 días; recolocación | Unidad para las Víctimas | ABC pagos Efecty | ~2021 | https://www.unidadvictimas.gov.co/wp-content/uploads/2021/07/abcpagosefecty.pdf | I | Gobierno |
| F14 | "Dificultades para conciliar"; 21.907 reintegrados | Asuntos Legales (Contraloría) | Nota | 2026-09-14 | https://www.asuntoslegales.com.co/actualidad/fallas-en-ayudas-humanitarias-para-victimas-llegan-a-revision-de-la-contraloria-4481181 | P | Gobierno; nota periodística |
| F15 | FSP sin reportes durante 6 meses (800.000 USD) | Inspector General del PMA | AR/21/13 Nigeria | 2021-07 | https://docs.wfp.org/api/documents/WFP-0000131312/download/ | A | 2021 |
| F16 | Comercios que reportan por email; 2 M USD sin conciliar | Inspector General del PMA | AR/21/14 Colombia | 2021-08 | https://docs.wfp.org/api/documents/WFP-0000131813/download/ | A | 2021 |
| F17 | "Determine reporting formats early" | Mercy Corps / ELAN | E-Transfer Implementation Guide | 2018-12 | https://mcdl.mercycorps.org/gsdl/docs/E-TransferGuideAllAnnexes.pdf | I | Prescriptivo |
| F18 | VenEsperanza: 3 FSP, Efecty, informe mensual, plantilla de incidencias | CaLP / VenEsperanza | Working with FSPs | 2023-10-23 | https://www.calpnetwork.org/wp-content/uploads/2023/10/VenEsperanza_Collaborating-with-FSPs_EN.pdf | I | Un consorcio |
| F19 | Conciliación diaria con acceso a la plataforma del FSP | Cash Hub | Webinar "Working with FSPs" | 2021-05-19 | https://cash-hub.org/wp-content/uploads/sites/3/2021/06/20210519_WebinarSummaryTakeaways_v2.pdf | I | Testimonios |
| F20 | Reversión masiva de no cobrados a petición escrita | Cash Hub / PRCS | Cash Case Study Pakistan | 2020-02 | https://cash-hub.org/wp-content/uploads/sites/3/2020/10/CashCaseStudy_Pakistan_Final-26Feb.pdf | I | Un caso |
| F21 | Lotes de hasta 1.000 pagos | Wise | Batch payments | actual | https://www.wise.com/help/articles/2663240/guide-to-batch-payments | C | — |

### E. ERP y sustitutos

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | Limitación |
|---|---|---|---|---|---|---|---|
| E1 | Conciliación del extracto frente a transacciones con reglas | Microsoft | Advanced bank reconciliation | actual | https://learn.microsoft.com/en-us/dynamics365/finance/cash-bank-management/advanced-bank-reconciliation-overview | T | Sin casos humanitarios |
| E2 | Cruce banco–libro mayor con reglas | Oracle NetSuite | Help | actual | https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_4842302228.html | T | — |
| E3 | ACNUR con Oracle Fusion Cloud desde 2023 | ACNUR / Junta de Auditores; UNGM | Key issues BoA; aviso | 2023–24 | https://www.unhcr.org/sites/default/files/2024-09/Advance-copu-key-issues-BOA-English.pdf | A | No trata la conciliación CVA |
| E4 | NRC usa Unit4 en 32 países | Unit4 | Caso de cliente | 2023–24 | https://www.unit4.com/our-customers/customer-overview-norwegian-refugee-council | C | No menciona CVA |
| E5 | Anticipos abiertos a FSP; 2,7 mil M USD vía FSP | Inspector General del PMA | AR-25-03 | 2025 | https://docs.wfp.org/api/documents/WFP-0000165178/download/ | A | Excluyó la conciliación |
| E6 | ~100.000 transacciones por ciclo en hojas de cálculo | Inspector General del PMA | AR/22/19 Palestina | 2022-12 | https://docs.wfp.org/api/documents/WFP-0000145990/download/ | A | — |
| E7 | 71 M USD sin conciliar; 3,6 M USD de tarjetas inactivas; comisión sobre no cobrado; 2,9 M USD de comisiones sin registrar; duplicado de 1,5 M USD | OIOS / ACNUR | 2023/043 | 2023-09-21 | https://oios.un.org/file/9971/download?token=USFilfBC | A | Emergencia |
| E8 | 5 de 7 operaciones manuales; pagos exitosos con importe cero; DHOTS con plazo a dic-2026 | OIOS / ACNUR | 2025/019 | 2025-06-27 | https://oios.un.org/system/files/confidential-files/Reports/2025_019_pd.pdf | A | Solo ACNUR |
| E9 | Conciliación manual sin integración con SCOPE; automatizar antes de jun-2026 | Inspector General del PMA | AR-25-18 Zambia | 2025-12 | https://docs.wfp.org/api/documents/WFP-0000171358/download/ | A | Compromiso, no ejecución |
| E10 | UiPath en el PMA para anticipos de viaje | UNICC | Nota | 2020-08 | https://www.unicc.org/news/2020/08/19/world-food-programme-puts-bots-to-work/ | I | No es CVA |
| E11 | BlackLine: mediana de 40.125 USD al año | Vendr | Marketplace | actual | https://www.vendr.com/marketplace/blackline | C (terceros) | Estimación |
| E12 | Xero: 27–97 USD al mes | Xero | Precios | actual | https://www.xero.com/us/pricing-plans/ | C | EE. UU. |
| E13 | Simetrik: más de 1.000 millones de transacciones al día | Forbes Colombia | Nota | 2025-01 | https://forbes.co/2025/01/20/negocios/simetrik-afirma-que-esta-conciliando-mas-de-1-000-millones-de-transacciones-diariamente/ | P | Sin clientes humanitarios |

### I. Integración

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | Limitación |
|---|---|---|---|---|---|---|---|
| I1 | Precios: 0 / 49 / 199 / 499 USD al mes | OpenFn | Pricing | 2026 | https://www.openfn.org/pricing | C | — |
| I2 | Promete "automatically reconcile records" | OpenFn | Payments | 2025–26 | https://openfn.org/payments | C | Sin casos |
| I3 | Clientes (UNICEF, IRC, Mercy Corps, NRC) | OpenFn | Customers | 2026 | https://www.openfn.org/customers | C | No indica el uso |
| I4 | Socios sin especialidad en cash | OpenFn | Partners | 2026 | https://www.openfn.org/partners | C | — |
| I5 | Modelo de venta por socios | OpenFn | Vacante | 2026-09-10 | https://apply.workable.com/openfn/jobs/view/B891AB4811.md | V | Inferencia |
| I6 | Adaptador M-Pesa | OpenFn | Foro | 2025-04-04 | https://community.openfn.org/t/new-m-pesa-adaptor-released/914 | T | — |
| I7 | Adaptador MTN MoMo | OpenFn | Foro | 2025-07-04 | https://community.openfn.org/t/new-mtn-momo-adaptor-released/1005 | T | — |
| I8 | Mojaloop en contextos frágiles | Mojaloop | Post | 2025-03-24 | https://mojaloop.io/digital-public-infrastructure-for-resilience-in-fragile-contexts/ | I | Sin despliegues |
| I9 | API de desembolso G2P con callbacks | CDPI | G2P Connect | s.f. | https://g2pconnect.cdpi.dev/protocol/interfaces/social-program-management/disbursement | T | Solo gobierno |
| I10 | Zapier: −15 % para nonprofits | Zapier | Ayuda | s.f. | https://help.zapier.com/hc/en-us/articles/8496197165581-Discounts-for-Zapier-plans | C | — |
| I11 | n8n desde 20 €/mes | toolradar | Blog | 2026 | https://toolradar.com/blog/n8n-pricing-2026 | C (terceros) | No oficial |
| I12 | OCHA: Power Apps para conciliar facturación entre agencias | OCHA | Vacante | 2024-10 | https://untalent.org/jobs/information-management | V | No es CVA |

### D. Demanda y procedimientos

| ID | Afirmación | Organización | Documento | Fecha | URL | Tipo | Limitación |
|---|---|---|---|---|---|---|---|
| D1 | Plataforma CVA multipaís con "reporting and reconciliation capabilities" | Solidarités / IAPG | CFT_PAR-SRV-CVA-001-26 | 2026-07 | https://iapg.org.uk/call-for-tender-service-provider-for-cash-and-voucher-assistance-cva-programming/ | L | Solo el anuncio |
| D2 | Plataforma digital de gestión CVA | Relief International | ITT IPU2026002 | 2026-02 | https://www.ri.org//content/uploads/2026/02/ITT-IPU2026002-Cash-and-voucher-digital-assistance-management-platform.docx | L | **No leído** |
| D3 | Acuerdo marco global de PSP/FSP, 31 misiones | DRC / IAPG | EOI-DKHQ-2025-001 | 2025-02 | https://iapg.org.uk/call-for-expressions-of-interest-partner-with-the-danish-refugee-council-to-deliver-global-cash-and-voucher-assistance-solutions/ | L | Briefing no leído |
| D4 | Acuerdo con FSP con "real-time monitoring and reporting" | Plan / IAPG | ITT FY25-0205 | 2025-06 | https://iapg.org.uk/itt-fy25-0205-global-financial-service-providers-2/ | L | — |
| D5 | El FSP entrega conciliación mensual en 10 días hábiles | UNICEF Bangladesh | UNGM 202453 | 2023-06 | https://www.ungm.org/Public/Notice/202453 | L | — |
| D6 | "CBI Payments Format and Data Dictionary" | ACNUR | UNGM 219904 | 2023-11 | https://www.ungm.org/Public/Notice/219904 | L | Anexos no leídos |
| D7 | 14 avisos (2 de plataforma); DRC Turquía 3.262.500 EUR | IAPG | Categoría "Cash Transfer Solution" | 2024–26 | https://iapg.org.uk/category/services-cash-transfer-solution/ | L | Resúmenes |
| D8 | Conciliación de listas frente a reportes de FSP y extractos; Excel avanzado | UNICEF Sudán | Vacante Finance Specialist (Cash Transfer) | 2026-04 | https://www.impactpool.org/jobs/1204324 | V | — |
| D9 | Cruce de listas de FSP con ActivityInfo | DRC Nigeria | Vacante IM Officer | 2026-09 | https://www.impactpool.org/jobs/1234351 | V | — |
| D10 | Conciliación mensual de CBT con el FSP | PMA Port Sudán | Vacante | 2024-08 | https://sudancareer.com/wfp/programme-associate-9/ | V | — |
| D11 | Conciliación mensual; cuentas inactivas | PMA Camerún | Vacante | fecha dudosa | https://ngojobsinafrica.com/job/programme-associate-cbt-reconciliations-yaounde-cameroon/ | V | Fecha incierta |
| D12 | Funciones de conciliación en vacantes de IFRC (Caracas, Colombia, Jamaica) | IFRC | Vacantes | 2026 | https://www.impactpool.org/jobs/1231477 ; https://www.impactpool.org/jobs/1232905 ; https://www.impactpool.org/jobs/1204467 | V | Una sola organización |
| D13 | No cobrados como prepago hasta su vencimiento; pasos | CICR | CTP SOPs v3 | 2018-01 | https://cash-hub.org/wp-content/uploads/sites/3/2020/08/ICRC-CTP-SOPs.pdf | T | Antiguo |
| D14 | Reparto de roles Finanzas / Programas / Logística | IFRC | Secretariat CBP SOPs | 2015 | https://cash-hub.org/wp-content/uploads/sites/3/2020/08/IFRC-Secretariat-Cash-Based-Programming-Standard-Operating-Procedures.pdf | T | Antiguo |
| D15 | Flujo del proceso CVA | IFRC África | CVA Process Flow | 2021 | https://cash-hub.org/wp-content/uploads/sites/3/2022/02/CVA_Process_Flow_2021_EN_FV.pdf | T | Sin plazos |
| D16 | "Interoperability challenges are not primarily technical but systemic" | CALP | ECHO Cash Consortia Learning Event | 2026-05 | https://www.calpnetwork.org/wp-content/uploads/2026/06/ECHO-Cash-Consortia-Learning-Event-Lessons-from-South-Sudan-and-Yemen-2026.pdf | I | — |
| D17 | Principios de interoperabilidad | Donor Cash Forum / CALP | Declaración | 2022-09 | https://www.calpnetwork.org/publication/donor-cash-forum-statement-and-guiding-principles-on-interoperability-of-data-systems-in-humanitarian-cash-programming/ | I | — |
| D18 | Hoja de cálculo por email como norma | IFRC / DIGID | Investigating Safe Data Sharing | 2023 | https://interoperability.ifrc.org/wp-content/uploads/2023/11/DIGIDInteroperability-InvestigatingSafeDataSharingandSystemsInteroperability.pdf | T | — |

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| Borrador 1 | 2026-10-07 | Versión inicial para revisión | Instrucción de la responsable; opportunity-prioritization.md v1 + 3 líneas de búsqueda web | No |
| Borrador 2 | 2026-10-07 | Reescritura narrativa y gerencial: misma evidencia, fuentes y conclusiones; tablas reducidas a la matriz de capacidades, la síntesis competitiva, los segmentos y las fuentes | Instrucción de la responsable | No |
| v1 | 2026-10-07 | Versión validada (= borrador 2) | Validación explícita de la responsable | Sí |
