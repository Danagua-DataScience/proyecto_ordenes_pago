# Automatización del Armado de Análisis de Órdenes de Pago Bancarias

## Contexto

Este proyecto forma parte de mi portfolio profesional y fue desarrollado para automatizar el armado del papel de trabajo utilizado en el análisis de órdenes de pago bancarias, específicamente para comisiones e impuestos bancarios.

Por motivos de confidencialidad, los archivos bancarios reales no se incluyen en el repositorio.  
El foco del proyecto está en la lógica de automatización, control de errores y preparación de información para su posterior contabilización.

---

## Descripción del proyecto

El proyecto consiste en una macro desarrollada en **Excel VBA** cuyo objetivo es automatizar el armado del análisis de movimientos bancarios necesarios para la confección de órdenes de pago por comisiones e impuestos bancarios.

La automatización incluye la limpieza, transformación y preparación de archivos **Datanet** (movimientos bancarios descargados desde Interbanking), reemplazando tareas manuales repetitivas, reduciendo errores operativos y agilizando el procesamiento mensual de múltiples resúmenes bancarios utilizados en tareas contables.

---

## Objetivo de la automatización

Automatizar el procesamiento de archivos Datanet para:

- Armar automáticamente la planilla de análisis de movimientos bancarios  
- Detectar operaciones correspondientes a meses posteriores al período analizado  
- Generar tablas dinámicas listas para análisis contable  
- Incorporar información contextual clave para la contabilización  

Este proceso se aplica típicamente a un gran volumen de archivos (aprox. **50 Datanets mensuales**).

---

## Qué hace la macro

La macro realiza automáticamente los siguientes pasos:

1. Permite seleccionar un archivo CSV (Datanet)
2. Detecta si el archivo seleccionado se encuentra vacío
3. Limpia y estructura los datos en columnas
4. Convierte los importes a formato numérico
5. Identifica movimientos correspondientes al mes siguiente
6. Separa los movimientos del mes analizado y del mes siguiente (si existen)
7. Genera tablas dinámicas:
   - Movimientos del mes en análisis  
   - Movimientos del mes siguiente (si corresponde)
8. Agrega encabezados descriptivos en la hoja de tablas dinámicas:
   - Período analizado  
   - Número de fondo (identificador interno del Datanet)  
   - Número de cuenta bancaria
9. Guarda automáticamente el archivo procesado en formato Excel

---

## Estructura del proyecto

```
proyecto_ordenes_pago/
│
├── data/                           # Archivos Datanet descargados desde Interbanking (no incluidos)
├── proceso_manual/                 # Ejemplo del proceso manual previo a la automatización
├── Limpieza_Datanet_V4.xlsm        # Macro principal de automatización
├── report/                         # Screenshots de la automatización
└── README.md

```

---

## Flujo de uso

1. Abrir el archivo Excel habilitado para macros  
2. Presionar el botón para ejecutar la macro  
3. Seleccionar el archivo CSV cuando se abra la ventana de Windows  
4. Seleccionar la carpeta donde se guardará el archivo procesado  
5. Esperar a que finalice la ejecución  

---

## Input

- Archivo CSV descargado desde Interbanking  
- Estructura fija y estandarizada  
- La macro contempla el caso de archivos vacíos  

> Nota: Los archivos reales no se incluyen en el repositorio por motivos de confidencialidad.

---

## Output

- Archivo Excel generado automáticamente  
- Nombre del archivo con el siguiente formato:  
  `numero_datanet + " " + MM-YYYY`

**Ejemplo:**  
`308 04-2025.xlsx`

---

## Herramientas utilizadas

- Microsoft Excel  
- VBA (Visual Basic for Applications)  

---

## Enfoque del proyecto

Este desarrollo está orientado a:

- Automatización de tareas rutinarias  
- Reducción de errores humanos  
- Ahorro significativo de tiempo operativo  
- Uso contable y administrativo  
- Preparación de información para contabilizar gastos e impuestos bancarios  

---

## Estado del proyecto

**Estado actual:** funcional y en uso operativo.  

El proceso se encuentra completamente automatizado y listo para ser utilizado de forma recurrente.

---

## Autor

**Dylan Anagua**  
Data Analyst | Finance & Reporting  

Proyecto orientado a eficiencia operativa, control contable y reducción de tareas manuales repetitivas.