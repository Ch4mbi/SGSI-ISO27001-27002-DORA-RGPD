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
