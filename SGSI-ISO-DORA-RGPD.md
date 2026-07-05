
# **9. Tratamiento de riesgos** 

Las decisiones de tratamiento de cada riesgo están vinculadas a los objetivos de seguridad de la información, es decir, los puntos mencionados en el apartado 6.2 (Explícito de los objetivos de la seguridad de la información):

* Garantizar la CID   
* Implementación del MFA  
* Detección y respuesta ante incidentes  
* Reducción de incidentes de phishing  
* Cumplimiento normativo DORA, ISO 27001 (con la 27002) y RGPD

De esta manera, en un primer lugar, todas las decisiones para tratar cada riesgo identificado acaban contribuyendo en cierta medida a los objetivos principales de la seguridad de la información introducidos con el SGSI, pudiendo también ser evaluadas en revisiones tras incidentes o auditorías.

* **Datos de clientes**  
  * Phishing🡪Mitigar  
    Cursos de concienciación a los empleados para que en un primer lugar puedan identificar y descartar correos de phishing. Aparte de eso, una medida que revise los correos de entrada al banco, que confirmen si son legítimos o no. Por otro lado, par los clientes se les mandarán correos de concienciación/advertencia.  
  * Robo de datos🡪Mitigar/Transferir  
    Se puede mitigar controlando el acceso (Con diferentes controles de accesos) y aplicando 2FA, aparte de encriptar los datos, filtrar correos con acceso y concienciar a los clientes y empleados.  
* **App de banca online**  
  * Inyecciones sql🡪Mitigar  
    Para poder prevenir dichos ataques lo más recomendable sería quitar todas las entradas permitidas de los usuarios, validar la entrada de datos, aplicar procedimientos correctos y usar consultas parametrizadas (java EE, .net, PHP, …).  
    (Anon., 2025)  
  * Ataques de scripting🡪Mitigar  
    Para mitigar los ataques de scripting, se deben de validar las entradas, llevar a cabo pruebas de penetración para hallar nuevas vulnerabilidades de la misma clase, o revisiones de los datos de entrada en el servidor para confirmar que no son código malicioso.  
    (CLOUDFLARE, 2026)  
  * Puertos desprotegidos🡪Mitigar   
    Se pueden aplicar diferentes medidas de seguridad, como bloquear puertos al menos que den afuera de la red del banco, implementar seguridad de los puertos (port security), y vigilar accesos a los mismos en tiempo real.  
* **Infraestructura cloud**  
  * Accesos no autorizados/Malas autenticaciones🡪Mitigar  
    Revisar en tiempo real los logs para comprobar que no haya comportamiento sospechoso respecto a intentos o ips desconocidas.  
  * Caídas del servicio🡪Transferir/Mitigar  
    Hay que tener un servidor de repuesto o varios para que sustituyan al principal. Por otro lado, hay que tener un equipo de expertos que resuelvan el problema de la caída del servicio.  
* **APIs financieras**  
  * Robo de tokens🡪Mitigar  
    Que los tokens de inicio de sesión sean temporales, que tengan cifrado, y que se tenga una autenticación más segura.  
* **Datos de los empleados**  
  * Robo y manipulación de cuentas profesionales🡪Mitigar  
    Se puede aplicar la MFA, controlar accesos y monitorizar la actividad interna en busca de comportamiento fuera de lugar.  
* **Registros financieros**  
  * Manipulación de datos🡪Mitigar  
    Aplicar backups periódicos para no perder mucha información en caso de alteración, controlar la integridad de los mismos y llevar a cabo auditorias de seguridad.  
* **Servicios internos**  
  * Interrupciones🡪Aceptar/Intentar mitigar  
    Implementar planes de continuidad en el banco, más no se puede hacer ya que es prácticamente inevitable.  
  * Toda clase de ataques internos🡪Mitigar  
    Se pueden controlar, a pesar de ser ciertamente casi inevitables, con equipos de defensa y de respuesta ante incidentes, segmentando la red y monitorizándola.  
* **Servidores**  
  * Ransomware🡪Mitigar  
    Implementar medidas de seguridad como segmentaciones de red (para evitar que se extienda), un EDR, y llevar a cabo backups recurrentes de las bases de datos.  
  * Ddos🡪Mitigar/Transferir  
    Tener otros servidores y/o servicios en la nube para desviar el tráfico no malintencionado y mantener continuidad.  
* **Red interna**  
  * Intrusión🡪Mitigar  
    Se pueden usar firewalls e implementar políticas de seguridad.  
* **Empleados**  
  * Error humano🡪Mitigar  
    Se debe formar a los empleados, implementar políticas de seguridad adecuadas y automatizas procesos críticos.  
* **Clientes**  
  * Fraude🡪Mitigar  
    Implementar sistemas antifraude, reforzar la autenticación de los clientes, e implementar seguros.

# **10. Plan de tratamiento de riesgos** 

El plan de tratamiento de riesgos de ChamBank traduce las decisiones tomadas en el tratamiento de riesgos en acciones concretas propuestas. DORA exige que las entidades financieras documenten dicho plan, lo que en ChamBank tiene una implantación práctica en la que los controles no pueden decidirse aleatoriamente, sino que deben de estar justificados, priorizados y deben de ser revisables para las auditorías.

## **10.1. Acciones propuestas** 

Anteriormente se establecieron prioridades en base al riesgo y a los gastos potenciales que suponen, ordenándose por ese mismo factor, en la sección de análisis de riesgos. Ya con una vez esos riesgos identificados, y ordenados en base a prioridad, se van a llevar a cabo diferentes acciones en el banco para abordarlos a lo largo del tiempo o de manera inmediata si son muy graves. También, se va a analizar el tipo de control que tiene cada acción propuesta. Las propuestas se pueden clasificar en controles:  

* Preventivos: Previenen que ocurran incidentes, actuando como la primera línea de defensa contra varias amenazas.  
* Detectivos: Son controles que identifican los incidentes de seguridad o anomalías mientras tienen lugar en el banco.  
* Correctivo: Se diseñan controles de seguridad para minimizar el impacto de los incidentes y facilitar en la medida de lo posible la recuperación.

(Sunrise, 2026)

La clasificación sería:

* Prioritarios/Urgentes

| Riesgo | Acciones propuestas | Tipo de control |
| :---: | ----- | :---: |
|  Robo de datos | Aplicar cifrados a los datos Controlar el acceso MFA |  Preventivo |
|  Ransomware | Backups periódicos Implementar soluciones EDR  | Detectivo/ Preventivo |
| Ataques internos | Monitorización continua Segmentación de la red Control de acceso privilegiado |  Preventivo |

* Correcciones a futuro

| Riesgo | Acciones propuestas | Tipo de control |
| :---: | ----- | :---: |
|  Phishing | Implementar programas de formación a los empleados Implementar filtros o revisiones previas de correos entrantes |  Preventivo |
|  Scripting | Aplicar validaciones de entradas de datos  Tener un equipo que bloquee las amenazas en caso de que pasen | Preventivo/ Correctivo |
|  Puertos desprotegidos | Aplicar seguridad a los puertos (port security) Desactivar puertos innecesarios  Monitorizar accesos | Preventivo/ Detectivo |
| Accesos no autorizados | Implementar MFA Controlar accesos/logs | Preventivo/ Detectivo |
| Tokens | Usar cifrados para los tokens Tokens temporales | Preventivo |
|  Caídas del servicio | Implementar sistemas de reemplazo o de desvío Tener planes de resiliencia Implementar equipos que se centren en la recuperación de los servicios |  Correctivo |
|  Manipulación de datos | Tener backups de las bases de datos (método 3-2-1) Implementar autenticaciones de identidad Implementar acceso a los datos en función del rango |  Preventivo |
| Denegación de servicios | Límite de intentos/solicitudes de una misma ip externa Implementar servicios de protección en la nube | Preventivo/ Correctivo |
|  Intrusiones | Firewalls IDS/IPS Implementar equipos de respuesta ante incidentes | Preventivo/ Detectivo/ Correctivo |

* Asumibles

| Riesgo | Acciones propuestas | Tipo de control |
| ----- | ----- | :---: |
|  Interrupciones | Desarrollar planes de continuidad del banco Resiliencia |  Correctivo |
| Dispositivos externos | Definir políticas de uso de dispositivos ajenos dentro del banco | Preventivo |
| Errores humanos | Formación continua de los empleados | Preventivo |

(ISOWin, 2017)  
(Caña, 2025)  
(OpenLearn, 2026)  
La decisión de los tratamientos de riesgos se ha tomado en cuenta en base al coste que supondrían cada uno de los riesgos, el impacto potencial, y la prioridad de ChamBank en base al propio concepto de banco digital:

* Robo de datos: Mitigar (prioritario)  
  Con su coste estimado y las consecuencias legales que conllevaría, el coste de mitigación es menor al coste potencial de una brecha. Además, la filtración de datos afecta a la reputación del banco y la confianza del cliente. Evitar este riesgo es imposible ya que los datos de los clientes son imposibles de ignorar.  
* Ransomware: Mitigar (prioritario)  
  Una parada de servicios por un ransomware en el sector financiero, a pesar de ser “tolerable” o recuperable si se ve desde un punto de vista de pérdidas financieras si existe un seguro en la entidad, definitivamente afectaría a la confianza del cliente. Hay que tener en cuenta también que el coste de implementar medidas preventivas o mitigadoras frente a este tipo de ataques tiende a ser menor que el coste de impacto del mismo y hay que tener en cuenta el tiempo de inactividad.  
* Interrupciones: Aceptar/mitigar (asumible)  
  Se acepta parcialmente debido a que el coste estimado del impacto potencial es bajo, y las interrupciones puntuales no generan consecuencias significativas. En ChamBank, invertir en el mismo presupuesto en mitigar ransomware o phishing tiene un retorno de seguridad mayor para ChamBank. No significa que se vaya a ignorar el riesgo, pero se priorizará adecuadamente en el presupuesto disponible.  
* Caídas del servicio cloud: Transferir/mitigar  
  Transferir el riesgo completamente no es viable ya que, aunque el proveedor pueda compensar económicamente el incidente, ante los clientes, el responsable de la caída del servicio sería ChamBank.

## **10.2. Impacto de los controles del SGSI** 

Los controles propuestos no actúan de manera aislada, su implementación tiene un efecto de acumulación respecto a la madurez y la resiliencia del SGSI en tres aspectos:

* **Reducción de la superficie de ataque**  
  La combinación de medidas como el MFA, el cifrado de datos, los controles de acceso, etc., no evita los incidentes, pero asegura que el banco esté más seguro. Cada control que se implemente reduce la probabilidad de los riesgos en cierta medida, lo cual, con el paso del tiempo, se deberá ver reflejado en los posteriores análisis de riesgos.  
* **Resiliencia**  
  Los controles como backups, servidores de respaldo, planes de recuperación o similares no evitan incidentes, pero garantizan que ChamBank pueda seguir operando correcta y continuamente o que sus tiempos de recuperación sean cortos. Para entidades financieras europeas, es exigido por el reglamento DORA.  
* **Apoyo a la mejora continua**  
  La aplicación de controles como la monitorización continua, logs de auditorías, las pruebas de penetración, etc., sirven para obtener resultados objetivos que el comité deberá revisar periódicamente. Una vez revisados dichos resultados, el comité puede optar por cambios y mejoras para estar preparados ante nuevas amenazas, o nuevas condiciones reglamentarias.

# **11. Implantación del SGSI** 

## **11.1. Recursos necesarios** 

Para implementar correctamente el SGSI en ChamBank, hay que disponer de los recursos adecuados que permitan establecer, mantener y poder mejorar dicho SGSI. Acorde a la ISO27001, estos recursos deben de ser garantizados por el banco. A pesar de que la ISO27001 no define explícitamente los recursos necesarios (ya que los decide cada empresa), normalmente se pueden clasificar en:

* **Recursos humanos**  
  * Equipos de expertos que puedan llevar a cabo diversas actividades de seguridad dependiendo del caso (Forense, defensa, mitigaciones, auditorias, pruebas de penetración, equipos especializados en la respuesta ante incidentes, …).  
  * Personas individuales que puedan administrar a dichos equipos (CISO, CTO, CSO, …) y/o que tengan relevancia a la hora de tomar decisiones.  
* **Recursos tecnológicos**  
  * Equipos electrónicos que puedan soportar las nuevas medidas de seguridad y/o las ya implementadas. Equipos que use el personal interno del banco a los cuales se les administre el acceso a los mismos de manera efectiva tanto desde fuera como dentro de la red. Los equipos no tienen por qué ser hardware, también pueden ser equipos de software como, por ejemplo, de detección (como un SIEM) o software de mitigación de amenazas o de administración de dispositivos centralizada (XDR para el caso de Windows) o, servicios cloud.  
  * Medidas preventivas en caso de incidentes no maliciosos (Apagones, accidentes, …).  
  * Infraestructura de backup 3-2-1. Tener 3 copias de backups “críticos”, 2 en 2 soportes distintos electrónicos y una tercera offline. La implantación y el mantenimiento de este proceso de backup anualmente puede rondar los 40000€.  
