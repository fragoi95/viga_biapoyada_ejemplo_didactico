# Viga biapoyada — ejemplo didáctico

**Francisco Goitia** · [francisco.goitia@upc.edu](mailto:francisco.goitia@upc.edu)

Calculadora interactiva de una viga simplemente apoyada (articulación a la izquierda y apoyo móvil a la derecha), sometida a una carga vertical uniformemente distribuida. Los diagramas se actualizan al modificar los datos.


## Aplicación oline

https://fragoi95.github.io/viga_biapoyada_ejemplo_didactico/


## Qué permite modificar

- Luz entre apoyos, **L** (m).
- Carga distribuida, **q** (kN/m).
- Sección rectangular: ancho y altura (mm).
- Perfil doble T idealizado: altura, ancho de ala y espesores de alma y alas (mm).
- Módulo de elasticidad, **E** (GPa).

## Qué muestra

A la izquierda están los datos de entrada. A la derecha aparecen, en orden:

1. Esquema estructural, carga distribuida y reacciones verticales.
2. Diagrama de momentos flectores, con el máximo en el centro de la luz.
3. Diagrama de cortante, con los valores extremos en los apoyos.
4. Deformada elástica, con la flecha máxima en el centro.

Los valores se indican directamente sobre los esquemas.

## Expresiones utilizadas

Para carga distribuida uniforme en toda la luz:

```text
RA = RB = q·L/2
|V|max = q·L/2
Mmax = q·L²/8
δmax = 5·q·L⁴/(384·E·I)
```

La inercia centroidal respecto al eje fuerte se calcula con:

- Sección rectangular: `I = b·h³/12`.
- Doble T con alas iguales: `I = [b·h³ − (b−tw)·(h−2·tf)³]/12`.

En el cálculo de la flecha se convierten todas las magnitudes a unidades compatibles; el resultado se expresa en **mm**.

## Hipótesis y alcance

Modelo de Euler–Bernoulli, con comportamiento elástico lineal, sección constante y pequeñas deformaciones. Se desprecia la deformación por cortante y no se consideran efectos de segundo orden. La doble T se idealiza con alas rectangulares iguales y alma centrada, sin radios de acuerdo.

La carga `q` debe incluir el peso propio si corresponde. La deformada se amplifica gráficamente para facilitar su visualización. Es una herramienta para docencia y comprobaciones preliminares, no una verificación normativa de resistencia o servicio.


