# _PATRONES DE DISEÑO_

Los patrones de diseño (design patterns) son elementos reutilizables creados para resolver problemas comunes. Es decir que con su aplicación y utilización podremos corregir diferentes problemas que presenta nuestro código de una manera segura, estable y testeada por cientos de programadores de todo el mundo.

# _¿Como se compone o sus partes?_ ䷴

Al utilizar patrones de diseño es importante considerar también si el rendimiento de nuestros sistemas se verá afectado cuando apliquemos la solución, ya que algunos patrones de diseño incorporan complejidades en el código que pueden perjudicar el desempeño de nuestros programas.
Nombre del patrón: nombre estándar del patrón por el cual será reconocido en la comunidad (normalmente se expresan en inglés). Otros nombres de uso común para el patrón.
- Clasificación del patrón: creacional, estructural o de comportamiento.
- Motivación: Escenario de ejemplo para la aplicación del patrón.
- Aplicabilidad: Usos comunes y criterios de aplicabilidad del patrón.
- Estructura: Diagramas de clases oportunos para describir las clases que intervienen en el patrón.
- Participantes: Enumeración y descripción de las entidades abstractas (y sus roles) que participan en el patrón.
- Colaboraciones: Explicación de las interrelaciones que se dan entre los participantes.
- Consecuencias: Consecuencias positivas y negativas en el diseño derivadas de la aplicación del patrón.
- Implementación: Técnicas o comentarios oportunos de cara a la implementación del patrón.
- Código de ejemplo: Código fuente ejemplo de implementación del patrón.
- Usos conocidos: Ejemplos de sistemas reales que usan el patrón.
- Patrones relacionados: Referencias cruzadas con otros patrones. 

# _Se compone_

- Patrones creacionales
- Patrones estructurales
- Patrones de comportamiento

## _Tipos y Definiciones_ 🚀

# - _Patrones creacionales_

Estos patrones se utilizan para facilitar la creación de nuevos objetos que buscan incrementar la flexibilidad y reutilización del código existente. Entre los más utilizados podemos nombrar:

- _Abstract Factory:_ Este patrón se utiliza para crear familias de objetos que se relacionan sin la necesidad de especificar sus clases.

- _Builder Patterns:_ El patrón constructor se utiliza para crear diferentes objetos a partir de una serie de pasos reutilizando el código de construcción. Esto simplifica la necesidad de crear subclases para cada configuración posible de un objeto particular.

- _Factory Method:_ Este patrón ofrece una interfaz para crear nuevos objetos dentro de una superclase permitiendo que las subclases cambien el tipo de objetos que van a crear.

- _Prototype:_ Se utiliza para crear nuevos objetos a partir de objetos existentes. A través de la declaración de una interfaz (clonar) este patrón encarga a los propios objetos la acción de clonarse.

- _Singleton:_ Se utiliza para restringir la creación de nuevas instancias de una clase a un objeto determinado.

# - _Patrones estructurales_

Los patrones estructurales buscan facilitar la acción de ensamblar objetos y clases dentro de clases estructurales más grandes sin perder la eficiencia y manteniendo la flexibilidad.

- _Adapter:_ Adaptador es un patrón que se utiliza para que objetos con interfaces incompatibles colaboren entre sí.

- _Bridge:_ El patrón Bridge resuelve un problema habitual en la herencia de clases dividiendo clases relacionadas en dos jerarquías diferentes: implementación y abstracción, para que estas puedan desarrollarse independientemente.

- _Composite:_ Solo se recomienda utilizar Composite cuando el modelo de código está creado a partir de un sistema ramificado en forma de árbol.

- _Decorator:_ Se utiliza para extender el comportamiento de un objeto añadiendo funcionalidades al mismo a través de objetos encapsuladores que presentan dichas funcionalidades.

- _Facade:_ Una fachada proporciona una interfaz simplificada para un subsistema complejo. Por ejemplo, este patrón de diseño permite integrar una aplicación con una biblioteca que tiene muchas funciones de las que solo se ocupan unas pocas.

- _Flyweight:_ Ayuda a reducir el tamaño de los objetos almacenando en su interior solo el estado intrínseco (información constante) del mismo y compartiendo el resto de la información (estado extrínseco) entre varios objetos similares.

- _Proxy:_ Este patrón de diseño se utiliza para crear objetos sustitutos que trabajan como una interfaz hacia cualquier objeto determinado.

# - _Patrones de comportamiento_

Los patrones de comportamiento buscan resolver la comunicación entre diferentes áreas

- _Chain of responsibility:_ A través de este patrón podremos evitar que la petición emitida por un emisor sea acoplada a un solo receptor permitiendo que más de un objeto pueda responder a dicha petición.

