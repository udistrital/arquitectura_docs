# Proceso de desarrollo en devops

DevOps es un concepto que engloba principios, metodologías y herramientas con el propósito de alinear los equipos de Desarrollo, TI y Calidad en la coordinación de acciones encaminadas a lograr los objetivos estratégicos de la organización para que asi se pueda utilizar los servicios proporcioandos por Sistemas con eficacia.

## Modelo

![devops](imagenes/devops.png "proceso de desarrollo en devops")

## Roles

- Líder del proyecto
- Equipo de desarrollo
  - Ingeniero de desarrollo
  - Ingeniero de calidad
  - Ingeniero devops
- Ingeniero de automatización

## Herramientas de apoyo al proceso devops

### Control y gestión de las entregas

El principal objetivo es que todos los equipos involucrados en la instalación y procesos de despliegue respondan rápidamente, de forma que se reduzca la espera, se comparta el conocimiento y se reduzcan las emergencias de última hora. Para alcanzar este objetivo evops propende a que los equipos deben planificar conjuntamente para obtener un mejor entendimiento de las dependencias y puedan identificar cuellos de botella antes que aparezcan, y pueden priorizar adecuadamente antes los conflictos que puedan surgir.

### Repositorio de fuentes

El repositorio de fuentes permite almacenar en una misma ubicación todos los elementos que se utilizarán durante la construcción, siendo éste el único punto desde el que los motores de construcción recuperaran las fuentes para construir. Los repositorios de fuentes y las técnicas adecuadas de desarrollo en paralelo permiten acelerar el desarrollo de múltiples cambios simultáneos en las aplicaciones.

### Repositorio de binarios

El repositorio de binarios o minificados es la piedra angular de la implantación ya que será de éste de donde se recuperará todos los artefactos que se deben de instalar. Estos artefactos pueden ser entregados por los equipos de Desarrollo o por los motores de construcción, y serán recuperados de éste por el motor de automatización de implantación.

### Integración continua CI

La integración continua es la encargada de recuperar del repositorio de fuentes los elementos necesarios para generar de forma controlada y automatizada los artefactos, que almacenará en el repositorio de ejecutables, y serán instalados posteriormente en los entornos de ejecución.

### Motor de despliegue

El motor de despliegue se encarga de recuperar los artefactos del repositorio de binarios y de su distribución a las máquinas donde son necesarios para que una aplicación pueda utilizarse. El motor de despliegue debe ofrecer aumentar la frecuencia de implantación garantizando la consistencia de las implantaciones de manera frecuente, predecible, trazable, escalable y repetible.

### Controles de Calidad (QA)

Los equipos de calidad teóricamente debieran colaborar con los equipos de desarrollo para escribir los casos de pruebas automáticos desde el comienzo del desarrollo. Estos casos de prueba deberán demostrar que la aplicación implementa la funcionalidad solicitada qapor Negocio.

Los casos de prueba deben ejecutarse cada vez que se realiza una modificación en el código, tanto de cara a validar que cada nueva versión implementa las nuevas funcionalidades permitiendo mediante pruebas de regresión verificar que las funcionalidades existentes siguen funcionando de igual forma.

### Monitorización

La monitorización consiste en la vigilancia de todos los servicios activos que una máquina ofrece y es vital dentro devops ya que cada vez que se despliegue una nueva versión de la aplicación se debe supervisar la información generada por la monitorización de cara a identificar posibles problemas antes de que se despliegue en producción asegurando así que la nueva versión de la aplicación no genera problemas en las infraestructuras existentes y evita posibles impactos en producción.

## Característcas

### Consistencia:

-- Todos los procedimientos son comunes para todos los entornos.
-- Todas las tareas necesarias para implantar están identificadas en un único lugar.
-- Se utilizan procedimientos de construcción homogéneos y controlados.
-- Se utiliza las mismas herramientas de implantación para todos los entornos.
-- Se utiliza las mismas herramientas de infraestructura para todos los entornos.

### Eficiencia:

-- Reducción de las tareas manuales.
-- Reducción de tareas redundantes y por lo tanto innecesarias.
-- La información estará siempre accesible.
-- Reducción de la dependencia del conocimiento de una persona.

### Seguridad:

-- Minimización del ratio de error manual
-- Mismo despliegue en todos los entornos

### Visibilidad:

-- Inventario de los artefactos que forman las aplicaciones.
-- Instalación controlada y gestionada
-- Simplicidad en las auditorias
