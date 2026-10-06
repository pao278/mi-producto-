---
source: secondary
method: web
date: 2026-10-05
question: ¿Existe, es frecuente, cuesta y es prioritario el problema de las roturas de stock, el sobrestock y la desincronización entre canales y sistemas en las pymes de e-commerce con stock propio; quién lo sufre y quién paga; cómo lo resuelven hoy; y qué deja sin cubrir el mercado de soluciones?
opportunity: inventario-pymes-ecommerce
---

# Research: gestión de inventario en pymes de e-commerce

> Estado: **VALIDADO — v1 (2026-10-05).**
> Ruta: `product/research/2026-10-05-2320-inventario-pymes-ecommerce.md`.
> Método: WebSearch + WebFetch, ejecución secuencial, consultas del 2026-10-05. Reutiliza datos del
> research `2026-10-05-1853-comparativa-problemas-pymes-ecommerce.md` (validado).
> Oportunidad: `inventario-pymes-ecommerce` (candidata A). **Su brief sigue en borrador y no está
> guardado**; el campo `opportunity:` anticipa su slug.
> Integra el competitive scan de la candidata como §9 (no se guarda como archivo aparte).
> Misma estructura que `2026-10-05-2259-margen-real-pymes-ecommerce.md`, para comparar candidatas.
> No modifica el brief, overview, intake, F2 ni las creencias.
> Etiquetas: **P** primaria publicada · **S** secundaria · **V** proveedor con interés comercial ·
> **I** inferencia nuestra · **?** vacío. Lo no consultado: `[conocimiento del modelo — verificar]`.
> Tres subproblemas, tratados por separado:
> **(R) Roturas de stock** · **(O) Sobrestock** y stock muerto · **(S) Sincronización** del stock
> entre canales y sistemas (incluye la sobreventa).
> Límite: evidencia **secundaria y de mercado**. Ninguna fuente es del segmento.

## Resumen: lo que cambia decisiones

1. **A diferencia de la candidata de margen, hay mediciones sobre datos reales, aunque de proveedores.**
   Katana modeló 12 meses de datos de 375 marcas de EE. UU. clientes suyos: sus productos más vendidos
   se agotan unas **14 veces al año**, unos 2 días cada vez (**un mes al año** sin el producto
   estrella), con una pérdida mediana modelada de unos **21.000 $ por marca y año** (V). 8fig analizó
   524 productos de 169 vendedores con más de 100.000 $ de facturación: el **51 %** tuvo al menos una
   rotura de 7 días o más; pérdida potencial del **5,2 % de los ingresos** (V).
2. **Prioridad intermedia, no máxima.** El coste de suministros e inventario es el **2.º problema** de
   las pymes de EE. UU. (NFIB, P), pero habla del **precio**, no de la gestión. En las encuestas de
   operaciones aparece con un **34–35 %** (Linnworks, Jitterbit, V). **Nunca es el primero.** Está por
   encima de la candidata C (ausente de las encuestas).
3. **El sobrestock crece, en gran parte por causas externas.** Entre las pymes clientes de Netstock
   (V), el stock muerto pasó del **12 % (2024) al 17 % (2025) y al 24 % (2026)**; en 2025, el 55 %
   tenía más de una quinta parte de su inventario como exceso. Los retos más citados son externos:
   plazos de proveedor (77 %) y costes (66–72 %), con los aranceles de EE. UU. de fondo.
4. **Tener software no elimina el problema.** *"every brand in the sample was already paying for
   inventory software"* (Katana, V). Señal ambigua: el hueco podría estar en la **ejecución** y no en
   las funciones, o es un argumento de venta del proveedor.

---

## 1. Magnitud del problema

