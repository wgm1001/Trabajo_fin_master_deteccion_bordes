# Trabajo_fin_master_deteccion_bordes

**Desarrollo de un prototipo de delimitación automática de parcelas a partir de imágenes de satélite.**

Trabajo de final de Máster. Máster universitario de Inteligencia de Negocio y Big-Data en Entornos Seguros en las Universidades de Burgos, León y Valladolid

![Escudos universidades](https://github.com/wgm1001/Trabajo_fin_master_deteccion_bordes/blob/main/Documentaci%C3%B3n/img/Escudos_universidades.png)

**Realizado por**: Willow Maui García Moreno.

**Tutor**: Dr. José Francisco Diez Pastor.

---

En el contexto de la agricultura, la detección precisa de los límites de las parcelas agrícolas es fundamental para una amplia gama de aplicaciones, como la gestión eficiente de los cultivos, el monitoreo de la producción y los rendimientos, el cumplimiento normativo y la solicitud de subvenciones, el análisis de cambios en el uso del suelo, y la gestión de la propiedad de la tierra.
	
En este trabajo, los autores del artículo "AI4Boundaries: an open AI-ready dataset to map field boundaries with Sentinel-2 and aerial photography" presentan un dataset compuesto por imágenes satelitales del satélite Sentinel-2 y ortofotos de varios países europeos, con el objetivo de abordar el reto de la detección automática de los límites de las parcelas. Utilizando este conjunto de datos, se entrenaron diversos modelos de inteligencia artificial, con especial énfasis en una red neuronal convolucional de tipo U-Net, para evaluar su eficacia en la tarea de delimitación de los campos de cultivo.
	
Los resultados obtenidos en este estudio sientan las bases para futuras investigaciones en este campo de gran relevancia para el sector agrícola, al demostrar el potencial de las técnicas de aprendizaje automático para automatizar la detección de los límites de las parcelas a partir de imágenes satelitales y aéreas.

---

Como se puede ver en la estructura de archivos este repositorio se divide en dos secciones:
<ol>
  <li>Documentación: Carpeta en la que se encuentra la memoria en formato LaTeX y los recursos necesarios para generarla.</li>
  <li>Notebook: Notebook de Python sobre el que se basa el proyecto, en la memoria se explica en mayuor detalle la configuración necesaria para poder correrlo.</li>
</ol>

Ahora se mostrarán algunos de los resultados obtenidos por cuaderno:

## La segmentación realizada por el método KNN:

![Segmentación KNN](https://github.com/wgm1001/Trabajo_fin_master_deteccion_bordes/blob/main/Documentaci%C3%B3n/img/Clasificacion_KNN.png)

Cómo se puede ver si bien se puede intuir la imagen en la predicción hay demasiado ruido y podría ser más conexo.
Las métricas de esta:

![Métricas KNN](https://github.com/wgm1001/Trabajo_fin_master_deteccion_bordes/blob/main/Documentaci%C3%B3n/img/Metricas_KNN.png)

## La segmentación realizada por el método Random Forest:

![Segmentación Random Forest](https://github.com/wgm1001/Trabajo_fin_master_deteccion_bordes/blob/main/Documentaci%C3%B3n/img/Clasificacion_Random_Forest.png)

Cómo se puede ver pasa igual que con el ejmeplo anterior.
Las métricas de este:

![Métricas Random Forest](https://github.com/wgm1001/Trabajo_fin_master_deteccion_bordes/blob/main/Documentaci%C3%B3n/img/Metricas_Random_Forest.png)

## Las segmentaciones de la red U-Net:

![Segmentaciones U-Net](https://github.com/wgm1001/Trabajo_fin_master_deteccion_bordes/blob/main/Documentaci%C3%B3n/img/resultados_unet.png)

Finalmente la red U-Net es muhco más consistente, limpia y conexa a las anteriores.
Las metricas de la mejor configuración:

![Métricas U-Net](https://github.com/wgm1001/Trabajo_fin_master_deteccion_bordes/blob/main/Documentaci%C3%B3n/img/metricas_u-net.png)
