| Identificador         | CU-1                                                                                                                         |                                                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Nombre                | Realizar Examen                                                                                                              |                                                                                                                                |
| Descripcion           | El sistema deberá permitir al administrador decidir qué aspirante hace determinado examen.                                   |                                                                                                                                |
| Precondicion          | Si el aspirante cumple todos los requisitos puede realizar examen a que se postula.                                          |                                                                                                                                |
| Postcondicion         | Condición final exitoso: Aspirante aprueba los exámenes. Condición final fallido: Aspirante no aprueba o suspende el examen. |                                                                                                                                |
| Actores               | Administrador y Aspirante.                                                                                                   |                                                                                                                                |
| Secuencia Normal      | Paso                                                                                                                         | Accion                                                                                                                         |
|                       | 1                                                                                                                            | Administrador determina si aspirante nuevo cumple todos los casos include para que el aspirante pueda hacer el examen          |
|                       | 2                                                                                                                            | Si cumple todos los casos de uso include                                                                                       |
|                       | 3                                                                                                                            | Aspirante hace examen al que postula.                                                                                          |
|                       | 4                                                                                                                            | Si no cumple todos casos include.                                                                                              |
|                       | 5                                                                                                                            | Pasa a secuencia alternativa.                                                                                                  |
|                       | 6                                                                                                                            | Si cumple todos los casos include y aspirante no se presenta al examen sin presentar justificación válida a secuencia de error |
| Secuencia Alternativa | Paso                                                                                                                         | Accion                                                                                                                         |
|                       | 1                                                                                                                            | Se listan todos los casos de uso no cumplidos.                                                                                 |
|                       | 2                                                                                                                            | Se da informe a aspirante del porqué suspende examen parcial o totalmente.                                                     |
|                       | 3                                                                                                                            | Sistema regresa a secuencia normal paso 1.                                                                                     |
| Secuencia de error    | Paso                                                                                                                         | Accion                                                                                                                         |
|                       | 1                                                                                                                            | El sistema desecha a aspirante                                                                                                 |
|                       | 2                                                                                                                            | Vuelve al paso 1 secuencia normal                                                                                              |
| Importancia           | Vital                                                                                                                        |                                                                                                                                |
| Urgencia              | Inmediata                                                                                                                    |                                                                                                                                |
| Observaciones         |                                                                                                                              |                                                                                                                                |

| Identificador         | CU-2|                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Nombre                | Suspender Examen|                                                                      |
| Descripcion           | El sistema deberá permitir al administrador decidir qué aspirante suspende determinado examen y en algunos casos en determinada etapa. Este caso de usoextiende de realizar examen. |                                                                       |
| Precondicion          | Si el aspirante no cumple todos los requisitos.|                                      |
| Postcondicion         | Condición final exitoso: Si aspirante entrega documentos legales. Condición final fallido: Si el aspirante no entrega documentos legales.                                          |                                                                            |
| Actores               | Administrador|                                                                        |
| Secuencia Normal      | Paso     | Accion                                                                     |
|                       | 1        | Aspirante no entrega documentos legales                                    |
|                       | 2        | Administrador determina que aspirante suspende examen según sea elcaso.    |
|                       | 3        | Aspirante hace examen al que postula.                                      |
|                       | 4        | Si suspende parcialmente su resultado anterior es válido por 1 año         |
|                       | 5        | Si suspende totalmente espera un tiempo de 3 meses.                        |
|                       | 6        | Si aspirante se retira sin justificación valida pasa a secuencia de error. |
| Secuencia Alternativa | Paso     | Accion                                                                     |
|                       |          |                                                                            |
|                       |          |                                                                            |
|                       |          |                                                                            |
| Secuencia de error    | Paso     | Accion                                                                     |
|                       | 1        | Se altera del retiro inesperado                                            |
|                       | 2        | El sistema desecha a aspirante                                             |
|                       | 3        | Y vuelve al paso 1 secuencia normal. Caso de uso realizar examen.          |
| Importancia           | Importante |                                                                          |
| Urgencia              | Hay presión |                                                                         |
| Observaciones         |          |                                                                            |

