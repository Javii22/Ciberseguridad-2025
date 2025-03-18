### **Tutorial: Explotación de la vulnerabilidad MS17-010 (EternalBlue) en THM**
 
 ---

 **Paso 1: Escaneo de puertos con Nmap**
 
 Ejecutamos el siguiente comando para escanear los servicios en la máquina objetivo:
 
 ![](Imagenes/2.png)
 
 **Nota:** EternalBlue es una vulnerabilidad en Microsoft Windows explotada por la NSA antes de ser revelada públicamente. Permite a un atacante obtener acceso remoto a computadoras vulnerables.
 
 En el escaneo, encontramos **3 puertos abiertos por debajo de 1000**.
 
 ![](Imagenes/3.png)
 
 ---
 
 **Paso 2: Buscar y seleccionar el exploit en Metasploit**
 
 Ejecutamos **msfconsole** y buscamos el exploit para la vulnerabilidad MS17-010 con:
 
 ![](Imagenes/27.png)
 
 La ruta completa del código del exploit es:
 
 ![](Imagenes/1.png)
 
 Seleccionamos el exploit con:
 
 Después, configuramos el payload:
 
 Mostramos las opciones con:
 
 ![](Imagenes/4.png)
 
 ---
 
  **Paso 3: Configurar parámetros y ejecutar el exploit**
 
 Definimos la IP de la máquina víctima:
 
 ![](Imagenes/6.png)
 
 Definimos nuestra IP en la VPN de THM:
 
 ![](Imagenes/10.png)
 
 Ejecutamos el exploit:
 
 
 ![](Imagenes/11.png)
 
 Una vez dentro de la máquina víctima, verificamos la IP con:
 
 ![](Imagenes/12.png)
 
 Colocamos la sesión en segundo plano con:
 
 
 ![](Imagenes/13.png)
 
 Revisamos las sesiones activas:
 
 ![](Imagenes/16.png)
 
 Ingresamos a Meterpreter con:

 ![](Imagenes/18.png)
 
 Ahora que tenemos privilegios elevados, ejecutamos:

 ![](Imagenes/19.png)
 
 Copiamos el hash y lo crackeamos en **Crackstation.net**.
 
 ![](Imagenes/20.png)
 
 Contraseña obtenida: **alqfna22**
 
 ---
 
 **Paso 4: Obtención de las flags**
 
 **Primera Flag**
 
 Nos movemos a la raíz del sistema:
 
 
 
 ![](Imagenes/21.png)
 
 Leemos la flag:
 
 
 Flag obtenida: **1/3**
 
 ---
 
**Segunda Flag**
 
 Nos dirigimos a la nueva ruta indicada:
 
 ![](Imagenes/22.png)
 
 Leemos la flag:
 
 
 
 Flag obtenida: **2/3**
 
 ---
 
 **Tercera Flag**
 
 Vamos a la ruta indicada:
 
 ![](Imagenes/24.png)
 
 Leemos la flag:
 
 
 
 Flag obtenida: **3/3**
 
 ---
 
**Conclusión**
 
 Hemos completado la explotación de la máquina **BLUE** en TryHackMe, utilizando **EternalBlue (MS17-010)** para obtener acceso, escalar privilegios y extraer información clave.
