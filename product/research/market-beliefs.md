---
source: secondary
method: web
date: 2026-10-06
question: ¿Qué dice la evidencia secundaria sobre las cuatro creencias no verificadas de product/overview.md v1?
---

# Research: contraste de creencias no verificadas — NexoAid

> Ruta propuesta: product/research/market-beliefs.md
> Estado: BORRADOR — pendiente de validación (no guardar ni hacer commit)
> Etapa: Problem Discovery
> Responsable: Paola Espejo
> Base: product/overview.md v1 (2026-10-06), product/intake.md v1 (2026-10-06)

## Alcance y método

- **Qué cubre:** las cuatro creencias registradas en `product/overview.md` v1, con su numeración original (C1–C4).
  No incluye soluciones ni funcionalidades. No decide qué producto construir.
- **Método:** búsqueda web real (WebSearch/WebFetch), una línea de investigación por creencia, en paralelo.
  Consulta: 2026-10-06. Las fuentes se identifican con un código (p. ej. `1.04`) que remite a la sección
  *Fuentes*, donde están URL, organización, fecha y afirmación concreta.
- **Etiquetas de procedencia:** todo lo listado en *Fuentes* está `[verificado: URL — 2026-10-06]`.
  Lo que procede de memoria del modelo aparece marcado `[conocimiento del modelo — verificar]`.
  Las fuentes de proveedores se marcan **COMERCIAL**.
- **Límite de este documento:** la evidencia secundaria describe el mercado y el sector. No verifica
  creencias sobre los usuarios de NexoAid. Ninguna creencia queda "validada" aquí, y este archivo
  no modifica `product/overview.md`.

## Resumen: los hallazgos que cambian decisiones

1. **La fragmentación existe, pero no está donde la creencia la sitúa.** Las agencias de la ONU, la
   Cruz Roja y varias INGO grandes ya usan un sistema integrado de gestión de personas receptoras
   (SCOPE, LMMS, HOPE, RedRose). Esos sistemas cubren todo el ciclo dentro de cada organización.
   El traspaso manual documentado aparece **entre organizaciones** (listas de pago a proveedores
   financieros, socios, clusters, deduplicación) y en **ONG medianas, pequeñas y nacionales**.
   Además, el sector dice que la interoperabilidad es sobre todo un problema de gobernanza y
   estándares, no de software. El segmento "ONG internacionales" de C1 debe precisarse.
2. **La viabilidad por donantes es la creencia más débil.** DG ECHO declara por escrito que
   financiar la transformación digital de sus socios no está a su alcance. Los costes de gestión de
   datos "no suelen presupuestarse". Existen herramientas gratuitas, propias y compartidas.
   El volumen mundial de CVA cayó en 2024 y se proyectan caídas de entre el 31 % y el 60 % en 2025,
   tras la retirada de EE. UU., que financiaba el 42 % del CVA. Los donantes **exigen** trazabilidad,
   pero no hay evidencia de que **paguen** la herramienta que la produce.
3. **En los contextos más difíciles, el cuello de botella no es la conectividad.** En Gaza,
   Sudán, Afganistán y Myanmar el problema documentado en primer lugar es la **liquidez de
   efectivo, el acceso bancario, la regulación y el de-risking**. Estos problemas no los resuelve
   una capacidad offline. C4 mezcla problemas distintos y conviene separarlos antes de la
   investigación primaria.

## Correspondencia con la lista inicial de la solicitud

La solicitud incluía cinco creencias (B1–B5) que no coinciden con `overview.md` v1. Por decisión
de la responsable, este research usa solo las cuatro del overview.

| Lista de la solicitud | Creencia de overview.md v1 | Tratamiento aquí |
|---|---|---|
| B1. Problemas operativos relevantes | — (es el propósito del intake §2, no una creencia registrada) | Fuera de alcance |
| B2. Fragmentación / interoperabilidad | C1 | Investigada |
| B3. Limitaciones de infraestructura | C4 | Investigada |
| B4. Conciliación y trazabilidad | C2 (conciliación) y C3 (trazabilidad exigida por donantes) | Investigadas |
| B5. Control programático vs. flexibilidad | — (intake §11, supuesto S8) | Fuera de alcance |
| — | C3. Financiación por donantes | Investigada |

---

## C1. Sistemas no interoperables y trabajo manual

> [product] [value] Los equipos de Programas/CVA de ONG internacionales usan varios sistemas no
> interoperables a lo largo del ciclo (registro → transferencia → comercio → reporte). Dedican
> trabajo manual recurrente a mover datos entre ellos y cambiarían su forma de trabajar actual
> para reducirlo. *Se refuta si la mayoría trabaja en una plataforma integrada, o si el traspaso
> manual no está entre sus problemas prioritarios.*

**Pregunta de investigación.** ¿Qué dice la evidencia reciente sobre la fragmentación de sistemas,
la interoperabilidad y el traspaso manual de datos en programas de CVA? ¿Hay plataformas integradas
de uso mayoritario? ¿El traspaso manual es un problema prioritario?

### Hechos encontrados
- "No single system has been broadly adopted and each system has its own data structure and
  processes." La ONU y la Cruz Roja tienen plataformas propias. SCOPE (WFP) costó US$47,3 M entre
  2013 y 2020 solo a nivel de sede. World Vision usa LMMS, Concern usa RedRose y GiveDirectly usa
  Salesforce. Muchas otras organizaciones, incluidas las ONG nacionales, usan ODK y Excel y envían
  las listas de pago a los proveedores financieros por correo. (1.01)
- "The simplest, most common way to share data across humanitarian organizations remains sending a
  spreadsheet in an email." (1.02)
- Hay dos perfiles: organizaciones pequeñas con Excel, a veces con Kobo/ODK, y organizaciones
  grandes con sistemas integrales como RedRose. El estudio se basa en 29 entrevistas y 2 mesas
  redondas y no ordena los problemas por prioridad. (1.02, 1.03)
- Las conexiones API con proveedores financieros exigen una inversión inicial alta. Las ONG
  globales encuestadas gastan "just 2 % on IT". (1.01)
- En la encuesta del SOWC 2023, los mayores retos para aumentar la CVA fueron la financiación
  (33 %), la inflación o depreciación (33 %) y la gestión de riesgos (31 %). Datos y sistemas no
  aparecen entre los primeros. (1.04)
