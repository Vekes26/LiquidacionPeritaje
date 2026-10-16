# Casos de uso

## UC-01: Liquidacion y Peritaje

**Actor:**
Liquidador, Perito, Asegurado y Gerente de siniestros.

**Precondición:**
El asegurado sufre un siniestro (choque, robo o daño) y se inicia el pedido a través de alguno de los canales de atención de la compañía.

**Flujo principal:**
1.El liquidador atiende la solicitud del asegurado y registra los datos del siniestro (vehículo, ubicación).

2.El liquidador gestiona y asigna un perito para la inspección.

3.El perito realiza la inspección, toma fotografías y envía el informe de pericia al liquidador.

4.El liquidador recibe el informe, analiza la cobertura y calcula el monto de la liquidación.

5.Se comunica la propuesta de liquidación (monto y condiciones) al asegurado.

6.El asegurado recibe la oferta y la acepta.

7.Se efectúa el pago por transferencia y se marca el siniestro como cerrado.

**Flujo(s) alternativo(s):**
4a. El monto supera el límite establecido:
    1. El liquidador solicita autorización al Gerente de Siniestros.
    2. El Gerente evalúa la solicitud y otorga la autorización (si es rechazado por el gerente, el proceso finaliza).
6a. El asegurado rechaza la oferta:
    1. El asegurado comunica el rechazo de la propuesta de liquidación y el proceso finaliza sin pago.
**Postcondición:**
El expediente del siniestro queda actualizado, con estado cerrado y pagado por transferencia (o rechazado en caso de no aceptación/autorización).
**Relaciones con otros casos de uso:**

| Relación               | Caso de uso relacionado    |  Tipo (include/extend)  | Justificación                    |
|------------------------|----------------------------|-------------------------|----------------------------------|
Autorizacion de gerencia  UC-02: Gestionar autorizacion   extend                  Se ejecuta opcionalmente bajo la 
                                                                                  la condicion especifca de que el monto calculado del siniestro supere el importe limite requerido para la aprobacion gerencial.

Recordar (ver skill/SKILL.md): include = siempre se ejecuta como parte
del flujo, sin excepción. extend = extiende opcionalmente bajo una
condición específica, el flujo base es completo sin ella. Toda relación
sin justificación no cuenta como completa.

## Fragmentos considerados para este caso de uso

Listar qué fragmentos del relevamiento se usaron para armar este caso
de uso, y qué parte del flujo justifica cada uno.

| Fragmento         | Qué aporta al caso de uso |
|-------------------|------------------------------|
Cuando un asegurado tiene un choque, un robo o un daño, llama al 0800 la denuncia se anota en una planilla Excel.

Justifica la recepción inicial del pedido del asegurado y el registro de los datos del siniestro.

El liquidador asigna un perito... El perito va, inspecciona, saca fotos y las manda. El informe de pericia llega por correo.

Justifica la gestión de asignación del perito, la inspección y la recepción del informe de pericias y fotos.

Con el informe, el liquidador determina si el siniestro está cubierto y calcula el monto. Si supera cierto importe, tiene que autorizarlo el Gerente de Siniestros.

Justifica el análisis del informe, la determinación de cobertura, el cálculo del monto y la condición de autorización superior.

Después se le ofrece el monto al asegurado, que puede aceptarlo o rechazarlo. Si se acepta, se paga por transferencia y se marca la fila como cerrada.

Justifica la comunicación de la oferta, la respuesta del asegurado, el pago por transferencia y el cierre definitivo del caso.