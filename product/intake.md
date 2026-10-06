# Product Intake — NexoAid

> Ruta: product/intake.md
> Estado: VALIDADO — v1 (2026-10-06)
> Etapa: Problem Discovery
> Responsable: Paola Espejo

## 1. Request / trigger
Proyecto individual del curso AI-First Product Manager (Alaimo Labs). La responsable propone
como caso de trabajo NexoAid, una iniciativa para investigar cómo las organizaciones humanitarias
gestionan y entregan asistencia monetaria o basada en valor a personas afectadas por crisis.
- Sponsor / responsable: Paola Espejo — Fuente: intake aportado por la responsable (2026-10-06).
- Disparador: ejercicio del curso. Sí hay referencia de mercado (OMNIAID), pero no hay un cliente,
  una organización ni un encargo real detrás. — Estado: hecho (declarado por la responsable).

## 2. Preliminary purpose (PRELIMINAR)
Comprender:
1. cómo se entrega y se usa hoy la asistencia monetaria o basada en valor;
2. qué actores participan;
3. qué restricciones enfrentan;
4. dónde hay problemas lo bastante relevantes para justificar una intervención de producto.

El propósito NO es crear una tarjeta, una billetera ni un sistema de vouchers.
Estado: decisión de la responsable. El propósito en sí es preliminar.

## 3. Product or initiative context
- Nombre provisional: NexoAid. Producto nuevo dentro del ejercicio; no existe nada construido.
- Naturaleza preliminar: producto digital/financiero para operaciones de asistencia humanitaria.
- Tipo de negocio: comercial B2B / B2B2C — **supuesto**, a confirmar en /start-product.
- Hipótesis de estructura de usuarios (**supuesto**):
  - Comprador/decisor: organización humanitaria, institución pública o entidad que ejecuta programas.
  - Usuarios operativos: equipos de programas y finanzas; comercios.
  - Usuario final: persona receptora de asistencia.
- Mecanismos de transferencia que se usan en el sector (contexto secundario): efectivo,
  transferencias bancarias, mobile money, billeteras digitales, vouchers físicos y digitales,
  tarjetas, comercios autorizados y combinaciones de varios de ellos. La elección depende del
  contexto operativo, la infraestructura, la conectividad y la población.
- Proceso actual hipotético, **no validado**, solo sirve para orientar preguntas:
  definición del programa y la población → registro → monto/derecho → selección del mecanismo →
  acceso al valor → uso → registro de la operación en el comercio → información a la organización →
  conciliación/liquidación → monitoreo y reporte.

## 4. Actors
| Actor | Role in the context | What is known | Source / status |
|---|---|---|---|
| Persona receptora | Recibe y usa el valor asignado | Nada de fuente primaria | supuesto |
| Comercio / proveedor local | Entrega bienes o servicios; luego recibe el pago | Nada de fuente primaria | supuesto |
| Organización humanitaria | Diseña y administra el programa; comprador potencial | Nada de fuente primaria | supuesto |
| Equipo de programas | Define población, criterios y modalidad | — | supuesto |
| Equipo financiero | Fondos, conciliación, pagos | — | supuesto |
| Equipo MEAL / IM | Supervisa la información del programa | — | supuesto |
| Donante | Financia; puede exigir trazabilidad | — | supuesto |
| Proveedor financiero | Procesa o liquida operaciones | — | supuesto |
| Autoridad / regulador | Define reglas aplicables | Varía por país | supuesto |
| Equipo tecnológico | Integraciones e infraestructura | — | supuesto |

Todos los roles son preliminares. Ningún actor tiene todavía evidencia primaria.

## 5. Existing systems, processes, or prior work
- Soluciones de mercado (referencia, no modelo para NexoAid):
  - OMNIAID: chip cards, vouchers/cupones, dispositivos offline especializados, plataformas
    de pago móvil; control programable del gasto, registro de transacciones y sincronización
    posterior. — Fuente: oferta pública de OMNIAID.
  - Humansis: gestión de programas, soporte offline, smartcards, vouchers digitales,
    trazabilidad. — Fuente: oferta pública de Humansis.
- Antecedente fuera del sector humanitario: Ingreso Mínimo Garantizado (Bogotá) exige smartphone
  para ciertos canales y ofrece alternativas a quien no lo tiene. — Fuente: Integración Social.
- Reglas del proyecto: WORKFLOW.md v2 (validado el 2026-10-05).
- Metodología del curso: documento "1. Skills Alaimos". No está en la carpeta del proyecto.

## 6. Known constraints and dependencies
Todas proceden de conocimiento general del sector. Ninguna se ha verificado para un país
o programa concreto.
- Infraestructura: conectividad limitada o intermitente, electricidad inestable, poca cobertura
  bancaria, pocos dispositivos. — supuesto de contexto (respaldo parcial: FMI).
- Regulación: normativa financiera, KYC, AML/CFT, reglas nacionales de pagos, protección
  del consumidor. — conocimiento general; varía por país; por verificar.
- Protección de datos: datos personales y posiblemente sensibles. Habrá que pensar en
  minimización, control de acceso, consentimiento, retención, seguridad y reparto de
  responsabilidades. — supuesto de diseño; por verificar.
- Escenarios operativos que cualquier solución tendría que contemplar: pérdida del medio de
  acceso, falta de conectividad, comercio que no puede procesar, errores de registro,
  transacciones duplicadas, conciliación, cambio de monto, baja del programa.
  — supuesto; sin priorizar.