- Hay interoperabilidad en funcionamiento: PING automatiza el intercambio entre PRIMES (UNHCR) y
  SCOPE (WFP) en Tanzania, "which was previously tedious and manual" (1.05). En Ucrania, 63 socios
  participan en la deduplicación de efectivo multipropósito, con un ahorro estimado de US$207 M a
  finales de 2024 (1.06).
- En Sudán (2026), los tableros del Cash Working Group y de seguridad alimentaria están separados.
  "There is broad agreement that interoperability and data-sharing matter, though not yet agreement
  on how to implement them." (1.07)
- "Interoperability challenges are not primarily technical but systemic (standards, processes,
  governance)." (1.08)
- Cruz Roja de Kenia: antes, los datos se registraban en Excel y "then manually added into a cash
  tool". (1.09)
- Diez donantes firmaron en 2022 principios sobre interoperabilidad de sistemas de datos en CVA.
  (1.10)

### Evidencia que apoya la creencia
- No hay una plataforma dominante. La combinación ODK/Kobo + Excel + correo a proveedores es
  habitual (1.01, 1.02, 1.09). En 2026 sigue habiendo fuentes de datos separadas (1.07).
- El traspaso manual está documentado de forma cualitativa en varias etapas del ciclo (1.02, 1.05,
  1.09).

### Evidencia que la contradice o matiza
- Las organizaciones grandes ya tienen un sistema integrado internamente (1.01). Si el segmento son
  las INGO grandes, la primera condición de refutación se acerca a cumplirse **dentro** de cada
  organización.
- El problema no figura entre los retos prioritarios del SOWC 2023 (1.04). Esto apunta a la segunda
  condición de refutación.
- Una parte del problema se está resolviendo para casos de uso concretos, como la deduplicación
  (1.05, 1.06).
- El sector sitúa el problema en la gobernanza y los estándares más que en la tecnología (1.02, 1.08).
- Hay barreras fuertes al cambio: dependencia del proveedor, un 2 % de gasto en TI, coste de las API
  e incentivos competitivos entre organizaciones (1.01, 1.02).

### Inferencias
- La creencia parece cumplirse más en INGO medianas, ONG nacionales y oficinas de país con varios
  socios que en las sedes de las grandes agencias.
- El traspaso manual parece concentrarse en las **fronteras entre organizaciones**: hacia el
  proveedor financiero, la conciliación de vuelta, los reportes a clusters y donantes y la
  deduplicación.
- El dolor parece real pero de segundo orden frente a la financiación. Ninguna fuente lo dice así.
- La disposición a cambiar parece depender de la sede y del donante, no solo del equipo de
  Programas/CVA.

### Vacíos
- No hay ninguna medición del tiempo de personal dedicado a traspasos manuales en CVA.
- No hay evidencia directa sobre la disposición a cambiar de los equipos de Programas/CVA.

### Estado
| Parte | Estado | Confianza | Por qué |
|---|---|---|---|
| (a) Varios sistemas no interoperables | Apoyada provisionalmente | Media-alta | CALP 2023 y IFRC/DIGID 2023 coinciden. Matiz: es más una fragmentación entre organizaciones que dentro de las grandes. |
| (b) Trabajo manual recurrente | Parcialmente apoyada | Media | Está documentado de forma cualitativa, sin medición. No aparece entre los retos prioritarios. |
| (c) Disposición a cambiar | No concluyente | Baja | Hay adopciones puntuales y presión de donantes, frente a barreras estructurales fuertes. |
| **C1 global** | **Parcialmente apoyada** | **Media** | La refutación por "plataforma integrada" no se cumple en el sector en conjunto, pero sí podría cumplirse en INGO grandes. La refutación por "no prioritario" queda abierta y hay indicios a favor (1.04). |

---

## C2. Discrepancias entre ONG y comercios

> [product] [value] Las discrepancias entre lo que registra la ONG y lo que cobran los comercios son
> frecuentes, retrasan pagos o reportes y afectan directamente al equipo de Programas/CVA, no solo
> a Finanzas. *Se refuta si las discrepancias son raras, si se resuelven sin esfuerzo relevante o si
> quedan enteramente dentro de Finanzas.*

**Pregunta de investigación.** ¿Con qué frecuencia hay discrepancias en la conciliación con
comercios en programas de vouchers y e-vouchers? ¿Retrasan pagos o reportes? ¿Qué áreas se ocupan
de ellas?

### Hechos encontrados
- Con vouchers en papel (Yemen), la conciliación tardaba de media 15 días hábiles y el pago a
  comercios, de 3 a 4 semanas. Finanzas contaba los vouchers a mano. Con e-vouchers el pago bajó a
  1–5 días. (2.01, 2016)
- CALP pide trabajar con Finanzas para pagar a tiempo a los comercios, "so as to minimise the
  drop-out rate of traders participating". (2.02, guía sin fecha, basada en fuentes de 2010–2011)
- Quién concilia varía según la organización:
  - ICRC: Logística recoge los vouchers y concilia; Finanzas paga. (2.03, 2024)
  - Cruz Roja de Zambia: Finanzas concilia; el punto focal de CVA da soporte técnico a los
    comercios. (2.04, 2022)
  - Mercy Corps: los equipos de CVA suelen incluir un "Payment Officer" con un rol mixto
    Finanzas/Programa "to speed internal processing of payments". (2.05, 2018)
- Oxfam, Kenia (2022–2023, con e-vouchers): uno de los cuatro desafíos fue el "misalignment in
  number of claims that need to be cross-verified with system reports". El mismo documento informa
  un "100 % redemption of vouchers so far". (2.06, 2025)
- Auditorías de WFP:
  - Palestina: el 90 % de la asistencia fue en vouchers de valor. Finanzas concilia en hojas de
    cálculo unas 100.000 transacciones por ciclo, en un proceso "inherently prone to errors".
    Programas, Finanzas y Supply Chain se reparten las tareas. (2.07, 2022)
  - Angola: "gaps in the documentation related to the reconciliation of commodity voucher". (2.08,
    2024)
  - Jordania: un socio tuvo dificultades para obtener a tiempo los recibos de los comercios para el
    monitoreo. (2.09, 2017)
  - Unidad de comercios: "no up-to-date and precise data regarding contracted retailers". (2.10,
    2023)
