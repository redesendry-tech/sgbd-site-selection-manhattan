📊 Sistema de Gestión de Bases de Datos (SGBD)
Modelo Relacional para Análisis Territorial – Manhattan


Este repositorio contiene la estructura completa de una base de datos analítica en MySQL basada en un modelo estrella (Star Schema). Incluye el script de creación de la base de datos, datasets en formato CSV para poblarla, el diagrama del modelo y documentación académica relacionada.

El objetivo es permitir la implementación del modelo desde cero, cargar los datos correctamente y validar su funcionamiento siguiendo una secuencia ordenada.

---

## 📁 Organización del repositorio

### 📂 sql/
Contiene el script principal para implementar la base de datos:

- **Estructura_DB_TFM_Manhattan.sql**
  - La primera parte del archivo crea la base de datos, tablas y relaciones.
  - La segunda parte contiene consultas de verificación que deben ejecutarse después de cargar los datasets.

---

### 📂 datasets/
Archivos CSV necesarios para poblar la base de datos:

- **ZONAS.csv** → Tabla principal del sistema (debe cargarse primero).
- **CENSO.csv** → Datos demográficos.
- **COSTO_ALQUILER.csv** → Información de precios de alquiler.
- **MOVILIDAD.csv** → Datos sobre transporte y accesibilidad.
- **SEGURIDAD.csv** → Indicadores de seguridad.
- **RESTAURANTES.csv** → Información comercial y gastronómica.
- **LUGARES_INTERES.csv** → Sitios relevantes o estratégicos.

---

### 📂 diagramas/
Representación visual del modelo de base de datos:

- **Diagrama ER.pdf** → Diagrama entidad-relación.
- **Diagrama ER.mwb** → Archivo editable en MySQL Workbench.

---

### 📂 docs/
Documentación académica del proyecto:

- Documento explicativo del modelo y su finalidad.

---

## ⚙️ Requisitos previos

Antes de ejecutar el proyecto se recomienda tener:

- MySQL Server 8.x instalado.
- MySQL Workbench u otro cliente SQL.
- Los archivos del repositorio descargados y descomprimidos.

---

## 🚀 Guía de ejecución paso a paso

### 1. Crear la base de datos y las tablas

1. Abrir MySQL Workbench.
2. Conectarse al servidor MySQL.
3. Abrir el archivo:

4. Ejecutar únicamente la primera parte del script, correspondiente a:
   - Creación de la base de datos.
   - Creación de las tablas.
   - Definición de las relaciones.

**Nota:**  
La parte final del script contiene consultas de verificación y no debe ejecutarse todavía.

---

### 2. Seleccionar la base de datos creada

Después de ejecutar la creación:

1. Actualizar la lista de esquemas en MySQL Workbench.
2. Ubicar la base de datos creada.
3. Seleccionarla como esquema activo antes de importar datos.

Esto evita cargar información en una base incorrecta.

---

### 3. Cargar los datasets en orden correcto

Para mantener la integridad de las relaciones entre tablas, los archivos deben cargarse en la siguiente secuencia:

**Orden recomendado:**

1. **ZONAS.csv**
   - Es la tabla principal y referencia para otras tablas.
   - Debe cargarse primero para evitar errores de claves foráneas.

2. Luego cargar:
   - CENSO.csv
   - COSTO_ALQUILER.csv
   - MOVILIDAD.csv
   - SEGURIDAD.csv
   - RESTAURANTES.csv
   - LUGARES_INTERES.csv

---

### 4. Importar los archivos CSV en MySQL Workbench

Para cada dataset:

1. Localizar la tabla correspondiente dentro de la base de datos.
2. Hacer clic derecho sobre la tabla.
3. Seleccionar **Table Data Import Wizard**.
4. Elegir el archivo CSV correspondiente.
5. Confirmar delimitador de columnas (generalmente coma).
6. Verificar coincidencia entre columnas del archivo y la tabla.
7. Ejecutar la importación.

Se recomienda revisar cada tabla después de importar para confirmar que los registros fueron cargados correctamente.

---

### 5. Verificar la creación y carga de datos

Una vez cargados todos los datasets:

1. Volver al archivo SQL principal.
2. Ejecutar la segunda parte del script.
3. Esta sección contiene consultas de verificación para:
   - Confirmar la carga de datos.
   - Validar relaciones entre tablas.
   - Comprobar la estructura del modelo.

---

## 📊 Finalidad del modelo

El modelo estrella implementado permite:

- Integrar datos territoriales de distintas dimensiones.
- Analizar zonas estratégicas.
- Apoyar la toma de decisiones basada en datos.
- Facilitar análisis comparativos y evaluaciones urbanas.

---

## 🎓 Uso académico
Este repositorio forma parte de un proyecto académico orientado al diseño de bases de datos analíticas y al análisis territorial mediante modelos estrella en MySQL.

