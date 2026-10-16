# Requerimientos

Completar a partir de los fragmentos de relevamiento del caso. Seguir
la convención de `skill/SKILL.md` (atómico, verificable, sin tecnología
mezclada).

## Requerimientos funcionales

| ID | Requerimiento | Fragmento(s) de origen |
|----|---------------|--------------------------|
| RF-01 |El sistema debe permitir registrar la asignación de un perito o siniestro.|caso aseguradora pampa 3.3, asignacion del perito|
| RF-02 |El sistema debe permitir registrar el informe de pericia y las fotografías de los datos correspondientes a un siniestro |caso aseguradora pampa 3.3 y tabla de documentos, informe de pericia |
| RF-03 |El sistema debe permitir registrar la determinación de cobertura y el monto calculado para la liquidación de un siniestro. |caso aseguradora pampa 3.3, gestion de liquidacion|
| RF-04 |El sistema debe solicitar automatización al gerente de siniestros cuando el monto estimado supera los $8.000.000, o cuando se trata de robo total o incendio total |acta, reglas de automatizacion de siniestros|
| RF-05 |El sistema debe permitir registrar si el asegurado acepta o rechaza el monto de liquidación ofrecido. |caso aseguradora pampa 3.3, comunicacion de la liquidacion al asegurado|

## Fragmentos que NO son requerimientos funcionales

Para cada fragmento del relevamiento que no calificó como RF, clasificar
según las categorías de `skill/SKILL.md` (objetivo/meta de negocio,
restricción técnica, RNF, dato de contexto) y justificar en una línea
por qué no es un RF.

| Fragmento | Texto | Categoría | Justificación |
|-----------|-------|-----------|----------------|
|El asegurado no tiene manera de consultar en qué estado está su siniestro. Llama al 0800, la operadora abre la planilla, busca la fila y le lee lo que dice la celda de estado.  |El sistema debe permitir consultar los datos de un siniestro|RNF | |
|Con el informe, el liquidador determina si el siniestro está cubierto y calcula el monto. Si supera cierto importe, tiene que autorizarlo el Gerente de Siniestros. |el sistema necesita autorizacion del gerente de siniestro si el siniestro supera cierto importe | | |

## Conflictos u observaciones detectadas

Si al procesar los fragmentos aparece un conflicto de valores (ver
"Detección de conflictos" en la skill), documentarlo acá aunque no
afecte directamente un RF puntual.
un conflicto u observacion es que no se define de cuanto es el importe para que el siniestro necesite autorizacion del gerente de siniestros
otra observacion que hicimos es que le solicitamos al sistema hacer la automatizacion del excel para que sea mas rapido de buscar y organizar

-