- Relief International con RedRose (Siria): pago semanal a comercios, ventana de 48 horas cumplida,
  "perfect reconciliation" según Finanzas. (2.11, 2016)
- Una revisión académica encuentra poco detalle en la literatura sobre conciliación o retrasos en el
  pago a comercios. (2.12, 2022)
- No se encontraron fuentes comerciales con afirmaciones verificables sobre este tema.

### Evidencia que apoya la creencia
- Hay discrepancias que obligan a verificar a mano, incluso con e-vouchers recientes (2.06). Las
  auditorías califican la conciliación como manual y propensa a errores (2.07, 2.08).
- Con vouchers en papel, la conciliación retrasa el pago (2.01). La guía normativa vincula los
  retrasos con el abandono de comercios (2.02).
- Programas aparece implicado: hay roles mixtos (2.05), soporte a comercios (2.04), monitoreo que
  depende de recibos de comercios (2.09) y procesos repartidos entre varias áreas (2.07).

### Evidencia que la contradice o matiza
- Los e-vouchers reducen mucho los plazos, de semanas a 1–5 días o 48 horas (2.01, 2.11).
- Formalmente, la conciliación pertenece a Finanzas (2.04) o a Logística (2.03), no a Programas.
- Las evaluaciones grandes revisadas no mencionan el tema. Puede que no sea un problema prominente,
  o que quede fuera de su alcance.
- Varias fuentes de apoyo son anteriores a 2018 y describen vouchers en papel (2.01, 2.02).

### Inferencias
- Con los e-vouchers, el problema probablemente pasó del volumen de papel y la lentitud al **cruce
  de datos** entre sistema, facturas y banco, y a la calidad de los datos de comercios.
- Programas aparece casi siempre como parte afectada o de apoyo, aunque no sea dueño formal del
  proceso.

### Vacíos
- Ninguna fuente da la frecuencia o el tamaño de las discrepancias.
- No hay datos sobre retrasos en reportes atribuibles a la conciliación.
- No hay mediciones recientes de abandono de comercios por pagos tardíos.

### Estado
| Parte | Estado | Confianza | Por qué |
|---|---|---|---|
| (a) Las discrepancias son frecuentes | No concluyente | Baja | Hay casos, pero ninguna frecuencia medida. Con e-vouchers la conciliación se describe como fluida (2.11). |
| (b) Retrasan pagos o reportes | Parcialmente apoyada | Media | La evidencia fuerte es de papel y anterior a 2018. Con e-vouchers los retrasos bajan a días. No hay nada directo sobre reportes. |
| (c) Afectan a Programas/CVA, no solo a Finanzas | Parcialmente apoyada | Media-baja | La implicación de Programas se infiere de roles y SOP más de lo que se mide. El dueño formal es Finanzas o Logística. |
| **C2 global** | **Parcialmente apoyada** | **Baja-media** | La creencia necesita precisarse por modalidad (papel o e-voucher) y por dueño del proceso. |

---

## C3. Financiación por donantes

> [product] [viability] Los donantes financiarían una herramienta de este tipo, con presupuesto del
> programa o con líneas de soporte, porque exigen trazabilidad sobre el uso de los recursos. *Se
> refuta si estos costes no son elegibles para los donantes, o si las ONG cubren la trazabilidad con
> herramientas propias o gratuitas.*

**Pregunta de investigación.** ¿Los donantes exigen trazabilidad en CVA? ¿Los costes de
herramientas digitales son elegibles en sus subvenciones? ¿Cómo financian hoy las ONG esas
herramientas, en el contexto de recortes de 2025–2026?

### Hechos encontrados
- La política de cash de DG ECHO (2022) tiene elementos obligatorios. Entre ellos: protección de
  datos, interoperabilidad de registros, seguimiento de efectivo y vouchers, marcos MEAL comunes y
  ratio coste-transferencia. Los programas de 10 M€ o más deben seguir una nota de orientación
  sobre separación de funciones y transparencia. (3.01)
- Diez donantes piden "maximise accountability" y "single, shared or interoperable registries". No
  dicen cómo se financian. (3.02, 2019)
- DG ECHO (2023): "fully funding our partners digital transformation […] would not be within the
  means of DG ECHO's budget or funding modalities". Espera que las herramientas digitales vengan
  integradas en las propuestas, con un análisis coste-beneficio. Hay algo de financiación vía ERC
  (Enhanced Response Capacity) y fondos de I+D de la UE. (3.03)
- ECHO limita los costes indirectos al 7 % como máximo. Los costes directos deben estar
  "directly linked to the action". En las páginas consultadas no hay ninguna regla explícita sobre
  software o licencias. (3.04)
- El tope del 7 % de costes indirectos se considera insuficiente. Con esos costes se pagan los
  sistemas de sede. (3.05, 2022)
- Revisión de RedRose en cinco Sociedades Nacionales de la Cruz Roja: "the cost for data management
  is not usually budgeted for". En Gambia y Zambia se cubrió con el fondo de emergencia DREF. En
  Ruanda, el paso de piloto a uso continuado falló por rotación de personal. (3.06, 2022)
- KoboToolbox es gratuito para más del 95 % de sus usuarios. (3.07, 2024, **COMERCIAL**, sin ánimo de
  lucro)
- RedRose dice operar en más de 50 países con grandes agencias y declararse "self-funded and
  profitable". No publica precios. (3.08, 2024, **COMERCIAL**, autodeclarado)
- Humansis la desarrolla Quanti para People in Need, con unos 7 FTE, a coste "without any profit
  margin". Es una herramienta propia. (3.09, **COMERCIAL**)
- El volumen de CVA bajó de 7.800 M USD (2023) a 6.600 M USD (2024). Para 2025 se proyectó una caída
  de alrededor del 31 %. (3.10, 2025)
- EE. UU. financiaba el 42 % del CVA mundial. CALP estimó una caída de casi el 60 % en el volumen de
  CVA de 2025. (3.11, 2026)
- BHA pasó de más de 1.000 personas a unas 50, integradas en el Departamento de Estado. (3.12, 2025,
  think tank)
- Solo se cubrió el 35 % de los llamamientos de 2025. (3.13, 2026) Alemania recortó un 50 % en 2025 y
  Reino Unido bajará al 0,3 % de la RNB en 2027. (3.14, 2026)