* **Presupuesto**  
  * Las medidas de seguridad no son gratuitas de por sí, ni su implementación ni su mantenimiento, por lo que hay que tener un presupuesto mínimo para poder implementarlas y mantenerlas y debe de ser alterable debido a nuevas actualizaciones, mejoras, o nuevas medidas que se quieran implementar.  
  * Seguros en caso de incidentes de seguridad maliciosos que hayan tenido éxito, principalmente en casos de recuperación por el tema de la compensación (por márgenes de tiempo).  
  * Backups con metodología 3-2-1 implementados y mantenidos.  
  * Una parte del presupuesto debe de ir a un fondo de emergencias para responder a los mismos y tener margen de acción.

(27001, 2025)  
Debido a que los recursos se deciden en el momento específico, por ejemplo, más servidores para soportar más clientes y/o datos de los mismos (Lo cual tendría la contra de que conllevaría más superficie de ataque), se han mencionado de manera general en lugar de especificaciones precisas. De esa manera, se pueden clasificar los recursos necesarios para implantar el SGSI sin entrar en especificaciones.	

## **11.2. Formaciones y competencias** 

Para implantar el SGSI correctamente, se necesita formar y preparar a los empleados y hay que asegurarse de que sean ciertamente competentes en sus respectivas áreas. Esta formación es lo que asegura el correcto funcionamiento y mantenimiento del SGSI. Algunas de las formaciones y competencias requeridas son:

* **Formación básica inicial**  
  Hay que determinar la competencia inicial de las personas que están involucradas directamente con el SGSI. De tal manera que se considera sus bases de educación y formación en sus respectivas áreas y/o la experiencia que tienen en las mismas.  
* **Formación en base al rol del empleado**  
  Aunque existan conocimientos y/o experiencias previas, hay que enviar al personal involucrado a cursos sobre implementación del SGSI, aunque debe de llevarse a cabo en un horario adecuado para no perjudicar el rendimiento de los trabajadores.   
* **Certificaciones**  
  Siguiendo el anterior punto de formación adecuada de los empleados implicados, la obtención de certificaciones en el área es muy recomendad no solo para evitar posibles represalias legales (por el hecho de no poder demostrar tener los conocimientos de seguridad necesarios). Las certificaciones las debe de aportar el banco para la correcta capacitación de los empleados del mismo. También habrá que repetirlas/renovarlas en caso de actualizaciones o si pasa un tiempo de 5 años desde que se obtuvo cierta certificación. Las certificaciones no solo se limitan a los empleados, sino que también se le aplica al propio banco de tal manera que este debe pasar auditorias específicas para determinar si es apto o no. 

(holloway, 2025)  
Aun así, la formación que se requiere o que se lleva a cabo una vez introducido el miembro ni garantiza que las buenas prácticas o comportamientos se mantengan. Por eso se deben llevar a cabo simulacros cada 3 meses, más o menos, para comprobar el estado de la concienciación en todas las áreas del banco.

## **11.3. Concienciación** 

Para concienciar a los empreados del banco respecto al correcto funcionamiento del SGSI, se deben de establecer medidas como: 

* Implantar programas de seguridad adecuados para todas las áreas del banco  
* Llevar a cabo sesiones de concienciación cada trimestre, implantadas de manera permanente, y/o cuando se implementen nuevas funciones o programas:  
  * Phishing  
  * Ataques simulados  
  * Recordatorios de buenas prácticas  
* Deben estar atentos a los cambios que se vayan presentando, los cuales se mandarán por correo como:  
  * Políticas de seguridad  
  * Notificar incidentes  
  * Actualizaciones de los sistemas y riesgos  
* Concienciar en la cultura de la seguridad:  
  * Supervisiones: Debido a los roles de importancia que tienen los trabajadores, se llevan a cabo revisiones de los trabajos para comprobar que se han hecho correctamente.  
  * Sugerencias: Principalmente se usa para que se puedan solucionar problemas de rendimiento y/o de seguridad, para que las advertencias lleguen a las personas adecuadas que puedan tomar decisiones.  
  * Auditorías: Se deben de llevar a cabo auditorías a los proveedores, asociados al banco y a las secciones del banco que tengan acceso a información crítica y al SGSI.  
  * Mejora continua

(Anon., 2015)  
Los auditores esperan que, tras la concienciación de los empleados:

* La concienciación se alinee con los objetivos del SGSI  
* Se poseen métodos de comunicación adecuados  
* Los registros de evidencia son fáciles de producir y acceder

La seguridad se debe aplicar de manera diaria de tal manera que se pueda estar al día con la misma, como alertas, actualizaciones, estados de seguridad de otras compañías similares, …  
La concienciación de los empleados pasa a ser un nuevo activo del banco, ya que si “falla” en algún aspecto, dará lugar a nuevas brechas de seguridad en diferentes áreas.  
(Edwards, 2025)

## **11.4. Emergencias** 

Ante situaciones de emergencia por ataques u otros eventos ajenos al banco, se deben de tener planes de reacción y recuperación ante dichos incidentes de emergencia. DORA exige que las entidades financieras tengan “preparados” dichos planes de continuidad del negocio y de recuperación ante incidentes. El protocolo de actuación suele tener los siguientes pasos:

1. **Detección y clasificación**  
   Los responsables de detectar el incidente con un SIEM deben crear una alerta para el equipo de respuesta ante incidentes en base a la severidad del incidente. Es decir, que los trabajadores del SOC deben evaluar la alerta en menos de 30 minutos y que la clasifiquen en base al nivel de severidad de esta.  
2. **Notificación inicial**  
   En caso de que el incidente se considera grave, DORA obliga a notificarlo, aunque no exige tiempos específicos precisos para la notificación, aparte de a el equipo de respuesta ante incidentes, a las respectivas entidades autoritarias, ya que si no se hace puede llevar a sanciones. La notificación inicial se debe llevar a cabo en menos de 4 horas desde que se clasifique como grave, y el resto de los incidentes se deben notificar con un margen de tiempo definido internamente pudiendo ser de 24 horas para las alertas intermedias y varios días para las alertas bajas. Aun así, el RGPD indica que se debe de notificar a los clientes en un plazo máximo de 72 horas.  
3. **Contención**  
   El equipo de respuesta ante incidentes debe de ejecutar las medidas del plan de tratamiento de riesgo, como la segmentación de la red, restauración con backups, desvío de tráfico, etc. Es decir, se debe de reaccionar acorde el playbook específico del incidente en base a sus características. Dicho playbook se debe de elegir una vez identificado el incidente.  
   (Ciberpyme, 2025)  
4. **Recuperación**  
   Se deben activar los planes de continuidad del negocio, como usar servidores de respaldo, restaurar las bases de datos con backups, desviar el tráfico hacia otra infraestructura, etc.  
5. **Informes**  
   El CISO debe de supervisar la elaboración de informes que DORA requiere, y entregarlo en los plazos de tiempo adecuados.

(Álvarez, 2025)  
(España, 2025)  
(Europeo/Consejo, 2026)  
Para emergencias no maliciosas, principalmente formadas por eventos ajenos a la/las compañías, como son apagones, u otros eventos similares, se debe disponer de planes de continuidad operativa (resiliencia). 

# **12. Operación del SGSI** 

De acuerdo con la ISO27001, el banco debe planificar, aplicar, controlar, evaluar y mantener los procesos que sean necesarios para el correcto mantenimiento del SGSI. La operación del SGSI consiste en aplicar los controles y tratamientos definidos y su integración en el trabajo diario.  
(Solutions, 2025)

## **12.1. Aplicar tratamientos de riesgos** 

Para tratar los riesgos se deben aplicar al SGSI los controles mencionados anteriormente, las acciones propuestas para mitigar varios de los riesgos. Para riesgos que se clasifiquen como prioritarios, como ransomware o robo de datos, la aplicación de las medidas debe de ser inmediata.

* **Cifrado de datos**  
  Se aplicará a las bases de datos de clientes del banco, también a los registros financieros y las comunicaciones API. Se usarán dos cifrados, AES-256 para datos en reposo y, para el cifrado para datos en tránsito, TLS 1.3. Se han elegido estos dos estándares debido a que el AES-256 es un estándar en el sector financiero principalmente, y su implementación, aunque compleja, es la más segura. Por otro lado, para los datos en tránsito, se elige TLS1.3 ya que este elimina suites de cifrados obsoletos y puede reducir la demora del handshake, lo cual es relevante en un entorno financiero en el que la conexión con las APIs es crucial.   
  (severion, 2025)  
* **MFA**  
  Se establece como obligatorio para todos los accesos a sistemas internos y a la banca online. Se implementará en un plazo máximo de 12 meses desde la implantación del SGSI. A pesar de que el MFA es más complejo, se ha decidido optar por ese más que por el 2FA que, a pesar de ser más fácil, es menos “seguro”. Esto se debe a que el MFA tiene diversas maneras de autenticación, por lo que 2FA es menos seguro.  
* **EDR**  
  Se desplegará en todos los endpoints del banco. Junto al EDR, se integrará el SIEM para relacionar datos y sacar conclusiones más acertadas de posibles ataques o intentos de los mismos. Se asume que se entiende que la integración del EDR vendría con la instalación del SIEM, y eso se ha decidido sobre un antivirus tradicional generalizado en el banco ya que dichos programas detectan amenazas por medio de firmas digitales, pero es inútil ante malware nuevo, por lo que depender de firmas digitales es poco seguro. Por otro lado, el SIEM con el EDR permite detectar con antelación acciones sospechosas internas, permitiendo detectar con antelación los ataques y pudiendo eliminar a la presunta amenaza con más antelación.  
* **Backups**  
  Se llevarán a cabo copias diarias automáticas de las bases de datos y los registros financieros. Los backups se llevarán a cabo con la metodología 3-2-1.  Esta metodología a pesar de parecer más compleja que un único backup en la nube, es más segura, ya que, a pesar de no ser un estándar como tal, es una práctica recomendable ya que la propia copia offline garantiza el no depender de terceros, y las otras dos, si están aseguradas, permiten “reintegrar” dichos backups más rápidamente.  
* **Filtros anti-phishing**  
  En el servidor del banco se implantará un sistema que marcará los mensajes sospechosos, los cuales se revisarán por el equipo de seguridad. Se ha decidido por un sistema centralizado en el servidor que conecte todos los dispositivos y mensajes entrantes o internos, de tal manera que de manera centralizada se pueden proteger los equipos del banco. Una solución por endpoint dependería de que cada dispositivo individualmente estuviera configurado, haciendo que las vulnerabilidades individuales se puedan llegar a convertir en vulnerabilidades para el SGSI.  
* **Tokens temporales cifrados**  
  Los tokens de autenticación de las APIs financieras durarán 60 minutos y se cifrarán con claves asimétricas para evitar su uso de nuevo. En el sector financiero una sesión de API no debería mantenerse por periodos de tiempo indefinidos. Se usarán claves asimétricas, las cuales son las más seguras, para el cifrado de las tokens, haciéndolas más difíciles de obtener en adición al corto tiempo de duración.

Lo más recomendable es empezar con los controles más relevantes, aquellos que tienen un mayor impacto a la hora de prevenir riesgos.

1. **Controles inmediatos**  
   * MFA: Es un control inmediato debido a que una gran parte de los accesos no autorizados vienen de credenciales de acceso débiles. También se tiene en cuenta que su coste de implementación es bajo, por lo que no hay que tardar en implementarlo.  
   * Filtros/sistemas anti-phishing: Su coste inicial es también bajo, y aporta un valor prácticamente inmediato al banco ya que se cubriría una buena parte de la superficie de ataque. A demás, su implantación es rápida.  
2. **Controles a corto plazo**  
   * Backups con metodología 3-2-1: Son relativamente rápidos de implementar y cubren, parcialmente el riesgo de ransomware y su aplicación regular no debería de interrumpir las acciones del banco (Es posible que por fallos o ediciones los backups fallen y queden corruptos).  
   * Tokens temporales cifradas: Es necesario modificar las APIs, lo que implica un cierto tiempo de desarrollo e implementación correcta de cierta medida, a la vez que tiempo de testeo y modificaciones ya que el banco no puede prescindir de las APIs. El riesgo que mitigaría, si no hay fallos en un primer lugar, consistiría en que ya no se podrán robar dichos tokens de acceso.  
