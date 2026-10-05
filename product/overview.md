# PredictiFlow (nombre provisional)

> Estado: VALIDADO — v2 (2026-10-05)
> Fuente: product/intake.md v2 (validado, 2026-10-05)

mode: new · commercial

> "new" es un hecho [F2]. "commercial" (la tienda pagaría) es una inferencia del intake, no
> validada: no existen todavía datos ni evidencia de disposición a pagar. Se pone a prueba
> con la creencia 4.

PredictiFlow es una idea de producto digital B2B para marcas pequeñas y medianas de comercio
electrónico, centrada en el problema de las devoluciones y los reclamos. Parte de una hipótesis
del equipo original: hoy el problema se detecta después del envío, cuando ya se han asumido el
transporte, la atención al cliente, la logística inversa y el inventario inmovilizado. Antes de
elegir una solución, este producto debe comprobar si ese problema existe, si es prioritario y si
se puede hacer algo antes del despacho. El concepto de modelo predictivo con alertas queda
aparcado (intake §5.1).

## Para quién

> Propuesta a validar en discovery, no es un segmento confirmado. La responsable del proyecto
> la considera una hipótesis inicial razonable, pero no hay evidencia del segmento.

Fundadores o responsables de operaciones de marcas D2C pequeñas y medianas que venden en su propia
tienda online (Shopify o WooCommerce), en categorías con muchas devoluciones (moda y calzado). En
estas tiendas, la gestión de devoluciones y reclamos recae en la misma persona o en un equipo de
1 a 3 personas que también decide sobre los pedidos.

- Marcas pequeñas y medianas: intención declarada [F2].
- Shopify y WooCommerce: mencionadas en [F1]; no validadas como segmento (S15).
- Moda y calzado: inferencia a partir de los benchmarks de [F1]; es un supuesto.
- Que una sola persona acumule varios roles: es un supuesto (§4.1).

## Punto de partida: evidencia y supuestos

- **Evidencia del segmento:** ninguna. No hay datos ni entrevistas de tiendas objetivo (intake §7.1, punto 18).
- **Evidencia de mercado (contexto, no extrapolable):**
  - 19,3 % de ventas online devueltas (retail EE. UU., 2025).
  - Coste de la devolución ≈ 17 % del coste del producto (moda y calzado, muestra de 2.229 devoluciones).
  - Ambos datos son hechos documentales de [F1]. No deben combinarse ni aplicarse al segmento (§7.2).
- **Supuestos heredados del intake:** H1–H6 y S1–S18 (§8). Las creencias de abajo reúnen las de
  mayor riesgo; el registro completo sigue en el intake.

## Creencias no verificadas

Ordenadas por impacto × incertidumbre. La primera es la siguiente que hay que poner a prueba.

1. [product] [value] Para las marcas del segmento, las devoluciones y los reclamos están entre sus
   tres problemas operativos o de margen más importantes, y alguien en la tienda dedica cada
   semana un tiempo que sabe estimar a gestionarlos. *(S1, H1)*
2. [product] [value] Al menos 1 de cada 4 devoluciones del segmento tiene una causa que ya se
   podía identificar antes del despacho (talla, expectativa sobre el producto, patrón de compra),
   y no una causa posterior (transporte, defecto, cambio de opinión). *(S3, H2. El 25 % es un
   umbral de trabajo para poder refutar la creencia; no es una cifra sustentada en evidencia.)*
3. [product] [value] Entre la compra y el despacho existe una acción que la tienda ya está
   dispuesta a tomar sobre un pedido concreto (contactar al cliente, confirmar la talla, retener
   el pedido), y la tomaría en lugar de seguir gestionando la devolución después.
   *(H4, crítica; S9)*
4. [product] [viability] La persona que decide la compra pagaría una cuota recurrente por reducir
   devoluciones, siempre que pueda ver el ahorro con sus propias cifras. Hoy no conoce el coste
   real de una devolución, y eso impide calcular el retorno. *(S17, S18; riesgo de "línea base
   económica", §5.3)*
5. [product] [value] El dolor por el que pagarían está en el coste de la devolución (margen,
   inventario) y no solo en la carga de gestionarla. Si fuera solo carga operativa, el problema
   sería de gestión y no de prevención. *(conflicto §11.4, sin resolver)*
6. [opportunity: coste-devoluciones-d2c] [value] En las marcas D2C pequeñas y medianas de moda y
   calzado, la tasa de devolución supera el 15 % de los pedidos enviados. *(El 15 % es un umbral
   de trabajo provisional para poder refutar la creencia; no es una cifra sustentada en evidencia.)*

**Primera en atacar:** la creencia 1. Si las devoluciones no son prioritarias para el segmento,
las demás pierden sentido.

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-05 | Versión inicial | product/intake.md v2; respuestas de la responsable del proyecto (2026-10-05) | Sí |
| v2 | 2026-10-05 | Se añade la creencia 6 `[opportunity: coste-devoluciones-d2c] [value]` al final del registro; las creencias 1–5 no cambian | `/frame-opportunity`: product/opportunities/2026-10-05-1510-coste-devoluciones-d2c.md. Sin evidencia nueva; pone a prueba la inferencia "moda y calzado" | Sí |