- Fuera de la búsqueda: en EE. UU. (2 CFR 200), el software asignado a una subvención puede cargarse
  como coste directo. `[conocimiento del modelo — verificar]`

### Evidencia que apoya la creencia
- Los donantes exigen trazabilidad, deduplicación, protección de datos y transparencia, en el caso de
  ECHO con carácter obligatorio (3.01, 3.02).
- Existe una vía formal: coste directo justificado dentro del proyecto, con análisis coste-beneficio
  (3.03, 3.04).
- Hay precedentes de pago con fondos de respuesta (3.06). Alguien paga las herramientas comerciales
  existentes (3.08, comercial).

### Evidencia que la contradice o matiza
- El principal donante europeo dice explícitamente que no puede financiar la transformación digital
  de sus socios (3.03).
- Los costes de datos no suelen presupuestarse y su sostenibilidad más allá del piloto es frágil
  (3.06).
- Los sistemas que sirven a varios proyectos tienden a ir a costes indirectos, que están limitados y
  se consideran insuficientes (3.04, 3.05).
- Hay alternativas gratuitas (3.07), propias (3.09) y comerciales ya extendidas (3.08). Los donantes
  empujan hacia registros compartidos (3.02).
- La financiación se contrae con fuerza en 2025–2026 (3.10–3.14). La presión va hacia la eficiencia
  y el ratio coste-transferencia, no hacia partidas nuevas.

### Inferencias
- La trazabilidad parece una **condición de cumplimiento** que la ONG debe resolver con sus propios
  medios. El donante exige el resultado, no paga la herramienta.
- Con los recortes, los donantes podrían preferir sistemas comunes o interagenciales antes que
  herramientas por ONG.
- El hueco, si existe, estaría en las ONG medianas y locales. Son justo las que menos costes
  indirectos reciben.

### Vacíos
- No hay casos documentados de licencias de plataformas de CVA aceptadas como coste directo por
  ECHO, FCDO, GFFO o SIDA.
- No se verificaron las reglas de PRM (sucesor de BHA), el NPAC de FCDO ni la guía de costes de GFFO.
- No hay datos sobre el gasto anual de las ONG en herramientas de CVA.

### Estado
| Parte | Estado | Confianza | Por qué |
|---|---|---|---|
| (a) Los donantes exigen trazabilidad | Apoyada provisionalmente | Alta | Coinciden varios documentos institucionales de donantes, uno de ellos con elementos obligatorios. |
| (b) Los costes de herramientas son elegibles | No concluyente, con inclinación a contradicha | Media-baja | La regla general deja margen, pero ECHO niega la financiación de la transformación digital y no hay regla explícita sobre software. |
| (c) Las ONG no lo cubren ya con herramientas propias o gratuitas | Contradicha provisionalmente | Media | Hay herramientas gratuitas, propias y comerciales en uso. No se sabe si cubren la trazabilidad de principio a fin en ONG medianas. |
| **C3 global** | **Parcialmente apoyada, con riesgo alto de viabilidad** | **Media** | La premisa (los donantes exigen trazabilidad) se sostiene. La conclusión (la financiarían) no tiene respaldo y choca con la contracción de 2025–2026. |

---

## C4. Entrega en contextos de conectividad limitada

> [product] [value] En contextos con conectividad limitada, la entrega sigue siendo un problema
> activo que las soluciones actuales no resuelven bien. *Se refuta si las ONG ya lo cubren de forma
> satisfactoria con herramientas existentes (OMNIAID, Humansis y otras ofrecen operación offline:
> H2, H3).*

**Pregunta de investigación.** ¿Cómo condicionan la conectividad, la red de agentes, el acceso a
cuentas, la electricidad y los dispositivos la entrega de CVA? ¿Las soluciones offline existentes lo
resuelven de forma satisfactoria?

### Hechos encontrados
- Los pagos digitales autogestionados excluyen a quien no tiene teléfono, conectividad o
  alfabetización digital, o tiene discapacidad. CALP recomienda un enfoque multicanal. Lo que más
  retrasa una respuesta es el tiempo para contratar proveedores financieros. En Somalia, el 63 % de
  los receptores de WFP pasó de e-voucher a mobile money en 2022. (4.01, 2023)
- Ucrania: el registro digital excluyó a personas mayores, con discapacidad y rurales (4.02). "Some
  people have old mobile phones with no browsers. They cannot apply for aid." (4.03, 2023)
- Sudán:
  - Solo el 15 % tenía cuenta antes de la guerra. Bankak registra más de 50 M de transacciones, pero
    los agentes cobran hasta un 20 % por retirar efectivo. Los bancos tardan "weeks to gather
    liquidity". (4.04, 2024)
  - Bankak estuvo caída varios días en mayo de 2023. (4.05, prensa)
  - En el apagón de febrero de 2024, una cocina comunitaria que alimentaba a 850 familias cerró
    porque no podía recibir fondos. (4.06, prensa especializada)
  - Piloto de mobile money por USSD en Gedaref (25 familias): entregó el dinero, pero hubo fallos del
    portal, falta de teléfonos y problemas con el PIN. (4.07, 2023)
- Gaza:
  - Desde marzo de 2024 el problema principal es la liquidez. (4.08, 2024)
  - Comisiones del 20–40 % por convertir saldo en efectivo. (4.09, 2025, prensa especializada)
  - Las e-wallets de WFP pasaron de unas 75.000 a 245.000 personas entre septiembre y octubre
    de 2025. (4.10)
  - Internet inestable y dificultades para abrir cuentas con documentos de reemplazo. (4.11, 2026,
    prensa)
- Afganistán: "No one financing channel is yet able to transfer NGO funds into, or around,
  Afghanistan" a la escala necesaria. (4.12, 2022) Myanmar: restricciones "draconian" al acceso
  bancario y paso a canales informales. (4.13, 2022)
- El 70 % de las organizaciones sin fines de lucro encuestadas tiene dificultades para transferir
  fondos. El 65 % señala la regulación como barrera principal. (4.14, 2025)
- Refugiados en Etiopía: el 57 % tiene internet móvil en casa. La identificación es la barrera
  principal; la electricidad, no. (4.15, 2025) Sudán del Sur: el coste es la barrera dominante
  (71 %). (4.16, 2026)
