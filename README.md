# Flow5_OpenWeather
Este repositorio obtiene información directamente del servicio de clima OpenWeatherMap.org a través de API
Tambien se abrira el puerto 1880 para que se puede acceder desde cualquier dispositovo, fuera de mi red, al dashboard del flow 5

## Abrir puertos del modem
-  Encontrar la IP de configuración local del modem
- Introducir el nombre y contraseña
- Buscar la sección de redireccionamiento de puertos o mapeo de puertos
- Abrir un puerto con las siguientes configuraciones
    - Rango de puertos (público y privado) 1880-1880
    - Protocolo TCP o TCP/UDP
    - IP LAN o HOST, es la IP de la máquina virtual, mi IP es 192.168.1.109
- Abrir el firewall de la máquina virtual
    - sudo ufw enable
    - sudp ufw allow 1880
- En caso de tener antivirus, se debe agregar una excepción al firewall
- Obtener la IP pública en el momento en que compartiran la liga de acceso, ya que puede cambiar cada que se reinicia el dispositivo
- Se construye la IP de acceso, usando la IP general del dashboard, se va a cambiar el localhost por la IP pública antes obtenida
    - http://localhost:1880/ui/#!/3?socketid=e1IwFbjlHjhK8_HDAAAB

IP de acceso: 
    - http://201.133.214.44:1880/ui/#!/3?socketid=e1IwFbjlHjhK8_HDAAAB