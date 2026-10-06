---
source: secondary
method: web
date: 2026-10-05
question: ¿Existe, es frecuente, cuesta y es prioritario el problema del fraude de pago, los contracargos y el abuso de reembolsos en las pymes de e-commerce con tienda propia; quién lo sufre y quién paga; cómo lo resuelven hoy; y qué deja sin cubrir el mercado de soluciones?
opportunity: fraude-contracargos-pymes-ecommerce
---

# Research: fraude, contracargos y abuso de reembolsos en pymes de e-commerce

> Estado: **VALIDADO — v1 (2026-10-05).**
> Ruta: `product/research/2026-10-05-2337-fraude-contracargos-pymes-ecommerce.md`.
> Método: WebSearch + WebFetch, ejecución secuencial, consultas del 2026-10-05. Reutiliza datos del
> research `2026-10-05-1853-comparativa-problemas-pymes-ecommerce.md` (validado).
> Oportunidad: `fraude-contracargos-pymes-ecommerce` (candidata E). **Su brief sigue en BORRADOR** y
> no está guardado: no se cierra mientras F3 se solape con la candidata D.
> Integra el competitive scan de la candidata como §9.
> Misma estructura que los research de inventario (`…-2320-…`) y margen (`…-2259-…`).
> No modifica el brief, overview, intake, F2 ni las creencias.
> Etiquetas: **P** primaria publicada · **S** secundaria · **V** proveedor con interés comercial ·
> **I** inferencia nuestra · **?** vacío. Lo no consultado: `[conocimiento del modelo — verificar]`.
> Subproblemas: **(F1)** fraude de pago de terceros · **(F2)** fraude amistoso / uso indebido por el
> titular · **(F3)** abuso de reembolsos y de políticas · **(F4)** gestión de disputas y penalizaciones.
> **Regla provisional de delimitación con D** (responsable del proyecto, 2026-10-05): intención de
> engañar → E (fraude); devolución o reclamación legítima sin intención de engañar → D (devoluciones).
> Límite: evidencia **secundaria y de mercado**. Ninguna fuente es del segmento.

## Resumen: lo que cambia decisiones

1. **La mejor fuente secundaria de las cuatro candidatas**: MRC 2025 (n = 1.082, metodología
   publicada, **subgrupo de pymes** 50.000 $–5 M$, 26 % de la muestra), aunque patrocinada por Visa y
   respondida por profesionales de fraude. En pymes: fraude = **2,8 % de los ingresos**, éxito en
   disputas **16,4 %**, **27 %** de los pedidos revisados a mano.
2. **El problema crece en F2 y F3, no en F1.** El abuso de reembolsos es el fraude más común (47 %) y
   crece para el 57 %; los falsos "no recibido" afectan al 50 %. El fraude de tarjeta de terceros (F1)
   es el que **ya cubren** el proveedor de pagos, 3DS/SCA y Shopify Protect.
3. **Las reglas de las redes cambian en 2025–2026 en dos direcciones.** Visa VAMP sube lo que está en
   juego (umbrales más bajos, tarifas por disputa); Visa CE 3.0 y Mastercard First-Party Trust dan al
   comercio **herramientas nuevas** para ganar las disputas de F2. Es un "por qué ahora" verificable
   que empuja a la oferta tanto como al problema.
4. **No aparece en las encuestas generales de prioridades** de comercios; solo en las de
   profesionales de fraude.

---

## 1. Magnitud del problema