- El 44 % de los proveedores de mobile money encuestados se asoció con organizaciones humanitarias
  para CVA en 2024 (31 % en 2023). (4.17, 2025, gremio de la industria)
- Smartcards offline con Humansis en Siria: 3.368 hogares y 69 comercios. Satisfacción del 64 % en
  receptores y 73 % en comercios. La tarjeta cuesta unos 4 USD frente a 8 USD del voucher de papel.
  Tardaron meses en corregir procedimientos. (4.18, 2020–21, ONG dueña de la herramienta)
- OmniAid se presenta con "offline payment rails" y pilotos en Kenia, Jordania y Sudán. (4.19,
  **COMERCIAL**)
- Fuera de la búsqueda: RedRose y SCOPE (WFP) funcionan con tarjetas en zonas sin conectividad.
  `[conocimiento del modelo — verificar]`

### Evidencia que apoya la creencia
- Los cortes de conectividad y electricidad interrumpen la entrega en conflictos activos (4.05,
  4.06, 4.09, 4.11).
- La exclusión digital persiste: personas mayores, sin teléfono, sin identificación (4.02, 4.03,
  4.07, 4.11, 4.15, 4.16).
- Las soluciones offline documentadas son pilotos o de escala pequeña, con resultados mixtos. Su
  evidencia viene de sus propios dueños o es comercial (4.18, 4.19).

### Evidencia que la contradice o matiza
- En los casos más graves, el cuello de botella es la **liquidez**, el **acceso bancario**, la
  **regulación** y el **de-risking**, no la conectividad (4.04, 4.08, 4.12, 4.13, 4.14).
- El ecosistema digital funciona y crece incluso en crisis (4.04, 4.10, 4.17).
- Hay soluciones offline que han funcionado en pilotos (4.07, 4.18). El sector también usa
  mecanismos no digitales, como hawala o efectivo en mano (4.04, 4.12, 4.13).
- El peso de cada barrera cambia según el contexto (4.15, 4.16).

### Inferencias
- "Infraestructura limitada" agrupa al menos cinco problemas con dueños distintos: conectividad y
  electricidad; red de agentes y liquidez; identificación y KYC; acceso bancario, regulación y
  de-risking; dispositivos y alfabetización digital. C4 solo nombra el primero.
- Que existan soluciones offline no prueba que funcionen bien. No se encontraron evaluaciones
  independientes a escala entre 2022 y 2026.
- El problema pendiente podría estar más en la ayuda local (organizaciones locales, salas de
  respuesta de emergencia) que en las INGO.

### Vacíos
- No hay evaluaciones independientes de herramientas offline (fallos de sincronización,
  conciliación, coste).
- No hay datos sobre qué falla primero cuando falla la entrega.
- No hay evidencia sobre la satisfacción de las ONG con sus herramientas actuales.

### Estado
| Parte | Estado | Confianza | Por qué |
|---|---|---|---|
| (a) La infraestructura limitada condiciona la entrega | Apoyada provisionalmente | Media-alta | Coinciden varias fuentes institucionales independientes, en varios contextos, de 2021 a 2026. Gran parte es cualitativa o de prensa. |
| (b) Las soluciones actuales no lo resuelven bien | No concluyente | Baja | Los fallos documentados son sobre todo de liquidez, acceso bancario y regulación, no de herramientas offline. La condición de refutación no se puede confirmar ni descartar con fuentes secundarias. |
| **C4 global** | **Parcialmente apoyada en la premisa, no concluyente en lo que importa para producto** | **Baja-media** | Conviene reformularla separando la conectividad de la liquidez y el acceso financiero. |

---

## Impacto en creencias

| Creencia (overview.md v1) | Veredicto | Confianza | Evidencia clave |
|---|---|---|---|
| C1. Sistemas no interoperables y trabajo manual | Parcialmente apoyada | Media | La fragmentación existe sobre todo entre organizaciones y en ONG no grandes (1.01, 1.02). No aparece entre los retos prioritarios (1.04). |
| C2. Discrepancias ONG–comercios | Parcialmente apoyada | Baja-media | Discrepancias y conciliación manual documentadas (2.06, 2.07). Sin frecuencias. Los e-vouchers reducen los retrasos (2.01, 2.11). |
| C3. Financiación por donantes | Parcialmente apoyada, con riesgo alto de viabilidad | Media | Los donantes exigen trazabilidad (3.01). ECHO no financia la transformación digital (3.03). Hay alternativas gratuitas y propias (3.07, 3.09). La financiación de CVA se contrae (3.10, 3.11). |
| C4. Conectividad limitada | No concluyente en su parte central | Baja-media | La infraestructura condiciona la entrega (4.04, 4.06). El cuello de botella principal es la liquidez y el acceso financiero (4.08, 4.12, 4.14). |

**Lo que este research no hace:** no anota `product/overview.md` y no cambia el orden de prioridad
de las creencias. Si alguna creencia debe reformularse (por ejemplo, separar C4 en conectividad y
liquidez, o acotar el segmento de C1), corresponde a `/review-evidence` con este archivo como
evidencia, siguiendo WORKFLOW §3.1.

## Qué sigue necesitando research primario

**Encuesta** (cuánto, con qué frecuencia, cuántos):
- C1: número de sistemas por etapa; horas por ciclo de pago dedicadas a traspasos; posición del
  traspaso manual en un ranking de problemas; tipo de organización y si tiene un sistema integrado.
- C2: porcentaje de ciclos con discrepancias y su tamaño; días entre canje y pago; horas de
  conciliación por rol; área dueña del proceso; modalidad (papel o e-voucher).
- C3: tipo de herramientas usadas (gratuitas, propias, comerciales); cómo se financian; gasto anual;
  si algún donante ha rechazado esos costes.
- C4: frecuencia de interrupciones por causa; uso real del modo offline; satisfacción con las
  herramientas actuales.

**Entrevistas** (por qué, qué hacen hoy):
- C1: dónde se rompe el flujo; si el dolor está dentro o entre organizaciones; quién decide la
  adopción de herramientas; qué intentos de cambio fracasaron y por qué.
- C2: cómo se resuelve en la práctica una discrepancia y quién la escala; tensiones entre Programas
  y Finanzas o Logística.
