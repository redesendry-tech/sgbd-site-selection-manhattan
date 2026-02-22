📊 Sistema de Gestión de Bases de Datos (SGBD)
Modelo Relacional para Análisis Territorial – Manhattan

Proyecto académico desarrollado en el marco del Máster Big Data & Business Intelligence, orientado al diseño e implementación de un modelo de base de datos relacional bajo esquema estrella para el análisis territorial en Manhattan.

🎯 Objetivo del Proyecto

Diseñar una arquitectura de datos estructurada que permita integrar múltiples fuentes heterogéneas (censo, movilidad, seguridad, competencia comercial, infraestructura urbana y costos de alquiler) con el fin de facilitar la evaluación estratégica de zonas geográficas.

🏗️ Arquitectura del Modelo

El sistema se basa en un modelo estrella, donde:

ZONAS actúa como tabla central del sistema.

CENSO y COSTO_ALQUILER mantienen relación 1:1 con la tabla central.

MOVILIDAD, SEGURIDAD, RESTAURANTES y LUGARES_INTERES mantienen relación 0:N mediante el identificador ID_ZONA.

Se implementan claves primarias, foráneas y restricciones NOT NULL para garantizar integridad referencial.

📂 Estructura del Repositorio
/docs        → Documento final del proyecto
/datasets    → Datos en formato CSV utilizados en el análisis
/diagramas   → Diagrama Entidad-Relación (PDF y modelo MySQL Workbench .MWB)
/sql         → Script SQL para creación y ejecución de la base de datos
⚙️ Tecnologías Utilizadas

MySQL

MySQL Workbench

SQL

GitHub

Datasets abiertos de NYC Open Data

🚀 Instrucciones de Ejecución

Ejecutar el script ubicado en la carpeta /sql para crear la base de datos.

Importar los datasets CSV en las tablas correspondientes.

Ejecutar las consultas analíticas incluidas en el script para realizar el análisis territorial.

📈 Proyección y Escalabilidad

La arquitectura del modelo permite su evolución hacia análisis avanzados orientados a Big Data, incluyendo procesos de clusterización, segmentación territorial y análisis multidimensional basado en la integración de múltiples variables.

👥 Equipo de Trabajo

Proyecto desarrollado por el Grupo 07 en la asignatura Sistemas de Gestión de Bases de Datos (SGBD).
