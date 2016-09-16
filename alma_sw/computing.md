<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. ALMA Software lingo</a></li>
</ul>
</div>
</div>

# ALMA Software lingo<a id="sec-1" name="sec-1"></a>

-   **ACACOR:** (O ACA Correlator) Correlador más pequeño que realiza FFT sobre los datos obtenidos por las antenas.
-   **Ambiente:** Sistema que emula todas las características de un servidor para el deployment de software. Anteriormente se utilizaban máquinas virtuales, actualmente se está pasando a hacer uso de Docker.
-   **Ambiente de Pre-producción:** Ambiente en el cual se prueba el software offline en una fase final, con bases de datos actualizadas, para luego ser desplegadas en producción.
-   **AOD:** Astronomer on Duty
-   **AOS:** STE/APE
-   **APE:** Nuevo ambiente de producción online.
-   **ARCHIVE:** Subsistema encargado del manejo de datos asociados a propuestas y observaciones astronómicas
-   **Bulk data:** Canal de transmisión de datos masivos. Utiliza TCP o UDP. Está basado en Data Distribution Service (DDS).
-   **Candidate:** Release de software candidato a ir a producción.
-   **CDP:** Correlator Data Processor. Está constituido por un servidor Master y nodos, los cuales se comunican mediante bulk data. Utiliza de comunicación unicast de nodos a master.
-   **Ciclo de release:** Ciclo 3 se encuentra ya en producción (deployed). Ciclo 4 estará estable en octubre. A partir del ciclo 5 se realizarán releases incrementales.
-   **Ciclos:** Puede referirse a etapa del ciclo de vida de software o etapa del proceso de observación astronómica. Ambos estan relacionados, ya que el software debe estar disponible para ciertos milestones del ciclo de observación.
-   **Data Distribution Service (DDS):** estándar de transmisión de datos hecho por los creadores de CORBA.
-   **Deployment:** Existe de producción y de pre-producción.
-   **Docker:** Sistema de deployment de aplicaciones Linux dentro de contenedores de software.
-   **DSACore:** Algoritmo de scheduling que corre en un servidor. Se usa tanto en online como en offline.
-   **OBOPS:** Susbsistema que agrupa herramientas, mayoritariamente offline, para manejo de usuarios, propuestas y ciclos de observación.
-   **OBSPREP:** Subsistema que agrupa herramientas para el manejo de propuestas de observación enviadas.
-   **Offline:** Sistema que agrupa todos aquellos componentes de software que no son críticos para el funcionamiento del radiotelescopio. La mayoría de las aplicaciones web pertenecen al sistema offline.
-   **Online:** Sistema que agrupa todos aquellos componentes de software que son críticos para el funcionamiento del radiotelescopio.
-   **Release:** En offline son más frecuentes que en online.
-   **SCHEDULING:** Subsistema encargado de administrar los tiempos de observación de cada proyecto.
-   **STE:** Antiguo ambiente de producción online.
-   **WAR:** Formato de paquetes de aplicaciones web de Java. Se utilizan para los componentes del sistema offline.