- C3: responsables de *grants* y Finanzas en ONG y oficiales de programa de donantes: si se han
  aceptado licencias como coste directo, qué pasa al negociar el presupuesto, qué cambió tras los
  recortes de 2025.
- C4: Cash Working Groups y responsables de CVA en Sudán, Gaza, Sahel o Myanmar: qué falla primero
  cuando falla la entrega; organizaciones locales, cuya experiencia está poco documentada.

**Fuentes documentales pendientes:** SOWC 2026 de CALP (previsto para noviembre de 2026); Anexo 5 del
acuerdo de subvención de ECHO; reglas de PRM; NPAC de FCDO; guía de costes de GFFO; informe completo
del Global Findex 2025.

---

## Fuentes

Consultadas el 2026-10-06. Tipo: I = institucional; A = auditoría; P = prensa; T = think tank o
académica; C = **COMERCIAL**.

### C1
| ID | Organización | Documento | Fecha | Tipo | Afirmación que respalda | URL |
|---|---|---|---|---|---|---|
| 1.01 | CALP Network | State of the World's Cash 2023, cap. 7 | 2023-11-15 | I | No hay sistema adoptado de forma amplia; ODK + Excel + correo; 2 % de gasto en TI; coste de las API | https://www.calpnetwork.org/web-read/the-state-of-the-worlds-cash-2023-chapter-7-data-and-digitalization/ |
| 1.02 | IFRC / DIGID | Investigating Safe Data Sharing and Systems Interoperability in Humanitarian Cash Assistance | 2023 | I | La hoja de cálculo por correo es la forma más común de compartir datos; dos perfiles; dependencia del proveedor | https://interoperability.ifrc.org/wp-content/uploads/2023/11/DIGIDInteroperability-InvestigatingSafeDataSharingandSystemsInteroperability.pdf |
| 1.03 | IFRC / DIGID | Landscape Mapping Overview | 2023 | I | 29 entrevistas y 2 mesas redondas; no ordena los problemas por prioridad | https://interoperability.ifrc.org/wp-content/uploads/2023/11/DIGIDInteroperability-LandscapeMappingOverview.pdf |
| 1.04 | CALP Network | State of the World's Cash 2023 (PDF completo), gráfico 2.8 | 2023 | I | Retos principales: financiación, inflación, riesgos | https://library.alnap.org/system/files/content/resource/files/main/The-State-of-the-Worlds-Cash-2023.pdf |
| 1.05 | UNHCR / WFP | Collaboration gone right: UNHCR and WFP take data sharing to the next level in Tanzania | 2024-09-16 | I | PING automatiza un intercambio antes manual | https://www.unhcr.org/blogs/collaboration-gone-right-unhcr-and-wfp-take-data-sharing-to-the-next-level-in-tanzania-refugee-camps/ |
| 1.06 | Ukraine Cash Working Group | Data Management – Systems and Governance Assessment Report | 2025-07 | I | 63 socios en deduplicación; ahorro de US$207 M | https://reliefweb.int/report/ukraine/ukraine-cwg-data-management-systems-and-governance-assessment-report-july-2025 |
| 1.07 | CashCap / CALP / gDCF | Cash Landscape and Pathways Forward – Sudan | 2026-04 | I | Tableros separados; no hay acuerdo sobre cómo implementar la interoperabilidad | https://www.calpnetwork.org/wp-content/uploads/2026/07/Cash-Landscape-and-Pathways-Forward_Cash-Landscape-Review_Sudan.pdf |
| 1.08 | CALP Network | ECHO Cash Consortia Learning Event: Lessons from South Sudan and Yemen | 2026-05 | I | La interoperabilidad es un problema sistémico, no técnico | https://www.calpnetwork.org/wp-content/uploads/2026/06/ECHO-Cash-Consortia-Learning-Event-Lessons-from-South-Sudan-and-Yemen-2026.pdf |
| 1.09 | IFRC | Digital Lifelines: Kenya Red Cross… 121 Platform | sin fecha (publicado 2025-04) | I (caso del implementador) | Antes, Excel y carga manual a la herramienta de pago | https://cash-hub.org/wp-content/uploads/sites/3/2025/04/Digital-Lifelines-How-the-Kenya-Red-Cross-Society-Transforms-Cash-Assistance-With-the-121-Platform.pdf |
| 1.10 | Donor Cash Forum (vía CALP) | Statement and Guiding Principles on Interoperability of Data Systems | 2022-09-06 | I | Diez principios de donantes sobre interoperabilidad | https://www.calpnetwork.org/publication/donor-cash-forum-statement-and-guiding-principles-on-interoperability-of-data-systems-in-humanitarian-cash-programming/ |

