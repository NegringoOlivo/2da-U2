🚀 Evaluación - Unidad 2: Logística de Agroexportación y Descomposición de Cosecha 🥑📦

Objetivo: 🎯 Desarrollar el pensamiento lógico-matemático y la capacidad de descomposición de datos numéricos en Java utilizando exclusivamente operadores aritméticos (/, %), variables de distintos tipos de precisión, constantes globales (final), lectura de datos por consola y modularidad básica (métodos auxiliares), sin recurrir a estructuras de control de flujo.

Contexto: 🚜 Logística agroindustrial en el Sur de Jalisco (Zapotlán el Grande).

📖 Contexto del Problema

Una importante planta empacadora de aguacates de exportación en Ciudad Guzmán necesita automatizar su reporte logístico diario. Al final de la jornada de cosecha, se recibe un camión con miles de aguacates a granel. El sistema debe calcular de manera automática e inmediata cómo empaquetar de forma óptima toda la producción y calcular las ganancias estimadas de la venta diaria.

Para eficientar el transporte, la empresa sigue un estricto orden de empaquetado y distribución descendente:

🥑 Aguacates Sueltos: Se cosechan y se agrupan.

📦 Rejas (Cajas): Cada reja se llena con exactamente 40 aguacates.

🪵 Tarimas (Pallets): Cada tarima almacena exactamente 24 rejas.

🚛 Contenedores de Exportación (Tractocamiones): Cada contenedor se carga con exactamente 18 tarimas.

Cualquier elemento sobrante que no complete la unidad superior se va rezagando en la cadena para su distribución local o subproductos (guacamole).

📥 Requerimientos de Entrada

El programa debe solicitar un único dato de entrada al operador del empaque:

🥑 Total de aguacates cosechados en el día (un número entero grande, ej: 58435).

⚙️ Reglas de Negocio y Cálculos (Salidas Esperadas)

Utilizando únicamente operaciones secuenciales, el programa debe realizar la descomposición en cascada y mostrar los siguientes resultados en consola:

1. 🚛 Reporte de Distribución Física:

Contenedores llenos listos para exportar (unidades máximas que se completan).

Tarimas sobrantes (que no alcanzaron a completar un contenedor y se van a refrigeración).

Rejas sobrantes (que no alcanzaron a completar una tarima y se venderán en el mercado local).

Aguacates sueltos sobrantes (que no completaron una reja y se enviarán a la procesadora de guacamole).

2. 💵 Reporte Financiero (Uso de Constantes):

Para calcular los ingresos brutos, la empresa maneja los siguientes precios fijos de venta (los cuales debes declarar como constantes final):

💲 Precio por Contenedor Exportado: $150,000.00 MXN

💲 Precio por Tarima Refrigerada: $7,500.00 MXN

💲 Precio por Reja Local: $280.00 MXN

💲 Precio por Aguacate suelto para Guacamole: $3.50 MXN

El sistema debe imprimir:

El desglose de ganancias por cada categoría.

El Ingreso Bruto Total (la suma de todos los conceptos anteriores).

El Impuesto de Exportación: Se aplica una retención aduanera del 5% (declarado como constante final double IMPUESTO_TASA = 0.05) únicamente sobre las ganancias obtenidas por los contenedores exportados.

El Ingreso Neto Real (Ingreso Bruto Total menos el Impuesto de Exportación).

⚠️ Restricciones Técnicas y Arquitectura

Para garantizar la calidad de la solución y evaluar la modularidad en etapas tempranas, los estudiantes deben apegarse a las siguientes reglas:

🛑 PROHIBIDO EL USO DE ESTRUCTURAS DE CONTROL: > Queda estrictamente prohibido usar instrucciones if, else, switch, for, while o do-while. La lógica debe resolverse combinando de manera inteligente los operadores de división entera (/) y módulo/residuo (%).

📁 Arquitectura de un Solo Archivo:

Toda la solución de software debe programarse dentro de un único archivo Java (por ejemplo, MainLogistics.java o EmpaqueLogistica.java).

Sin embargo, para mantener el código limpio y practicar la modularidad, la clase debe estructurarse de la siguiente manera:

Método Principal main: Se encarga únicamente de interactuar con el usuario (leer los aguacates con Scanner), llamar a los métodos de cálculo correspondientes e imprimir el reporte final en pantalla.

Métodos Estáticos Auxiliares (public static): Debes declarar subrutinas o métodos dedicados dentro de la misma clase (fuera del main pero dentro de la clase) para que realicen las operaciones matemáticas específicas y retornen el resultado al main.

Ejemplo de funciones sugeridas: un método para calcular el sobrante de una división, un método para calcular la ganancia bruta de una categoría, o un método para aplicar la tasa impositiva.

📤 Ejemplo de Salida Esperada en Consola ✨

Si el operador ingresa un total de 58,435 aguacates cosechados:

=====================================================
 🚜 SISTEMA LOGÍSTICO - EMPACADORA "ORO VERDE" 🚜
=====================================================
Ingrese el total de aguacates cosechados hoy: 58435

>> Procesando distribución en cascada...

-----------------------------------------------------
📦 REPORTE DE EMBALAJE (DISTRIBUCIÓN FÍSICA):
-----------------------------------------------------
🚛 Contenedores completos para exportar: 3
🪵 Tarimas sobrantes (en frío): 6
📥 Rejas sobrantes (mercado local): 10
🥑 Aguacates sueltos (procesadora): 35

-----------------------------------------------------
📊 DESGLOSE FINANCIERO ESTIMADO:
-----------------------------------------------------
+ Ingresos por Contenedores:   $450,000.00 MXN
+ Ingresos por Tarimas:        $45,000.00 MXN
+ Ingresos por Rejas:          $2,800.00 MXN
+ Ingresos por Aguacate Suelto: $122.50 MXN
-----------------------------------------------------
💰 INGRESO BRUTO TOTAL:        $497,922.50 MXN
💸 Impuesto Aduanero (5%):     -$22,500.00 MXN (Solo s/ exportación)
=====================================================
 💵 INGRESO NETO REAL:         $475,422.50 MXN
=====================================================
Reporte generado exitosamente. ¡Listo para embarque!
