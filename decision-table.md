# Tabla de decisión

## [nombre de la decisión a tabular]

Completar condiciones (una fila por condición, con sus valores
posibles) y acciones (una fila por acción), una columna por regla.
Usar guion (`-`) donde la condición no importa para esa regla.

| Condición / Acción | Regla 1 | Regla 2 | Regla 3 | Regla 4| Regla 5|Regla por defecto |
|----------------------|---------|---------|---------|-----|---------------------|
|el monto es superior a $8.000.000 |no |si |no |no | - |
| es robo total |no |- |si |no | - |
| es incendio total |no |- |- |si | - |
| el gerente autoriza |- |si |si |si | no |
| el asegurado acepta la oferta |si |si |si |si | - |
| liquidar sin autorizacion gerencial |x | | | | |
| solicitar autorizacion al gerente| | x| x|x |x |
| realizar el pago por transferencia |x |x |x | x| |
| cerrar el siniestro como pagado |x |x | x| x| |


**Regla por defecto:** describir qué pasa cuando ninguna regla nombrada
aplica — no puede quedar implícita.

**Cómo se lee esta tabla:** (una o dos líneas explicando el orden de
evaluación de las reglas, si corresponde).

## Observaciones (obligatorio si el material relevado tiene conflictos o huecos)

- **Conflictos detectados:** (ver "Detección de conflictos" en
  skill/SKILL.md — valores distintos para la misma condición, sin
  aclarar cuál prevalece)
- **Huecos del material:** (una condición necesaria para la tabla que
  ningún fragmento aclaró)
- **Decisiones de negocio pendientes:** (qué haría falta confirmar con
  el cliente/usuario antes de dar esta tabla por definitiva)
