# WORKFLOW — Mi Producto AFPM

> Reglas permanentes de trabajo del proyecto.
> Se aplican a todas las skills, sesiones y artefactos.
> Estado: VALIDADO — v1 (2026-10-05)

## 1. Flujo obligatorio

Cada paso del proyecto sigue esta secuencia, sin saltos:

**Skill → borrador → revisión → validación explícita → guardado/actualización → siguiente skill**

1. **Skill:** se ejecuta la skill que corresponde al paso.
2. **Borrador:** el resultado se presenta como borrador completo para revisión.
3. **Revisión:** la responsable del proyecto revisa el borrador y pide ajustes si hace falta.
4. **Validación explícita:** solo cuenta una confirmación expresa (por ejemplo, "está validado").
   El silencio, un comentario parcial o la petición de pasar al siguiente tema no cuentan como validación.
5. **Guardado/actualización:** el artefacto validado se guarda en los tres entornos (sección 5).
6. **Siguiente skill:** no se empieza otro paso hasta cerrar el anterior.

## 2. Borradores

- Ningún borrador se considera versión definitiva antes de su validación.
- Los borradores no se guardan en el Claude Project, ni en Obsidian, ni en GitHub como versión aprobada.
- Si por razones técnicas un borrador tiene que existir en disco, debe indicarse en el propio
  archivo con `Estado: BORRADOR` y no se incluye en ningún commit.

## 3. Artefactos validados

- Un artefacto validado no se sobrescribe sin aviso.
- No se modifican documentos anteriores solo para que coincidan con conclusiones posteriores.
- Cada artefacto validado indica en su encabezado su estado y la fecha de validación.

### 3.1 Propuesta de cambio sobre un artefacto validado

Si una skill posterior propone modificar un artefacto ya validado, antes de tocarlo se presenta:

| Campo | Contenido |
|---|---|
| Artefacto | Ruta del archivo afectado |
| Qué cambia | Sección y texto concretos (antes / después) |
| Por qué cambia | Motivo del cambio |
| Evidencia | Hallazgo, dato o información nueva que lo justifica, con su fuente |
| Impacto | Otros artefactos que dependen de este y que habría que revisar |

El cambio solo se aplica después de la validación explícita de esta propuesta.

## 4. Trazabilidad del razonamiento

- Se conserva la relación entre **hipótesis inicial → evidencia posterior → decisión tomada**.
- Cuando una hipótesis cambia, no se borra la versión original. Se registra su evolución:
  - la hipótesis original se mantiene y se marca como `refutada`, `matizada` o `reemplazada`;
  - la nueva formulación se añade con un identificador derivado (por ejemplo, H2 → H2.1);
  - se indica la evidencia que motivó el cambio y la fecha.
- Cada artefacto validado que se modifique incluye al final una sección **Historial de cambios**:

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | AAAA-MM-DD | Versión inicial | — | Sí |

- Los hechos, supuestos y decisiones pendientes se mantienen separados, como en `product/intake.md`.

## 5. Entornos y sincronización

| Entorno | Función | Contenido |
|---|---|---|
| Claude Project | Entorno de trabajo con las skills | Última versión validada de cada artefacto |
| Obsidian | Repositorio de conocimiento y documentación | Última versión validada de cada artefacto |
| GitHub | Control de versiones e historial de cambios | Todas las versiones validadas, con su historial |

- Siempre que sea posible, se usa la misma estructura de carpetas, rutas y nombres de archivo
  en los tres entornos (por ejemplo, `product/intake.md` en los tres).
- Si un entorno no se puede actualizar en ese momento (falta de conexión o de permisos),
  se informa de forma explícita qué entorno quedó pendiente y qué acción falta.

## 6. Reglas de GitHub

- GitHub es la fuente del historial: cada versión validada corresponde a un commit.
- Cada commit incluye **solo** los archivos del artefacto validado en ese paso.
  - Se añaden por ruta exacta (`git add product/intake.md`), nunca con `git add .` ni `git add -A`.
  - Los demás archivos modificados o nuevos que aparezcan en el repositorio no se incluyen;
    se informa de ellos para que se decida qué hacer.
- Mensaje de commit: qué artefacto se añade o cambia y que se trata de una versión validada.
  Ejemplo: `Añade product/intake.md (versión validada)`.
- No se reescribe el historial (no `rebase`, `amend` ni `push --force` sobre versiones validadas).

## 7. Estructura de carpetas

Estructura actual:

    mi-producto-/
    ├── WORKFLOW.md
    ├── README.md
    └── product/
        └── intake.md

Las carpetas nuevas se crean solo cuando una skill validada produce un artefacto que las necesita.
La ruta de cada artefacto nuevo se indica en el borrador, antes de la validación.

## Historial de cambios

| Versión | Fecha | Cambio | Motivo / evidencia | Validado |
|---|---|---|---|---|
| v1 | 2026-10-05 | Versión inicial | Reglas definidas por la responsable del proyecto | Sí |
