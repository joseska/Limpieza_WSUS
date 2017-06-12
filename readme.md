## Limpieza de un Servidor WSUS Server desde Powershell

Un simple Script que permite ejecutar el Asistente de Limpieza del WSUS desde Powershell. La unica variable obligatoria que tienes que modificar es "$updateServer" por el nombre de tu servidor WSUS.

$useSecureConnection -> si utilizas SSL  
$portNumber -> Puerto que utilizas. Por defecto 80. Si utilizas SSL 443  

### Parametros Conexion WSUS:  
[String]$updateServer = "WSUS-R-38"  
[Boolean]$useSecureConnection = $False  
[Int32]$portNumber = 80  

Y las diferentes opciones de limpieza. Si no quieres alguna, simplemente hay que cambiar el estado a $False.  
### Parametros de Limpieza:  
[Boolean]$supersededUpdates = $True  
[Boolean]$expiredUpdates = $True  
[Boolean]$obsoleteUpdates = $True  
[Boolean]$compressUpdates = $True  
[Boolean]$obsoleteComputers = $True  
[Boolean]$unneededContentFiles = $True  

