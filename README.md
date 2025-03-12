# Análisis del Comportamiento de las Rutas de Transporte Público Urbano

## Descripción
Este repositorio contiene el proyecto final del curso de ETL, donde se analiza el comportamiento de las rutas de transporte público en Transportes Montebello. Se aplican procesos ETL para organizar y analizar datos de seguimiento vehicular, optimizando la asignación de despachos.

## Descripción del Proyecto
Este repositorio contiene el desarrollo del proyecto final del curso de ETL de la maestría en Inteligencia Artificial y Ciencias de Datos. El objetivo principal del proyecto es analizar el comportamiento de las rutas de transporte público urbano en la empresa **Transportes Montebello** durante el año 2024. A través de un proceso de Extracción, Transformación y Carga (ETL), se organizarán y analizarán los datos provenientes del sistema de información de la empresa **Registel**.

## Contexto
La empresa **Registel** proporciona servicios de monitoreo a empresas de transporte público mediante unidades de localización vehicular y conteo de pasajeros. Actualmente, el despacho de los vehículos se realiza de manera manual por operarios, lo que puede generar favoritismos y afectar la calidad del servicio prestado. 

Este proyecto busca organizar los datos y realizar un diagnóstico operacional de las rutas mediante el análisis de variables clave como:
- Tiempo de inicio y finalización de las rutas.
- Ubicación y disponibilidad de los vehículos.
- Asignación de despachos.
- Cantidad de pasajeros y capacidad de los vehículos.
- Distancia total de la ruta.
- Velocidad promedio.

## Problema a Resolver
Actualmente, el despacho de vehículos en la empresa **Registel** opera de manera manual y subjetiva, basándose solo en la disponibilidad de los vehículos sin considerar la demanda real ni los patrones históricos de uso. Esto genera irregularidades en los despachos y problemas de equidad entre los conductores, afectando la calidad del servicio.

Este proyecto tiene como objetivo estructurar y analizar los datos disponibles para proporcionar indicadores clave que permitan mejorar la eficiencia y transparencia en la asignación de los vehículos.

## Tecnologías Utilizadas
- **Lenguajes de Programación:** Python, SQL
- **Bases de Datos:** MySQL
- **Herramientas de ETL:** Apache Airflow, Pandas
- **Visualización de Datos:** Power BI, Matplotlib, Seaborn

## Estructura del Repositorio
```
/
|-- data/               # Datos de entrada y salida
|-- notebooks/          # Notebooks de Jupyter para análisis exploratorio
|-- scripts/            # Código de extracción, transformación y carga
|-- reports/            # Informes generados con los resultados
|-- README.md           # Documentación del proyecto
```

## Integrantes del Proyecto
- **Diana Carolina Sánchez Velasco**
- **Diego Mauricio Ortiz**
- **Deybar Andres Mora Segura**
- **Carlos Alex Macias**
- **Esteban Andrés Arroyave López**

## Cómo Contribuir
1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature-nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -m 'Agrego nueva funcionalidad'`).
4. Envía tus cambios (`git push origin feature-nueva-funcionalidad`).
5. Abre un Pull Request para revisión.

## Licencia
Este proyecto es de uso educativo y no cuenta con una licencia de distribución pública.

---
Cualquier duda o sugerencia, por favor comunicarse con los integrantes del equipo.

