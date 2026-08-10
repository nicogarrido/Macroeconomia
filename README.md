# ICOM401 — Macroeconomía II

Material del curso **Macroeconomía II** (ICOM401), Escuela de Ingeniería Comercial,
Facultad de Economía y Negocios, Universidad Andrés Bello.

## Contenido

| Archivo | Descripción |
|---|---|
| `index.html` | Portada del curso: material, programa, calendario de 18 semanas, evaluación y bibliografía. |
| `clase1-noticias-macro-chile-2026.html` | Clase 1 — la economía chilena en agosto de 2026, con gráficos, preguntas de discusión y un simulador IS-LM de economía cerrada. |
| `islm-da-oa-pib.html` | Repaso de economía cerrada — tres paneles sincronizados (IS-LM, DA-OA y la serie del PIB en el tiempo), con construcción interactiva de la DA y seis shocks animados. |
| `balanza-de-pagos-pii.html` | Unidad I — la balanza de pagos derivada desde los balances de residentes y no residentes. Siete operaciones sobre dos balances espejo, con la PII recalculándose, el informe del año armándose solo y la derivación algebraica de CC = S − I por dos caminos. |

Todas las páginas son HTML autocontenido: sin dependencias externas, sin build,
sin conexión necesaria. Se abren con doble clic o se publican tal cual.

## Publicar en GitHub Pages

1. Subir los archivos a la raíz del repositorio.
2. En el repositorio: **Settings → Pages → Source: Deploy from a branch**,
   rama `main` y carpeta `/ (root)`.
3. El sitio queda en `https://<usuario>.github.io/<repositorio>/`.

`index.html` en la raíz se sirve automáticamente como portada.

## Agregar una clase nueva

En `index.html`, dentro de la sección `#material`, hay un bloque comentado con la
plantilla de tarjeta. Copiarlo, cambiar `href`, etiqueta, título y descripción.
Para material que todavía no está listo, usar `class="mat soon"` y dejar el `href` vacío.

## Datos

Las cifras macroeconómicas de la clase 1 están actualizadas al 3 de agosto de 2026
y cada una lleva su fuente al pie de la página (Banco Central de Chile, INE, prensa).

En `islm-da-oa-pib.html`, la serie del PIB real de Chile es un índice 2018 = 100
construido a partir de las tasas de crecimiento anual del Banco Central, con tendencia
por filtro Hodrick-Prescott (λ = 100). La vista en pesos ancla ese índice al PIB nominal
2025 efectivo ($339.978 miles de millones, DIPRES), de modo que la serie queda expresada
en billones de pesos de 2025; las constantes `ANCLA_BILLONES` y `ANCLA_ANIO` están
aisladas al comienzo del script para poder cambiar el ancla en una línea. La cifra de
2026 (1,3%) es la proyección de mercado, no un dato observado.

En `balanza-de-pagos-pii.html`, el ejemplo de las siete operaciones es una construcción
didáctica con números redondos, calibrada para que la cuenta corriente, la cuenta
financiera y la variación de la PII coincidan exactamente en −18. "Escondida" se usa
como nombre reconocible de una empresa residente con dueños no residentes, no como
referencia a sus cifras reales. Las cifras reales de
la Posición de Inversión Internacional son del anuario de Balanza de Pagos del Banco
Central al cierre de 2024. Las definiciones de residencia siguen el MBP6 del FMI.