3. **Controles a medio plazo**  
   * Cifrado AES-256: A pesar de ser una medida crítica para la seguridad del banco, su implementación requiere una planificación previa para no afectar a la disponibilidad u otros servicios. Un cifrado mal implementado puede causar más daño que el riesgo previsto (potencialmente).  
4. **Controles a largo plazo**  
   * EDR y SIEM: Son los controles más complejos de desplegar en un primer lugar. Requiere establecer reglas claras de SIEM, instalar agentes adecuados en todos los endpoints, formación constante de los equipos responsables, etc. Una mala implementación puede generar un exceso de alertas falsas fatigando a los responsables en ese sector.

## **12.2. Integrar SGSI en el día a día** 

Para implementar un SGSI correctamente es necesario integrarlo en la “ideología” del banco más que como un proyecto de mejora individual. Como ya se ha mencionado otras veces, se debe de convertir en parte del sistema que se usa en el día a día en el banco. Para que la seguridad del SGSI se integre correctamente en el día a día, se usarán mecanismos como:

* **Controles diarios organizacionales**  
  Los empleados con acceso a sistemas críticos deben cerrar sesión cuando terminen de acuerdo con las políticas de control de acceso. Los incidentes y/o comportamientos anómalos se reportan por un canal interno con el equipo de respuesta ante incidentes, el cual registra y analiza dichos comportamientos para poder clasificarlos.  
* **Revisiones automatizadas**  
  En el SIEM entrarán muchos logs de diferentes fuentes, haciéndolo imposible para los trabajadores del campo revisarlos todos. Para solucionarlo, se debe automatizar el SIEM para que haga una clasificación en un primer lugar de alertas sospechosas y que genere informes automáticos. El informe detallado se le mandará al CISO y al equipo de seguridad para su evaluación  
* **Gestionar cambios con un enfoque en la seguridad**  
  Antes de llevar a cabo algún cambio en la seguridad del banco, se debe de revisar, simular y aprobar antes de su implementación, validando el impacto en la superficie de ataque antes de aprobar el cambio.

(27001, 2025)  
La integración del SGSI en el día a día requiere adaptar a los nuevos empleados, debiendo recibir formación al menos básica de seguridad y de funcionamiento de procesos internos. Y, hay que tener en cuenta si un empleado deja el banco, ya sea por una oferta mejor o la razón que sea. Consiste en un proceso legal e interno que incluye: confidencialidad externa (A pesar de que ya se hace con empleados, se debe hacer con los que se van), retirar sus credenciales de acceso, etc. Estos procesos de “despido” son críticos para el SGSI.

# **13. Evaluación del desempeño** 

En ChamBank, la evaluación de desempeño se clasifica en 3 niveles:

## **13.1. Monitorización**

La monitorización continua se implementa por medio de indicadores de desempeño y de riesgo. Se analizarán datos “voluminosos”, es decir, que solo se monitorizarán y analizarán aquellos riesgos de los cuales existen datos significativos y fiables. También hay que tener en cuenta que los objetivos se harán en base a los riesgos mas graves, por lo que los asumibles no se incluirán.

| Indicador | Objetivo | Frecuencia  |
| :---: | ----- | :---: |
| **Media de incidentes phishing detectados** | En 12 meses haber detectado exitosamente al menos un 35% de los casos |  Mensual |
| **Media de tiempo de detección** | Detectar el ataque o incidente en menos de 24 horas | Semanal |
| **Media de tiempo de respuesta** | Mitigar el incidente en torno a las 48 horas de su detección | Semanal |
| **Empleados con MFA** | Que todos los empleados del banco tengan MFA activo | Mensual |
| **Backups 3-2-1** | Cubrir con backups los sistemas críticos | Semanal |
| **Disponibilidad banca online** | Que la disponibilidad de la banca online sea de al menos el 90% del tiempo |  Trimestral |
| **Empleados al día respecto a formación** | Que el 85% de los empleados estén formados correctamente | Trimestral |
| **Porcentaje de éxito de simulacros phishing** | Que el porcentaje de éxito de las campañas de phishing se reduzca |  Trimestral |

(Sánchez, 2024)  
(López, 2025)  
(TOOLS, 2026)

## **13.2. Auditorías internas** 

El objetivo de las auditorías internas, en este caso, es comprobar si el SGSI implementado cumple con los requisitos de la norma con la que se ha aplicado, la ISO27001. Se comprueba que los requisitos y procesos integrados en la organización por el SGSI se han integrado correctamente. En ChamBank, las auditorías internas se llevarán a cabo 2 veces al año (Como mínimo en caso de que no sucedan incidentes graves). El alcance consiste en todo el SGSI implementado acorde a la ISO. El proceso de auditoría normalmente consiste en una serie de pasos predefinidos:

1. **Planificar la gestión de la auditoría**  
   Se debe definir un plan de auditoría que contemple las fechas de ejecución, el alcance y la metodología de la auditoría. Las auditorías deben de ser llevadas a cabo por personas ajenas a la implementación del SGSI, para poder tener objetividad en la misma.  
2. **Ejecución**  
   El auditor debe informar a los responsables de las áreas auditadas y les pedirá la documentación para analizarla y llevar a cabo la auditoría. La auditoría del SGSI tiene 2 fases:  
* Sistema de gestión: Se revisa la documentación, el marco de gestión del SGSI, el alcance, la gestión de riesgos, políticas de seguridad, roles, gestión de no conformidades, etc.  
* Pruebas de cumplimiento: Se comprueba la eficacia de la implantación de los controles de seguridad del banco. Se llevarán a cabo entrevistas a: propietarios de activos, responsables de procesos del banco, usuarios del SGSI (Directos e indirectos), etc.; y se revisarán objetivos, riesgos, etc.   
3. **Informe**  
   Tras recopilar los recursos que los auditores se propusieron conseguir para comprobar el funcionamiento de los controles de la norma, se debe de llevar a cabo un informe. Dicho informe se deberá presentar a los responsables del banco y a las áreas auditadas, siendo el responsable del SGSI el responsable de dicha comunicación. El informe cubre aspectos como: áreas y alcance auditado, no conformidades y/u observaciones, fortalezas y debilidades, recomendaciones, etc.  
4. **Plan de acción**  
   El responsable del SGSI debe de llevar a cabo una planificación de las acciones para poder llevar a cabo las correcciones mencionadas en el informe. Dichos planes deberán de ser aprobados en el banco garantizando las correcciones en todas las áreas negativas.

