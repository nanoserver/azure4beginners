---
layout: default
---
#Tipos de redes virtuales

A la hora de trabajar con redes virtuales podemos configurar tres tipos diferentes segun las necesidades que tengamos:

- **Redes virtuales solo en Azure**: redes configuradas a traves del portal de gestión que permiten organizar nuestras máquinas virtuales y nuestros servicios en la nube dentro del rango de direccionamiento privado que deseemos.
- **Redes virtuales Punto a Sitio**: redes privadas virtuales establecidas entre un ordenador cliente situado fuera de Azure y una red virtual desplegada dentro de Azure. Permiten establecer una conexión segura desde el exterior a nuestra red virtual. Este tipo de conexión tiene que ser configurada de forma individual en cada equipo remoto que quiera acceder. Se inicializa de forma manual por el usuario y la ventaja es que no requiere del uso de ningún tipo de hardware especial.

    Este tipo de redes pueden ser utilizadas por ejemplo en escenario de desarrollo y pruebas donde el desarrollador necesita acceder a los recursos desplegados en Azure de una forma directa y similar a como lo haria dentro de su propia oficina. La conexión se realiza a traves del protocolo SSTP facilitando la comunicación sin necesidad de configuraciones extras de puertos o proxies.
    
- **Redes virtuales Sitio a Sitio**: redes privadas virtuales establecidas entre una red remota y una red virtual desplegada en Azure. Para desplegar una red sitio a sitio es necesario que exista un dispositivo VPN en la red remota que establezca la conexión segura con el gateway de Azure. Una vez establecida la conexión, a diferencia de las punto a sitio, todos los equipos dentro de la red remota tienen acceso directo a los recursos en Azure sin necesidad de realizar alguna configuración extra.

    Este tipo de redes pueden ser utilizadas por ejemplo en escenarios que deseen una integración entre diferentes servicios y recursos disponibles en nuestro datacenter y Azure. Además de la conexión empleando dispositivos hardware VPN es posiblie emplear soluciones software como OpenSwan o Windows Server 2012 R2 con el rol de RRAS configurado.
- **Reves virtuales privadas a traves de un proveedor**: este tipo de configuración te permite crear una red virtual que conecte directamente tu infraestructura con el datacenter de Azure. El tráfico, a diferencia de los anteriores, no es enrutado a través de Internet si no que es transportado por las redes de un tercero que ofrece servicios de red como British Telecom o Equinix. 
    El uso de este tipo de redes virtuales proporcionan una mejor velocidad, latencia reducida, mayor estabilidad y mayor seguridad que las conexiones habituales de Internet.
