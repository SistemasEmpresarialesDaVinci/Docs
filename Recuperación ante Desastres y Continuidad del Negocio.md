# Recuperación ante Desastres y Continuidad del Negocio

La recuperación ante desastres y continuidad del negocio se han vuelto temas críticos para toda organización moderna, frente a la creciente dependencia de los sistemas tecnológicos y la amenaza de interrupciones por causas como desastres naturales, fallas técnicas o ciberataques. Una interrupción prolongada puede tener consecuencias catastróficas si no se está adecuadamente preparado. 

## Objetivos de Tiempo de Recuperación 

Los dos parámetros clave que definen los objetivos en la recuperación ante desastres son:

**RPO - Objetivo de Punto de Recuperación:** Es la antigüedad máxima aceptable de los datos recuperados tras una interrupción. Indica cuánta información reciente se puede llegar a perder como máximo.

Por ejemplo, un RPO de 24 horas significa que deben poder restaurarse los datos hasta con 24 horas de antigüedad respecto al momento preciso del desastre.

**RTO - Objetivo de Tiempo de Recuperación:** Es el lapso total máximo aceptable para recuperar las operaciones después de un desastre. 

Por ejemplo, un RTO de 4 horas implica que todos los sistemas esenciales deben estar funcionando nuevamente en un plazo no mayor a 4 horas tras la interrupción.

Estos objetivos se deben definir en base al impacto que tendría el no disponer de ciertos sistemas o datos por un determinado período. El negocio debe realizar un análisis para identificar RTO y RPO razonables acordes a su realidad.

Ya que el RTO contempla restaurar operaciones y el RPO la pérdida de datos, es posible que el RPO sea mayor al RTO. Por ejemplo 1 día de RPO y 4 horas de RTO.

## Evaluación de Riesgos 

Antes de diseñar un plan de recuperación ante desastres, es esencial realizar una evaluación de riesgos, contemplando:

- **Análisis de Impacto:** Estimar las consecuencias que tendría la no disponibilidad de ciertos sistemas o procesos por distintos períodos. Esto permite asignar prioridades y establecer RTO y RPO realistas.

- **Identificación de Amenazas:** Determinar qué tipos de eventos disruptivos son aplicables en el contexto de la empresa, ya sean naturales (terremotos, inundaciones), técnicos (cortes eléctricos, fallas de hardware) o humanos (errores, ciberataques).

- **Análisis de Vulnerabilidades:** Detectar debilidades en la infraestructura o procesos que podrían agravar las consecuencias de una interrupción o dificultar la recuperación. 

- **Evaluación de Probabilidades:** Estimar la frecuencia o probabilidad de ocurrencia de las distintas amenazas, en base a datos históricos y estadísticos cuando sea posible.

Esto permite enfocar los esfuerzos en aquellos riesgos que tengan mayor criticidad (alto impacto y alta probabilidad). Hay que prepararse para el peor escenario plausible.

## Estrategias de Recuperación

Existen dos estrategias principales para la recuperación ante desastres:

**Sitio Alterno:** Mantener una infraestructura redundante equipada y actualizada que pueda tomar el relevo en caso de falla del sitio principal. Requiere altas inversiones.

**Reubicación:** Relocalizar las operaciones en temporales en un sitio alternativo, como instalaciones de recuperación externas o nube. Opción más flexible y escalable.

La opción ideal dependerá de factores como criticidad de operaciones, presupuesto disponible y tiempos de recuperación objetivo.

Una consideración relevante son los requerimientos de distancia geográfica entre sitios, para mitigar que un desastre regional afecte tanto al primario como al alterno. Distancias mayores a 50 km suelen ser recomendadas.

## Plan de Recuperación ante Desastres

El plan de recuperación ante desastres es un documento que detalla todos los procesos, recursos y acciones necesarias para responder y recuperarse ante una interrupción mayor, incluyendo:

**Estructura Organizacional:** Define roles y responsabilidades del personal involucrado. Establece la cadena de mando y autoridad para la toma de decisiones.

**Procedimientos de Notificación:** Describe el proceso para contactar y convocar al personal clave tan pronto se declare una contingencia. Deben mantenerse listas y datos de contacto actualizados.

**Planes Operativos:** Detalla los procedimientos específicos para recuperar cada sistema, aplicación o proceso critico, como restaurar servidores desde backups, redirigir tráfico de red, etc.

**Recursos Alternos:** Identifica los sitios e infraestructura que se utilizarán para la recuperación, ya sean propios o externos. 

**Proveedores críticos:** Indica acuerdos con proveedores esenciales como telecomunicaciones, energía, seguridad.

**Análisis de dependencias:** Mapea interdependencias entre sistemas y procesos para una recuperación secuencial.

**Pruebas:** Establece un programa de pruebas periódicas para validar la efectividad del plan. Las pruebas son esenciales.

**Actualización:** Debe mantenerse revisado frente a cambios en sistemas, procesos, infraestructura, roles de personal, regulaciones, etc.

Es una buena práctica mantener copias del plan en formato electrónico y físico, en ubicaciones distintas. Idealmente debe estar a acceso rápido incluso si los sistemas primarios fallan.

## Recuperación de Datos

Una parte indispensable de cualquier plan es la recuperación de datos críticos. Esto se logra a través de:

**Backups:** Crear regularmente copias de respaldo de todos los sistemas, bases de datos, aplicaciones y datos esenciales. Los backups deben probarse.

**Replicación:** Mantener replicación continua de los datos a un emplazamiento alterno. Permite minimizar la pérdida de datos.

**Almacenamiento remoto**: Los respaldos deben almacenarse off-site para estar aislados de cualquier amenaza local.

Idealmente, se deben utilizar backups y replicación combinados. Los backups protegen contra corrupción de datos, mientras que la replicación reduce la pérdida de datos al mínimo.

## Pruebas y Mantenimiento

Las pruebas regulares son esenciales para garantizar que los planes funcionarán en situaciones reales:

- Simulacros de escritorio para probar procesos y coordinación.

- Pruebas de restauración de backups para validar su integridad. 

- Pruebas de conmutación de sistemas críticos al sitio alterno.

- Ejecutar escenarios lo más realistas posible, previamente planificados.

Todo plan debe mantenerse continuamente actualizado a medida que cambian los sistemas, aplicaciones, infraestructura, procesos, personal y amenazas. De lo contrario, se vuelve obsoleto y pierde efectividad.

Un programa sólido de recuperación ante desastres combina estrategias técnicas, humanas y organizativas. Permite a las empresas sobrevivir incluso a interrupciones mayores y preservar sus operaciones críticas. Es una capacidad indispensable en la era digital actual.