## instalar ssh en windows y comandos basicos Para instalar OpenSSH mediante PowerShell, ejecute PowerShell como administrador. 
# Para asegurarse de que OpenSSH esté disponible, ejecute el siguiente cmdlet:
Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'

# A continuación, instale los componentes de servidor o cliente según sea necesario:

# Install the OpenSSH Client
Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

# Install the OpenSSH Server
Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0

# Para iniciar y configurar el servidor OpenSSH para su primer uso, abra PowerShell como administrador y,
luego, ejecute los siguientes comandos para iniciar sshd 
# Start the sshd service
Start-Service sshd
# OPTIONAL but recommended:
Set-Service -Name sshd -StartupType 'Automatic'

# conectarse a una maquina por ssh (maquina@ip)
~~~
ssh vmwmigue@192.168.0.114
~~~

# copiar todo el directorio y subcarpetas desde el servidor a nuestra maquina en el directorio que estamos parado en nuestra maquina cliente.
~~~
scp -r username@hostname:/path/from/remote .
scp -r vmwmigue@192.168.0.114:C:\Users\vmWmigue\hola .
~~~

# copiar carpeta y contenido desde el cliente al servidor
~~~
scp -r /path/from/local username@hostname:/path/to/remote
~~~

## comandos basicos consola powershell windows

# abrir powershell de windows
~~~
powershell
~~~

# crear directorio
~~~
mkdir nombre
~~~

# listar carpetas
~~~
dir
~~~

# cambiar de directorios
~~~
cd.. 
~~~
~~~
cd /carpeta
~~~


# muestra todos los subdirectorios
~~~
TREE Carpeta
~~~


# limpiar pantalla
~~~
CLS
~~~

# copiar archivos
~~~
COPY Archivo Destino
~~~

# mover archivos
~~~
MOVE Archivo Destino
~~~





