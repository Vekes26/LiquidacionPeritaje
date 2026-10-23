# Revisión del PR · Grupo 13 → Peritaje y liquidación

**Repositorio:** Vekes26/LiquidacionPeritaje · **Fuentes contrastadas:** Caso §3.3, Acta §3.6 y §3.7, reglas de `SKILL.md`

## Defectos y solución

| # | Defecto | Solución propuesta |
|---|---------|--------------------|
| 1 | RF-04 fija $8.000.000, pero «Conflictos» dice que el importe no está definido. El Acta §3.6 sí lo define y la fuente se cita vaga. Dice «automatización» en vez de «autorización» y junta dos condiciones. | Separar en dos RF (monto > $8.000.000; robo o incendio total, sin importar el monto), citar Acta §3.6 y borrar el conflicto falso. |
| 2 | Flujos 4a y 6a inventan qué pasa si el gerente o el asegurado rechazan. El 4a no incluye robo ni incendio total. | Marcar `[NEEDS CLARIFICATION]` con decisor D. Almirón y agregar robo o incendio total al 4a. |
| 3 | Tabla de fragmentos que no son RF sin justificaciones ni categorías. | Completar categoría y justificación de una línea en cada fila (`SKILL.md`). |

## Qué agregaríamos
- RF de estado del siniestro con lista fija, sin texto libre (Acta §3.7).
- RF de número de denuncia al registrarla (Acta §3.5).
- RF de monto comprometido en siniestros abiertos (D. Almirón).
- Clave de issue de Jira en cada requerimiento y commit.

## Pendientes de decisión (D. Almirón)
- Qué pasa si el Gerente no autoriza.
- Qué pasa si el asegurado rechaza la oferta.
- Conjunto de estados del siniestro.
