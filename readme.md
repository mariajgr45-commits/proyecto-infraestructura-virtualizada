Infraestructura de Red Virtualizada
 Descripción

Este proyecto implementa una infraestructura de red virtualizada que simula un entorno empresarial real mediante máquinas virtuales con Windows Server y Windows 11.

Permite la gestión centralizada de usuarios, el control de accesos y la compartición de recursos dentro de una red local.

 Manual de instalación
 Requisitos
Ordenador con al menos 8 GB de RAM (recomendado)
VirtualBox instalado
Imagen ISO de:
Windows Server
Windows 11 Pro
 Paso 1: Crear máquinas virtuales
Abrir VirtualBox
Crear dos máquinas virtuales:
Servidor (Windows Server)
Cliente (Windows 11)
Asignar recursos (RAM, disco, CPU)
 Paso 2: Instalar sistemas operativos
Instalar Windows Server en el servidor
Instalar Windows 11 en el cliente
Paso 3: Configurar red
Configurar red interna en VirtualBox
Asignar IPs estáticas:
Servidor: 192.168.1.10
Cliente: 192.168.1.20
Paso 4: Crear dominio
Instalar rol Active Directory Domain Services (AD DS)
Promocionar el servidor a controlador de dominio
Crear dominio: empresa.local
Paso 5: Crear usuarios
Acceder a Active Directory
Crear usuarios y grupos
Paso 6: Unir cliente al dominio
Configurar el cliente
Unirlo al dominio empresa.local
Reiniciar equipo
Paso 7: Compartir recursos
Crear carpeta en el servidor
Configurar permisos
Acceder desde el cliente
Paso 8: Comprobaciones
Ejecutar ping entre equipos
Verificar acceso a recursos
Comprobar inicio de sesión
▶Manual de uso
Inicio de sesión

El usuario debe iniciar sesión en el cliente con credenciales del dominio:

DOMINIO\usuario
 Acceso a recursos compartidos
Abrir explorador de archivos
Acceder a la red
Entrar en la carpeta compartida del servidor
 Control de acceso
Los permisos dependen del usuario o grupo
Posibilidades:
Lectura
Escritura
Sin acceso
 Comprobación de red

Para verificar la conectividad:

ping 192.168.1.10
 Posibles errores
 No conecta al dominio → revisar IP
 No accede a carpeta → revisar permisos
 Ping falla → comprobar red virtual
 Tecnologías utilizadas
VirtualBox
Windows Server
Windows 11 Pro
Active Directory
 Limitaciones
Dependencia del hardware
No escalable
Entorno de pruebas
Conclusión

Se ha conseguido implementar una infraestructura de red funcional y realista en un entorno virtualizado, permitiendo la gestión centralizada de usuarios y recursos.