### C2
| ID | Organización | Documento | Fecha | Tipo | Afirmación que respalda | URL |
|---|---|---|---|---|---|---|
| 2.01 | Save the Children / MasterCard | E-Vouchers in Yemen: Field Experiences and Lessons Learned | 2016-06-01 | I (con proveedor) | Papel: 15 días de conciliación y 3–4 semanas de pago; e-voucher: 1–5 días | https://image.savethechildren.org/evouchers-yemen-ch11043967.pdf/511y0x074r3xw243sd0mqu7pfixf3uhw.pdf |
| 2.02 | CaLP | Vouchers: A Quick Delivery Guide for Cash Transfer Programming in Emergencies | sin fecha (fuentes 2010–2011) | I | Pago puntual para evitar el abandono de comercios | https://www.calpnetwork.org/wp-content/uploads/2020/03/calp_vouchers_screen-1.pdf |
| 2.03 | ICRC | 2024 ICRC CVA SOPs | 2024 | I | Logística concilia los vouchers; Finanzas paga | https://cash-hub.org/wp-content/uploads/sites/3/2025/05/2024_ICRC-CVA-SOPs_EN.pdf |
| 2.04 | Cruz Roja de Zambia | Cash and Voucher Assistance SOPs | 2022-01 | I | Finanzas concilia; el punto focal de CVA da soporte a los comercios | https://cash-hub.org/wp-content/uploads/sites/3/2022/02/ZambiaRCS_CVA_SOPs_January2022.pdf |
| 2.05 | Mercy Corps | E-Transfer Implementation Guide | 2018-12 | I | Rol mixto Finanzas/Programa; reportes automáticos que sustituyen la conciliación manual | https://mcdl.mercycorps.org/gsdl/docs/E-TransferGuideAllAnnexes.pdf |
| 2.06 | Oxfam | Electronic Vouchers & Humanitarian Response | 2025-07 | I | Desajuste de reclamaciones que exige verificación cruzada; 100 % de canje | https://www.oxfamwash.org/wp-content/uploads/E-Voucher-Paper-July-2025-Final-1.pdf |
| 2.07 | WFP, Oficina del Inspector General | Internal Audit of WFP Operations in the State of Palestine (AR/22/19) | 2022-12 | A | Conciliación manual en hojas de cálculo, propensa a errores; reparto entre áreas | https://docs.wfp.org/api/documents/WFP-0000145990/download/ |
| 2.08 | WFP, Oficina del Inspector General | Internal Audit of WFP Operations in Angola (AR/24/05) | 2024-04 | A | Vacíos de documentación en la conciliación de vouchers | https://docs.wfp.org/api/documents/WFP-0000159123/download |
| 2.09 | WFP, Oficina del Inspector General | Internal Audit of WFP Operations in Jordan (AR/17/08) | 2017 | A | Recibos de comercios no obtenidos a tiempo para el monitoreo | https://docs.wfp.org/api/documents/WFP-0000012908/download |
| 2.10 | WFP, Oficina del Inspector General | Internal Audit of WFP's Supply Chain CBT, Retail and Markets Unit (AR-23-14) | 2023-10 | A | Datos de comercios no actualizados ni precisos | https://docs.wfp.org/api/documents/WFP-0000154643/download/ |
| 2.11 | Relief International | E-Transfers for Hygiene through Red Rose in Northern Syria | 2016-08 | I (sobre herramienta comercial) | Pago en 48 horas; "perfect reconciliation" | https://www.calpnetwork.org/wp-content/uploads/2020/01/relief-internationale-transfers-for-hygiene-through-red-rose-in-syria-2.pdf |
| 2.12 | Maghsoudi et al., *Disasters* | Cash and voucher assistance along humanitarian supply chains: a literature review | 2022-09 | T | Poca literatura sobre conciliación y retrasos de pago a comercios | https://pmc.ncbi.nlm.nih.gov/articles/PMC10087535/ |

### C3
| ID | Organización | Documento | Fecha | Tipo | Afirmación que respalda | URL |
|---|---|---|---|---|---|---|
| 3.01 | DG ECHO | Thematic Policy Document No 3 – Cash Transfers | 2022-03-22 | I | Requisitos obligatorios de trazabilidad, protección de datos e interoperabilidad | https://www.calpnetwork.org/wp-content/uploads/2022/04/thematic_policy_document_no_3_cash_transfers_en.pdf |
| 3.02 | Diez donantes | Common Donor Approach for Humanitarian Cash Programming | 2019-02 | I | Rendición de cuentas y registros compartidos | https://resources.peopleinneed.net/documents/595-common-donor-approach-feb-19.pdf |
| 3.03 | DG ECHO | Humanitarian Digitalisation Policy Framework | 2023-03 | I | No puede financiar la transformación digital de sus socios | https://civil-protection-humanitarian-aid.ec.europa.eu/system/files/2023-03/DG%20ECHO%20Policy%20Framework%20on%20Digitalisation%20-%20final_0.pdf |
| 3.04 | DG ECHO Partners Helpdesk | Eligibility conditions (MGA 2021–2027) | vigente | I | Costes indirectos máximo 7 %; costes directos vinculados a la acción | https://www.dgecho-partners-helpdesk.eu/ngo/eligibility-of-costs/eligibility-conditions |
| 3.05 | Development Initiatives | Overhead cost allocation in the humanitarian sector | 2022-11-17 | I | El 7 % de costes indirectos es insuficiente | https://devinit.org/resources/overhead-cost-allocation-humanitarian-sector/equitable-overhead-provision-change-barriers-opportunities/ |
| 3.06 | IFRC | RedRose Learning Review | 2022-12-15 | I (sobre herramienta comercial) | Los costes de gestión de datos no suelen presupuestarse | https://cash-hub.org/wp-content/uploads/sites/3/2023/06/IFRC-Red-Rose-Learning-Review.pdf |
| 3.07 | KoboToolbox | Introducing KoboToolbox's new plan model | 2024-05-10 | C (sin ánimo de lucro) | Gratuito para más del 95 % de usuarios | https://www.kobotoolbox.org/blog/supporting-future-growth-and-accessibility-introducing-kobotoolboxs-new-plan-model |
| 3.08 | RedRose (notas de CALP) | RedRose Special Session notes | 2024-02-13 | C | Más de 50 países; rentable y autofinanciada | https://www.calpnetwork.org/wp-content/uploads/2024/02/RedRose-Special-Session-notes-13th-February-2024.pdf |
| 3.09 | Quanti | Caso de estudio Humansis | sin fecha | C | Herramienta propia de People in Need, a coste sin margen | https://quanti.cz/en/case-studies/humansis |
| 3.10 | CALP Network | Annual Report 2024-25 | 2025-11-11 | I | Caída del volumen de CVA en 2024 y proyección para 2025 | https://www.calpnetwork.org/?p=583826 |
| 3.11 | CALP Network | One Year on From the U.S. Government Cuts | 2026-01-26 | I | EE. UU. financiaba el 42 % del CVA; caída de casi el 60 % | https://www.calpnetwork.org/?p=588066 |
| 3.12 | CSIS | What has happened to U.S. government capabilities in international humanitarian assistance | 2025-11-13 | T | BHA reducida a unas 50 personas | https://www.csis.org/analysis/what-has-happened-us-government-capabilities-international-humanitarian-assistance |
| 3.13 | ALNAP | SOHS 2026, cap. 1.1 | 2026 | I | Solo el 35 % de los llamamientos de 2025 cubierto | https://alnap.org/help-library/resources/sohs-2026/chapter-1-prioritisation-under-pressure/1-1-the-reality-of-funding-gaps/ |
| 3.14 | ALNAP | Humanitarian Year in Review – Towards managed decline | 2026 | I | Recortes de Alemania, Reino Unido y otros donantes | https://alnap.org/help-library/resources/humanitarian-year-in-review-shocks-and-reverberations-e-report/towards-managed-decline-bracing-for-sustained-and-continued-cuts/ |