(27001, 2025)  
(Solutions, 2025)  
Las auditorías no son independientes del diseño del SGSI, sino que son su mecanismo de validación. La ISO 27001 define qué se debe de auditar (al menos las cláusulas de la 4 a la 10), mientras que la ISO 27002 determina si los controles seleccionados en el [SoA](https://github.com/Ch4mbi/SGSI-ISO27001-27002-DORA-RGPD/blob/main/SoA--SGSI-Ch4mbi.md) son adecuados para los riesgos identificados. Sin la relación entre la 27001 y la 27002, los auditores solo podrían revisar la documentación sin revisar si el diseño es apropiado para ChamBank. Esto significa que cada hallazgo de auditoría se traduce en una revisión del [SoA](https://github.com/Ch4mbi/SGSI-ISO27001-27002-DORA-RGPD/blob/main/SoA--SGSI-Ch4mbi.md), cerrando así el proceso de plan-do-check. En ChamBank, un auditor que revisara el SGSI diseñado podría encontrar, en la documentación: el compromiso de la dirección (documentado en la sección de liderazgo) , el alcance definido (en la sección de alcance), el análisis de riesgos , y controles aplicados con justificación. La ISO 27002 respalda los controles: cifrados AES-256 y TLS 1.3 a los requerimientos criptográficos, MFA a los controles de acceso, backups 3-2-1 a la disponibilidad continua. Sin la alineación entre los controles de lo que la ISO 27001 exige y lo que la 27002 especifica, los controles no serían medidas auditables, sino que podrían ser medidas “subjetivas” de los equipos de seguridad.

## **13.3. Revisión** 

La dirección de ChamBank (CISO, CEO, CTO, CDO, etc), debe de revisar y evaluar el SGSI tras la obtención del informe. Las revisiones o auditorías se llevarán a cabo de manera trimestral o tras incidentes graves de seguridad. Dichas revisiones incluyen: los resultados de las auditorías, los indicadores (KPI) del trimestre, el estado del plan de tratamiento de riesgos, incidentes que hayan tenido lugar, cambios internos o externos, y las sugerencias de mejora de la auditoría. Tras la revisión, se deben documentar los resultados de la misma, y, posteriormente, tomar decisiones en base a dichos resultados del análisis.

# **14. Debilidades** 

Para poder mejorar el SGSI, es necesario identificar vulnerabilidades, formado parte así del proceso de mejora continua.

## **14.1. Resultados** 

Tras la implantación del SGSI, el banco puede detectar fallas/debilidades potenciales en el propio sistema, las cuales se deben de abordar en la primera auditoría. Estas fallas normalmente pueden ser identificadas como las propias limitaciones del análisis.

| Debilidad potencial | Justificación |
| :---: | ----- |
|  **Problemas con el MFA** | Ya que el paso al SGSI es reciente en ChamBank, pueden existir equipos antiguos o desactualizados que no toleren medidas de seguridad como el MFA. En caso de que existan dichos equipos, esta característica representaría una no conformidad respecto a uno de los objetivos impuestos al implantar el SGSI. También hay que tener en cuenta que conllevaría un gasto económico el reemplazar dicho hardware o software. En la práctica esto significa que durante el periodo de “transición” habrá cuentas de empleados sin MFA, siendo una exposición ante atacantes. |
|  **Depender de terceros** | La dependencia de ChamBank de terceros como servicios cloud u otros servicios no necesariamente similares hace que, en parte, no se controlen aspectos de la seguridad que se mencionan en el SGSI del banco. Esto se debe a que cada servicio externo tiene sus propias políticas y sistemas propios, haciendo difícil la correlación a pesar de aportar servicios, de tal manera que se convierte en una debilidad propia de ChamBank. Principalmente el problema recae en las debilidades ajenas de dichos servicios. Aun así, el reglamento DORA puede abordar dicho problema, con la gestión de riesgos de terceros u otros aspectos, pero la supervisión de los terceros conllevará recursos al llevar a cabo revisiones periódicas. Pero el propio incumplimiento de llevar a cabo las revisiones puede llevar a sanciones por parte de DORA. Aun así, la debilidad no se puede eliminar del todo ya que los procesos críticos de los clientes pueden requerir dichos servicios externos o ajenos al banco. |
|  **Variación del personal** | Existen diferentes áreas de trabajo en ChamBank, haciendo que, tanto en este instante como en el futuro, haya diferencias entre la formación del personal interno, por ejemplo, en la seguridad, aunque se puede observar en otras áreas respecto a la experiencia en el sector, uso de herramientas, dedicación, etc. Siendo el error humano uno de los principales riesgos de cualquier compañía independientemente del sector en el que dicho error se cometa, es importante invertir en especializaciones y concienciaciones de cada área para asegurar el correcto funcionamiento. El nivel de riesgo, no es igual en todas las áreas del banco acorde a la formación individual. Un ejemplo de este aspecto es el departamento de recursos humanos el cual tiene acceso inicial, aunque limitado, a la información de clientes, y su formación en seguridad suele ser básica, siendo un objetivo para ataques de phishing. |
|  **Ausencia inicial de métricas pasadas** | Al ser la primera implantación del SGSI, y como un requerimiento del mismo, se van a guardar registros y métricas de eventos. Pero antes de su implantación, no se guardaban, por lo que sería un inicio de cero. Por esa razón, habrá que esperar unos meses para empezar a recolectar métricas, dificultando la interpretación de KPIs durante ese tiempo. Esto claramente hará que durante los primeros periodos de tiempo tras la implantación del SGSI, será imposible revisar si de verdad está contribuyendo a la mejora del banco, afectando a la toma de decisiones estratégicas a corto plazo. Aun así, se pueden usar estándares de otras entidades bancarias, con un SGSI implantado, para tener una base inicial e intentar estar a la par para que, después de un tiempo de recolección de métricas ChamBank pueda mejorar por sí mismo con sus propias métricas. |
|  **Riesgo residual alto** | Es casi imposible cubrir todas las vulnerabilidades de los sistemas, principalmente si son zero-day. Este riesgo es el más difícil de cubrir y el que tiene mayor impacto potencial. ChamBank lo asume y se debe gestionar con la monitorización continua y planes de respuesta ante incidentes o desastres, pero hay que tener en cuenta que es casi imposible eliminar dicho riesgo. Por ejemplo, podría existir una vulnerabilidad no localizada en el cifrado de las APIs, o que sea conocida pero que no se haya solucionado. En este caso, una solución sería la de segmentar la red para limitar el alcance, pero no evitar el ataque. Esto demostraría que los controles del SGSI no eliminan el riesgo residual, sino que lo limitan reduciendo su impacto potencial sin eliminarlo. |

## **14.2. Evaluación de cultura de seguridad**

Siendo la cultura de la seguridad las actitudes y comportamientos en una organización, siendo en este caso ChamBank, es la forma en la que se interpretan las acciones de seguridad en un entorno. La cultura de la seguridad es necesaria para reducir los riesgos que vayan apareciendo en la medida de lo posible en las tareas del día a día, también sirve para concienciar y garantizar el cumplimiento de normativas. Un banco con una buena cultura de seguridad tiende a notificar incidentes, a seguir las políticas establecidas, y a ver la seguridad como algo general en todo el banco.  
(Odebrecht, 2024)  
La cultura de la seguridad en Chambank se puede evaluar por medio de diferentes mecanismos:

* Reportes de incidentes  
  Los reportes de incidentes en redundante, por decirlo de alguna manera, ya que engloba aspectos que se pueden mencionar individualmente. Los reportes de incidentes recopilan datos de dichos incidentes tales como: tiempos de detección y de reacción ante los mismos, soluciones propuestas, lecciones aprendidas, errores, proactividad (En caso de el/los empleados responsables del mismo reporten sus fallos o errores que afecten a la seguridad en el momento en el que los cometen), etc. Los reportes deben de ser precisos y se deben crear con la ayuda de los afectados, los expertos, y otras ayudas internas si es necesario demostrando así una buena cultura de seguridad y un pensamiento en la mejora constante.  
* Resultados de simulacros  
  La realización de simulacros y su posterior análisis de resultados de los mismos muestra una buena cultura de seguridad en el banco. Esto se debe a que, aparte de probar medidas de seguridad integradas, las defensas activas del banco y la concienciación de los propios empleados en la seguridad, se evalúan los resultados en busca de la mejora constante de la seguridad del mismo. El objetivo es que los resultados de dichos simulacros aumenten en cantidad, pero que se vean reducidos en tasas de éxito de los mismos.   
* Encuestas de seguridad  
  Las encuestas de seguridad se llevan a cabo con encuestas normales (normalmente digitalizadas para que lleguen a todas las áreas) anónimas. Se llevan a cabo con el fin de evaluar la percepción general de la seguridad y la concienciación de la misma. También se usa para poder generar reportes generales, no solo sobre la concienciación, sino también sobre el uso de herramientas y la comodidad con las mismas. Los resultados de las encuestas se mandan al comité y se usarán para sacar conclusiones de cambios que hacer, ya sea en programas, metodologías, o concienciación.  
* Revisión de cumplimiento de políticas  
  Aleatoriamente, se llevarán a cabo revisiones del cumplimiento de las políticas implementadas, como el tema de las contraseñas, uso de dispositivos externos, USBs, etc. Cuantas más políticas se cumplan, significará que las políticas se habrán integrado mejor.

(sothis, 2026)  
(ICSI, 2019)  
(OSH, 2026)

# **15. Plan de mejora** 

El plan de mejora, y la mejora continua, en ChamBank es una necesidad operativa. Al comenzar el SGSI sin historial previo ni métricas ni incidentes documentados, las primeras aplicaciones del ciclo PCDA son críticas: permiten calibrar si los controles implantados responden a las necesidades de Chambank o si solo se basan en estimaciones teóricas basadas en generalismos del sector.  
(Edwards, 2022)  
(Reyes, 2024)

## **15.1. No conformidades** 

Una no conformidad es un incumplimiento de un requisito del SGSI, normalmente obligatorio. Las no conformidades se pueden detectar con auditorías internas, análisis tras incidentes, revisiones mandadas por la dirección, etc. Al momento de que se detecte una no conformidad, ChamBank debe seguir una serie de pasos para “cubrirla”:

1. **Identificación**  
   Se deben de hacer revisiones periódicas para detectar no conformidades (o auditorías programadas o no programadas). Así se puede asegurar encontrar no conformidades del sistema respecto a las obligaciones de la ISO27001.  
2. **Análisis**  
   Tras detectar una o varias no conformidades, se deben analizar para poder clasificarlas, por ejemplo, en que si la causa de las mismas es puntual o persistente, o si forma parte de una serie de patrones. También se analiza si dicha no conformidad afecta a varios procesos o si es el origen de fallos más generales, y también, aunque sea redundante, clasificarlas en base a gravedad. El análisis también debe incluir la localización del error, ya sea un programa, proceso o procedimiento para poder abordarlo correctamente.  
3. **Aplicar correcciones**  
   Tras llevar a cabo el análisis de las no conformidades, se debe actuar en consecuencia para solucionarlas. Primero se deben definir las acciones correctivas y después aplicarlas.  
4. **Verificar correcciones**  
   Tras un tiempo predefinido en base a la gravedad de la no conformidad detectada, se debe revisar para ver si ha solucionado el problema de la no conformidad. En caso de que la no conformidad siga presente, se debe de solucionar con más urgencia.  
5. **Documentación**  
   Todo el proceso de detección de las no conformidades, las medidas propuestas para solucionarlas, el tiempo de detección y de reacción ante las mismas, fechas, responsables, etc. Se debe documentar, normalmente en tiempo real, para tener un informe lo más objetivo posible de cara a revisiones futuras. 

(Calidad, 2026)  
(27001, 2025)  
(Peters, 2022)  
La detección de las no conformidades no significa fracaso en la implementación del sistema, sino que se está llevando a cabo correctamente el proceso de mejora continua que especifica la ISO 27001, más aún si se llevan a cabo las respectivas acciones correctivas a las no conformidades detectadas.

## **15.2. Correcciones**

Ante ciertas no conformidades detectadas previamente se van a implementar medidas para solucionar las causas raíz de dichos sucesos. Hay que tener en cuenta que las no conformidades tienden a tener soluciones más persistentes en el tiempo, lo analizado previamente eran acciones inmediatas que se llevaban a cabo para solucionar riesgos. Los puntos sobre los que implementar acciones correctivas son:

* **MFA**  
  Se deben sustituir o actualizar los sistemas que no soporten el MFA actual. Los responsables serían el CISO y el CTO y se deberá implementar en un plazo máximo de 6 meses.  
* **Dependencia de terceros**  
  Se deben revisar y actualizar los acuerdos con los proveedores como medida de seguridad, como cláusulas de seguridad alineadas con el reglamento DORA. El CISO y el CDO deben de revisarlo periódicamente, cada 6 meses.  
* **Variación del personal**  
  En base a los resultados obtenidos de la evaluación inicial de competencias, en un plazo de 3 meses, el CISO con la ayuda del comité, debe de personalizar el plan de formación de los empleados.  
* **Falta de métricas anteriores al SGSI**  
  Se deben usar los primeros 6 meses para obtener datos iniciales del SGSI. Esto se hace para poder revisar y ajustar dicho sistema.

(Laprovittera, 2025)

## **15.3. Mejora continua**

La mejora continua es lo que da sentido a todo el SGSI. El objetivo de la mejora continua en ChamBank es el de evolucionar de manera activa junto con el sistema. Aunque hay que tener en cuenta que las mejoras continuas no siempre tienen la misma “urgencia” o importancia. Se puede establecer un orden que consista en:  
1. Lecciones aprendidas de incidentes ya que indican fallos que ya han ocurrido.  
2. Indicadores de rendimiento que indiquen una tendencia negativa continuada porque pueden llegar a anticipar un fallo antes de que ocurran.  
3. Cambios regulatorios debido a que su incumplimiento puede llevar a consecuencias legales.  
4. Resultados de las auditorias que sugieren mejoras proactivas pero que no deberían, en la mayoría de casos, ser urgentes.  
Las fuentes de mejora de ChamBank son:

   * **Indicadores de rendimiento**  
  En caso de que algún indicador ya mencionado muestre resultados negativos en un tiempo prolongado, aunque no llegue a ser una no conformidad directamente (ya sea porque se mantenga en resultados negativos pero aceptables), se analizará dicho indicador en sus aspectos y se propondrán soluciones en caso de fallo y mejoras respecto a la prevención de no conformidades en ese indicador.  
   * **Lecciones aprendidas de incidentes**  
  Tras resolver cada incidente (no necesariamente de seguridad), ya sean ataques o fallos humanos, en el informe se debe de analizar de manera objetiva los fallos que se han tenido a la hora de resolverlo y/o los métodos usados ya sean antiguos o nuevos. Esto se traduce en lecciones aprendidas para que, en incidentes futuros similares, se pueda actuar mejor y más rápido ante los mismos.  
   * **Estar al día en ciberseguridad**  
  El hecho de aplicar medidas de seguridad o procedimientos no es suficiente para mantener un sistema a salvo de ciberataques. Normalmente debe de haber uno o varios equipos que lleven a cabo reportes sobre actualizaciones en políticas, reglamentos o certificaciones, o sobre nuevos métodos de ataque, nuevos malware, técnicas de phishing, etc. Dicha búsqueda activa de ciberataques en otros campos ayuda a mejorar la seguridad por medio de la preparación preventiva.  
   * **Cambios regulatorios**  
  Como ya se mencionó en el anterior punto, hay que estar al día de cambios regulatorios, o nuevas certificaciones necesarias. Esto se debe, en el aspecto de nuevas regulaciones, a que se debe mantener un sistema actualizado, aparte de que se quiere evitar ciberataques internos, también es para evitar sanciones legales. Se debe mantener de manera activa un seguimiento de dichas normativas con las que se ha implantado el SGSI.  
   * **Sugerencias**  
  También, cualquier empleado del banco de cualquier sector, puede llevar a cabo sugerencias de mejora del SGSI, ya sea de seguridad o de cualquier otro aspecto de mejora interno. Las sugerencias se enviarán al comité para que consideren dichas sugerencias y decidan aplicarlas y como aplicarlas o no aplicarlas.  
   * **Resultados de pruebas**  
  Otra manera de mejorar principalmente en el aspecto de la seguridad y/o la concienciación son las pruebas de penetración que se llevan a cabo. Se llevarán a cabo diariamente ataques “simulados” pero no identificados (para simular un escenario más realista) que intentarán acceder al sistema y que generarán un reporte de los ataques que se llevarán a cabo y puntos fuertes y débiles que tenga la defensa. En ese caso, se podrá mejorar la seguridad de la empresa.

(Sharron, 2023)  
(Peters, 2025)  
Aunque se aplique la mejora continua, siempre hay sitio para los errores o escenarios que, aunque se intenten prevenir de cualquier manera, pueden seguir pasando. Como, por ejemplo:

* **Ataques que pueden evadir el EDR**  
  Malwares nuevos sin firma digital y que no son detectados. En este aspecto la segmentación de la red debería de servir como medida de seguridad, la cual, si no está bien configurada, puede llevar a la propagación de este antes de que se detecte con el SIEM. Aunque una solución a este problema podría ser la de implementar reglas al SIEM sobre malware sin firma. Esto podría ayudar a que se aísle de manera automática en caso de comportamiento sospechoso.  
* **Fallos del proveedor al ocurrir un incidente de seguridad**  
  Si el proveedor cloud se cae mientras ChamBank está respondiendo a un incidente serio, el banco perdería acceso a sus backups en la nube, al menos cuando más se requieren. Aunque la copia offline de este escenario cubre este problema, aunque su tiempo de recuperación será mayor.  
* **Existencia de playbooks sin experiencia**  
  Ante nuevos incidentes que no se hayan documentado, al menos no que sean iguales, los equipos de respuesta deben improvisar o seguir, parcialmente, el procedimiento de otros incidentes. Aunque después se optimizarían procesos. Una solución activa ante este problema son las pruebas de penetración o los simulacros ya que permiten tener playbooks preparados con técnicas de ataque y defensa que se usan en el momento.

# **16. Análisis crítico** 

## **16.1. Propósito de la ISO 27001 y 27002** 

ChamBank opera como una entidad financiera digital, usando APIs abiertas, aportando banca móvil y con un alcance internacional, lo cual significa que posee una superficie de ataque mayor que otras entidades bancarias. La ISO 27001 es la única norma que ofrece un marco certificable para gestionar esa superficie. Sin ella, ChamBank no tendría ningún criterio para priorizar controles frente a los riesgos identificados anteriormente (los cuales se han identificado por especulación/ejemplos de otros bancos ya que ChamBank carece de historial previo). La ISO 27002 sirve como complemento a la 27001 especificando como aplicar los controles en un entorno bancario. Sin su guía, implantaciones como el cifrado o los controles de acceso quedarían bajo el criterio subjetivo del equipo responsable, generando, posiblemente, inconsistencias notables en las auditorías.  
La ISO 27001, en el contexto de ChamBank, ha sido, como ya se ha mencionado, la base de la aplicación del SGSI, diseñando, definiendo el contexto, los roles, la gestión de riesgos tras su identificación y la mejora continua. Mientras que la ISO 27002, como extra, ha servido como una referencia para la implementación de controles en el [SoA](https://github.com/Ch4mbi/SGSI-ISO27001-27002-DORA-RGPD/blob/main/SoA--SGSI-Ch4mbi.md) que se debe de llevar a cabo en ChamBank como entidad financiera.

## **16.2. Relación entre SGSI implantado y estándares** 

El SGSI de ChamBank sigue diversas cláusulas de la ISO27001 las cuales son obligatorias legalmente hablando y no son negociables. Como prueba, se ve que en la implantación del SGSI se han cubierto diversos puntos como: la definición de roles, el alcance, roles, identificación y análisis de riesgos, formación interna, auditorías, etc.  
Por otro lado, respecto a la ISO 27002, se puede ver cómo se aplican controles organizativos (como la gestión de incidentes), controles en los empleados (la formación y concienciación), y controles tecnológicos (cifrados, SIEM, tokens, etc.).  
(holloway, 2025)  
Adicionalmente, el SGSI de ChamBank también se complementa con normativas como la RGPD o DORA, las cuales ayudan respecto a la resiliencia operativa que la ISO27001 no llega a cubrir en profundidad (DORA) y que garantizan la protección de los datos personales de los clientes. La combinación final hace que el SGSI implantado sea más completo que si solo se hubieran aplicado las ISOs.  
Comparando el diseño del SGSI con los requisitos de ChamBank, se ve como el sistema da respuesta ante cada necesidad identificada, por ejemplo, la protección de los datos queda cubierta con el cifrado AES-256, controles de acceso, MFA, etc., la disponibilidad se cubre con los backups, los planes de continuidad, servidores de reserva, etc., entre otros. Aun así, hay partes sin cubrir entre el diseño y su requisito, como las estimaciones teóricas de los datos en lugar de datos históricos del banco o la inaccesibilidad del SGSI para llegar a terceros.  
Sin embargo, existen límites reales. El SGSI diseñado asume que ChamBank controla su cadena de terceros, pero en la práctica, los proveedores de dichos servicios (como cloud (Azure, Aws, etc)) tienen sus propios marcos de seguridad que ChamBank no puede auditar. La ISO 27001 exige la gestión de los proveedores, pero no garantiza que dichos proveedores cumplan o siquiera sigan dichos estándares, siendo este uno de los mayores puntos de fricción del SGSI y su aplicación.  
El contraste que existe entre lo que exigen las normas y el SGSI de ChamBank puede mostrar grietas concretas: ChamBank, en el análisis de riesgos, se ve obligado a usar estimaciones o tomar como referencia a otros bancos a pesar de que la ISO 27001 exige llevarlos a cabo en base a datos reales propios, haciendo al plan de tratamiento de riesgos “provisional”; por otro lado, la ISO 27002 exige que los controles seleccionados sean proporcionales al riesgo, pero sin datos reales, dicha proporcionalidad acaba siendo teórica; adicionalmente, DORA exige la gestión de terceros, pero ChamBank no puede auditarlos completamente. Las “grietas” en el diseño mencionadas, no lo invalidan, pero pueden llegar a condicionar su madurez inicial y obligan a revisar el SoA.

## **16.3. Ventajas de certificarse** 

Aparte del cumplimiento normativo que hace la implantación de normativas obligatorias en el sector financiero, la certificación en la ISO 27001 en ChamBank contaría con varios beneficios de diversos tipos:

| Ventaja | Impacto |
| :---: | ----- |
| **Confianza de clientes** | Diferenciación competitiva en el sector financiero (incluyendo digital). Incluye la protección de datos y demuestra madurez |
| **Cumplimiento RGPD/DORA** | Reducción de riesgo de sanciones (de hasta 3,86 millones de €) y puede llegar a facilitar el cumplimiento normativo |
| **Optimización de procesos** | Menor coste operativo, auditorías internas integradas, agilidad de procesos, compromiso de ChamBank a la mejora continua |
| **Gestión de riesgos organizada** | Revisión trimestral con datos reales a partir del sexto mes con la finalidad de mejorar y revisar la correcta implantación |
| **Posicionamiento frente a competencia** | Señal de madurez ante diferentes clientes u otras compañías |

(iuvity, 2025)  
(BMC, 2025)  
Aun así, hay que plantearse si la certificación es algo prioritario en la fase inicial de ChamBank, estimando en torno a unos 400000€ de implantación inicial estimada (como mínimo), siendo un banco nuevo sin apenas historial propio, la certificación formal puede tener más sentido a partir de los 12 meses, cuando el SGSI ya tenga datos reales propios de ChamBank y el entorno en general haya madurado operativamente. El certificarse demasiado pronto, con análisis basados en estimaciones teóricas o en datos generales de otros bancos implica el riesgo de no obtener la certificación o de obtenerla, pero que no refleje la realidad del banco, es decir, un SGSI de la ISO 27001, pero solo en papel.

## **16.4. Limitaciones y riegos de enfoque muy normativo** 

Aun así, certificarse y aplicar los estándares de las normas ISO 27001, 27002, DORA y RGPD puede llegar a aplicar a ChamBank cierta “rigidez operacional” si no se aplican correctamente o si se aplican excesivamente bien desde el punto de vista normativo. Dicha rigidez mencionada consiste en los riesgos que conlleva la implementación de los reglamentos de manera “excesiva” o rígida:

* **Convertir el SGSI en un ejercicio**  
  Es decir, realizar o “acordarse” del SGSI solo para las auditorías y actualizarlo o volver a aplicarlo al banco cuando se vayan a llevar a cabo auditorías y no para el banco en sí. Este enfoque es un riesgo, ya que cabe otras empresas lo han “sufrido”, por lo que se puede catalogar como un riesgo. El SGSI se debe de implementar como algo propio y constante en ChamBank. Hay que aplicarlo de manera activa, tomar decisiones sobre él, hacer cambios, asumir riesgos y estar activo respecto a la recolección de datos de nuevas amenazas para poder proteger el banco y reforzar la integración operativa del SGSI. Por eso ChamBank se propone que el SGSI tenga presencia en las reuniones trimestrales de la dirección con o sin auditoría programada.  
* **Coste**  
  A pesar de que los costes ya se han discutido antes (En torno a unos 500000€ la certificación inicial en entidades bancarias gigantes), siguen siendo un posible problema o algo a tener en consideración. A pesar de que ChamBank sea un banco, es inicial, nuevo, recién implementando su SGSI con normativas, el precio, a pesar de que es una buena inversión a futuro, es posible que a Chambank al principio le cueste asumir dichos gastos. A demás, si en el futuro los gastos no se administran correctamente, puede afectar al mantenimiento del sistema, incapacidad para llevar a cabo auditorías, o pérdidas de seguros.  
* **Carga administrativa notable**  
  La posible complejidad de las normativas y la administración interna de las mismas, principalmente en el sector financiero, es una consideración a tener en cuenta a la hora de tener un enfoque muy rígido, principalmente porque en el sector financiero hay aún más obligaciones que cumplir. Esto puede generar una carga adicional respecto a otros sectores que no se someten a dichos reglamentos. Una solución a este problema, para evitar la carga excesiva de trabajo/estrés, es tener una buena coordinación planeada y aplicada al aplicar, a la vez las ISOs, DORA, y RGPD.  
* **Rigidez de “adaptación” ante nuevas amenazas**  
  Los reglamentos como las ISOs se actualizan cada cierta cantidad de tiempo, siendo las “actualizaciones” relevantes más o menos cada 5 años (Siendo una media aproximada). Este tiempo de actualización o de revisión de la norma es lento en sí, y, frente a nuevas amenazas emergentes se puede quedar corta o ser insuficiente. Esto se debe a que, prácticamente, todas las amenazas hoy en día están evolucionando y cambiando. Un enfoque normativo enfocado en los controles existentes en la norma deja a ChamBank sin respuesta ante los nuevos vectores de ataque emergentes que ni se mencionan en la versión actual de la norma. En ChamBank la respuesta no es esperar a la próxima revisión de la norma, sino mantener un proceso de vigilancia interna de amenazas emergentes desvinculado del ciclo de auditoría ISO, para que los controles se puedan actualizar más fácilmente.  
* **Sensación de seguridad**  
  El hecho de lograr certificarse de la ISO no asegura que el banco esté seguro o que se haya librado de una amenaza de seguridad. La dirección del banco puede llegar a reducir la inversión en mejora continua que se mencionó, dejando al banco mayoritariamente expuesto.

(Mexico, 2021)

## **16.5. Evaluación crítica del sistema** 

### **16.5.1. Viabilidad organizativa** 

El SGSI es, técnicamente, asequible para un banco como ChamBank, ya que cuenta con roles definidos con una estructura de gobernanza clara. Aun así, la viabilidad organizativa del banco no solo depende de la estructura planteada/implementada, sino de la propia cultura del banco. Objetivamente, el riesgo más probable no es operacional, ni de sistemas, sino humano, que los equipos no relacionados con la seguridad (recursos humanos, atención al cliente, etc.) perciban el SGSI como una carga extra impuesta por la dirección (Es algo “normal” cuando se implanta un SGSI ya que, en todas las empresas, los diferentes sectores internos tienen mentalidades diferentes que no siempre se alinean con la seguridad). Dicha percepción del SGSI se puede notar, pasivamente, con formularios sin criterio, formaciones superadas, pero sin implantación, o incluso incidentes de seguridad no reportados para evitar los procedimientos. En ChamBank, donde el CISO depende del apoyo de la dirección para poder aplicar controles, un CEO poco comprometido con el SGSI puede convertirlo en un sistema que solo existe en papel, pero que no está aplicado. Por lo que la viabilidad siempre es posible, pero está condicionada por un compromiso activo y continuado por parte de la dirección y no solo su firma en las políticas de la seguridad.

### **16.5.2. Costes estimados** 

Los costes estimados normalmente dependen del propio alcance de la entidad financiera y las características que posee. ChamBank, al contar con varias funciones y alcance internacional, se pueda considerar, como mínimo, una entidad mediana pudiendo llegar a ser grande si se expandiera. Dadas las características de ChamBank, y su estimación de capacidades dándole un “puesto” medio-alto, y teniendo en cuenta que la distribución del coste se debe de “distribuir” en diferentes secciones y se van a hacer aproximaciones estimadas:

* Consultoría de implantación: 100000€  
* Auditoría de certificación externa: 22000€  
* SIEM (licencia e implementación): 115000€  
* EDR: 60000€  
* Backup (implementación infraestructura 3-2-1): 40000€  
* Cifrado AES-256 y TLS 1.3: 30000€  
* MFA (en todos los sistemas): 20000€  
* Formación y certificación del personal clave: 30000€  
* Filtros antiphishing (con sistemas de correo seguro): 15000€

En total, estimado, los costes de implementación del SGSI serían de unos 432000€ aproximadamente.   
Aunque el SGSI se implemente correctamente hay que mantenerlo y mantener y mejorar las posibles medidas de seguridad que se implementen con él. Se van a estimar unos costes de mantenimiento de las medidas del SGSI:

* SIEM y EDR: 10000€  
* Backups (3-2-1): 40000€  
* Auditorías internas (2 al año como mínimo): 20000€  
* Auditorias de vigilancia de la ISO 27001: 12000€  
* Formación continua del personal: 15000€  
* Seguro: 40000€

En total el coste de mantenimiento, anual estimado, es de 137000€ aproximados si no ocurren incidentes graves (los cuales llevarían a una auditoría extra independiente de las programadas).  
A pesar de que la inversión es considerable para un banco inicial (432000€ de implantación y 137000€ de mantenimiento anual esperado, haciendo que el primer año ronden los 569000€), pero el coste de no implantarlo es mayor. El coste medio de una sanción por violaciones de datos en el sector financiero europeo superó los 3,86 millones de euros junto con daño reputacional. Desde ese punto de vista, el gasto en la implantación y mantenimiento del SGSI no es un gasto en vano y es muy útil, ya que es una inversión en reducciones de riesgos, cumplimiento normativo, reputación, etc.  
(Wagenbach, 2026)

### **16.5.3. Nivel de madurez** 

A la hora de implantar el SGSI, ChamBank inicia con un nivel de madurez básico, es decir, antes del SGSI ChamBank tenía lo mínimo necesario y no estaba preparado para ninguna prueba y era objetivo fácil para ataques o fallas al analizar los mismos, por ejemplo, la falta de logs/eventos iniciales que se mencionó (y que se empiezan a guardar una vez implantado el SGSI). Al principio, ChamBank no tenía tampoco controles de seguridad aplicados (ni documentados).  
Tras los primeros 6 meses tras la implantación del SGSI, con los controles aplicados correctamente (MFA, backups, antiphishing, cifrados, etc.), es prevé alcanzar un nivel intermedio en la “escala de madurez” en ese margen de los primeros 6 meses. Con la mejora constante y el mantenimiento correcto que se esperan llevar a cabo de manera continua, se implementarán nuevos cambios en base a fatores como nuevos ataques, nuevas normas, nuevos controles, etc. Idealmente, se espera llegar a una madurez alta/elevada a los 3 años de implantar el SGSI en el banco con todas sus medidas y actualizaciones de seguridad a las que debería haberse ido sometiendo.   
El periodo más crítico es, claramente, el de los primeros 6 meses. En ese margen de tiempo ChamBank habrá implantado controles, pero sin datos históricos reales ni experiencia previa (al menos documentada). En este periodo es, específicamente, cuando la probabilidad de incidente de seguridad es más alta y la capacidad de respuesta más limitada. Un ataque exitoso durante este periodo, sin un SIEM operativo, podría no detectarse a tiempo, siendo un riesgo organizativo que el SGSI no puede eliminar incluso implantado, solo reducir su impacto.

### **16.5.4. Riesgo residual** 

Hay que tener en cuenta, como ya se mencionó respecto a las vulnerabilidades, que existen debilidades incluso en un SGSI ya implantado, y se puede llegar a razonar que ningún SGSI o sistema en general puede eliminar el riesgo residual completamente. Los riesgos residuales de ChamBank son, básicamente:

* Vulnerabilidades zero-day, las cuales tienden a seguir en los sistemas no detectadas y que los atacantes pueden hallar y aprovechar.  
* Errores humanos de personas tanto cualificadas como no cualificadas, con formación en seguridad o sin formación. Los errores humanos siguen siendo, prácticamente, la principal causa de ataques a las empresas.  
* Vulnerabilidades o fallos de terceros. Esta clase de vulnerabilidades son prácticamente imposibles de corregir para ChamBank ya que no se posee control sobre las entidades de terceros que ayudan al banco.

Los riesgos no se pueden eliminar, lo único que se puede hacer con ellos es asumirlos y reducir su impacto potencial como parte de la mejora continua del SGSI. Eso se puede gestionar con el uso de SIEM, tener playbooks y planes de respuesta ante incidentes, llevar a cabo pruebas de penetración para hallar nuevas vulnerabilidades y entrenar a los equipos de respuesta y revisar los riesgos cada trimestre. 

### **16.5.5. Sostenibilidad a largo plazo** 

La sostenibilidad del SGSI a largo plazo en ChamBank se puede enfrentar a varias amenazas las cuales es conveniente considerar para la sostenibilidad a futuro del SGSI: la falta de presupuesto (con un coste anual estimado de 137000€, una reducción de dicho presupuesto puede llevar a quedarse sin financiación para auditorías, monitorización o, simplemente, mejora continua), la falta o pérdida de roles (siendo el CISO un perfil requerido para la implantación junto con los técnicos de seguridad perfiles escasos, su pérdida puede dejar al SGSI sin capacidad operativa durante periodos de tiempo largos) o la fatiga normativa (gestionar la ISO 27001, DORA, y RGPD implica auditorías programadas, actualizaciones y formación constante lo que, con el paso del tiempo, puede hacerse más pesado sintiéndose como un fin en lugar de una herramienta).

| Amenaza a la sostenibilidad | Probabilidad | Impacto | Mitigación |
| :---: | :---: | :---: | ----- |
| **Recorte presupuestario** | Media | Alto | Establecer y mantener un presupuesto vinculado a indicadores de riesgos |
| **Rotación/Falta de personal** |  Media-Alta |  Alto | Documentar todo para pasar el conocimiento a los nuevos puestos y establecer planes para la sucesión de roles |
| **Fatiga normativa** | Alta | Medio | Integrar revisiones ISO, DORA y RGPD en un calendario general anual |
| **Pérdida de compromiso** | Media | Alto | KPIs de seguridad en el cuadro de mando trimestral |

En caso de que las medidas de mitigación se implanten y mantengan a largo plazo, se puede asegurar con casi total certeza que el SGSI se mantendrá activo y funcional por mucho tiempo, ya que estas medidas le permiten a ChamBank mejorar el SGSI el cual mejora las condiciones de seguridad y cumplimiento legal junto con el hecho de que puede, a futuro, apoyar la madurez y reducir, parcialmente el riesgo potencial (Englobando en este aspecto al impacto del mismo).

## **16.6. Análisis crítico de principios clave del SGSI** 

Diseñar e implantar un SGSI en base a la ISO 27001 puede llegar a ser complejo, pero el hecho de mantenerlo se puede considerar incluso más complicado. Se han ido tomando decisiones en base a las normas ISO 27001 y 27002, DORA, y RGPD, pero se debe de llevar a cabo un análisis crítico intentando mantenerse todo lo neutral posible respecto al mismo para poder llegar a encontrar las incomodidades del banco respecto al sistema, y lo que se puede garantizar de manera práctica. Para evaluar si ChamBank cumple con los principios clave de la ISO 27001, es necesario contrastar con las cláusulas obligatorias de dicha ISO:

| Clausula | Explicación |
| :---: | ----- |
| **4** | Exige identificar el contexto interno y externo, partes interesadas (y sus requisitos o responsabilidades), y definirles el alcance del SGSI. |
| **5** | Exige el compromiso de la dirección (una vez “realizada” la cláusula 4). |
| **6** | Exige un análisis de riesgos propiamente documentado, con la definición de objetivos respecto a los mismos y la planificación de controles apropiados. |
| **7** | Esta cláusula exige la posesión de recursos de apoyo suficientes, tanto a nivel operacional, como a nivel formativo. |
| **8** | Esta cláusula trata de la evaluación y el análisis de riesgos, y su implementación, necesitando estar construida sobre las cláusulas 6 y 7. |
| **9** | Esta cláusula requiere el llevar a cabo evaluaciones de rendimiento, con monitorización, auditorías y revisiones |
| **10** | Trata del control de daños, viniendo acompañada de la cláusula 9. Exige la gestión de no conformidades y la mejora continua. |

(secureframe, 2024)  
A continuación, se van a comprobar algunas de las cláusulas respecto a un análisis crítico de ChamBank y sus posibles debilidades:

* **El compromiso de la dirección puede ser débil**   
  Para que se aplique la cláusula 5 de la ISO 27001, se debe de contar con el apoyo total. En ChamBank, los roles y responsables están asignados, se revisa trimestralmente, hay políticas de seguridad, etc. Aun así, el mantenimiento del SGSI en Chambank sigue estando anclado al apoyo de la dirección. Hay varias posibilidades respecto a este aspecto:  
  * Compromiso débil al inicio: Este aspecto es posible, aunque se hayan asignado roles, la dirección puede no estar interesada y no invertir en el sistema.  
  * Compromiso no prolongado: La dirección puede estar interesada en la implantación del SGSI e intentar mantenerlo, pero es posible que cada vez le den menos importancia hasta que pase una catástrofe.  
  * Compromiso solo inicial o necesario: Es decir, solo compromiso cuando se va a implantar el sistema y olvidarse de él hasta las auditorías, momento el cual “reactivan” todo el sistema en un intento de pasar la auditoría

  Este riesgo, es de los más difíciles de mitigar ya que depende de decisiones de personas responsables en ChamBank y no del sistema en sí. 

* **La formación esperada no se puede medir completamente de manera práctica, solo teórica**  
  Se exige que las personas relacionadas con el SGSI sean competentes en el área, y que empleados de otras áreas tengan formación en seguridad. Aunque se intente concienciar a otras áreas del banco sin conocimientos de seguridad en seguridad, hay áreas que se “resisten” a dicha formación o que solo la demuestran de manera teórica. Provocando que en el futuro haya incidentes de seguridad causados por esa falta de aplicación práctica. También puede ser culpa de la implantación del SGSI, de que la documentación respectiva esté mal redactada, pudiendo afectar a su rendimiento o al uso de herramientas o aplicaciones de formación. La práctica se debe de reforzar con el tiempo, por ejemplo, con campañas de phishing, los recursos humanos tienen acceso inicial a los datos de los clientes, si caen en phishing la seguridad se ve afectada (a pesar de haber implantado filtros). Establecer medidas de seguridad o formación no asegura la seguridad del banco, pero la práctica puede ayudar.  
* **Análisis de riesgos inicial limitado**  
  Se exige, en la cláusula 6, un análisis de riesgos coherente, documentado y basado en datos. A pesar de que ya se ha llevado a cabo un análisis de riesgos inicial, no se basa en ningún dato real propio de ChamBank, ya que se parte de un punto inicial sin datos históricos. Un error que se suele hacer es el llevar a cabo un análisis de riesgos puramente teórico. Aunque es verdad que las cifras son coherentes respecto a estándares bancarios, no reflejan la realidad de ChamBank. Esto obliga a que el plan de tratamiento de riesgos y el análisis de riesgos se deban de revisar o incluso rehacer pasados los 6 meses esperados hasta que se consigan datos propios.  
* **La certificación no significa seguridad (Sensación de seguridad mencionada antes)**  
  Como ya se mencionó, se exige una mejora contina en todas las secciones del banco (Exigido en este caso por las cláusulas 9 y 10). Aunque anteriormente se hayan cubierto los KPIs y se haya establecido el plan de mejora, hay un riesgo que no se puede eliminar, y es que la certificación garantiza que el sistema está bien asegurado y documentado a la hora de la auditoría, pero no garantiza la seguridad posterior. Un SGSI certificado con la ISO 27001 pero sin llevar a cabo controles periódicos o pruebas de seguridad o de concienciación es menos seguro que uno sin certificar pero que hace dichas pruebas regularmente. El indicador de seguridad aplicada de manera exitosa de ChamBank no radica en la certificación, sino en el conjunto de comportamientos sobre la cultura de seguridad que se mantengan constantes en el tiempo.

(secureframe, 2024)  
En resumen, el mayor riesgo para la sostenibilidad del SGSI de ChamBank principalmente es organizativo, que el sistema se active solo para auditorías, quedando inactivo el resto del tiempo. Eso ocurre cuando el SGSI se siente como un ejercicio impuesto más que como una herramienta de gestión interna, y está documentado en entidades financieras que obtuvieron la certificación de la ISO 27001 pero que han sufrido incidentes relevantes. Para ChamBank la mitigación más efectiva consiste en: hacer los KPIs formen parte de los resultados de cada trimestre independientemente de la existencia de una auditoría programada, y establecer un método de comunicación de incidentes sin consecuencias para quien reporta dicho incidente, eliminando así la tendencia de ocultar fallos. Sin ese par de medidas, el riesgo resultaría en un SGSI certificado, pero sin impacto real. Mantener el SGSI activo requiere de haber tomado decisiones previas en planes ante fallos que el sistema no puede eliminar. Si el CISO abandona ChamBank, el SGSI perdería a su principal responsable, por lo que se tiene que tener un plan de acción inmediato que, por ejemplo, asigne desde un principio a un segundo responsable del SGSI que tome el rol al menos temporalmente. O en caso de que el presupuesto en seguridad se recorte por algún motivo, se deben de priorizar controles más importantes para que se mantengan el mayor tiempo posible, como el MFA o los filtros anti-phishing por su bajo coste y alto alcance, mientras que las auditorías externas deberán de ser las primeras en reducirse, en caso de reducción presupuestaria, sin comprometer a la operativa diaria. Sin esas decisiones tomadas con antelación en planes, el SGSI dependería de la improvisación en momentos críticos.  

# **17. Mapa de implementación del SGSI** 

La implementación del SGSI en ChamBank se puede estimar en un año, dividiendo dicho periodo de tiempo en diferentes fases las cuales sirven para priorizar controles o medidas de seguridad en base a su impacto potencial (positivo) en el banco, incluyendo, evidentemente, una fase final que engloba todo el tiempo posterior a la implementación, es decir, el plan de mejora continua.

|  | Periodo | Despliegue | Responsable |
| :---: | :---: | ----- | :---: |
|  **Fase 1** |  1-3 Meses | Implementación MFA en los procesos internos Implementación filtros antiphishing en el servidor de correo Iniciar la formación interna |  CISO |
| **Fase 2** | 3-6 Meses | Implementación Backups 3-2-1 Tokens temporales cifrados en APIs financieras Inicio de recolección de KPIs  |  CISO y CTO |
|  **Fase 3** |  6-12 Meses | Al principio, primera auditoría interna Cifrado en base de datos (AES-256) y comunicaciones (TLS 1.3) Revisión y contraste de plan de tratamiento de riesgos con datos sobre los mismos recogidos Implementación de SIEM y EDR (Como fase final de esta fase) |  CISO,  CTO,  Auditor interno |
|  **Fase 4** | Mejora continua (Tras 12 meses) | Pruebas de penetración continuas Segunda auditoría anual Auditorías internas Proceso de certificación de la ISO 27001 | CISO, el comité, CEO, auditor/empresa certificadora |

Hay que tener en cuenta que en las fases del mapa de implementación del SGSI se incluye normalmente lo que se ha hecho en este documento, es decir, el planteamiento y planificación inicial, la elección de normativas, integración diaria, análisis de los activos o interesados, responsabilidades, etc. Por lo que esas fases se han saltado, pero serían las primeras que se deben de llevar a cabo.  
(Kantor, 2025)  
(27001, 2025)  
En el mapa de implementación planeado no se han asignado los controles que se planean implementar el primer año de manera aleatoria, sino que se ha pensado en los costes, el tiempo de implantación y el impacto potencial positivo que puede llegar a tener. Por ese motivo, se han implementado, por ejemplo, el MFA y los filtros antes, ya que tienen un impacto potencial considerable y son cuestan poco, por ese mismo motivo, la siguiente fase consiste en los backups y tokens cifrados, ya que llevan tiempo y desarrollo implementarlos, y así, el SIEM y el EDR van “últimos” ya que su implantación incorrecta puede llevar a diversos problemas. Después ya vienen planes a implementar a futuro y cuando las medidas “principales” ya se hayan implantado durante el primer año, como la mejora continua o las auditorias.

# **18. Conclusiones** 

El SGSI diseñado para ChamBank permite integrarlo óptimamente en el mismo. A lo largo del planteamiento y diseño de dicho SGSI, se vio la complejidad real que significaba implantarlo. No era simplemente seguir unas pocas normas y ya, sino que era más que eso. Consistió en integrar una cultura en la seguridad en el banco de todos los empleados del mismo, una mentalidad proactiva ante problemas o incidentes, una aceptación de problemas que no se pueden resolver, pero si disminuir, también consistió en la investigación de normativas y la planificación de evolución junto con las mismas como parte de un proceso de manera continua el cual acompaña al SGSI.  
Uno de los retos más relevantes del sector bancario consiste en la defensa ante las nuevas amenazas de los atacantes, es decir, las nuevas vulnerabilidades o los nuevos métodos de ataque ya que, objetivamente, los atacantes tienden a atacar a las entidades bancarias debido a su gran cantidad de datos relevantes de los clientes. Otro de los retos a los que las entidades financieras se enfrentan consiste en el hecho de que los bancos como ChamBank tienen una mayor carga regulatoria que otros sectores, con marcos como los que se mencionan: DORA, RGPD o ISO27001 e ISO 27002. Este hecho hace que el SGSI no se un documento estático, sino un sistema que evolucione ante nuevas amenazas, cambios regulatorios, novedades, nuevas tecnologías, etc.  
Desde un punto de vista estratégico, la implantación del SGSI a ChamBank le aporta un valor extra aparte de la seguridad. La certificación de la ISO 27001, el cumplimiento aplicado de DORA y RGPD no son solo reglamentos obligatorios, o certificaciones, es un indicador de madurez como entidad financiera, haciéndola confiable y preparada.  
Cabe destacar que el mayor riesgo sigue siendo organizativo, el hecho de que el SGSI se convierta en un ejercicio en lugar de una de una herramienta que va cambiando frente a eventos o decisiones. La diferencia entre un ejercicio y un sistema cambiante recae en el compromiso de la dirección del banco, la cual decidió implementar el SGSI en un primer lugar y en la integración de la seguridad como parte del propio funcionamiento del banco, no como una sección aparte.
 

# **Bibliografía** 

27001, I., 2022. *Liderazgo en ISO 27001.* [En línea]   
Available at: https://www.normaiso27001.es/liderazgo-en-iso-27001/  
[Último acceso: 28 3 2026].  
27001, I., 2022. *Objeto y Campo de Aplicación Definición del Alcance del SGSI.* [En línea]   
Available at: https://www.normaiso27001.es/objeto-y-campo-de-aplicacion/  
[Último acceso: 28 3 2026].  
27001, I., 2022. *Planificación en ISO 27001.* [En línea]   
Available at: https://www.normaiso27001.es/planificacion-en-iso-27001/  
[Último acceso: 28 3 2026].  
27001, I., 2025. *A8 GESTION DE ACTIVOS.* [En línea]   
Available at: https://www.normaiso27001.es/a8-gestion-de-activos/  
[Último acceso: 1 4 2026].  
27001, I., 2025. *Evaluación del desempeño en ISO 27001.* [En línea]   
Available at: https://www.normaiso27001.es/evaluacion-del-desempeno-en-iso-27001/  
[Último acceso: 22 4 2026].  
27001, I., 2025. *FASE 6 Implementando un SGSI.* [En línea]   
Available at: https://www.normaiso27001.es/fase-6-implementando-un-sgsi/  
[Último acceso: 22 4 2026].  
27001, I., 2025. *FASE 6 Implementando un SGSI.* [En línea]   
Available at: https://www.normaiso27001.es/fase-6-implementando-un-sgsi/  
[Último acceso: 20 5 2026].  
27001, I., 2025. *FASE 8 Auditoria interna según ISO 27001.* [En línea]   
Available at: https://www.normaiso27001.es/fase-8-auditoria-interna-segun-iso-27001/  
[Último acceso: 23 4 2026].  
27001, I., 2025. *Mejora en ISO 27001.* [En línea]   
Available at: https://www.normaiso27001.es/mejora-en-iso-27001/  
[Último acceso: 25 4 2025].  
27001, I., 2025. *Soporte en ISO 27001.* [En línea]   
Available at: https://www.normaiso27001.es/soporte-en-iso-27001/  
[Último acceso: 20 4 2026].  
AG, O., 2025. *SGSI – Gestione y proteja los datos corporativos con un Sistema de Gestión de Seguridad de la Información.* [En línea]   
Available at: https://otrs.com/es/casos-de-uso/sgsi/  
[Último acceso: 26 3 2026].  
Allianz, 2025. *Activos financieros: qué son, tipos y mercados donde se negocian.* [En línea]   
Available at: https://www.allianz.es/blog/empresas/5-tipos-activos-financieros.html  
[Último acceso: 1 4 2026].  
alvarez, j., 2024. *Análisis del Valor Monetario Esperado.* [En línea]   
Available at: https://prezi.com/p/2cxt8dqymbgo/analisis-del-valor-monetario-esperado/  
[Último acceso: 4 4 2026].  
Álvarez, J. D. P., 2024. *¿Qué es el reglamento DORA?.* [En línea]   
Available at: https://www.incibe.es/empresas/blog/que-es-el-reglamento-dora  
[Último acceso: 22 3 2025].  
Álvarez, J. D. P., 2025. *DORA ya es obligatorio: ¿estás preparado para notificar incidentes graves?.* [En línea]   
Available at: https://www.incibe.es/empresas/blog/dora-ya-es-obligatorio-estas-preparado-para-notificar-incidentes-graves  
[Último acceso: 21 4 2026].  
Anon., 2015. *ISO 27001: La importancia de capacitar y concienciar a los empleados.* [En línea]   
Available at: https://www.pmg-ssi.com/2015/04/iso-27001-la-importancia-de-capacitar-y-concienciar-a-los-empleados/  
[Último acceso: 20 4 2026].  
Anon., 2022. *Mejora en ISO 27001.* [En línea]   
Available at: https://www.normaiso27001.es/mejora-en-iso-27001/  
[Último acceso: 28 3 2026].  
Anon., 2023. *Riesgo residual en ciberseguridad: aceptar lo inevitable para gestionar mejor.* [En línea]   
Available at: https://4biz.es/2025/08/31/riesgo-residual-en-ciberseguridad-aceptar-lo-inevitable-para-gestionar-mejor/  
[Último acceso: 26 3 2026].  
Anon., 2025. *Ciberseguridad en las finanzas: amenazas y estrategias clave.* [En línea]   
Available at: https://www.sentinelone.com/es/cybersecurity-101/cybersecurity/cyber-security-in-finance/  
[Último acceso: 2 4 2026].  
Anon., 2025. *Cómo prevenir un ataque de inyección de SQL.* [En línea]   
Available at: https://blog.lacnic.net/como-prevenir-ataque-inyeccion-sql/  
[Último acceso: 4 4 2026].  
Anon., 2026. *¿Qué son los activos financieros y cómo se clasifican?.* [En línea]   
Available at: https://www.bbva.es/finanzas-vistazo/ef/fondos-inversion/activos-financieros.html  
[Último acceso: 1 4 2026].  
BMC, 2025. *ISO 27001 (Sistema de Gestión de Seguridad de la Información).* [En línea]   
Available at: https://bm.consulting/es/glosario/iso-27001/  
[Último acceso: 15 5 2026].  
Calidad, A. E. p. l., 2026. *No Conformidad.* [En línea]   
Available at: https://www.aec.es/conocimiento/centro-del-conocimiento/no-conformidad/  
[Último acceso: 25 4 2026].  
Caña, T., 2025. *Cómo desarrollar planes de tratamiento de riesgos ISO 27001 que generen resultados.* [En línea]   
Available at: https://es.isms.online/iso-27001/risk-management/risk-treatment-plans/  
[Último acceso: 7 4 2026].  
Ciberpyme, 2025. *Playbook de respuesta a incidentes de seguridad cibernática: los 10 mejores elementos imprescindibles.* [En línea]   
Available at: https://www.ciberseguridadpyme.es/actualidad/playbook-de-respuesta-a-incidentes-de-seguridad-cibernetica-los-10-mejores-elementos-imprescindibles/  
[Último acceso: 14 5 2026].  
Clay, J., 2026. *Qué es un ataque XSS o Cross-Site Scripting?.* [En línea]   
Available at: https://www.trendmicro.com/es_es/what-is/cyber-attack/xss-cross-site-scripting.html  
[Último acceso: 2 4 2026].  
CLOUDFLARE, 2026. *Cómo prevenir los ataques XSS.* [En línea]   
Available at: https://www.cloudflare.com/es-es/learning/security/how-to-prevent-xss-attacks/  
[Último acceso: 5 4 2026].  
Danby, S., 2026. *La ISO 27001 y la Gestión de Activos: ¿Qué dice el anexo A.8.1?.* [En línea]   
Available at: https://blog.invgate.com/es/iso-27001-gestion-activos  
[Último acceso: 1 4 2026].  
digna, 2023. *7 Incidentes Más Terribles Causados por la Mala Calidad de Datos en el Sector Bancario.* [En línea]   
Available at: https://www.digna.ai/es/7-m%C3%A1s-despamados-incidentes-causados-por-baja-calidad-de-datos-en-el-sector-bancario  
[Último acceso: 2 4 2026].  
DNV, 2026. *ISO 27001 vs ISO 27002: Una comparación.* [En línea]   
Available at: https://www.dnv.es/assurance/articles/iso-27001-vs-iso-27002-the-key-differences/?gad_source=1&gad_campaignid=23691807022&gbraid=0AAAAADwvkUiKasecQq36PR4qO4pdlhsz2&gclid=CjwKCAjwq6DQBhBVEiwA4ZD5XIzp7QR25Ijjmg5YDBm7tldxNApnixZjmT01sKMTforiZSJZIiaKPRoCilsQA  
[Último acceso: 12 5 2026].  
Edwards, M., 2022. *Requisitos y cláusulas de la norma ISO 27001:2022 – 10.1 Mejora continua.* [En línea]   
Available at: https://es.isms.online/iso-27001/requirements-2022/10-1-continual-improvement-2022/  
[Último acceso: 25 4 2026].  
Edwards, M., 2025. *Requisitos y cláusulas de la norma ISO 27001:2022 – 7.3 Concienciación.* [En línea]   
Available at: https://es.isms.online/iso-27001/requirements-2022/7-3-awareness-2022/  
[Último acceso: 20 4 2026].  
Enrique, E., 2026. *Gobierno de la seguridad de la información, políticas y principios del SGSI.* [En línea]   
Available at: https://drive.google.com/file/d/1ZSgQ6bdV-LfsYL9Fn_UrbotFF8DsGBzI/view  
[Último acceso: 3 4 2026].  
España, B. d., 2024. *Tipos de productos y servicios bancarios.* [En línea]   
Available at: https://www.consumoresponde.es/art%C3%ADculos/tipos_de_productos_y_servicios_bancarios  
[Último acceso: 21 3 2026].  
España, S. E. B. d., 2025. *Notificación de incidentes graves y ciberamenazas importantes bajo normativa DORA.* [En línea]   
Available at: https://sedeelectronica.bde.es/sede/es/tramites/notificacion-incidentes-graves-ciberamenazas-importantes-p314.html  
[Último acceso: 21 4 2026].  
Europea, C. d. l. U., 2025. *Regulación bancaria.* [En línea]   
Available at: https://www.consilium.europa.eu/es/policies/banking-regulation/  
[Último acceso: 21 3 2026].  
Europeo/Consejo, P., 2026. *Reglamento de Resiliencia Operativa Digital (DORA).* [En línea]   
Available at: https://www.managementsolutions.com/es/publicaciones-y-eventos/apuntes-normativos/notas-tecnicas-normativas/reglamento-de-resiliencia-operativa-digital-dora  
[Último acceso: 21 4 2026].  
Fernandez, A., 2024. *5 pasos clave para el cumplimiento de la DORA.* [En línea]   
Available at: https://www.hycu.com/es/blog/5-key-steps-dora-compliance  
[Último acceso: 5 4 2026].  
Fortinet, 2025. *¿Qué es la inyección SQL?.* [En línea]   
Available at: https://www.fortinet.com/lat/resources/cyberglossary/sql-injection  
[Último acceso: 2 4 2026].  
Fortinet, 2025. *¿Qué es la tríada CIA?.* [En línea]   
Available at: https://www.fortinet.com/lat/resources/cyberglossary/cia-triad  
[Último acceso: 1 4 2026].  
Fortinet, 2026. *¿Qué es la tríada CIA?.* [En línea]   
Available at: https://www.fortinet.com/lat/resources/cyberglossary/cia-triad  
[Último acceso: 26 3 2026].  
Fortinet, 2026. *Significado de la superficie de ataque.* [En línea]   
Available at: https://www.fortinet.com/lat/resources/cyberglossary/attack-surface  
[Último acceso: 26 3 2026].  
Holloway, D., 2022. *Criterios de riesgo ISO 27001: Guía completa.* [En línea]   
Available at: https://es.isms.online/iso-27001/risk-management/risk-criteria/  
[Último acceso: 2 4 2026].  
holloway, D., 2025. *La guía definitiva para ISO 27002.* [En línea]   
Available at: https://es.isms.online/iso-27002/  
[Último acceso: 14 5 2026].  
holloway, D., 2025. *Requisito 27001 de ISO 7.2 – Competencia.* [En línea]   
Available at: https://es.isms.online/iso-27001/requirements-2013/7-2-competence-2013/  
[Último acceso: 20 4 2026].  
IBM, 2025. *¿Qué son los controles de seguridad?.* [En línea]   
Available at: https://www.ibm.com/es-es/think/topics/security-controls  
[Último acceso: 26 3 2026].  
ICSI, 2019. *¿Cómo evaluar la propia cultura de seguridad?.* [En línea]   
Available at: https://www.icsi-eu.org/es/actu/evaluar-cultura-seguridad  
[Último acceso: 24 4 2026].  
INCIBE, 2023. *Roles en ciberseguridad: desde el CEO a los usuarios finales.* [En línea]   
Available at: https://www.incibe.es/empresas/blog/roles-en-ciberseguridad-desde-el-ceo-los-usuarios-finales  
[Último acceso: 27 3 2026].  
ISO, 2024. *ISO/IEC 27001:2022.* [En línea]   
Available at: https://www.iso.org/es/norma/27001  
[Último acceso: 22 3 2025].  
ISOWin, 2017. *El Plan de Tratamiento de Riesgos en la norma ISO 27001 2017.* [En línea]   
Available at: https://isowin.org/blog/plan-tratamiento-riesgos-ISO-27001/  
[Último acceso: 7 4 2026].  
iuvity, 2025. *ISO 27001 en el sector financiero: relevancia, requisitos y beneficios.* [En línea]   
Available at: https://www.iuvity.com/es/blog/iso-27001  
[Último acceso: 15 5 2026].  
Kantor, I., 2025. *ISO 27001 Implementation: Comprehensive Guide.* [En línea]   
Available at: https://iterasec.com/blog/iso-27001-implementation-guide-for-it-companies/  
[Último acceso: 20 5 2026].  
Kaseya, 2025. *¿Qué es el robo de tokens?.* [En línea]   
Available at: https://www.kaseya.com/es-la/blog/what-is-token-theft/  
[Último acceso: 2 4 2026].  
Kelly, B., 2021. *Amenazas de seguridad en los servicios financieros.* [En línea]   
Available at: https://www.globalsign.com/es/blog/5-friday-5-security-threats-facing-financial-services-industry  
[Último acceso: 26 3 2025].  
Laprovittera, C., 2025. *Mejora en ISO 27001.* [En línea]   
Available at: https://achirou.com/mejora-en-iso-27001/  
[Último acceso: 25 4 2025].  
López, J., 2025. *KPIs esenciales para medir la eficacia de tu estrategia de ciberseguridad empresarial.* [En línea]   
Available at: https://www.qualoom.es/indicadores-clave-kpis-para-medir-la-eficacia-de-tu-estrategia-de-ciberseguridad/  
[Último acceso: 22 4 2026].  
Mexicana, B. I., 2026. *¿Qué significa el certificado ISO 27001 en un banco?.* [En línea]   
Available at: https://www.bim.mx/que-significa-el-certificado-iso-27001-en-un-banco/  
[Último acceso: 13 4 2026].  
Mexico, I., 2021. *Los 7 errores al implementar un sistema de gestión de seguridad de la información..* [En línea]   
Available at: https://www.infosecuritymexico.com/es/blog/los-7-errores-al-implementar-un-sistema-de-gestion-de-seguridad-de-la-informacion.html  
[Último acceso: 16 5 2026].  
Mota, A., 2023. *Definiendo los Roles y Responsabilidades ISO 27001.* [En línea]   
Available at: https://innevo.com/blog/roles-y-responsabilidades-iso-27001  
[Último acceso: 27 3 2026].  
Odebrecht, J., 2024. *Cultura de seguridad: beneficios y consejos para implantarla en tu empresa.* [En línea]   
Available at: https://es.checklistfacil.com/blog/cultura-de-seguridad/  
[Último acceso: 24 4 2026].  
OpenLearn, 2026. *Different types of control.* [En línea]   
Available at: https://www.open.edu/openlearn/mod/oucontent/view.php?id=88999&section=6.2#:~:text=A%20simple%20diagram%20of%204,must%20be%20a%20corrective%20element.  
[Último acceso: 8 4 2026].  
OSH, S., 2026. *Cómo podemos medir la Cultura de Seguridad en el lugar de trabajo de forma sencilla.* [En línea]   
Available at: https://www.smartosh.com/como-podemos-medir-la-cultura-de-seguridad-en-el-lugar-de-trabajo-de-forma-sencilla/  
[Último acceso: 24 4 2026].  
Peters, S., 2022. *Requisito 27001 de ISO 10.1: No conformidades y acciones correctivas.* [En línea]   
Available at: https://es.isms.online/iso-27001/requirements-2013/10-1-nonconformity-and-corrective-action-2013/  
[Último acceso: 25 4 2026].  
Peters, S., 2025. *Requisito 27001 de ISO 10.2: mejora continua.* [En línea]   
Available at: https://es.isms.online/iso-27001/requirements-2013/10-2-continual-improvement-2013/  
[Último acceso: 25 4 2026].  
raisin, 2025. *Activos financieros: definición y características.* [En línea]   
Available at: https://www.raisin.com/es-es/inversion/activos-financieros-que-son-como-se-clasifican-ejemplos/  
[Último acceso: 1 4 2026].  
Reyes, J., 2024. *PDCA: What is the Plan Do Check Act Cycle?.* [En línea]   
Available at: https://safetyculture.com/topics/pdca  
[Último acceso: 25 4 2026].  
Sánchez, G., 2024. *Indicadores Clave de Rendimiento (KPIs) para SGSI.* [En línea]   
Available at: https://blog.tecnetone.com/indicadores-clave-de-rendimiento-kpis-para-sgsi  
[Último acceso: 22 4 2026].  
Santander, B., 2024. *¿Qué es un incidente de seguridad?.* [En línea]   
Available at: https://www.bancosantander.es/glosario/incidente-seguridad  
[Último acceso: 26 3 2026].  
Santander, B., 2024. *¿Qué son los activos financieros y cómo se clasifican?.* [En línea]   
Available at: https://www.bancosantander.es/glosario/activos-financieros  
[Último acceso: 26 3 2025].  
Secureframe, 2024. *ISO 27001 vs ISO 27002: ¿Cuál es la diferencia?.* [En línea]   
Available at: https://secureframe.com/es-es/hub/iso-27001/vs-iso-27002  
[Último acceso: 14 5 2026].  
secureframe, 2024. *Los requisitos básicos de las Cláusulas 4-10.* [En línea]   
Available at: https://secureframe.com/es-es/hub/iso-27001/clauses  
[Último acceso: 21 5 2026].  
severion, 2025. *Data-at-Rest vs. Data-in-Transit Encryption Explained.* [En línea]   
Available at: https://www.serverion.com/nn/uncategorized/data-at-rest-vs-data-in-transit-encryption-explained/#:~:text=Side%2Dby%2DSide%20Comparison&text=Data%20in%20transit%20is%20particularly,added%20security%20during%20active%20exchanges.  
[Último acceso: 21 4 2026].  
SGSI, 2020. *ISO27000.ES.* [En línea]   
Available at: https://www.iso27000.es/sgsi.html  
[Último acceso: 22 3 2025].  
Sharron, M., 2023. *ISO 27001 para el sector bancario.* [En línea]   
Available at: https://es.isms.online/sectors/iso-27001-for-the-banking-sector/  
[Último acceso: 25 4 2026].  
Solutions, G., 2025. *¿Qué es la norma ISO 27001 y para qué sirve?.* [En línea]   
Available at: https://www.globalsuitesolutions.com/es/que-es-la-norma-iso-27001-y-para-que-sirve/?gad_source=1&gad_campaignid=21493661700&gbraid=0AAAAAD7gb8ibBkIBYpW2xSEmEbIhEAtqG&gclid=CjwKCAjwwJzPBhBREiwAJfHRnUdKstG5DDAOXLBaVDvLZ48s9Zi0JPEh5zdzvj-KMn5hW2QA81uMnhoCrd0  
[Último acceso: 21 4 2026].  
Solutions, G., 2025. *Cómo hacer la auditoría interna de un SGSI basado en la ISO 27001.* [En línea]   
Available at: https://www.globalsuitesolutions.com/es/auditoria-interna-sgsi-basado-iso-27001/  
[Último acceso: 23 4 2026].  
sothis, 2026. *¿Qué indicadores de un SGSI pueden ser útiles para la alta dirección?.* [En línea]   
Available at: https://www.sothis.tech/que-indicadores-de-un-sgsi-pueden-ser-utiles-para-la-alta-direccion-2/  
[Último acceso: 24 4 2026].  
Stripe, 2024. *¿Qué es la normativa PSD2? Lo que las empresas deben saber.* [En línea]   
Available at: https://stripe.com/es/resources/more/what-is-psd2-here-is-what-businesses-need-to-know  
[Último acceso: 24 3 2025].  
Sunrise, D., 2026. *Explorando los Tipos de Controles de Seguridad para la protección de datos.* [En línea]   
Available at: https://www.datasunrise.com/es/centro-de-conocimiento/tipos-de-controles-de-seguridad/  
[Último acceso: 5 4 2026].  
Team, S. C., 2025. *Análisis de riesgo cualitativo y cuantitativo.* [En línea]   
Available at: https://safetyculture.com/es/temas/analisis-cualitativo  
[Último acceso: 3 4 2026].  
Team, S. C., 2025. *Análisis de riesgos: Una guía completa.* [En línea]   
Available at: https://safetyculture.com/es/temas/analisis-de-riesgos  
[Último acceso: 3 4 2026].  
TOOLS, I., 2026. *Indicadores más útiles para un sistema de gestión de seguridad de la información.* [En línea]   
Available at: https://isotools.org/2022/05/13/indicadores-mas-utiles-para-un-sistema-de-gestion-de-seguridad-de-la-informacion/  
[Último acceso: 22 4 2026].  
TryHackMe, 2026. *The CIA Triad.* [En línea]   
Available at: https://tryhackme.com/room/theciatriad  
[Último acceso: 26 3 2026].  
Union, E., 2022. *Reglamento general de protección de datos (RGPD).* [En línea]   
Available at: https://eur-lex.europa.eu/ES/legal-content/summary/general-data-protection-regulation-gdpr.html  
[Último acceso: 22 3 2025].  
Wagenbach, M., 2026. *ISO 27001 para el Sector Financiero Español: Requisitos, Plazos y Automatización.* [En línea]   
Available at: https://matproof.com/es/blog/iso27001-sector-financiero-espana  
[Último acceso: 16 5 2026].  
Wikipedia, 2020. *Riesgo bancario.* [En línea]   
Available at: https://es.wikipedia.org/wiki/Riesgo_bancario  
[Último acceso: 26 3 2025].
