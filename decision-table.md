# Tabla de decisión — UC-01: Liquidación y Peritaje

## 1. Objetivo

La tabla de decisión permite representar las condiciones y acciones del proceso de liquidación y peritaje de siniestros. Contempla la necesidad de autorización gerencial, la decisión del gerente y la aceptación o rechazo de la oferta por parte del asegurado.

**Convenciones:**
- **Sí:** la condición se cumple.
- **No:** la condición no se cumple.
- **—:** la condición no influye en esa regla o no corresponde evaluarla.

## 2. Tabla de decisión

| Condiciones / Reglas | R1 | R2 | R3 | R4 | R5 |
|---|:---:|:---:|:---:|:---:|:---:|
| ¿Requiere autorización gerencial? | No | No | Sí | Sí | Sí |
| ¿El gerente autoriza? | — | — | Sí | Sí | No |
| ¿El asegurado acepta la oferta? | Sí | No | Sí | No | — |
| **Acciones / resultados** | | | | | |
| Liquidar sin autorización gerencial | x | x |  |  |  |
| Solicitar autorización al gerente |  |  | x | x | x |
| Comunicar la oferta al asegurado | x | x | x | x |  |
| Realizar el pago por transferencia | x |  | x |  |  |
| Cerrar el siniestro como pagado | x |  | x |  |  |

### Descripción de las reglas

- **R1:** no se requiere autorización gerencial y el asegurado acepta la oferta. Se realiza el pago por transferencia y se cierra el siniestro como pagado.
- **R2:** no se requiere autorización gerencial y el asegurado rechaza la oferta. No se realiza el pago.
- **R3:** se requiere autorización gerencial, el gerente aprueba y el asegurado acepta la oferta. Se realiza el pago y se cierra el siniestro como pagado.
- **R4:** se requiere autorización gerencial, el gerente aprueba y el asegurado rechaza la oferta. No se realiza el pago.
- **R5:** se requiere autorización gerencial y el gerente rechaza la solicitud. No se comunica la oferta ni se realiza el pago.

## 3. Regla para determinar si se requiere autorización

Se requiere autorización del gerente cuando se cumple al menos una de estas condiciones:

- El monto estimado de liquidación supera los $8.000.000.
- El siniestro corresponde a un robo total.
- El siniestro corresponde a un incendio total.

Si no se cumple ninguna de estas condiciones, el siniestro puede continuar sin autorización gerencial.

El importe de exactamente $8.000.000 no activa el criterio por monto, porque la regla relevada indica que el monto debe ser superior a ese valor.

## 4. Regla por defecto

Si ninguna de las reglas R1 a R5 aplica, el sistema no debe autorizar ni realizar el pago automáticamente. El siniestro debe quedar pendiente de revisión hasta que se aclaren las condiciones necesarias para continuar.

Esta regla por defecto es una propuesta pendiente de validación con el cliente, ya que el material relevado no establece expresamente el procedimiento para todos los casos no contemplados.

## 5. Cómo se lee la tabla

Se identifica primero si el siniestro requiere autorización gerencial. Luego, si corresponde, se evalúa la decisión del gerente. Finalmente, cuando se puede comunicar la oferta, se registra si el asegurado la acepta o la rechaza y se ejecutan las acciones correspondientes.

Cada regla representa una combinación diferente de condiciones. Si ninguna coincide, se aplica la regla por defecto.

## 6. Observaciones

### 6.1. Conflictos detectados

- La autorización gerencial depende del monto y del tipo de siniestro. La autorización es necesaria si el monto supera los $8.000.000, o si se trata de robo total o incendio total, independientemente del monto.
- La tabla inicial no contemplaba explícitamente el rechazo de la oferta por parte del asegurado en todas las reglas.
- Los registros de siniestros relevados utilizan diferentes estados, por ejemplo: «cerrado», «pagado», «en trámite», «pericia», «con perito» y «abierto». Es necesario definir criterios uniformes para registrar el estado de cada siniestro.

### 6.2. Huecos del material

- No se especifica qué estado debe asignarse al siniestro cuando el gerente rechaza la autorización.
- No se especifica qué estado debe asignarse cuando el asegurado rechaza la oferta.
- No se define el procedimiento que debe seguirse cuando faltan datos para determinar si corresponde solicitar autorización.
- No se aclara qué registro formal debe quedar de la aprobación o rechazo del gerente.

### 6.3. Decisiones de negocio pendientes

Antes de considerar definitiva la tabla, se debe confirmar con el cliente:

1. ¿Qué estado debe tener el siniestro cuando el gerente rechaza la autorización?
2. ¿Qué estado debe tener cuando el asegurado rechaza la oferta?
3. ¿Cómo debe actuar el sistema cuando faltan datos necesarios para tomar una decisión?
4. ¿La aprobación del gerente debe registrarse formalmente antes de comunicar la oferta al asegurado?
5. ¿Qué estados oficiales se utilizarán para unificar los registros de siniestros?