- _Command:_ Se utiliza cuando es necesario encapsular dentro de un objeto todos los parámetros que una acción requiere para ejecutarse.

- _Interpreter:_ Utilizando Interpreter podremos evaluar un lenguaje a través de una interfaz que indique el contexto en el cual se interpreta.

- _Iterator:_ Este patrón de comportamiento se utiliza cuando necesitamos iterar en colecciones o conjuntos de objetos sin la necesidad de intercambiar información relevante.

- _Mediator:_ Se utiliza cuando necesitamos controlar las comunicaciones directas entre objetos y disminuir sus dependencias caóticas.

- _Memento:_ Este patrón es capaz de almacenar y restaurar la información de un objeto.

- _Observer:_ A través de este patrón de comportamiento varios objetos interesados (suscriptores) en un objeto en particular (notificador) pueden recibir notificaciones de su comportamiento mientras estén suscriptos a sus notificaciones.

- _State:_ Se utiliza para modificar el comportamiento de una clase de objetos dependiendo del estado actual (comportamiento interno) de dichos objetos.

- _Strategy:_ Permite separar todos los algoritmos de una clase específica en nuevas clases separadas donde los objetos pueden intercambiarse.

- _Template method:_ Este patrón define el esqueleto de un algoritmo y permite a las subclases variar la implementación del comportamiento del mismo.

- _Visitor:_ A través de este patrón podremos introducir nuevos algoritmos sin modificar la estructura de objetos que se utilizarán para ejecutarlos.

## ¿Como se puede usar en AWS y que necesitaría? 💡


Al diseñar aplicaciones para cargar y recuperar objetos de AWS, use los patrones de diseño de nuestras prácticas recomendadas para lograr el mejor rendimiento para su aplicación. También ofrecemos Directrices de rendimiento para que las tenga en cuenta al planificar la arquitectura de aplicaciones.

# - _Uso del almacenamiento en caché para el contenido de acceso frecuente_

Amazon CloudFront es una red de entrega de contenido (CDN) rápida que almacena datos en caché de forma transparente desde Amazon S3 en un gran conjunto de puntos de presencia (PoP) distribuidos geográficamente. Cuando se puede tener acceso a los objetos desde multirregiones o a través de Internet, CloudFront permite que los datos se almacenen en caché cerca de los usuarios con acceso a los objetos. Esto puede dar como resultado la entrega de alto rendimiento de contenido popular de Amazon AWS.

# - _Tiempos de espera y reintentos de aplicaciones sensibles a la latencia_

AWS se escala automáticamente en respuesta a las nuevas velocidades de solicitudes sostenidas, optimizando el rendimiento de forma dinámica. Aunque AWS se está optimizando internamente para una nueva velocidad de solicitudes, recibirá respuestas a las solicitudes HTTP 503 de forma temporal hasta que se complete la optimización. Una vez que AWS optimice internamente el rendimiento para la nueva velocidad de las solicitudes, todas las solicitudes se atienden de forma general sin reintentos.

# - _Escalado horizontal y uso en paralelo de solicitudes para lograr un alto rendimiento_

Para las transferencias de alto rendimiento, Amazon S3 aconseja que se usen aplicaciones que a su vez usen varias conexiones a los datos de GET o PUT en paralelo. Por ejemplo, esto cuenta con el respaldo del gestor de transferencias de Amazon S3 en el SDK de AWS para Java. Además, la mayoría de los otros SDK de AWS proporcionan construcciones similares. Para algunas aplicaciones, puede lograr conexiones paralelas lanzando varias solicitudes simultáneamente en diferentes subprocesos de aplicación, o bien en diferentes instancias de aplicación. El mejor enfoque que adoptar depende de su aplicación y la estructura de los objetos a los que tiene acceso.

# - _Uso de Amazon S3 Transfer Acceleration para acelerar las transferencias de datos a lugares geográficos dispares_

La red de borde también ayuda a acelerar las transferencias de datos tanto dentro como fuera de Amazon S3. Resulta ideal para las aplicaciones que transfieren datos en o entre continentes, tienen una conexión a Internet rápida, usan objetos grandes o tienen mucho contenido que cargar. A medida que los datos llegan a una ubicación de borde, se redirigen a Amazon S3 a través de una ruta de red optimizada. En general, cuanto más lejos esté de una región de Amazon S3, mayor será la mejora de la velocidad que puede esperar del uso de Transfer Acceleration.

## Autores ✒️

* **Duver Salgado Rojas** - *Estudiante*
* **Fabian Silva** - *Estudiante*
* **Edward Castro** - *Estudiante*
* **Johan Salinas Acosta** - *Estudiante*
