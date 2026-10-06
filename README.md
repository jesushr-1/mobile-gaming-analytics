# Análisis de juegos móviles: retención de jugadores y pruebas A/B

Este proyecto analiza el comportamiento de los jugadores en un juego móvil, centrándose en dos áreas clave: la **retención de jugadores** y la **monetización**.

A partir de datos de registro, actividad de inicio de sesión y pruebas A/B, el análisis mide la retención en días específicos (D1, D7, D14 y D30) y evalúa el rendimiento de dos ofertas promocionales mediante la **tasa de conversión, el ARPU y el ARPPU**.

Se emplean pruebas de hipótesis estadísticas para determinar si las diferencias entre los grupos de control y de prueba aportan evidencia suficiente para respaldar un cambio en la estrategia promocional.

## Problema de negocio

El rendimiento a largo plazo de los juegos móviles depende tanto del **compromiso de los jugadores** (*engagement*) como de la **monetización**. Comprender si los jugadores regresan tras registrarse y cómo responden a las ofertas promocionales puede orientar las decisiones sobre el producto y el marketing.

Este proyecto aborda dos cuestiones empresariales clave:

1. **Retención de jugadores:** ¿Cuántos jugadores regresan al juego 1, 7, 14 y 30 días después de registrarse?

2. **Rendimiento de la oferta promocional:** ¿Mejora la nueva oferta promocional (Grupo B) la monetización en comparación con la oferta existente (Grupo A) sin afectar negativamente a la proporción de jugadores que realizan una compra?

El objetivo es transformar los datos de actividad de los jugadores y de ingresos en información práctica que respalde la toma de decisiones sobre retención y monetización.

## Conjunto de datos

El análisis utiliza tres conjuntos de datos provenientes del **Gamelytics Mobile Analytics Challenge**:

- **`reg_data.csv`** — Datos de registro de 1.000.000 de jugadores, que incluyen el ID de usuario (`uid`) y la marca de tiempo del registro (`reg_ts`).

- **`auth_data.csv`** — Más de 9,6 millones de registros de inicio de sesión de jugadores, que contienen el ID de usuario (`uid`) y la marca de tiempo de autenticación (`auth_ts`).

- **`ab_test.csv`** — Datos de una prueba A/B con 404.770 jugadores, que incluyen el ID de usuario (`user_id`), los ingresos generados (`revenue`) y el grupo experimental (`testgroup`).

Los conjuntos de datos de registro y autenticación se utilizan para analizar la retención de jugadores, mientras que el conjunto de datos de la prueba A/B se emplea para evaluar el impacto de diferentes ofertas promocionales en la monetización.

## Principales hallazgos

- La retención en el día exacto fue mayor en el día 7 (5,88%) entre los puntos de control analizados.
- El Grupo B registró un aumento del 5,3% en el ARPU observado y del 12,7% en el ARPPU; sin embargo, ninguno de estos incrementos fue estadísticamente significativo.
- El Grupo B mostró una disminución estadísticamente significativa en la tasa de conversión.
- A la luz de los resultados, el análisis no respalda la sustitución de la oferta promocional A por la oferta B.