| Pregunta | Dato | Muestra y límites | Etiqueta | Fuente |
|---|---|---|---|---|
| **¿Cuántos sufren fraude?** | El 98 % de los comercios sufrió algún tipo de fraude en 12 meses | MRC 2025: n = 1.082; 38 países (NA 45 %, Europa 20 %, APAC 24 %, LatAm 11 %); 46 % grandes, 26 % mid-market, **26 % pymes (50.000 $–5 M$)**; oct.–nov. 2024; patrocinado por Visa Acceptance Solutions y Verifi | S | [verificado: https://info.merchantriskcouncil.org/hubfs/Documents/Reports/Fraud%20Reports/2025_Global_Fraud_and_Payments_Report.pdf — 2026-10-05] |
| **Peso económico** | Fraude = **3,1 %** de los ingresos (global), **2,8 % en pymes**; 3,0 % de los pedidos | Ídem | S | Ídem |
| **(F3) Abuso de reembolsos y políticas** | **47 %** (1.er tipo de fraude); crece para el **57 %** (para el 22 %, más de un 50 %); falsos "no recibido" **50 %**; devoluciones usadas o dañadas **46 %**; fuera de plazo **39 %**; manipulación del artículo o del seguimiento **37 %** | Ídem | S | Ídem |
| | El 9 % de las devoluciones es fraudulento; el 45 % de los compradores cree aceptable "bend the rules" | Retail de EE. UU.; metodología no consultada | S/V (NRF + Happy Returns) | [verificado: https://www.nrf.com/research/2025-retail-returns-landscape — 2026-10-05] |
| **(F2) Fraude amistoso** | 42 % de los comercios; crece para el 62 %; 20 % de las disputas fraudulentas; coste medio de resolver una disputa **78 $** | MRC | S | Ídem MRC |
| | El 72 % de los contracargos de los emisores son fraude: 59 % de terceros, **13 % amistoso**; 28 % quejas genuinas | Mastercard *State of Chargebacks 2025*, vía prensa; **unidades de volumen ambiguas** en la fuente secundaria (261 → 324 "millones", 2025–2028) | S/V | [verificado: https://www.electronicpaymentsinternational.com/?p=79651 — 2026-10-05] |
| | El 73 % dice que al menos el 20 % de sus contracargos son fraude amistoso | Riskified + Paladin, 300+ responsables de contracargos; 2024 | V | [verificado: https://www.crowdfundinsider.com/2024/03/223112-online-retailers-leave-significant-number-of-chargebacks-undisputed-contributing-to-lost-revenue-report/ — 2026-10-05] |
| **(F1) Fraude de terceros** | EEE: fraude con tarjeta 1.329 M€ en 2024 (**+29 %**); fraude total en pagos 4.200 M€; **17 veces mayor** cuando el comercio está fuera del EEE (sin SCA) | Supervisores (EBA/BCE) | **P** | [verificado: https://www.eba.europa.eu/publications-and-media/press-releases/joint-eba-ecb-report-payment-fraud-strong-authentication-remains-effective-fraudsters-are-adapting — 2026-10-05] |
| | UK: fraude de compra a distancia de casi 400 M£ en 2024 (**+11 %**), 2,6 M de casos (**+22 %**) | UK Finance (asociación bancaria) | **P** | [verificado: https://www.ukfinance.org.uk/news-and-insight/press-release/fraud-report-2025-press-release — 2026-10-05] |
| **(F4) Disputas** | Éxito en disputas 17,4 % global; **16,4 % pymes**; NA 17,9 %, Europa 15,1 %, **LatAm 11,5 %** | MRC | S | Ídem MRC |
| | ≈ **60 %** deja sin disputar al menos 2 de cada 4 contracargos; el **55 %** dice que su proceso consume demasiado tiempo | Riskified + Paladin | V | Ídem Riskified |
| **Coste total** | **5,13 $** por cada 1 $ de pérdida directa (EE. UU.), 5,23 $ (Canadá); 37 % con pérdidas importantes de ingresos | LexisNexis 2026: 513 responsables de riesgo y fraude; EE. UU. y Canadá | V | [verificado: https://risk.lexisnexis.com/about-us/press-room/press-release/20260624-tcof-retail-and-commerce — 2026-10-05] |
| **Pedidos buenos rechazados** | El 32 % rechaza por error el 2–5 % de los pedidos legítimos; el 14 %, más del 10 % | MRC | S | Ídem MRC |

**Lectura (I):** hay **frecuencia medida** (MRC, con subgrupo de pymes) y **peso económico** del
2,8–3,1 % de los ingresos: más que en C y comparable a A. Pero son **porcentajes de comercios** que
sufren cada tipo, no de pedidos afectados en pymes, y MRC solo encuesta a empresas con responsables de
fraude.

## 2. Prioridad

| Encuesta | ¿Aparece el fraude? | Posición | Etiqueta |
|---|---|---|---|
| NFIB 2024 | **No** | — | P (research 1853) |
| SBR / Morning Consult 2025 | **No** | — | S |
| Linnworks 2025 | **No** | — | V |
| Jungle Scout 2025 | **No** (competencia de terceros, no fraude) | — | V |
| Sendle 2024 | **No** | — | V |
| Jitterbit 2022 | **No** | — | V |
| ChannelEngine 2025 | **No** (sí devoluciones complejas, 48 %) | — | V |
| SmartScout 2025 | Indirectamente (suspensiones de cuenta 35 %) | — | V |
| MRC 2025 | **Sí** (solo profesionales de fraude) | Reducir fraude y contracargos, 42 % de sus prioridades | S |

**Conclusión explícita:** el fraude, los contracargos y el abuso de reembolsos **no aparecen en
ninguna encuesta general de prioridades de comercios**; solo en las de profesionales de fraude.
Prioridad declarada parecida a la de C y menor que la de A.

## 3. Segmento

| Dimensión | Evidencia | Etiqueta |
|---|---|---|
| **Tamaño** | Las pymes (50.000 $–5 M$) sufren **menos variedad** de ataques (3,3 tipos frente a 4,6), **menos** fraude amistoso y de pagos en tiempo real, **más** suplantación de identidad; fraude del 2,8 % de los ingresos | S (MRC) |
| **Medios de pago** | Pymes: 3,9 medios de pago (4,6 en grandes); 2,6 pasarelas (3,4); tokenización 26 % (77 %) | S (MRC) |
| **Plataformas** | Shopify Protect: **solo EE. UU.**, solo Shop Pay | P |
| **Tienda propia frente a marketplaces** | En los marketplaces, las disputas las gestiona el marketplace (I). **El problema se concentra en la tienda propia**, coherente con el segmento del overview v3 | I |
| **País** | Ver §8 | — |
| **Quién lo gestiona** | En pymes, **sin dato**. MRC solo encuesta a profesionales de fraude, perfil que la pyme no suele tener (I) | ?, I |

## 4. Quién sufre el problema

| Rol | F1 Fraude de terceros | F2 Fraude amistoso | F3 Abuso de políticas | F4 Disputas | Evidencia |
|---|---|---|---|---|---|
| **Usuario** | Quien revisa pedidos (fundador u operaciones) | Quien prepara las pruebas | **Atención al cliente** | Quien disputa | I; 27 % de pedidos revisados a mano en pymes (MRC, S) |
| **Persona que siente el dolor** | Fundador (pérdida + mercancía) | Fundador (pérdida + tarifa) | Atención al cliente y fundador | Quien disputa (tiempo) | I |
| **Comprador** | Fundador; a menudo **no compra nada** (usa lo que incluye el proveedor de pagos) | Fundador | Fundador | Fundador | I, §9 |
| **Prescriptor** | **El proveedor de pagos** (Stripe, Shopify Payments, PayPal) | Proveedor de pagos y apps de la App Store | Plataforma de devoluciones o atención al cliente (I) | Proveedor de pagos | I |
| **Actor que impone el coste** | Emisor y red de tarjetas | Emisor (decide la disputa) | — | Red y adquirente (programas de control, tarifas) | P (Visa, Mastercard) |

**Lectura (I):** el comprador es el fundador, como en A, pero hay un **tercero que fija las reglas**
(red, emisor, proveedor de pagos) y que además **ya incluye** herramientas.

## 5. Comportamiento actual

| Forma de resolverlo | Evidencia | Etiqueta |
|---|---|---|
| **Funciones del proveedor de pagos o de la plataforma** | Análisis de fraude de Shopify, 3DS dinámico (UE), protección contra pruebas de tarjetas, Shopify Flow, Shopify Protect (EE. UU.); Stripe Radar incluido; PayPal Seller Protection | P (documentación) |
| **Revisión manual** | Pymes: 27 % de los pedidos revisados a mano; ≈ 20 % de los revisados se rechaza | S (MRC) |
| **No disputar** | ≈ 60 % deja sin disputar la mitad o más de sus contracargos | V (Riskified) |
| **Disputar con pruebas** | El 87 % presenta pruebas en disputas de fraude amistoso | S (MRC) |
| **Software especializado** | Chargeflow (420 reseñas), NoFraud/Wyllo (163), Signifyd (90), ClearSale (53) | Fichas (§9) |
| **Garantías tipo seguro** | NoFraud/Wyllo, Signifyd, ClearSale ofrecen garantía de contracargos | Fichas (§9) |
| **Endurecer la política de devoluciones** | Sin datos | ? |
| **Aceptarlo como coste del negocio** | Sin datos directos; los contracargos no disputados lo sugieren (I) | ?, I |

## 6. Coste actual del problema

| Tipo de coste | Dato | Etiqueta |
|---|---|---|
| **Pérdida directa** | 2,8 % de los ingresos en pymes (MRC) | S |
| **Coste total por cada 1 $ perdido** | 5,13 $ (EE. UU.) | V (LexisNexis) |
| **Coste por disputa** | 78 $ de media para resolverla (MRC); tarifa de disputa de Stripe 15 $ [verificado: https://www.nerdwallet.com/business/software/learn/stripe-fees — 2026-10-05] | S |
| **Tarifas por superar el umbral de Visa** | 8 $ por disputa de pago a distancia; riesgo de perder la aceptación de Visa | S [verificado: https://www.ravelin.com/blog/visa-vamp-changes-chargeback-disputes — 2026-10-05] (proveedor) |
| **Horas** | El 55 % dice que el proceso consume demasiado tiempo (V). **Horas por disputa: sin dato** | V / ? |
| **Pedidos buenos rechazados** | 2–5 % para el 32 % (MRC); el 56 % de los retailers de EE. UU. dice que sus medidas antifraude aumentaron la pérdida de clientes (LexisNexis) | S, V |
| **Mercancía perdida por abuso de devoluciones** | **Sin importe** en pymes | ? |
| **Gasto en herramientas** | Gratis (proveedor de pagos) a 250–450 $/mes con garantía; 20–25 % de lo recuperado; 15–29 $ por alerta | Fichas, V (§9) |

**Ninguna ausencia de datos se convierte en estimación.**

## 7. Tendencias y "por qué ahora"

| Tendencia | ¿Afecta al **problema** o a la industria/oferta? | Subproblema | Evidencia | Etiqueta |
|---|---|---|---|---|
| **Visa VAMP** (sustituye a VDMP y VFMP) | **Al problema**: umbral de **2,2 %** (jun. 2025–mar. 2026) y **1,5 %** desde abril de 2026; 8 $ por disputa; control de pruebas de tarjetas (20 %). Un resumen de proveedor indica un mínimo de **1.500 disputas/mes**, que dejaría fuera a muchas pymes (**por verificar**) | F4, F1 | [verificado: https://www.ravelin.com/blog/visa-vamp-changes-chargeback-disputes — 2026-10-05] | S (proveedor) |
| **Visa Compelling Evidence 3.0** (abril de 2023) | **A la capacidad de defensa**: con dos compras previas sin disputa (120–365 días antes) y datos coincidentes (IP, dispositivo, dirección, cuenta), la responsabilidad pasa al emisor. Solo código 10.4 | F2 | [verificado: https://verifi.review.visa.com/compelling-evidence-ce30.html — 2026-10-05] | P (Visa/Verifi) |
| **Mastercard First-Party Trust** | **A la capacidad de defensa**: intercambio de datos comercio–emisor. EE. UU., ampliado en **junio de 2025** a Canadá, **LatAm**, Caribe y APAC. Previsión: contracargos de 42.000 M$ en 2028, *"nearly half"* fraudulentos | F2 | [verificado: https://www.mastercard.com/news/latin-america/en/newsroom/press-releases/pr-en/2025/june/to-counter-friendly-fraud-mastercard-expands-technology-to-new-markets — 2026-10-05] | P (Mastercard, con interés) |
| **Fraude con tarjeta al alza** | **Al problema**: EEE +29 % (2024); UK +11 % en pérdidas, +22 % en casos | F1 | EBA/BCE; UK Finance | **P** |
| **Abuso de devoluciones al alza** | **Al problema**: crece para el 57 % | F3 | MRC | S |
| **Brasil: Pix MED 2.0** | **Al problema** en pagos Pix: botón de contestación obligatorio desde el **1-10-2025**; rastreo de fondos obligatorio desde el **2-2-2026**; **solo fraude y estafas, no desacuerdos comerciales** | F1 (Pix) | [verificado: https://tecnoblog.net/noticias/pix-ganha-novas-regras-para-devolver-dinheiro-de-golpes-veja-o-que-muda/ — 2026-10-05] | S |
| **Más medios de pago (monederos, BNPL, pagos inmediatos)** | **Al problema**: nuevas vías de disputa y fraude; fraude en pagos inmediatos 45 % (MRC) | F1, F2 | MRC (S); Worldpay (research de margen, V) | S, V |
| **IA en el fraude y en la defensa** | **A los dos lados** | Todos | LexisNexis (V); §9 | V |
| **Crecimiento general del e-commerce** | **Solo a la industria** | — | — | — |

**Lectura (I):** E tiene el "por qué ahora" **más concreto y fechado** de las candidatas, pero buena
parte **mejora la defensa** (CE 3.0, First-Party Trust) y la aprovechan proveedores ya existentes. Si
se confirma el mínimo de disputas de VAMP, la presión sobre la pyme pequeña sería menor.

## 8. Geografía

| Dimensión | EE. UU. | Reino Unido | España / UE | Latinoamérica |
|---|---|---|---|---|
| **Evidencia del problema** | MRC (NA 45 %), LexisNexis, Riskified | UK Finance (P) | EBA/BCE (P, EEE); Europa en MRC (20 %). **Nada específico de pymes españolas** (?) | MRC (11 % de la muestra) |
| **Éxito en disputas** | 17,9 % (NA) | ? | 15,1 % (Europa) | **11,5 %**, el más bajo |
| **Autenticación** | Sin SCA obligatoria | SCA `[conocimiento del modelo — verificar]` | **SCA/3DS obligatoria** (PSD2): fraude 17 veces menor con comercio dentro del EEE | Variable `[conocimiento del modelo — verificar]` |
| **Protección nativa** | Shopify Protect (solo EE. UU.) | — | 3DS dinámico de Shopify | ClearSale (Brasil, 3,6 ★); Mercado Pago **?** (documentación no disponible) |
| **Cambios recientes** | VAMP; First-Party Trust | VAMP | VAMP (Europa desde el 1-4-2025) | First-Party Trust (jun. 2025); Pix MED 2.0 |

**No se asume que las cifras de EE. UU. sirvan para España o LatAm.** En España, F1 está **más
contenido por la SCA**, lo que podría desplazar el peso hacia F2 y F3 (I).

---

## 9. Competencia (competitive scan)

### 9.1 Funciones nativas (plataforma y proveedor de pagos)

| Función | Subproblema | Qué cubre | Qué no cubre | Fuente |
|---|---|---|---|---|
| **Análisis de fraude de Shopify** | F1 | Marca pedidos de riesgo con aprendizaje automático (con procesadores de terceros, en Grow, Advanced y Plus) | F2, F3 | [verificado: https://help.shopify.com/en/manual/payments/fraud-prevention/preventing-fraud — 2026-10-05] |
| **Shopify Protect** | F1 (y F2 según la ficha general) | Reembolsa contracargos fraudulentos y sus tarifas | **Solo EE. UU.**, Shop Pay, bienes físicos; envío en 7 días y seguimiento válido; excluye Shop Pay Installments | [verificado: https://help.shopify.com/en/manual/payments/shop-pay/shopify-protect/protect-order-with-shopify-protect — 2026-10-05] |
| **3DS dinámico de Shopify** | F1 | Autenticación en regiones PSD2 | — | Ídem análisis de fraude |
| **Protección contra pruebas de tarjetas / Shopify Flow** | F1 | Bloqueo y reglas para retener o cancelar pedidos | — | Ídem |
| **Stripe Radar** | F1 | Incluido; Radar for Fraud Teams 2–7 ¢ por transacción; disputa 15 $ | F3 | [verificado: https://www.nerdwallet.com/business/software/learn/stripe-fees — 2026-10-05] (S) |
| **PayPal Seller Protection** | F1, F2 ("no recibido") | No autorizadas y "no recibido", con prueba de entrega | **Excluye "muy distinto de lo descrito"** e intangibles | [verificado: https://www.paypal.com/uk/webapps/mpp/ua/seller-protection — 2026-10-05] |

### 9.2 Competencia directa: prevención antes de la compra (F1, F3)

| Herramienta | Segmento | Precio | Adopción | Quejas | Fuente |
|---|---|---|---|---|---|
| **NoFraud** (ficha ahora como **Wyllo**) | Pymes y medianas; incluye **fraude en devoluciones y abuso de políticas** | Gratis (100 pedidos/mes); 250–450 $/mes con garantías de 500–2.000 $ | 4,8 ★ · 163 reseñas | Rechazos ocasionales de pedidos legítimos | [verificado: https://apps.shopify.com/nofraud-chargeback-prevention-and-protection — 2026-10-05] |
| **Signifyd** | Tiendas grandes | % del valor aprobado (por presupuesto) | 4,4 ★ · 90 reseñas (17 % de una estrella) | Factura un 30 % más alta; soporte que no responde; cobra pedidos cancelados | [verificado: https://apps.shopify.com/signifyd/reviews — 2026-10-05] |
| **ClearSale** | Brasil, LatAm | Gratis de instalar; garantía | **3,6 ★ · 53 reseñas (19 % de una estrella)** | Valoraciones polarizadas | [verificado: https://apps.shopify.com/reviews/1995221 — 2026-10-05] |
| **FraudLabs Pro** | Tiendas pequeñas (< 500 pedidos/mes) | Gratis (500 consultas); 29,95–249,95 $/mes | ? | ? | [verificado: https://www.chargeback.io/blog/best-shopify-chargeback-prevention-app — 2026-10-05] (V) |
| **Kount, Riskified** | Grandes y alto volumen | Por presupuesto | ? | ? | Ídem (V); Riskified `[conocimiento del modelo — verificar]` |

### 9.3 Competencia directa: disputas y contracargos (F2, F4)

| Herramienta | Modelo | Precio | Adopción | Quejas | Fuente |
|---|---|---|---|---|---|
| **Chargeflow** | Disputas automáticas con IA; alertas Verifi y Ethoca; red de 20.000+ comercios | **25 % de lo recuperado** + 0,20 $/pedido a partir de 1.000 + alertas | 4,5 ★ · 420 reseñas | Facturación distinta de la anunciada; *"success rate is about 10%"*; pruebas que repiten la factura | [verificado: https://apps.shopify.com/chargeflow — 2026-10-05] |
| **Chargeback.io** | Alertas antes de la disputa + reembolso automático | 15–29 $ por alerta | ? | ? | (V, autor de la comparativa) |
| **Disputifier** | Comisión por disputa ganada | 20 %, tope de 250 $ | ? | ? | (V) |
| **Chargebacks911, Justt, Midigator** | Gestión externalizada | ? | ? | ? | `[conocimiento del modelo — verificar]` |

### 9.4 Sustitutos

- **El proveedor de pagos** (Shopify Payments, Stripe, PayPal): herramientas incluidas; incumbente
  natural.
- **La red de tarjetas**: CE 3.0 y First-Party Trust trasladan la defensa a datos que ya tiene el
  comercio, sin producto nuevo (I).
- **La política de devoluciones** (plazos, condiciones) para prevenir F3 (I).
- **Seguros y garantías** de las propias herramientas.

### 9.5 Soluciones manuales

- Revisión manual de pedidos (27 % en pymes, S).
- Pruebas preparadas a mano en el panel del proveedor de pagos (I).
- No disputar (≈ 60 % deja la mitad o más sin disputar, V).

### 9.6 Matriz de cobertura por subproblema

✓ cubre · ◐ parcial · — no cubre · ? no verificado

| Solución | F1 | F2 | F3 | F4 | Garantía | Pymes fuera de EE. UU. |
|---|---|---|---|---|---|---|
| Shopify (análisis, 3DS, Flow) | ✓ | — | — | ◐ | — | ✓ |
| Shopify Protect | ✓ | ◐ | — | ✓ | ✓ | **— (solo EE. UU.)** |
| Stripe Radar | ✓ | ? | — | ◐ | — | ✓ |
| PayPal Seller Protection | ✓ | ◐ "no recibido" | — | ◐ | ✓ | ✓ |
| NoFraud / Wyllo | ✓ | ? | **✓ (declarado)** | ? | ✓ | ? |
| Signifyd | ✓ | ? | ? | ? | ✓ | ? |
| ClearSale | ✓ | ? | ? | ? | ✓ | ✓ (Brasil) |
| Chargeflow | — | ✓ | — | ✓ | — | ? |
| Chargeback.io / Disputifier | — | ✓ alertas | — | ✓ | — | ? |
| Manual | ◐ | ◐ | ◐ | ◐ | — | ✓ |

**Lectura (I):** F1 y F4 muy cubiertos; F2 con oferta creciente apoyada en las reglas de las redes;
**F3 es la columna con menos ✓** (solo NoFraud/Wyllo lo declara, sin verificar en detalle).

### 9.7 Quejas y abandono

| Patrón | Dónde aparece |
|---|---|
| Facturación inesperada | Signifyd, Chargeflow |
| Retorno de la inversión dudoso | Chargeflow (*"success rate is about 10%"*) |
| Soporte | Signifyd |
| Pedidos legítimos rechazados | NoFraud/Wyllo; 32 % con 2–5 % de rechazos erróneos (MRC) |
| Valoraciones polarizadas en LatAm | ClearSale (19 % de una estrella) |
| Cobertura geográfica limitada | Shopify Protect (solo EE. UU.) |

**Contraevidencia:** notas de 4,4–4,8 en las herramientas principales.

### 9.8 Espacios no cubiertos (hipótesis de mercado)

| # | Espacio | Evidencia | Fuerza |
|---|---|---|---|
| X1 | **Abuso de políticas y reembolsos (F3) en pymes** | Tipo de fraude más común (47 %) y creciente (57 %); columna con menos oferta | Media (S) en el problema; baja en la ausencia de oferta (no verificada) |
| X2 | **Protección equivalente a Shopify Protect fuera de EE. UU.** | Solo EE. UU.; éxito en disputas más bajo en Europa (15,1 %) y LatAm (11,5 %) | Baja-media |
| X3 | **Pymes que no disputan** (aprovechar CE 3.0 y First-Party Trust sin equipo) | ≈ 60 % no disputa la mitad o más (V); reglas que favorecen al comercio (P). **En contra:** Chargeflow y otros ya lo hacen a comisión | Baja (ocupado) |
| X4 | **LatAm** (éxito bajo, Pix, First-Party Trust reciente) | MRC (S); Mastercard (P); ClearSale polarizado | ? (P6) |

### 9.9 Respuestas del competitive scan

1. **¿Saturado?** **Sí en F1 y F4**; **creciente en F2**; **no demostrado en F3**.
2. **Bien resuelto:** filtrado del fraude de terceros (F1), autenticación en la UE, disputas
   automatizadas a comisión (F4) en EE. UU.
3. **Mal resuelto:** abuso de políticas y reembolsos en pymes (F3); protección fuera de EE. UU.; éxito
   en disputas en Europa y LatAm.
4. **¿Espacio?** No en F1 ni F4 genéricos. Quizá en **F3** (X1), que **solapa con D**.
5. **¿Evidencia del hueco?** Problema medido (S) y oferta escasa en F3 **sin verificar**; ninguna
   fuente P sobre pymes.
6. **¿Dónde está el hueco?** En **F3 y en la geografía**, no en el fraude de tarjeta.
7. **¿Comprador?** El fundador; el **proveedor de pagos** es incumbente y prescriptor.
8. **¿Qué depende del país?** Mucho: SCA en la UE, Shopify Protect solo en EE. UU., Pix en Brasil,
   tasas de éxito por región; las reglas de las redes son globales con fechas por región.

---

## 10. Evidencia en contra

| Afirmación en contra | Evidencia | Etiqueta |
|---|---|---|
| **Ya lo resuelven bien** | El proveedor de pagos incluye filtros, 3DS y Shopify Protect gratis en EE. UU.; herramientas con notas de 4,4–4,8 | P, fichas |
| **No es prioritario** | Ausente de todas las encuestas generales de prioridades (§2) | P, S, V |
| **En las pymes es menor** | 2,8 % frente a 3,1 % de los ingresos; menos variedad de ataques; menos fraude amistoso (MRC) | S |
| **Las funciones nativas bastan para F1** | SCA en la UE: fraude 17 veces menor (EBA/BCE) | P |
| **Lo absorbe un tercero** | Proveedor de pagos y redes trasladan responsabilidad (3DS, CE 3.0); en marketplaces, el marketplace | P, I |
| **No pagarían otra solución** | Herramientas incluidas sin coste; modelos a comisión (I); quejas de retorno de la inversión (Chargeflow) | P, V, I |
| **VAMP puede no afectar a las pymes pequeñas** | Mínimo de disputas indicado por un proveedor (por verificar) | S |
| **F3 solapa con D** | Devoluciones usadas o fuera de plazo pueden ser abuso o simple devolución; medir las dos a la vez infla el problema (I) | I |

## 11. Calidad de la evidencia

| Dimensión | Mejor evidencia disponible | Lo que falta |
|---|---|---|
| 1. Magnitud | **S con metodología y subgrupo de pymes** (MRC); **P** para el fraude con tarjeta (EBA/BCE, UK Finance) | Pymes de España y LatAm; pedidos afectados |
| 2. Prioridad | P, S, V sobre la **ausencia** en los rankings; S (MRC) dentro de equipos de fraude | Ranking general que incluya la opción |
| 3. Segmento | S (MRC por tamaño); P (documentación de Shopify) | Quién lo gestiona en pymes |
| 4. Quién lo sufre | I + P (reglas) | Cualquier dato directo |
| 5. Comportamiento | S, V | Datos de pymes |
| 6. Coste | S (2,8 %, 78 $), V (5,13 $) | Horas; importe del abuso de devoluciones |
| 7. Tendencias | **P** (Visa, Mastercard, EBA/BCE, UK Finance); S (VAMP vía proveedor, Pix) | Documento oficial de VAMP |
| 8. Geografía | P (UE, UK); S (regiones de MRC) | España y LatAm en pymes |
| 9. Competencia | Fichas y documentación oficial | Precios de Signifyd, Riskified, Mercado Pago |
| 10. En contra | P, S | — |

**Síntesis:** **la mejor calidad de evidencia de las candidatas analizadas** en magnitud y tendencias,
pero **prioridad declarada tan baja como en C**, y la evidencia sobre pymes procede de un subgrupo de
una muestra de profesionales de fraude.

## 12. Conclusión de la oportunidad

1. **¿Es frecuente?** **Sí, con evidencia S**: 98 % de los comercios sufre algún fraude; abuso de
   políticas 47 % (57 % lo ve crecer); falsos "no recibido" 50 % (MRC). En pymes, menos variedad.
2. **¿Es económicamente importante?** **Moderadamente, con evidencia S**: 2,8 % de los ingresos en
   pymes; 78 $ por disputa; 5,13 $ de coste total por dólar perdido (V). Sin importe del abuso de
   devoluciones en pymes.
3. **¿Es prioritario?** **No hay evidencia de que lo sea**: ausente de las encuestas generales.
4. **¿Quién lo sufre y quién pagaría?** Fundador y atención al cliente; pagaría el fundador, pero el
   **proveedor de pagos** es incumbente, prescriptor y a menudo la solución gratuita.
5. **¿Cómo lo resuelven hoy?** Herramientas del proveedor de pagos, revisión manual (27 %), disputas
   (87 % presenta pruebas), herramientas a comisión, o sin disputar (≈ 60 % deja la mitad o más).
6. **¿Está saturado?** **Sí en F1 y F4; creciente en F2; no demostrado en F3.**
7. **¿Qué está bien resuelto?** Fraude de terceros (proveedor de pagos, SCA), disputas automatizadas a
   comisión, protección en EE. UU. (Shopify Protect).
8. **¿Qué sigue mal resuelto?** Abuso de políticas y reembolsos en pymes (F3); protección fuera de
   EE. UU.; éxito en disputas en Europa y LatAm.
9. **¿Hay un hueco concreto para seguir investigando?** **Sí, uno: F3 (X1)**, el fraude más frecuente
   y creciente con la columna de oferta más vacía. Pero **coincide casi por completo con la parte
   abusiva de D**: sin delimitar D y E no se investiga de forma independiente. X2 y X4 dependen de P6.
10. **¿Qué falta validar con research primario?**
    - Ranking frente a A–D y F.
    - Reparto del dolor entre F1, F2 y F3 en el segmento.
    - Si las pymes distinguen devolución legítima de abuso.
    - Contracargos y reclamaciones abusivas al mes, y si los disputan.
    - Qué incluye su proveedor de pagos y si les basta.
    - País.

## Implicaciones pendientes (no aplicadas)

- **Solapamiento fuerte E–D.** El hueco más concreto de E (F3) es la parte abusiva de las
  devoluciones. **Regla provisional** (responsable del proyecto, 2026-10-05): intención de engañar →
  E; devolución o reclamación legítima sin intención de engañar → D. El brief de E queda en BORRADOR
  hasta cerrar esta delimitación.
- **El proveedor de pagos como incumbente**: a diferencia de A y C, el principal competidor de E es
  gratuito y viene incluido en la pasarela.
- **La geografía cambia el subproblema**: en la UE la SCA reduce F1; en LatAm el éxito en disputas es
  el más bajo.
- Brief, overview, intake, F2 y creencias: **aplazados** hasta comparar las cuatro candidatas.

## Impacto en creencias

Registro validado: overview v3. Las creencias del brief de E (en borrador) se comentan aparte. Nada
de esta tabla se traslada al overview (eso corresponde a `/review-evidence`).

| Creencia | Veredicto | Evidencia |
|---|---|---|
| 1–6 (devoluciones), overview v3 | **No dice nada**, salvo la **1**: el abuso de reembolsos es frecuente (S), lo que da más peso a la vía del abuso que a la de la frecuencia, como ya señalaba el research 1853 | §1 |
| *(borrador E) (a) Prioridad* | **contradice débilmente** (ausente de los rankings generales) | §2 |
| *(borrador E) (b) El dolor está en F2/F3* | **apoya**: F3 es el tipo más común y creciente; F1 cubierto por el proveedor de pagos y la SCA | §1, §9 |
| *(borrador E) (c) Pago y hueco* | **mixto**: hay pago, pero el incumbente es gratuito; el hueco solo aparece en F3 | §5, §9 |

## Qué sigue necesitando research primario

Ver §12, punto 10. **Encuesta**: ranking; contracargos y reclamaciones al mes; reparto F1/F2/F3;
herramientas y proveedor de pagos; país. **Entrevistas**: cómo distinguen la devolución legítima del
abuso; por qué no disputan; qué les cubre su proveedor de pagos.

## Vacíos

- Pymes de España y LatAm (cualquier dato).
- Documento oficial de Visa VAMP y su mínimo de disputas.
- Importe del abuso de devoluciones en pymes.
- Horas por disputa.
- Protección al vendedor de Mercado Pago (documentación no disponible).
- Precios de Signifyd y Riskified.
- Si NoFraud/Wyllo cubre de verdad F3.

## Fuentes

Todas las fuentes figuran en línea con la etiqueta `[verificado: URL — 2026-10-05]`. Las del research
1853 se citan como "(research 1853)".

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-05 | Versión inicial, con la misma estructura que los research de inventario y margen. Antes de validar se añade la regla provisional de delimitación D/E | `/research-market` de la candidata E | Sí |
