
![](Images/Triggerdblogo.png)

# Lab: Herramientas SQL Server RML

#### <i>Triggerdb Consulting SRL</i> | www.triggerdb.com | https://blogs.triggerdb.com

## Acerca de este workshop

Bienvenido/a a este Workshop armado por **Maximiliano Damian Accotto** Microsoft MVP en Data Platform y socio fundador de **Triggerdb Consulting SRL**

El objetivo de este workshop es que pueda aprender a usar las distintas herramientas RML las cuales son de gran ayuda para hacer trabajos como

1. Análisis de trazas o eventos extendidos
2. Hacer pruebas de carga (Stress)



<p style="border-bottom: 1px solid lightgrey;"></p>
<h2><img style="float: left; margin: 0px 15px 15px 0px;" raw=true"><b>     Agenda</b></h2>

En este workshop veremos los siguientes temas

| Tema                                | Descripción                                     |
| ----------------------------------- | ----------------------------------------------- |
| [Introducción] (#1. Introducción)   |                                                 |
| [Instalación] (#2. Instalación)     | Instalar las herramientas                       |
| [Ostress](./Lab%20RML%20Ostress.md) | Usando Ostress para emular cargas de trabajo    |
| [Readtrace] (./Lab RML Readtrace.md)| Analizando trc o Extended Events de performance |

[I'm a relative reference to a repository file](./Lab%20RML%20Ostress.md)


<table style="tr:nth-child(even) {background-color: #f2f2f2;}; text-align: left; display: table; border-collapse: collapse; border-spacing: 5px; border-color: gray;">

  <tr><td style="background-color: AliceBlue; color: black;"><b>Module</b></td><td style="background-color: AliceBlue; color: black;"><b>Topics</b></td></tr>

  <tr><td ><a href="./Lab RML Ostress.md" target="_blank">01 - Ostress</a></td><td> Learn how SQL Server 2019 solves challenges for the modern data professional</td></tr>
  <tr><td><a href="./sql2019workshop/02_IntelligentPerformance.md" target="_blank">02 - Intelligent Performance</a></td><td> Learn the how SQL Server can boost your performance with no application changes</td></tr>
  <tr><td><a href="./sql2019workshop/03_Security.md" target="_blank">03 - Security</a> </td><td > Learn new security features of SQL Server 2019 such as Data Classification and Auditing</td></tr>
  <tr><td><a href="./sql2019workshop/04_Availability.md" target="_blank">04 - Availability</a></td><td> Learn new capabilities to make your SQL Server more available such as Accelerated Database Recovery</td></tr>
  <tr><td ><a href="./sql2019workshop/05_ModernDevPlatform.md" target="_blank">05 - Modern Development Platform</a></td><td> Learn how SQL Server 2019 provides new capabilities for the modern data developer</td></tr>
  <tr><td><a href="./sql2019workshop/06_Linux_and_Containers.md" target="_blank">06 - Linux and Containers</a></td><td>Learn how to deploy SQL Server in containers and SQL Server Replication on Linux.</td></tr>
  <tr><td><a href="./sql2019workshop/07_SQLOnKubernetes.md" target="_blank">07 - SQL Server on Kubernetes</a></td><td>Learn how to deploy SQL Server on a Kubernetes Cluster</td></tr>
  <tr><td><a href="./sql2019workshop/08_DataVirtualization.md" target="_blank">08 - Data Virtualization</a> </td><td>Learn how to use SQL Server as a data hub and reduce data movement using Polybase++</td></tr> 
  <tr><td><a href="./sql2019workshop/09_BigDataClusters.md" target="_blank">09 - Big Data Clusters</a> </td><td>Learn how to use and manage an integrated solution with SQL Server, Hadoop, and Spark</td></tr>
  <tr><td><a href="./sql2019workshop/10_Additional_Migration.md" target="_blank">10 - Additional Capabilities,  Migration, and Next Steps</a></td><td>Learn more about Additional Capabilities in SQL Server 2019, Migration Tools, Database Compatibility, and Next Steps</td></tr>
  <tr></tr>
  <tr></tr>
</table>
## 1. Introducción

Las RML son herramientas de linea de comando que ya tienen unos cuantos años de estar disponibles.

Estas herramientas son distribuidas por el equipo de soporte de **Microsoft**  totalmente gratuita .

Dentro de las utilidades se encuentran

| Nombre    | Descripción                                 |
| --------- | ------------------------------------------- |
| ReadTrace | Permite analizar trc o xtend events         |
| Reporter  | Permite visualizar los datos de Readtrace   |
| Ostress   | Permite realizar cargas de trabajo (stress) |

## 2. Instalación

Como primer paso lo que debemos hacer es instalar las herramientas en nuestro equipo (no es necesario hacerlo sobre los servidores de MSSQL).

Para ello lo que haremos primero es acceder al siguiente [link](https://www.microsoft.com/en-us/download/details.aspx?id=4511) e instalarlas en tu equipo local.

Luego de hacer dicha instalación se recomienda hacer una actualización de las mismas si es que va a usar trazas de SQL Server 2016 o 2017.

Para dicho fin siga las siguientes instrucciones

1. Descargue la herramienta Database Experimentation Assistant (DEA) desde el siguiente [link]( https://www.microsoft.com/en-us/download/details.aspx?id=54090) 

2. Instale la herramienta en su equipo local.
3. Copie los 4 archivos de la carpeta "C:\Program Files (x86)\Microsoft Corporation\Database Experimentation Assistant\Dependencies\X64" a "C:\Program Files\Microsoft Corporation\RMLUtils"



Luego de instalar las herramientas podremos acceder al cmd shell desde windows

![](Images/01-install.GIF)


