# Priorización estratégica de oportunidades — NexoAid

> Ruta: product/research/opportunity-prioritization.md
> Estado: VALIDADO — v1 (2026-10-07)
> Etapa: Problem Discovery
> Fecha: 2026-10-07
> Responsable: Paola Espejo
> Origen: product/research/cva-market-opportunities.md v1.1 y product/research/market-beliefs.md v1.1
> Cadena de research: creencias (market-beliefs.md) → exploración del mercado y comparación de oportunidades (cva-market-opportunities.md) → recomendación para research primario (este documento)

Este documento responde una sola pregunta: con toda la evidencia disponible, ¿qué problemática concreta merece avanzar primero en discovery, y por qué?

Es la síntesis estratégica de `cva-market-opportunities.md` y no repite su análisis. Solo usa la evidencia de ese documento y de `market-beliefs.md`; no se hicieron búsquedas nuevas.

No propone solución, funcionalidades, MVP ni arquitectura.

## Recomendación principal

La primera candidata para seguir en discovery es esta:

*Los equipos de Finanzas y de Cash/CVA de las organizaciones que pagan asistencia a través de uno o varios proveedores financieros no logran cerrar a tiempo, persona por persona, el recorrido que va de la lista aprobada al pago confirmado y al registro contable. En cada traspaso la información cambia de formato y de sistema. Por eso detectan tarde los duplicados, los pagos marcados como exitosos que no se entregaron y los fondos que nadie cobró. Los cierres financieros acumulan descuadres y las auditorías encuentran controles insuficientes.*

Corresponde a OP3 de `cva-market-opportunities.md`. Incluye como causa probable OP2, la integridad de la lista y del identificador. Con la evidencia actual no se pueden separar con seguridad, así que conviene investigarlas juntas.

## Por qué esta problemática

Es la única del research que reúne, con evidencia verificable, dolor operativo y señales de que alguien gasta dinero en el tramo donde ese dolor ocurre.

**Severidad.**
- Una auditoría de OIOS sobre ACNUR en Ucrania encontró 71 M USD sin conciliar entre el sistema de pagos y el sistema contable.
- La auditoría de CashAssist halló pagos marcados como exitosos con importe cero: más de cinco mil solo en Kenia.
- Moldavia recuperó 3,6 M USD de tarjetas inactivas.
- Hubo comisiones cobradas sobre efectivo que nunca se retiró.

Ninguna otra área del research tiene ese grado de cuantificación.

**Recurrencia.** No son incidentes aislados. El tramo se recorre en cada ciclo de pago:
- En Sudán del Sur, las conciliaciones se aprobaban de tres a seis meses después de la distribución, con más de cien hojas Excel.
- En cinco de siete operaciones auditadas de ACNUR, los datos se pasan a mano entre el sistema y el proveedor financiero.
- En Chad, el tablero de conciliación no funcionaba porque las fechas de ciclo no coincidían con las de SCOPE.

**Impacto.** El problema afecta a la vez a tres cosas:
- el control financiero: estados financieros incorrectos y comisiones sin registrar;
- la protección del dinero: duplicados y fondos no cobrados que se detectan tarde;
- la carga de trabajo: Oxfam documentó cinco personas a tiempo completo dedicadas a conciliar a mano.

**Demanda.** Es la oportunidad con el comportamiento de compra más claro de todo el research:
- Entre 2024 y 2026, Prosper Global (antes Mercy Corps), Plan, CRS y Solidarités licitaron acuerdos que unen proveedor financiero y tecnología. En algunos casos incluían dashboard o conciliación.
- Diakonie y Relief International licitaron plataformas de gestión de CVA por separado. La de Relief International no se pudo leer.
- Una ONG local en Siria licitó un sistema con conciliación offline.

Ninguna de esas compras tiene como objeto solo la conciliación, pero todas tocan el tramo donde está el problema.

**Comprador.** Hay uno plausible: el área de procurement de las INGO grandes y medianas, que ya compra este tramo como coste de proyecto o dentro del contrato con el proveedor financiero.

