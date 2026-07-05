# **7. Identificación de activos** 

Los activos de ChamBank se clasifican siguiendo criterios de la ISO 27001: por tipo (información, infraestructura, software, humano) y por su criticidad CID (Confidencialidad, integridad y disponibilidad). Dicha clasificación permite vincular cada activo identificado en este apartado con los riesgos de cada uno del apartado 8, y los controles del plan de tratamiento Los activos detectados en ChamBank son:

| Activo | Descripción | Grupo | Impacto CID |
| ----- | ----- | ----- | ----- |
|  **Datos de clientes**  | En este activo se engloba la información personal de los clientes, como credenciales de acceso, información privada, historial, etc. Su exposición puede provocar fraudes, sanciones, pérdida de confianza de los clientes, etc. |  Información | Confidencialidad: Alta Integridad:  Alta Disponibilidad: Media |
|  **App de banca online** | Es el canal principal de interacción entre los clientes y sus cuentas bancarias. Lo usan para llevar a cabo transacciones, gestionar sus cuentas o solicitar diversos servicios. |  Software/ Programas | Confidencialidad: Alta Integridad:  Alta Disponibilidad: Alta |
|  **Infraestructura cloud** | Es el conjunto de servicios que aporta la nube ya sea para almacenar datos, ejecutar apps, llevar a cabo operaciones, …Una mala configuración de la misma da lugar a comprometer diversos servicios. |  Infraestructura | Confidencialidad: Alta:  Integridad: Alta Disponibilidad: Alta |
|  **APIs financieras**  | Engloba las diferentes maneras de los trabajadores de comunicarse con diversos servicios, si se ven comprometidas, pueden dar acceso no autorizado a datos o permitir ejecuciones de código. |  Software/ Programas | Confidencialidad: Alta Integridad: Alta Disponibilidad: Alta |
|  **Datos  de los empleados**  | Información personal de los empleados del banco, como credenciales de acceso, cuentas, datos administrativos, … La exposición de estos datos, aparte de la de los clientes permite facilitar ataques. |  Información | Confidencialidad: Alta Integridad: Media Disponibilidad: Media |
|  **Registros financieros**  | Historiales, balances, transacciones y logs operacionales que sirven para mantener constancia de lo que se lleva a cabo y para seguir el cumplimiento regulatorio. |  Información | Confidencialidad: Alta Integridad: Alta Disponibilidad: Alta  |
|  **Servicios internos**  | Son los sistemas y aplicaciones usados internamente para las operaciones del banco, formando la base tecnológica interna del banco. |  Servicios/ Programas | Confidencialidad: Media Integridad:  Alta Disponibilidad: Alta |
|  **Servidores**  | Los equipos del banco que conecta sistemas, dispositivos, o que hostea servicios internos. Si se ven comprometidos, facilitan ataques en los que se infectan varios dispositivos. |  Infraestructura | Confidencialidad: Alta Integridad: Alta Disponibilidad: Alta |
|  **Red  interna**  | Red que conecta sistemas dentro del banco. Si se compromete de alguna manera, puede facilitar ataques como movimientos laterales. |  Infraestructura  | Confidencialidad: Media Integridad: Alta Disponibilidad: Alta |
|  **Empleados**  | Personal del banco que interactúa con los sistemas del mismo. Errores humanos o malas prácticas dan lugar a incidentes.  |  Factor humano | Confidencialidad: Media Integridad: Media Disponibilidad: Alta |
|  **Clientes**  | Usuarios que usan los servicios del banco. Pueden ser víctimas de phishing que afecta, indirectamente, a la seguridad del banco. |  Factor humano | Confidencialidad: Alta Integridad: Media Disponibilidad: Media |

(Danby, 2026)  
(27001, 2025)  
(Fortinet, 2025)  
(Anon., 2026)  
(raisin, 2025)  
(Allianz, 2025)

* **Datos de los clientes**: La confidencialidad es crítica por el gran volumen de datos personales y financieros regulados por el RGPD. Su filtración implica sanciones y pérdida de reputación. La integridad es también crítica porque su alteración permite fraudes o suplantaciones. Y la disponibilidad se valora como media porque su interrupción temporal es “asumible”.  
* **App de banca online**: Es crítico en todos sus aspectos porque es el canal principal de interacción del cliente con su cuenta. Un acceso no autorizado expone cuentas, su modificación permite fraude y su caída impacta en los ingresos y la confianza del usuario.  
* **Infraestructura cloud**: Reúne datos, servicios y operaciones. Cualquier incidente afecta a la vez a varios activos, y empeora con el hecho de que ChamBank apenas tiene control sobre terceros.  
* **APIs financieras**: Es el método de comunicación entre sistemas, significando que su compromiso pueda llevar a fraudes, exposición de datos, interrupciones de servicios, etc.  
* **Datos de empleados**: La confidencialidad es alta por el riesgo de suplantación o accesos no autorizados mientras que su integridad y disponibilidad se mantienen en medio por la existencia de backups que permiten su recuperación.  
* **Registros financieros**: Tiene triple criticidad ya que contienen información operacional cuya alteración puede llevar a consecuencias legales y su indisponibilidad paraliza la toma de decisiones del banco  
* **Servicios internos**: La confidencialidad es media porque no todos manejan datos sensibles, mientras que la integridad y disponibilidad son altas ya que, si ocurre un incidente de seguridad, se puede llegar a propagar a otros procesos.  
* **Servidores**: Son el núcleo de la infraestructura interna, por lo que su compromiso en cualquiera de los tres aspectos afectaría a otras áreas inevitablemente.  
* **Red interna**: La confidencialidad es media ya que no toda la red transmite datos confidenciales. Y la integridad y la disponibilidad se clasifican como altas porque una intrusión puede afectar a la disponibilidad y permitir el movimiento lateral interno.  
* **Empleados**: La confidencialidad e integridad son medianos ya que depende del rol del empleado y sus permisos. La disponibilidad es alta ya que sin acceso a las herramientas que usa el mismo, o su función, las operaciones internas pueden detenerse o verse afectadas.  
* **Clientes**: La confidencialidad es alta por las credenciales y datos que se manejan. La integridad y la disponibilidad son medias porque las acciones de un cliente afectan a su cuenta principalmente.