| Identificador         | CU-3|                                                                                |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Nombre | Cumplir requisitos.|                                                                                |
| Descripcion | El sistema deberá permitir al administrador verificar el cumplimiento de todos losrequisitos administrativos que el aspirante debe entregar. Este caso es include derealizar examen. ||
| Precondicion | Si el aspirante cumple todos los requisitos puede realizar examen a que se postula.| |
| Postcondicion         | Condición final exitoso: Si aspirante entrega toda la documentación. Condición final fallido: Si el aspirante no entrega toda la documentación.|                                                                                             |
| Actores | Administrador|                                                                                  |
| Secuencia Normal      | Paso| Accion                                                                      |
|                       | 1| Aspirante entrega todos los requisitos administrativos.                        |
|                       | 2| Administrador determina si tiene todos los requisitos.                         |
|                       | 3| Si cumple todos los requisitos.                                                |
|                       | 4| Aspirante cumple un paso necesario para realizar examen.                       |
|                       | 5| Si no cumple todos requisitos                                                  |
|                       | 6| Pasa a secuencia alternativa                                                   |
|                       | 7| Si requisitos están adulterados o sin certificación pasa a secuencia de error. |
| Secuencia Alternativa | Paso| Accion                                                                      |
|                       | 1| Se listan requisitos faltantes o erróneos.                                     |
|                       | 2| Se registran requisitos                                                        |
|                       | 3| Se validan requisitos.                                                         |
|                       | 4| Si todo está bien pasa secuencia normal paso 3.                                |
|                       | 5| Si documentos no pasan validación se va a secuencia de error.                  |
| Secuencia de error    | Paso| Accion                                                                      |
|                       | 1| Se alerta del error en documento                                               |
|                       | 2| El sistema desecha a aspirante                                                 |
|                       | 3| Y vuelve al paso 1 secuencia normal.                                           |
| Importancia           | Vital|                                                                            |
| Urgencia              | Hay presión|                                                                      |
| Observaciones         |                                                                                   |


| Identificador         | CU-4||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Nombre                | Tribunal||
| Descripcion           | El tribunal deberá decidir el número siempre impar de jueces, también define el criterio de evaluación y las notas de cada aspirante. Este caso es extiende de realizar examen                                                    ||
| Precondicion          | Si el aspirante cumple Abono y requisitos administrativos||
| Postcondicion         | Condición final exitoso: Si aspirante tiene buena capacidad y cumple criterios de valoración será promovido. Condición final fallido: Si aspirante no tiene buena capacidad o no cumple criterios de valoración no será promovido |                                                                                                    |
| Actores               | Jueces, Administrador|                                                                                                    |
| Secuencia Normal      | Paso| Accion                                                                                             |
|                       | 1| Aspirante presenta pruebas de examen                                                               |
|                       | 2| Tribunal califica cada prueba.                                                                     |
|                       | 3| Tribunal presenta resultados.                                                                      |
|                       | 4| Si aspirante no aprueba alguna fase de las pruebas                                                 |
|                       | 5| Pasa a secuencia alternativa.                                                                      |
|                       | 6| Si juez deja en blanco alguna calificación pasa a secuencia de error.                              |
|                       ||                                                                                                    |
| Secuencia Alternativa | Paso| Accion                                                                                             |
|                       | 1| Si reprueba parcialmente un examen.                                                                |
|                       | 2| Aspirante puede volver a continuar el examen en la fase que se quedó solo por el periodo de 1 año. |
|                       | 3| Si reprueba totalmente un examen                                                                   |
|                       | 4| Aspirante no puede volver a examen solo por el periodo de 3 meses.                                 |
|                       | 5| Si aspirante vuelve al examen vuelve al paso 2 secuencia normal.                                   |
| Secuencia de error    | Paso| Accion                                                                                             |
|                       | 1| Se alerta del error en determinada nota.                                                           |
|                       | 2| El sistema pide que ingresen la nota                                                               
|                       | 3| Y vuelve al paso 1 secuencia normal.|
| Importancia           | Vital||
| Urgencia              | Hay presión||
| Observaciones         |||

| Identificador         | CU-5|                                                                           |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Nombre                | Examen Cinturón Negro 1er DAN||
| Descripcion           | El sistema deberá permitir al aspirante que califique a dar el examen que corresponda en este caso examen cinturón negro 1er DAN. Este caso generaliza de realizar examen. |                                                                           |
| Precondicion          | Si el aspirante cumple todos los requisitos puede realizar examen a que se postula.|                                                                           |
| Postcondicion         | Condición final exitoso: Aspirante aprueba y es promovido. Condición final fallido: Aspirante no aprueba o suspende el examen.||
| Actores               | Tribunal y Aspirante.|                                                                           |
| Secuencia Normal      | Paso| Accion|
|                       | 1| Aspirante presenta pruebas bloque común.                                  |
|                       | 2| Aspirante presenta pruebas bloque específico.                             |
|                       | 3| Si aspirante no presenta algún bloque de las pruebas con dispensa médica. |
|                       | 4| Pasa a secuencia alternativa.                                             |
|                       | 5| Si aspirante no presenta algún bloque de las pruebas sin dispensa médica. |
|                       | 6| Pasa a secuencia error                                                    |
|                       ||                                                                           |
| Secuencia Alternativa | Paso| Accion                                                                    |
|                       | 1| Aspirante solo puede presentar examen a Cinturón Negro de Karate.         |
|                       | 2| Vuelve al paso 1 secuencia normal.                                        |
| Secuencia de error    | Paso| Accion                                                                    |
|                       | 1| El sistema desecha a aspirante                                            |
|                       | 2| Vuelve al paso 1 secuencia normal.                                        |
| Importancia           | Vital|                                                                           |
| Urgencia              | Inmediata|                                                                           |
| Observaciones         | En la secuencia alternativa en el paso 2 vuelve la paso 1 secuencia normal pero de examen a Cinturón Negro de Karate||