**Competencia.** Existe, pero es parcial: plataformas de CVA como RedRose, HOPE, 121 o Humansis; herramientas internas de la ONU; portales de los proveedores financieros; ERP y Excel. Las fallas aparecen incluso con plataforma corporativa. Que el gap esté en conciliar persona a persona entre varios proveedores y el ERP es una **inferencia**: no se encontró ninguna oferta que lo resuelva, pero eso no prueba que no exista.

**Tendencia.** La necesidad sube por dos razones: hay más proveedores y rieles de pago por país (ACNUR gestiona 78 contratos con proveedores financieros) y las recomendaciones de auditoría vencen en 2026. Que esto se convierta en mercado es incierto, porque los presupuestos se contraen.

## Por qué no elegiría las otras primero

**Quejas y feedback vinculados a la corrección de datos y pagos (OP7).** El problema está bien documentado: cinco auditorías recientes muestran que la queja no llega hasta la corrección, y la CHS señala este compromiso como el más débil del sector. Pero lo que se compra hoy es el servicio de central de llamadas, el software de canal y de CRM es barato o gratuito, y la propia CHS atribuye el fallo a la práctica más que a la herramienta. Es importante, pero su atractivo comercial está menos demostrado.

**Deduplicación entre organizaciones (OP1).** El problema es intenso y tiene ahorros medidos en cientos de millones. Pero su cuello de botella es la gobernanza, no la tecnología. Existen herramientas gratuitas de la ONU (Building Blocks, HOPE) y la ONU está consolidando una identidad común en el marco de UN80. El comprador es débil y el espacio para terceros se reduce.

**Entrega con liquidez o conectividad limitada (OP9).** Es probablemente el dolor más grave para las personas, con comisiones del 20 % al 60 % en Gaza. Pero su causa es la liquidez, la regulación y el de-risking, y entrar exige ser un proveedor financiero.

**Carga de cumplimiento trasladada a los actores locales (OP10).** El problema está documentado. Pero quien lo sufre no paga, el intermediario no muestra señales de que pagaría y la solución que plantean las fuentes es un acuerdo político.

**Otras áreas:**
- Reporting a donantes (OP5): el estándar lo controla el donante, las herramientas son baratas y la evidencia sobre la carga es de 2016.
- Monitoreo por terceros (OP6): se compra como servicio de campo, no como producto.
- Contratación de proveedores financieros (OP4): se compra el proveedor, no su gestión.
- Comercios (OP11): poca evidencia y tendencia a la baja.
- Protección social (OP12): el comprador es el gobierno, fuera del perfil B2B.
- Detección de anomalías (OP8): no hay demanda observable fuera del screening; probablemente se revise mejor como parte de la problemática principal.

## Qué la hace atractiva desde negocio

La diferencia entre un problema importante y uno monetizable está en si alguien tiene a la vez el incentivo y una línea de presupuesto. Aquí hay indicios de las dos cosas, aunque incompletos.

**Incentivos.**
- El dinero mal conciliado es dinero en riesgo.
- Las auditorías obligan a cerrar recomendaciones con plazo.
- Los donantes exigen trazabilidad; en el caso de ECHO, como elemento obligatorio de su política de cash.

**Quién paga y con qué presupuesto.**
- Los compradores más plausibles son las INGO grandes y medianas que pagan a través de proveedores financieros. Hoy canalizan ese gasto de dos maneras: dentro del contrato con el proveedor (como comisión o servicio) o como coste directo de proyecto, cuando licitan una plataforma.
- ECHO considera elegibles los servicios de IT de la oficina del proyecto y no incluye el software entre los costes no elegibles. Pero no financia la transformación digital de sus socios, y los costes indirectos están limitados al 7–8 %.
- Las agencias ONU tienen capacidad de pago, pero construyen sus propios sistemas.
- Las ONG locales tienen necesidad, pero presupuestos mínimos.

