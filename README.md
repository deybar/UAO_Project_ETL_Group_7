# Análisis del Comportamiento de las Rutas de Transporte Público Urbano

## Descripción
Este repositorio contiene el proyecto final del curso de ETL, donde se analiza el comportamiento de las rutas de transporte público en Transportes Montebello. Se aplican procesos ETL para organizar y analizar datos de seguimiento vehicular, describiendo el comportamiento de las rutas sus tiempos y distancias.

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

## Diccionario de los datos disponibles

| Nombre de Columna       | Descripción                                                                 | Tipo de Dato      | Formato/Ejemplo   | Valores Posibles                                                                 | Notas                                                                 |
|-------------------------|-----------------------------------------------------------------------------|-------------------|-------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| FECHA_INICIAL           | Fecha real en que se inició el despacho.                                    | datetime          | YYYY-MM-DD        | Cualquier fecha válida.                                                         |                                                                       |
| HORA_INICIAL_PLAN       | Hora planificada para el inicio del despacho.                               | timedelta o time  | HH:MM:SS          | Horas en formato de tiempo.                                                     | Puede convertirse a segundos o horas decimales.                       |
| HORA_INICIAL_REAL       | Hora real en que se inició el despacho.                                     | timedelta o time  | HH:MM:SS          | Horas en formato de tiempo.                                                     | Valores nulos indican que no se registró la hora real.                |
| HORA_INICIAL_AUX        | Hora de inicio obtenida de la información registradora.                     | timedelta o time  | HH:MM:SS          | Horas en formato de tiempo.                                                     | Usada como respaldo o verificación.                                   |
| FECHA_FINAL             | Fecha real en que se finalizó el despacho.                                  | datetime          | YYYY-MM-DD        | Cualquier fecha válida.                                                         |                                                                       |
| HORA_FINAL_PLAN         | Hora planificada para la finalización del despacho.                         | timedelta o time  | HH:MM:SS          | Horas en formato de tiempo.                                                     |                                                                       |
| HORA_FINAL_REAL         | Hora real en que se finalizó el despacho.                                   | timedelta o time  | HH:MM:SS          | Horas en formato de tiempo.                                                     | Valores nulos indican que no se registró la hora real.                |
| HORA_FINAL_AUX          | Hora de finalización obtenida de la información registradora.               | timedelta o time  | HH:MM:SS          | Horas en formato de tiempo.                                                     | Usada como respaldo o verificación.                                   |
| FK_RUTA                 | Llave foránea que identifica la ruta asociada al despacho.                  | int o string      | Ejemplo: RUTA_001 | Valores únicos correspondientes a rutas en otra tabla.                          | Relación con la tabla de rutas.                                       |
| PASAJEROS               | Número de pasajeros transportados en el despacho.                           | int               | Ejemplo: 45       | Números enteros ≥ 0.                                                            |                                                                       |
| DISTANCIA               | Distancia recorrida durante el despacho (en kilómetros u otra unidad).      | float             | Ejemplo: 12.5     | Números ≥ 0.                                                                    | Unidad de medida debe especificarse en metadata.                      |
| FK_VEHICULO             | Llave foránea que identifica el vehículo utilizado.                         | int o string      | Ejemplo: VEH_123  | Valores únicos correspondientes a vehículos en otra tabla.                      | Relación con la tabla de vehículos.                                   |
| FK_CONDUCTOR            | Llave foránea que identifica al conductor del despacho.                     | int o string      | Ejemplo: COND_456 | Valores únicos correspondientes a conductores en otra tabla.                    | Relación con la tabla de conductores.                                 |
| ESTADO_DESPACHO         | Estado del despacho según su progreso.                                      | int o categoría   | Ejemplo: 3        | 0: No controlado, 2: Controlado (Adelantado/Atrasado), 3: Controlado (En tiempo), 4: Terminado manualmente | Codificación numérica de estados.                                     |
| PK_INTERVALO_DESPACHO   | Llave primaria única que identifica el intervalo del despacho.              | int               | Ejemplo: 1001     | Valores únicos y no nulos.                                                      | Identificador único para cada registro.                               |


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

