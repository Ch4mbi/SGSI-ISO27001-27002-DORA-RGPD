
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