## 7. Facts and evidence available
Todo es **evidencia secundaria**. Falta registrar los enlaces exactos.
- H1. Existen múltiples mecanismos tecnológicos para distribuir asistencia monetaria o en vouchers.
  — Fuente: OMNIAID, Humansis.
- H2. OMNIAID ofrece al menos cuatro modalidades: chip cards, vouchers/cupones, dispositivos
  offline y pagos móviles. — Fuente: OMNIAID.
- H3. Hay contextos donde las limitaciones de conectividad o de infraestructura de pagos afectan
  la entrega de transferencias; en ellos, e-vouchers, smart cards y procesamiento offline han
  permitido sostener operaciones. — Fuente: FMI (eLibrary IMF).
- H4. Algunos canales digitales dependen de dispositivos o infraestructura concretos
  (por ejemplo, el smartphone en ciertos canales de IMG en Bogotá). — Fuente: Integración Social.
- H5. Algunos sistemas de vouchers mejoran la resiliencia operativa, pero pueden restringir la
  elección a ciertos comercios. — Fuente: FMI (eLibrary IMF).

## 8. Assumptions not yet verified
Razón común a todos: no hay evidencia primaria de ningún actor.
- S1. Algunas organizaciones tienen dificultades para entregar asistencia donde la conectividad es limitada.
- S2. Los mecanismos actuales generan problemas de conciliación entre organizaciones y comercios.
- S3. Las organizaciones necesitan más trazabilidad sobre el uso de los recursos.
- S4. Algunas personas receptoras quedan excluidas cuando la modalidad exige smartphone, cuenta
  o conectividad. (H4 lo hace plausible, pero viene de un programa público, no humanitario.)
- S5. Los comercios tienen dificultades para verificar que una transacción será reconocida y pagada.
- S6. Las organizaciones usan varios sistemas no interoperables (registro, transferencias,
  comercios, reporting).
- S7. Operar offline es importante en ciertos contextos.
- S8. Las organizaciones valoran poder restringir el gasto.
- S9. El modelo de negocio es B2B/B2B2C y el comprador es la organización humanitaria.
- S10. Hay tres tipos de usuario diferenciados (final, operativo, comprador).

## 9. Decisions already made
- Nombre provisional: NexoAid. — Responsable: Paola.
- Etapa: Problem Discovery; se empieza por el problema y no por la tecnología. — Responsable: Paola.
- No se define todavía: tarjeta con chip, voucher, app móvil, POS, billetera, blockchain,
  plataforma financiera, integración bancaria, arquitectura offline ni IA.
  Tampoco se enuncia aún el problema. — Responsable: Paola.
- OMNIAID se usa como referencia de mercado, no como modelo de funcionalidades. — Responsable: Paola.
- NexoAid se trata como producto nuevo dentro del ejercicio. — Responsable: Paola.
- Flujo de trabajo y entornos según WORKFLOW.md v2. — Responsable: Paola.

## 10. Open questions and pending decisions
Decisiones pendientes (Responsable: Paola):
1. Contexto geográfico.
2. Tipo de organización del segmento inicial.
3. Programas de asistencia que se investigarán.
4. Actores que necesitan evidencia primaria y si hay acceso real a ellos.
5. Señales que merecen convertirse en oportunidades de investigación.

Preguntas abiertas:
- Personas receptoras: cómo reciben la asistencia, qué mecanismos usan de verdad, dónde aparecen
  dificultades, qué pasa sin smartphone o sin conectividad, qué alternativas usan cuando algo falla.
- Comercios: cómo se incorporan, cómo verifican, cuándo cobran, cómo concilian, qué pasa
  cuando hay discrepancias.
- Organizaciones: cómo eligen la modalidad, qué sistemas usan, qué necesitan controlar,
  dónde hay procesos manuales, duplicaciones o necesidades de integración.
- Finanzas: cómo concilian, qué datos comparan, cuántos sistemas intervienen, qué errores
  aparecen, cuánto trabajo manual exige.
- Contexto: país, entorno urbano/rural, fase (emergencia, recuperación o programa recurrente),
  infraestructura financiera disponible.
- Desconocidos transversales: frecuencia, severidad, coste operativo, volumen afectado,
  alternativas actuales, disposición a cambiar y a pagar.

## 11. Conflicts or uncertainties in the sources
- **Evidencia análoga.** H4 viene de un programa público de transferencias en Bogotá, no de una
  operación humanitaria; su validez para el contexto humanitario es incierta.
- **Fuentes sin trazabilidad completa.** OMNIAID, Humansis, FMI e Integración Social están
  citadas por nombre, sin URL ni fecha de consulta.
- **Tensión visible, sin resolver:** control programático (organización/donante) frente a
  libertad de elección (persona receptora). — Fuente: FMI (H5) + supuesto S8.

## 12. Handoff to /start-product
- Contexto reutilizable:
  - propósito preliminar, mapa de actores, proceso hipotético;
  - hechos H1–H5 (secundarios), restricciones, decisiones de la sección 9.
- Lo que /start-product debe confirmar:
  - tipo de producto (nuevo, comercial B2B/B2B2C);
  - quién compra, quién opera y quién es usuario final;
  - segmento inicial y contexto geográfico;
  - qué actores entran en alcance.
- Supuestos que NO deben tratarse como evidencia:
  - S1–S10;
  - la estructura de tres usuarios;
  - el proceso hipotético;
  - todas las restricciones regulatorias y de infraestructura de la sección 6.
- Estado de la evidencia: contexto secundario. No hay problema validado, oportunidad definida
  ni solución seleccionada.

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-06 | Versión inicial del intake de NexoAid | Intake aportado por la responsable; /prepare-product-context | Sí |