**Por qué es importante pero no necesariamente monetizable.**
- La señal de compra existe, pero viene empaquetada: las INGO prefieren comprar pago y tecnología en un mismo contrato. El proveedor financiero puede ser a la vez el canal por el que se compra y el principal sustituto.
- El sector se contrae: Prosper Global perdió cerca de dos tercios de su financiación gubernamental.
- No hay precios ni montos públicos de la parte tecnológica, así que el tamaño direccionable no se puede estimar.

## Qué la hace atractiva desde producto

**Dónde está el problema.** En el tramo que va de la lista final a la instrucción de pago, de ahí al informe del proveedor, luego a la conciliación persona a persona, al tratamiento de no cobrados y reversiones, y por último al cierre contable.

**Quiénes intervienen.**
- Programas aporta la prueba de entrega.
- Finanzas valida.
- Logística gestiona el contrato con el proveedor.
- Los socios ejecutores preparan las listas.
- Gestión de información mantiene el registro.

Las vacantes de IFRC en Caracas, Colombia y Jamaica muestran roles de CVA y de Finanzas que comparten la conciliación.

**Dónde se concentra el trabajo manual.**
- Exportar e importar archivos con un formato distinto para cada proveedor.
- Cruzar listas en las que los identificadores faltan o han cambiado. OIOS cuenta casi 224.000 registros sin identificador único y 14,5 M USD pagados a identificadores inválidos en Afganistán.
- Cotejar informes que llegan con distinta periodicidad.
- Gestionar los no cobrados mediante peticiones por escrito.
- En contextos sin conectividad, conciliar con hojas impresas.

**Por qué las soluciones actuales no lo resuelven del todo.**
- Cada pieza resuelve una parte: el portal del proveedor ve sus transacciones, el ERP ve el libro contable, la plataforma de CVA ve a la persona.
- Las fallas documentadas aparecen justo donde esas piezas se cruzan.
- La evidencia de que las plataformas existentes resuelven el cruce es solo comercial o de los propios dueños.
- El caso de Sierra Leona muestra que, en contextos sencillos, el acceso directo a la plataforma del proveedor puede bastar: se pasó de conciliar a fin de mes a hacerlo a diario.

**Interoperabilidad.** Aquí aparece como **causa**, no como el problema. La falta de un identificador común y de formatos compartidos es lo que produce el descuadre, el retraso y el duplicado. Quien vive el problema no dice "falta interoperabilidad"; dice "no cuadra", "llegó tarde" o "pagamos dos veces". Por eso la recomendación se formula sobre el cierre del ciclo de pago. La interoperabilidad podría ser una capacidad de solución más adelante, pero eso no se decide ahora.

## Principal riesgo de equivocarnos

**El sesgo de la evidencia.** Casi toda la evidencia cuantitativa viene de auditorías de ACNUR y del PMA, que son el segmento que menos compra a terceros.

**Evidencia primaria que refutaría la recomendación.** La recomendación se debilita si las INGO medianas y las ONG locales:
- trabajan con un solo proveedor financiero por país;
- consideran suficiente el portal o el dashboard del proveedor;
- dedican horas, no días, a conciliar en cada ciclo;
- no mencionan la conciliación entre sus tres problemas principales cuando se pregunta sin sugerirla.

**Comportamientos que la debilitarían.**
- Que Finanzas absorba el problema sin que Programas lo note.
- Que nadie recuerde haber intentado cambiar el proceso ni haber pedido presupuesto para hacerlo.
- Que procurement solo esté dispuesto a pagar este tramo dentro del contrato con el proveedor financiero.

**Soluciones existentes que podrían mostrar que el problema ya está resuelto.**
- Que los usuarios de RedRose o 121 confirmen que el cruce persona a persona ya funciona bien.
- Que los acuerdos marco con dashboard, como el de Plan, cubran la conciliación de forma satisfactoria.

**Si la causa es otra.** Si la raíz resulta ser sobre todo disciplina de proceso y calidad del registro, el problema seguiría existiendo, pero el foco se desplazaría hacia la lista y el identificador.

## Segunda mejor alternativa