### C4
| ID | Organización | Documento | Fecha | Tipo | Afirmación que respalda | URL |
|---|---|---|---|---|---|---|
| 4.01 | CALP Network | State of the World's Cash 2023, cap. 7 | 2023-11 | I | Exclusión digital; enfoque multicanal; Somalia pasa a mobile money | https://www.calpnetwork.org/web-read/the-state-of-the-worlds-cash-2023-chapter-7-data-and-digitalization/ |
| 4.02 | CALP Network | State of the World's Cash 2023, recuadro 1.2 | 2023-11 | I | El registro digital en Ucrania excluyó a grupos vulnerables | https://library.alnap.org/system/files/content/resource/files/main/The-State-of-the-Worlds-Cash-2023.pdf |
| 4.03 | Ground Truth Solutions | Cash is king – if you can get it (Ucrania) | 2023-07 | I | Teléfonos sin navegador; viajes largos al banco | https://library.alnap.org/system/files/content/resource/files/main/GTS_Ukraine_CCD_July_2023_EN.pdf |
| 4.04 | CGAP | Can what remains of Sudan's financial system be used to fight famine? | 2024-12-03 | I | Liquidez, recargos de hasta 20 %, falta de bancos | https://www.cgap.org/blog/can-what-remains-of-sudans-financial-system-be-used-to-fight-famine |
| 4.05 | The New Arab | Sudan banking app goes offline | 2023-05-12 | P | Bankak caída varios días | https://www.newarab.com/news/sudan-millions-stranded-banking-app-goes-offline |
| 4.06 | The New Humanitarian | Sudan communication blackout… | 2024-03-04 | P | Una cocina comunitaria cierra por no recibir fondos | https://www.thenewhumanitarian.org/news-feature/2024/03/04/sudan-communication-blackout-mutual-aid-efforts-besieged |
| 4.07 | Mercy Corps (CALP/ALNAP) | Piloting Mobile Money Cash Assistance in Sudan | 2023-11 | I | El piloto USSD entrega el dinero con fallos operativos | https://library.alnap.org/system/files/content/resource/files/main/SudanConflictCVACaseStudyMobileMoneyPilot.pdf |
| 4.08 | Cash Working Group Gaza | Mobile money and e-wallet modalities – guiding note | 2024-06 | I | La liquidez es el problema principal | https://reliefweb.int/report/occupied-palestinian-territory/cash-working-group-gaza-strip-mobile-money-and-e-wallet-modalities-gaza-cwg-guiding-note-june-2024 |
| 4.09 | The New Humanitarian | Cash became a commodity… (Gaza) | 2025-04-17 | P | Comisiones del 20–40 %; pocos cajeros | https://www.thenewhumanitarian.org/news-feature/2025/04/17/cash-became-commodity-liquidity-crisis-compounding-suffering-gaza |
| 4.10 | FEWS NET | Gaza analysis note | 2025-11 | I | Las e-wallets de WFP se triplican; comisiones a la baja | https://fews.net/middle-east-and-asia/gaza/fews-net-analysis-note/november-2025 |
| 4.11 | Al Jazeera | Gaza forced to use unreliable online payments amid 'cash famine' | 2026-08-28 | P | Internet inestable; problemas con documentos de reemplazo | https://www.aljazeera.com/news/2026/8/28/gaza-forced-to-use-unreliable-online-payments-amid-cash-famine |
| 4.12 | NRC | Life and death: financial access in Afghanistan | 2022-01 | I | Ningún canal transfiere fondos de ONG a la escala necesaria | https://www.NRC.no/globalassets/pdf/reports/life-and-death/executive-summary_financial-access-in-afghanistan_nrc_jan-2022.pdf |
| 4.13 | COAR | Cash Transfer Programmes Review… Myanmar | 2022-04 | I | Restricciones bancarias; paso a canales informales | https://library.alnap.org/system/files/content/resource/files/summary/financial_modalities_executive_summary_english.pdf |
| 4.14 | ODI/HPG | Financial access challenges specific to non-profit organisations | 2025-04 | I | 70 % con dificultades para transferir fondos; 65 % señala la regulación | https://media.odi.org/documents/HPG_financial_access_4_final.pdf |
| 4.15 | UNHCR / GSMA | Access and Barriers to Digital Connectivity… Ethiopia | 2025-11 | I | La identificación es la barrera principal; la electricidad, no | https://www.unhcr.org/innovation/wp-content/uploads/2025/11/CoNUA-Ethiopia.pdf |
| 4.16 | GSMA / REACH / UNHCR | Digital access and connectivity in South Sudan | 2026-06 | I | El coste es la barrera dominante (71 %) | https://www.gsma.com/solutions-and-impact/connectivity-for-good/mobile-for-development/gsma_resources/digital-access-and-connectivity-in-south-sudan-barriers-for-refugees-and-host-communities/ |
| 4.17 | GSMA | State of the Industry Report on Mobile Money 2025 | 2025-04 | I (gremio) | 44 % de proveedores asociados con organizaciones humanitarias | https://gsma.com/sotir/wp-content/uploads/2025/04/The-State-of-the-Industry-Report-2025_English.pdf |
| 4.18 | People in Need | Scaling up electronic vouchers in Syria | 2020–21 | I (dueña de la herramienta) | Smartcards offline: escala, satisfacción y coste | https://resources.peopleinneed.net/documents/1043-smart-cards.pdf |
| 4.19 | OmniAid (oferta de empleo) | About OmniAid | sin fecha | C | Se presenta con "offline payment rails" y pilotos | https://impactpool.org/jobs/1190645 |

### Advertencias sobre las fuentes
- 2.01, 2.02, 2.09 y 2.11 son anteriores a 2018. Se usan como antecedente, no como estado actual.
- Una extracción automática del PDF completo del SOWC 2023 devolvió frases que no aparecían en el
  texto real. Se descartaron. Las citas del capítulo 7 proceden de la versión web de CALP.
- No se pudo leer el informe completo de la auditoría de WFP sobre comercios en Jordania y Líbano
  (AR/17/03).
- Las fechas de 4.11 y 4.16 son las que muestra la página; no se comprobaron por otra vía.

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-06 | Versión inicial | /research-market, Research 1 | Pendiente |