| Pregunta | Dato | Muestra y límites | Etiqueta | Fuente |
|---|---|---|---|---|
| **(R) Frecuencia de roturas** | Los más vendidos se agotan ≈ **14 veces al año**, ≈ **2 días** cada vez, ≈ **1 mes al año** en total; los casos repetidos concentran el **65 %** de las pérdidas recuperables | 375 marcas de EE. UU., **clientes de Katana**, multicanal (Shopify, Amazon, mayorista); jun. 2025–may. 2026; **pérdidas modeladas, no observadas**; sin productos de temporada | V | [verificado: https://ecommercefastlane.com/katana-375-brand-study/ — 2026-10-05] |
| | **51 %** de los productos con al menos una rotura (7+ días sin ventas); **35 días** sin ventas de media al año; Amazon 48 %, Shopify 53 % | 524 productos de 169 vendedores de Amazon y Shopify con más de 100.000 $; productos con ≥ 7 unidades/día | V (8fig, financiador) | [verificado: https://8fig.co/blog/the-hidden-cost-of-stockouts-a-data-driven-analysis-showing-how-missing-inventory-impacts-your-ecommerce-revenue — 2026-10-05] |
| | **44 %** sufre roturas al menos una vez al mes | 400 profesionales de EE. UU., 30 sectores (construcción 25,5 %); mar. 2026; **no es e-commerce** | V (inFlow) | [verificado: https://inflowinventory.com/blog/state-of-inventory-management-2026 — 2026-10-05] |
| **(R) Pérdida económica** | Mediana ≈ **21.000 $ por marca y año**; cuartil superior ≈ 82.900 $; 10 % superior, más de 268.000 $ | Katana; tamaño de las marcas no indicado | V | Ídem Katana |
| | **5,2 %** de los ingresos potenciales (4 M$ sobre 82,7 M$) | 8fig | V | Ídem 8fig |
| **(R) Reacción del cliente** | Dos tercios se irán a otra tienda si el artículo está agotado | Encuesta de Navidad 2024 de AlixPartners; **n y país no indicados** | S | [verificado: https://sgbonline.com/study-out-of-stocks-drive-66-percent-of-consumers-to-another-retailer/ — 2026-10-05] |
| | En retail físico, ante una rotura el 31 % compra en otro sitio y el 9 % abandona; tasa media de rotura ≈ 8 % | Artículo de un proveedor de planificación (Slimstock) en Alimarket; **retail físico**; datos clásicos sin fecha | V | [verificado: https://www.alimarket.es/logistica/noticia/139016/el-verdadero-impacto-de-las-roturas-de-stock-en-el-mundo-del-retail — 2026-10-05] |
| **(O) Sobrestock** | **55 %** con más de una quinta parte del inventario como exceso (48 % en 2024); stock muerto (1+ año): **12 % → 17 % → 24 %** (2024–2026) | Pymes clientes de Netstock (120–150+); muestra y país no detallados | V | [verificado: https://www.retailbrew.com/stories/2025/10/27/small-businesses-grapple-with-tariff-induced-supply-chain-challenges — 2026-10-05]; [verificado: https://www.supplychaindive.com/news/beyond-tariffs-a-storm-of-pressures-is-hampering-smb-supply-chains/831880/ — 2026-10-05] |
| | Sobrestock como reto para el **37,5 %** | inFlow (no es e-commerce) | V | Ídem inFlow |
| **(S) Desincronización y datos inexactos** | Datos inexactos **44,8 %**; el 49,5 % sitúa la exactitud como primera prioridad de mejora | inFlow | V | Ídem inFlow |
| | **83 %** de pymes Shopify con dificultades para sincronizar inventario, producción y contabilidad; 15 % con control completo en tiempo real | Katana + WBR, n = 100 | V | research 1853 |
| | Sincronizar inventario 34 % (Linnworks); visibilidad de inventario 35 % (Jitterbit) | Mid-market; retailers | V | research 1853 |
| **(S) Sobreventa** | Amazon fija un **2,5 %** como límite de cancelaciones del vendedor (pedidos gestionados por el vendedor, 7 días móviles); superarlo puede llevar a la desactivación; roturas y sobreventa están entre las causas | Política de Amazon descrita por un proveedor (Feedvisor) | S | [verificado: https://feedvisor.com/university/canceling_orders — 2026-10-05] |
| | **Prevalencia de la sobreventa: sin datos.** Solo quejas en reseñas (§9) | — | **?** | — |
| **Escala global** | Roturas y sobrestock ≈ 1,73 billones $ (6,5 % de las ventas del retail) | IHL Group; grandes retailers | V | research 1853 |

**Lectura (I):** a diferencia de C, (R) tiene **mediciones sobre datos de transacciones**, aunque de
clientes de proveedores; (O) tiene una **serie temporal** creciente; (S) solo percepción declarada y
quejas.

## 2. Prioridad

| Encuesta | ¿Aparece el inventario? | Posición | Lo que aparece arriba | Etiqueta |
|---|---|---|---|---|
| NFIB 2024 (n = 2.873) | **Sí, como coste** | **2.º** (coste de suministros e inventario) | Seguro médico | P (research 1853) |
| SBR / Morning Consult 2025 | No | — | Inflación, publicidad, marca | S |
| Linnworks 2025 (n = 200) | **Sí** | Sincronizar inventario 34 % (por debajo del envío 40 % y de marketplaces 43 %) | Marketplaces, logística, envío | V |
| Jungle Scout 2025 | Indirectamente | Coste de los productos 34 % | Envío 38 % | V |
| Jitterbit 2022 | **Sí** | Visibilidad de inventario 35 % (3.º) | Expectativas 46 %, fidelización 43 % | V |
| ChannelEngine 2025 (n = 470) | **No** entre los principales | — | Devoluciones 48 %, lanzamiento 47 %, cambios de precio 46 % | V |
| Netstock 2026 (150+ clientes) | Sí (audiencia de planificadores) | Plazos de proveedor 29 % como primer reto | Plazos, costes, fletes, demanda | V |
| inFlow 2026 (n = 400, no e-commerce) | Sí | Datos inexactos 44,8 %, sobrestock 37,5 %, roturas 33,5 % | Fiabilidad del proveedor 52 % | V |

**Conclusión explícita:** el inventario **sí aparece** en varias encuestas de prioridades (34–35 % en
las de operaciones; 2.º como coste en NFIB). **En ninguna es el primer problema del e-commerce.** Más
presencia que la candidata C; menos que el coste de envío.

## 3. Segmento

| Dimensión | Evidencia | Etiqueta |
|---|---|---|
| **Tamaño y facturación** | Muestras: marcas de EE. UU. clientes de Katana (tamaño no indicado); vendedores de más de 100.000 $ (8fig); pymes de hasta 500 M$ (Netstock). Las herramientas segmentan por facturación (Prediko < 100.000 $, < 500.000 $, < 2 M$) o excluyen a los pequeños (Inventory Planner, "too small" por debajo de 1 M$) | V |
| **Número de canales** | 56 % de las marcas en 3+ canales; 63 % añadirá al menos uno en 2025 (ShipBob, 550+ directivos) | V [verificado: https://ajot.com/news/shipbobs-2025-state-of-ecommerce-fulfillment-report-provides-insights-into-merchants-global-omnichannel-supply-chains — 2026-10-05] |
| **Ubicaciones** | 38 % ampliará el número de almacenes desde los que envía en 2025 (ShipBob) | V |
| **Plataformas** | Shopify y Amazon dominan las muestras (Katana, 8fig) | V |
| **País (España)** | 8,6 % de las empresas con menos de 10 empleados vende online (INE) | **P** [verificado: https://www.ine.es/dyngs/Prensa/ETICCE20241T2025.htm — 2026-10-05] |
| **Tienda propia frente a marketplaces** | (S) solo existe en serio con varios canales o ubicaciones; (R) y (O) existen con un solo canal (I). Amazon FBA impone reglas propias de stock (§7) | I, S |
| **Stock propio frente a FBA o 3PL** | Con FBA o 3PL, parte de la visibilidad y la reposición la gestiona el almacén externo (I) | I |
| **Quién lo gestiona hoy** | **Sin datos directos.** Inferencia: fundador u operaciones en pymes; compras en empresas algo mayores | **?**, I |

## 4. Quién sufre el problema

| Rol | (R) Roturas | (O) Sobrestock | (S) Sincronización | Evidencia |
|---|---|---|---|---|
| **Usuario** | Operaciones o compras; fundador en tiendas pequeñas | Ídem | Operaciones; quien da de alta productos en los canales | V (Prediko, Sumtracker se dirigen a "D2C brands"), I |
| **Persona que siente el dolor** | Fundador (ventas perdidas); marketing (publicidad hacia productos agotados) (I) | Fundador o finanzas (caja inmovilizada) (I) | Atención al cliente (cancelaciones); quien responde ante el marketplace (penalizaciones) (I) | I; Amazon 2,5 % (S) |
| **Comprador** | Fundador u operaciones: herramientas de 0–319 $/mes | Ídem | Ídem | V (§9) |
| **Prescriptor** | 3PL, agencias, partners de Shopify (I); Shopify con sus funciones nativas | Ídem | Integradores de marketplaces (ChannelEngine: el 66 % cambiaría de integrador) (V) | I, V |
| **Actor que impone el coste** | — | — | **El marketplace** (límite de cancelaciones; tarifas por stock bajo en FBA) | S |

**Lectura (I):** dolor, compra y uso **más concentrados en la tienda** que en la candidata C; no hay
un tercero como la gestoría que absorba el problema, salvo en parte el 3PL.

## 5. Comportamiento actual

| Forma de resolverlo | Evidencia | Etiqueta |
|---|---|---|
| **Excel / Sheets** | 52 % (Cin7, 530 profesionales, 38 % retail y e-commerce); 85 % (inFlow, no e-commerce); 52 % de vendedores en marketplace (ChannelEngine) | V |
| **Funciones nativas** | Shopify: órdenes de compra, transferencias, conteos, Sidekick (reposición con IA), Marketplace Connect. WooCommerce: lo básico + ATUM gratis (más de 10.000 instalaciones) | P (documentación), V |
| **Software especializado** | 218 apps de inventario para Shopify; Trunk 410 reseñas, syncX 816, Prediko 255 (§9) | V |
| **ERP** | Cin7, Zoho Inventory, Katana, Holded, Stockagile | V |
| **3PL / FBA** | El 3PL o Amazon (Restock Inventory) llevan parte de la visibilidad y la reposición | V |
| **Ninguna herramienta** | Un tercio de las pymes Shopify de la muestra de Katana no usa software de inventario | V |
| **Con software y aun así con roturas** | Todas las marcas del estudio de 375 ya pagaban software de inventario | V |
| **Aceptar el problema** | 92 % satisfecho con su método actual, aunque el 49,5 % prioriza mejorar la exactitud (inFlow) | V |

## 6. Coste actual del problema

| Tipo de coste | Dato | Etiqueta |
|---|---|---|
| **Ventas perdidas por roturas** | Mediana modelada ≈ 21.000 $/marca/año (Katana); 5,2 % de los ingresos potenciales (8fig) | V |
| **Horas** | **16 h/semana** sincronizando inventario entre sistemas desconectados (Cin7) | V |
| **Coste de personal** | ≈ **21.632 $/año** por empleado de nivel inicial dedicado a esa sincronización (Cin7) | V [verificado: https://www.cin7.com/hubfs/PDFs/ebook/2025-State-of-Inventory-Intelligence.pdf — 2026-10-05] |
| **Caja inmovilizada / stock muerto** | Porcentajes de exceso y de stock muerto (Netstock), **sin importe** | V / ? |
| **Rebajas o liquidación del sobrestock** | **Sin datos** | ? |
| **Sobreventa: cancelaciones y penalizaciones** | Límite del 2,5 % en Amazon (riesgo de desactivación); **sin datos de coste ni de frecuencia** | S / ? |
| **Tarifas por stock bajo** | Tarifa de Amazon FBA con menos de 4 semanas de stock frente a ventas (desde el 1-4-2024) | S [verificado: https://www.valueaddedresource.net/amazon-updates-us-referral-fulfillment-fees-for-2024/ — 2026-10-05] |
| **Gasto en herramientas** | Gratis–319 $/mes; Katana desde 299 $/mes; Linnworks ≈ 200 $/mes | V (§9) |

**Ninguna ausencia de datos se convierte en estimación.**

## 7. Tendencias y "por qué ahora"

| Tendencia | ¿Afecta al **problema** o solo a la industria? | Subproblema | Evidencia | Etiqueta |
|---|---|---|---|---|
| **Más canales y más ubicaciones** | **Al problema**: más sitios donde el stock tiene que cuadrar | (S), (R) | 56 % en 3+ canales; 63 % añadirá uno; 38 % ampliará almacenes (ShipBob) | V |
| **Aranceles de EE. UU.** | **Al problema** (compras anticipadas, más stock muerto) y al precio | (O), precio | 63 % de las pymes nota el impacto; stock muerto 12 % → 24 % (Netstock) | V, S |
| **Fin del de minimis en EE. UU.** | **Al problema** para quienes importan envíos pequeños: más coste y plazo; empuja a tener stock local (I) | (O), (R) | Suspendido para todos los países desde el **29-08-2025** [verificado: https://www.thompsonhinesmartrade.com/2025/07/president-suspends-duty-free-de-minimis-imports-for-all-countries-and-imposes-new-tariffs-on-low-value-shipments/ — 2026-10-05] | S |
| **UE: arancel de 3 € en paquetes < 150 €** | **Al problema** para quienes importan desde fuera de la UE (I) | (O), (R) | Decidido el 12-12-2025; en vigor desde el **1-7-2026**; temporal [verificado: https://www.deloitte.com/hu/en/services/tax/perspectives/eu-to-replace--150-euros-exemption-with--3-euros-customs-duty.html — 2026-10-05] | S |
| **Cambios en Amazon FBA** | **Al problema**: tarifa por stock bajo (abr. 2024), tarifa de colocación de entradas (mar. 2024), recorte de capacidad de hasta un 75 % (may. 2025). Empujan a repartir el stock entre FBA, AWD y 3PL | (R), (O), (S) | [verificado: https://www.valueaddedresource.net/amazon-updates-us-referral-fulfillment-fees-for-2024/ — 2026-10-05] (S); [verificado: https://amzprep.com/amazon-fba-capacity-cut-seller-guide/ — 2026-10-05] (V, 3PL) | S, V |
| **Plazos de proveedor variables** | **Al problema**: más incertidumbre en la reposición | (R), (O) | 77 % lo menciona (Netstock) | V |
| **Cierre de Stocky** | **A la oferta**; desplaza a los comercios | Todos | 31-08-2026 (Shopify Help, P; §9) | P |
| **IA en la planificación** | **A la oferta**: Sidekick gratis, forecasting con IA; abarata y vuelve commodity la reposición (I) | (R), (O) | 81 % quiere usar IA, 11 % la usa (inFlow) | V |
| **Crecimiento general del e-commerce / asistentes de compra con IA** | **Solo a la industria** | — | INE (P), ChannelEngine (V) | P, V |

**Lectura (I):** a diferencia de C, el "por qué ahora" **no es local ni normativo-contable**: viene
del **comercio internacional** (aranceles, de minimis), de las **reglas de los marketplaces** (FBA) y
de la **expansión multicanal**. Sus pruebas son sobre todo de EE. UU.

## 8. Geografía

| Dimensión | EE. UU. | Reino Unido | España | Latinoamérica |
|---|---|---|---|---|
| **Evidencia del problema** | Katana (375 marcas), 8fig, inFlow, Netstock | Linnworks (UK/US); Cin7 (31 % UK) | Solo retail físico (Slimstock, V); **sin evidencia de e-commerce** (?) | **Ninguna** (?) |
| **Cambios recientes** | Aranceles; fin del de minimis (29-08-2025); cambios en FBA | ? | Arancel de la UE de 3 € (1-7-2026) para importaciones | ? |
| **Herramientas con adopción visible** | Todas las de §9 | Linnworks, Cin7 | Stockagile (3 reseñas), Holded | Multivende (1 reseña); Mercado Libre Full `[conocimiento del modelo — verificar]` |
| **Marketplace dominante y sus reglas** | Amazon (2,5 % de cancelaciones; FBA) | Amazon | Amazon `[conocimiento del modelo — verificar]` | **Mercado Libre**: más de 57.000 pymes se sumaron en dos años; 1 de cada 4 negocios obtiene allí el 51–99 % de sus ingresos [verificado: https://eleconomista.com.ar/negocios/mas-57000-pymes-sumaron-mercado-libre-ultimos-dos-anos-n69023 — 2026-10-05] (S, 2023). Reputación penalizada por cancelaciones `[conocimiento del modelo — verificar]` (documentación oficial: 403) |

**No se asume que las cifras de EE. UU. sirvan para España o LatAm.**

---

## 9. Competencia (competitive scan)

### 9.1 Funciones nativas

| Plataforma | Qué cubre | Qué no cubre | Fuente |
|---|---|---|---|
| **Shopify (admin)** | Stock por ubicación; órdenes de compra con proveedores; transferencias; ajustes con motivo; conteos; sincronización con el TPV | Coste medio ponderado; ubicaciones dentro del almacén; enviar la orden de compra por correo; importar el histórico de Stocky | [verificado: https://help.shopify.com/en/manual/products/inventory/transitioning-from-stocky — 2026-10-05] |
| **Shopify Sidekick (IA)** | *"Sidekick recommends items based on sales data and drafts the purchase order or transfer for you"* | Método no documentado; precisión desconocida (?) | Ídem (cita literal) |
| **Shopify Marketplace Connect** (app oficial) | Sincronización con Amazon, eBay, Walmart y Target Plus; 50 pedidos/mes gratis, después 1 % con tope de 99 $/mes | Etsy, TikTok y marketplaces de LatAm o la UE no incluidos (?) | [verificado: https://apps.shopify.com/marketplace-connect — 2026-10-05] |
| **WooCommerce (core)** | Cantidad por producto, umbral global de stock bajo con aviso, reservas, estado de stock | Edición masiva, varios almacenes, proveedores, informes, lotes y caducidad | [verificado: https://wiserreview.com/blog/woocommerce-inventory-management-plugins/ — 2026-10-05] (blog, V) |
| **ATUM** (plugin gratuito para WooCommerce, casi nativo de facto) | Panel central de stock; registros (reservado, perdido en envío, devoluciones, entrante, dañado); varias ubicaciones. De pago: órdenes de compra y proveedores | Forecasting (no aparece en la ficha) | [verificado: https://wordpress.org/plugins/atum-stock-manager-for-woocommerce/ — 2026-10-05] · más de 10.000 instalaciones · 4,7 ★ · 128 reseñas |
| *Complemento:* Amazon Restock Inventory | Reposición con estacionalidad, **solo FBA** | No ve otros canales; metodología no publicada | [verificado: https://gotrellis.com/reports/amazon-restock-inventory-recommendations-report — 2026-10-05] (V) |
| *Complemento:* Mercado Libre Full | Previsiones propias | ? | [conocimiento del modelo — verificar] |

### 9.2 Competencia directa

| Herramienta | Segmento | Funciones | Precio | Adopción | Quejas | Fuente |
|---|---|---|---|---|---|---|
| **Prediko** | D2C en Shopify | Forecasting con IA, órdenes de compra, transferencias, lista de materiales, conteos, 100+ integraciones WMS/3PL, sincronización | 49 $ (< 100 k$) · 119 $ (< 500 k$) · 199 $/mes (< 2 M$) | 4,9 ★ · 255 reseñas | Interfaz poco eficiente, errores sin resolver, forecasting poco personalizable, *"questionable AI utility"* (1 reseña) | [verificado: https://apps.shopify.com/prediko — 2026-10-05] |
| **Sumtracker** | D2C en Shopify y Amazon (> 70 % solo Shopify) | Sincronización, packs, órdenes de compra, forecasting, conteos | 59 $/mes · 119 $/mes | 4,8 ★ · 115+ reseñas (dato del proveedor) | ? | [verificado: https://www.sumtracker.com/llm-info — 2026-10-05] (V) |
| **Inventory Planner (Sage)** | Mid-market; Essentials para un almacén | Forecasting, reposición, órdenes de compra | Essentials 119,99 $/mes; plan principal sin precio público | 4,5 ★ · 153 reseñas (**ficha principal no disponible**); Essentials 2,8 ★ · 2 reseñas | *"increased threefold"*; *"too small"*, volver con 1 M$; soporte lento; fallos de sincronización; sin integración con algunos 3PL | [verificado: https://apps.shopify.com/inventory-planner/reviews — 2026-10-05]; [verificado: https://apps.shopify.com/inventory-planner-essentials — 2026-10-05] |
| **Cogsy** | Marcas D2C | Planificación de demanda, reposición | 199 $/mes | 4,9 ★ · 13 reseñas | ? | [verificado: https://apps.shopify.com/cogsy — 2026-10-05] |
| **Katana** | Marcas que fabrican | Inventario + producción | Gratis hasta 30 SKU; Core desde 299 $/mes; complementos 149–249 $/mes | ? | ? | [verificado: https://katanamrp.com/pricing/ — 2026-10-05] |
| **Zoho Inventory** | Pymes generalistas | Inventario, pedidos, varios canales | Gratis (50 pedidos/mes) · 29 $ · 79 $ · 129 $ · 249 $/mes | Mediana de gasto ≈ 500 $/año (agregador) | ? | [verificado: https://costbench.com/software/inventory-management/zoho-inventory/ — 2026-10-05] |
| **Cin7 Core** | Pymes y mid-market multicanal | Inventario, compras, almacén, contabilidad | Sin precio en la ficha | 4,3 ★ · 739 reseñas | *"Support is extremely slow"*; *"Appalling integration with Shopify and Xero"*; caro para pymes; migración forzada desde OrderHive | [verificado: https://www.capterra.com/p/133038/Cin7-Core/reviews/?page=7 — 2026-10-05] |
| **Linnworks** | Mid-market multicanal | Pedidos, inventario, marketplaces | ≈ 200 $/mes según reseñas | 4,1 ★ · 47 reseñas | Caro para pymes; curva de aprendizaje; abandonos *"after a few months"* | [verificado: https://www.capterra.co.uk/reviews/116088/linnworks — 2026-10-05] |
| **Stockagile** (España) | Retail con tienda física, e-commerce y mayorista | Sincronización TPV, online y mayorista; órdenes de compra; almacén; ERP | 49–319 $/mes | 4,7 ★ · 3 reseñas | 1 reseña de daño por borrado de productos | [verificado: https://apps.shopify.com/stockagile — 2026-10-05] |
| **Multivende** (Chile) | LatAm: Mercado Libre, Falabella, Dafiti | Catálogo, stock y pedidos multicanal | Gratis + cargo por pedidos | 5,0 ★ · 1 reseña | ? | [verificado: https://apps.shopify.com/multivende?locale=es — 2026-10-05] |

### 9.3 Sincronización multicanal

| Herramienta | Canales | Precio | Adopción | Quejas | Fuente |
|---|---|---|---|---|---|
| **Trunk** | Amazon, eBay, Etsy, Faire, TikTok, Walmart, WooCommerce, Square, Wix y otros | 35–119 $/mes | 4,9 ★ · 410 reseñas | Ninguna recurrente | [verificado: https://apps.shopify.com/trunk — 2026-10-05] |
| **syncX: Stock Sync** | Feeds de proveedores (CSV, XML, Sheets, FTP, ERP, WMS) | Gratis (2.000 SKU, 1 proveedor) + planes de pago | 4,7 ★ · 816 reseñas | Limitado con varios proveedores; configuración | [verificado: https://apps.shopify.com/stock-sync — 2026-10-05] |
| **Sellbrite** | Amazon, eBay y otros | ? | 121 reseñas | *"allowing Amazon to oversell our inventory for over a month"*; *"2-hour update time … causing overselling"*; soporte | [verificado: https://appnavigator.io/app/sellbrite/reviews/?rating=1 — 2026-10-05] |
| **Marketplace Connect** | Ver 9.1 | Ver 9.1 | 4,1 ★ · 2.116 reseñas · **15 % de una estrella** | *"OVERWRITES your Amazon inventory with the previous day's Shopify count, causing items to continuously oversell"*; catálogos grandes que no sincronizan en 24 h | [verificado: https://apps.shopify.com/reviews/861405 — 2026-10-05] |

### 9.4 Sustitutos

- **El 3PL** con su panel de visibilidad y reposición
  [verificado: https://www.shipbob.com/blog/inventory-visibility/ — 2026-10-05] (V).
- **ERP o contabilidad con módulo de inventario** (Zoho, Cin7, Odoo) (I).
- **Herramientas financieras que entran en inventario** (Finaloop, MyWorks), que solapan con la
  candidata C [verificado: https://www.finaloop.com/blog/stocky-discontinued-in-2026-what-shopify-merchants-should-do — 2026-10-05] (V).
- **Asistentes generales de IA** (señal débil).

### 9.5 Soluciones manuales

Ver §5 (hojas de cálculo 52–85 %; un tercio sin software). Comercios *"drowning in spreadsheets"*,
herramientas *"way too complex"*
[verificado: https://www.indiehackers.com/post/from-reddit-rants-to-the-shopify-app-store-building-an-ai-inventory-tool-for-the-little-guys-Z9GuJpVby1K3oissAjVG — 2026-10-05] (V, anecdótico).
Rastreador externo: 218 apps de inventario para Shopify
[verificado: https://www.appjubilee.io/categories/inventory — 2026-10-05].

### 9.6 Por subproblema

| Subproblema | Oferta | Bien resuelto | Mal resuelto | Fuerza |
|---|---|---|---|---|
| (S) Sincronización entre canales | Nativa + Trunk, Sumtracker, Sellbrite, syncX, Multivende, Stockagile | La función existe y es barata (gratis–119 $/mes) | **Fiabilidad**: sobreventa por retrasos y sobrescrituras | Media |
| (S) Integración con 3PL y ERP | Prediko, syncX, Cin7, Stockagile | Hay conectores | Integraciones que fallan o no existen; la integración es barrera de adopción para el 52 % (inFlow) | Media-baja |
| (R) Forecasting y reposición | Sidekick, Prediko, Sumtracker, Cogsy, Inventory Planner | Sugerencias y órdenes de compra desde 0 $ o 49 $/mes | Precisión desconocida; precios que suben; pymes rechazadas; **las roturas persisten con software** (Katana) | Baja-media |
| (O) Sobrestock | Tratado como el reverso de la reposición | Detección en informes (I) | **Sin oferta encontrada para decidir qué hacer con el sobrestock** | ? |
| Conteos y recepción | Nativo; ATUM | Bien cubierto | Barcode y etiquetas por lotes | Baja |

### 9.7 Quejas y abandono

| Patrón | Dónde aparece |
|---|---|
| Fallos de sincronización y sobreventa | Marketplace Connect, Sellbrite, Inventory Planner |
| Precio que sube o tamaño mínimo | Inventory Planner, Linnworks, Cin7 |
| Complejidad y puesta en marcha | Linnworks, Cin7, syncX; formación 50,5 % (inFlow) |
| Soporte lento | Cin7, Sellbrite, Inventory Planner, Marketplace Connect |
| Migraciones forzadas | Stocky; OrderHive → Cin7 |
| Cobertura fragmentada | Hilo de Stocky [verificado: https://community.shopify.com/t/stocky-app-going-away-after-august-31-2026/587292?page=7 — 2026-10-05] |

**Contraevidencia:** Prediko y Sumtracker dicen cubrirlo todo, con notas de 4,8–4,9.

### 9.8 Espacios no cubiertos (hipótesis de mercado)

| # | Espacio | Evidencia | Fuerza |
|---|---|---|---|
| E1 | Fiabilidad de la sincronización | 15 % de reseñas de una estrella en Marketplace Connect (de 2.116); Sellbrite; datos inexactos 44,8 % | Media |
| E2 | Pymes pequeñas mal atendidas por precio o complejidad | "Too small"; coste como barrera 62 %. **En contra:** Sidekick y ATUM gratis; Prediko desde 49 $ | Baja-media |
| E3 | Decidir qué hacer con el sobrestock | Sin oferta encontrada; **stock muerto 12 % → 24 % (Netstock, §1)** | Baja-media |
| E4 | Mercados fuera de EE. UU. y de Amazon/eBay | Herramientas locales con 1–3 reseñas | ? (P6) |
| E5 | Comercios que dejó Stocky | Cierre el 31-08-2026; ventana disputada | Baja como hueco |
| E6 | Planificación entre varias ubicaciones (FBA, AWD, 3PL, almacén propio) | Cambios de FBA 2024–2025 (§7); 38 % amplía almacenes (ShipBob) | Baja (V) |
| E7 | Cumplir lo que el software ya recomienda (roturas repetidas con herramienta) | Katana: todas pagaban software; casos repetidos = 65 % de las pérdidas | Baja (dato y argumento de un proveedor) |

### 9.9 Respuestas del competitive scan

1. **¿Saturado?** Sí, en la categoría funcional genérica. No demostrado para todos los segmentos.
2. **Bien resuelto:** sincronización básica, órdenes de compra y transferencias, conteos, alertas,
   reposición sencilla.
3. **Mal resuelto:** fiabilidad de la sincronización e integración con 3PL y ERP. Con señales
   débiles: precio y complejidad para pymes pequeñas, precisión del forecasting, decisión sobre el
   sobrestock.
4. **¿Espacio?** No para otro producto genérico. Quizá en un nicho (E1, E3, E4, E6).
5. **¿Evidencia del hueco?** Solo señales; ninguna fuente P.

---

## 10. Evidencia en contra

| Afirmación en contra | Evidencia | Etiqueta |
|---|---|---|
| **Ya lo resuelven bien** | 92 % satisfecho con su método actual (inFlow). Herramientas con notas de 4,7–4,9 y cientos de reseñas (§9) | V |
| **No es prioritario** | Nunca es el primer problema del e-commerce; por debajo del envío en Linnworks; ausente en las prioridades de ChannelEngine (§2) | V |
| **El dolor está en el precio, no en la gestión** | NFIB mide el **coste** del inventario. Los primeros retos de Netstock son externos (plazos de proveedor, costes, fletes). El stock muerto crece con los aranceles | P, V |
| **Las funciones nativas bastan** | Sidekick (reposición con IA, gratis), conteos y órdenes de compra nativos, Marketplace Connect, ATUM gratis (§9.1) | P, V |
| **El software no resuelve** | Las 375 marcas de Katana ya pagaban software y seguían sufriendo roturas | V |
| **No pagarían otra solución** | Un tercio sin software; coste como barrera 62 %; precios de entrada de 0–49 $/mes, techo bajo (I); quejas por precio (§9.7) | V, I |
| **El 3PL o FBA absorben parte del problema** | Visibilidad y reposición del 3PL; Amazon Restock (§9.1, §9.4) | V |

## 11. Calidad de la evidencia

| Dimensión | Mejor evidencia disponible | Lo que falta |
|---|---|---|
| 1. Magnitud | **V con datos de transacciones** (Katana, 8fig); V declarativa (inFlow, Netstock) | Fuente P o S independiente; muestras del segmento |
| 2. Prioridad | **P** (NFIB, sobre el coste); V (Linnworks, Jitterbit) | Un ranking que separe gestión y precio |
| 3. Segmento | P (INE España); V (ShipBob, Katana) | Quién lo gestiona; desglose por tamaño |
| 4. Quién lo sufre | I + V | Cualquier dato directo |
| 5. Comportamiento | V | Datos de España y LatAm |
| 6. Coste | V modelada (ventas perdidas, horas); **? para sobrestock en dinero, rebajas y sobreventa** | Todo lo que no es venta perdida |
| 7. Tendencias | S (normativa aduanera, FBA); V (Netstock, ShipBob) | Fuentes oficiales primarias de la UE y de CBP |
| 8. Geografía | **Solo EE. UU.** con evidencia del problema | España y LatAm |
| 9. Competencia | Fichas y documentación oficial | Precisión del forecasting |
| 10. En contra | V, P | — |

**Síntesis:** **mejor calidad que la candidata C** en magnitud (mediciones sobre datos, no solo
conversaciones) y en prioridad (aparece en encuestas). Sigue **sin fuente P sobre la gestión del
inventario** en pymes de e-commerce, y toda la evidencia del problema es de EE. UU.

## 12. Conclusión de la oportunidad

1. **¿Es frecuente?** **Señales razonables, de proveedores con datos reales**: los más vendidos se
   agotan unas 14 veces al año (Katana); el 51 % de los productos sufre roturas (8fig). En
   sincronización solo hay percepción declarada (V).
2. **¿Es económicamente importante?** **Estimaciones modeladas**: mediana de unos 21.000 $ por marca
   y año, o un 5,2 % de los ingresos (V; clientes de proveedores de EE. UU.; tamaño no indicado).
   Sobrestock y sobreventa sin importe.
3. **¿Es prioritario?** **Prioridad intermedia**: 34–35 % en encuestas de operaciones; 2.º como coste
   en NFIB. Nunca el primero. Más que C, menos que el envío.
4. **¿Quién lo sufre y quién pagaría?** El fundador u operaciones sufren y pagan, sin intermediario
   como la gestoría. El marketplace impone parte del coste (penalizaciones, tarifas). (I, V.)
5. **¿Cómo lo resuelven hoy?** Hojas de cálculo (52–85 %, V), funciones nativas gratuitas, apps
   especializadas, 3PL o FBA. Un tercio sin software. Incluso con software, las roturas persisten.
6. **¿Está saturado el mercado de soluciones?** Sí, en la categoría funcional genérica; la plataforma
   absorbe lo básico.
7. **¿Qué está bien resuelto?** Sincronización básica, órdenes de compra, conteos, alertas,
   reposición sencilla.
8. **¿Qué sigue mal resuelto?** Fiabilidad de la sincronización (E1); decisiones sobre el sobrestock,
   con el stock muerto en aumento (E3); planificación entre ubicaciones (E6); cumplir las
   recomendaciones de reposición (E7); mercados fuera de EE. UU. (E4).
9. **¿Hay un hueco concreto para seguir investigando?** **Más concreto que en C, sin estar
   demostrado.** E1 tiene señales repetidas e independientes; E3 combina una tendencia medida (stock
   muerto 12 % → 24 %) con ausencia de oferta. Ambos dependen del segmento (¿multicanal?) y del país
   (P6). E7 es interesante, pero procede del argumento de venta de un proveedor.
10. **¿Qué falta validar con research primario?**
    - Ranking frente a B, C, D, E y F.
    - Frecuencia de roturas y de sobreventa en el segmento, y cuánto cuesta cada una.
    - Qué hacen con el sobrestock.
    - Qué parte del dolor atribuyen al **precio** y qué parte a la **gestión**.
    - Qué herramientas usan, cuáles abandonaron y por qué.
    - Canales, ubicaciones (FBA o 3PL) y país.

## Implicaciones pendientes (no aplicadas)

Registradas por decisión de la responsable del proyecto (2026-10-05). **No se aplican** al brief,
overview, intake, F2 ni creencias hasta comparar las cuatro candidatas.

1. **Posible foco en la fiabilidad de la sincronización (E1).** Señales repetidas e independientes
   (reseñas de Marketplace Connect y Sellbrite; datos inexactos 44,8 %). Solo relevante si el
   segmento es multicanal o con varias ubicaciones; tensión con la exclusión de marketplaces del
   overview v3.
2. **Posible foco en el sobrestock (E3).** Tendencia medida de stock muerto (12 % → 17 % → 24 %,
   Netstock, V) y sin oferta encontrada para decidir qué hacer con él.
3. **Posible foco en la planificación entre varias ubicaciones (E6).** Empujado por los cambios de
   Amazon FBA (2024–2025) y la ampliación de almacenes (38 %, ShipBob).
4. **Distinción entre problema de gestión y problema de precio.** NFIB, Netstock y los aranceles
   apuntan a causas externas (precio, plazos); los casos repetidos de Katana (65 % de las pérdidas
   recuperables) apuntan a la gestión. Debe medirse por separado en el research primario.
5. **Solapamiento con conciliación y margen (candidata C).** El desajuste inventario–contabilidad y la
   calidad del COGS (espacio M3 del research de margen) tocan a las dos candidatas; conviene
   delimitarlo al compararlas.

## Impacto en creencias

Registro validado: overview v3. Las creencias del brief de inventario (en borrador) se comentan
aparte. Nada de esta tabla se traslada al overview (eso corresponde a `/review-evidence`).

| Creencia | Veredicto | Evidencia |
|---|---|---|
| 1–6 (devoluciones) | **no dice nada** | — |
| *(borrador) (a) Prioridad* | **apoya débilmente**: aparece en encuestas de prioridades, en posición intermedia (fuera del segmento) | §2 |
| *(borrador) (b) Gestión frente a precio* | **mixto**: **contradice en parte** (retos principales y stock muerto con causas externas); **apoya en parte** (casos repetidos = 65 % de las pérdidas recuperables, Katana) | §1, §2, §10 |
| *(borrador) (c) Pago y hueco* | **apoya** "ya pagan" (todas las marcas de Katana pagaban software); **contradice** el hueco genérico; **apoya** el hueco en E1 y, más débilmente, en E3 | §5, §9 |

**Corrección al research 1853** (el 1853 no se modifica, WORKFLOW §3): la saturación del software de
inventario pasa de "Media-alta (no verificado)" a **"Alta en la categoría genérica, verificada"**.

## Qué sigue necesitando research primario

Ver §12, punto 10. **Encuesta** (cuántos, con qué frecuencia, cuánto): ranking frente a B–F;
frecuencia de roturas y sobreventa; qué atribuyen a precio y qué a gestión; herramientas y gasto;
canales, ubicaciones y país. **Entrevistas** (por qué, qué hacen hoy): qué hacen con el sobrestock;
cómo se enteran de que el stock publicado no es el real y qué les cuesta; por qué abandonaron una
herramienta o por qué les basta la hoja de cálculo.

## Vacíos

- Prevalencia y coste de la **sobreventa**.
- **Importe** del sobrestock y de las rebajas.
- Quién gestiona el inventario en pymes.
- Evidencia de e-commerce en **España y LatAm**.
- Política oficial de reputación de Mercado Libre (documentación: 403).
- Precisión del forecasting de cualquier herramienta.
- Fuentes primarias de CBP y de la UE para las medidas aduaneras (consultadas vía despachos y
  consultoras).
- Tamaño de las marcas del estudio de Katana.

## Fuentes

Todas las fuentes figuran en línea con la etiqueta `[verificado: URL — 2026-10-05]`. Las del research
1853 se citan como "(research 1853)".

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-05 | Versión inicial. Integra el competitive scan de inventario (§9, con E6 y E7) y añade magnitud, prioridad, segmento, roles, comportamiento, coste, tendencias, geografía, evidencia en contra, calidad y conclusión. Registra cinco implicaciones pendientes | `/research-market` completo, con la misma estructura que el de margen, para comparar las cuatro candidatas con la misma vara | Sí |