Se mantiene en observación la problemática de **quejas y feedback vinculados a la corrección de datos y pagos (OP7)**. Comparte el mismo tramo del ciclo y tiene a su favor:
- evidencia reiterada de que la queja no llega hasta la corrección;
- financiación específica (la partida de AAP del CERF) y compras de servicio (el RFP de ACNUR en Pakistán);
- un punto de entrada en América Latina: la auditoría del PMA en Ecuador.

Podría pasar por delante de la recomendación principal si las entrevistas muestran alguna de estas cosas:
- que la conciliación ya está razonablemente cubierta por los proveedores financieros;
- que los errores de pago se descubren sobre todo por las quejas de las personas;
- que existe un comprador con presupuesto propio para cerrar ese ciclo, distinto de la central de llamadas.

## Decisión recomendada

Con la evidencia secundaria disponible, la recomendación es:

- **Avanzar primero** con el cierre del ciclo de pago con proveedores financieros y la conciliación, e investigar a la vez la integridad de la lista y del identificador como su probable causa raíz.
- **Mantener como alternativa** las quejas y el feedback vinculados a la corrección de datos y pagos.
- **No priorizar por ahora** la deduplicación entre organizaciones, la entrega con liquidez o conectividad limitada, la integración con protección social, la contratación de proveedores financieros, el monitoreo por terceros ni la gestión de comercios.
- **Dejar en reserva** la carga de cumplimiento trasladada a los actores locales, hasta que aparezca un comprador.

**Nivel de confianza de la recomendación: medio.**
- La confianza es **media** para el orden relativo: esta problemática supera a las demás en casi todos los criterios con evidencia propia, y ninguna alternativa combina dolor y señales de compra como ella.
- La confianza es **baja** para su atractivo absoluto: la severidad está probada sobre todo en la ONU, la frecuencia fuera de la ONU es desconocida, la compra observada viene empaquetada con el proveedor financiero y el gap competitivo es una inferencia.

## Siguiente paso

Antes de formular una oportunidad definitiva, hay que validar con investigación primaria dos cosas: si el problema que documentan las auditorías de la ONU existe con la misma intensidad en las INGO medianas, y quién lo pagaría.

**Actor prioritario a entrevistar.**
- Primer perfil: responsable de Finanzas de país, o Cash/CVA Finance Officer, de una INGO mediana que trabaje con dos o más proveedores financieros en el mismo país. Los consorcios de Colombia, como VenEsperanza, son un punto de acceso plausible.
- Segundo perfil: la persona de procurement que redactó una licitación de proveedor financiero con tecnología.

**Preguntas críticas.**
1. Cuéntame cómo cerraste el último ciclo de pago, desde la lista aprobada hasta darlo por cerrado en contabilidad: qué pasos seguiste, quién intervino y qué archivos se movieron.
2. Piensa en la última vez que algo no cuadró: ¿cómo lo detectaste, cuánto tardaste y quién tuvo que intervenir?
3. ¿Qué te entrega cada proveedor financiero y qué tienes que hacer tú con eso antes de poder cerrar?
4. ¿Cuánto tiempo dedica el equipo a esto en cada ciclo, y qué deja de hacerse por ello?
5. ¿Alguna vez se intentó cambiar este proceso? ¿Quién lo decidió, con qué presupuesto y qué pasó?

**Evidencia que confirmaría la problemática.**
- Varios días de trabajo manual por ciclo.
- Excepciones recurrentes con consecuencias concretas: pagos retrasados, cierres o reportes demorados, hallazgos de auditoría.
- Intentos previos de resolverlo, con gasto asociado.
- Un dueño de presupuesto identificable.

**Evidencia que la refutaría.**
- Un solo proveedor por país.
- Un portal o dashboard del proveedor que ya resuelve el cruce.
- Un esfuerzo de horas, no de días.
- Que no aparezca entre los problemas prioritarios.
- Que nadie haya invertido nunca en cambiarlo, ni esté dispuesto a hacerlo fuera del contrato con el proveedor.

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-07 | Versión inicial: síntesis gerencial elaborada a partir de cva-market-opportunities.md | Instrucción de la responsable de guardar la síntesis como tercer documento de research | Sí |
