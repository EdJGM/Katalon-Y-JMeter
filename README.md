# Katalon-Y-JMeter
Repositorio que contiene ejemplso de uso de las herramientas de testing Katalon y JMeter

## Instalación de Katalon Studio

Para instalar Katalon Studio, sigue los siguientes pasos:

### Requisitos del sistema

- **Sistema Operativo**: Windows 7, 8, 10 (64-bit), macOS 10.11+ (64-bit), Ubuntu 14+ (64-bit)
- **Memoria RAM**: Mínimo 4GB, se recomienda 8GB
- **Espacio en Disco**: Mínimo 1GB para la instalación básica
- Si tienes mas dudas sobre los requisitos puedes consultar el siguiente [link](https://docs.katalon.com/katalon-studio/supported-environments-for-katalon-studio-and-katalon-runtime-engine-kre#id_1) 

### Pasos de instalación

1. **Descargar Katalon Studio**:
   - Ve a la [página de descargas de Katalon Studio](https://www.katalon.com/download/).
   - Inicialmente aparecerá para descargar la versión Enterprise sin embargo tiene una duración de 30 días, nosotros instalaremos la versión free que se encuentra al final de la página.
   - Selecciona tu sistema operativo y descarga el archivo correspondiente.

2. **Instalar en Windows**:
   - Navega a la carpeta donde estes tus descargas y ejecuta `katalon.exe`.
   - Se abrirá un ventana indicando la descarga de recursos necesarios, espera hasta que finalice. 


3. **Instalar en macOS**:
   - Haz doble clic en el archivo descargado para continuar con la instalación.`.dmg`.
   - Arrastra Katalon Studio a la carpeta Aplicación cuando se le solicite.
   - Para iniciar Katalon Studio, hacer doble clic en la aplicación Katalon Studio.
   - Una vez iniciada, la aplicación debería mostrar una pantalla de presentación.

4. **Instalar en Ubuntu**:

Antes de instalar, asegúrese de configurar el entorno necesario para Katalon Studio.

   - Instala OpenJDK 17 (NO Oracle JDK). Abre tu Terminal y escribe: 
   ```sh
   sudo apt-get install openjdk-17-jre
   ```
   - Una vez que finalice la instalación, su información se mostrará cuando ejecute el comando `java -version`
   - Si tiene varias versiones de OpenJDK instaladas en su Ubuntu y no se utiliza la versión correcta, utilice el comando `alternatives` para cambiar entre ellas:
   ```sh
   sudo update-alternatives --config java //then choose the openjdk-8-jre option
   ```
   - Mas información sobre los pasos de instalación para otras distribuciones de Linux en el documento de OpenJDK [aquí](http://openjdk.java.net/install/)
   - Utilice el comando para extraer el archivo, por ejemplo: 
   ```sh
   .-xftar.gz$tar -xf Katalon_Studio_PE_Linux_64-8.5.5.tar.gz
   ```
   - En la carpeta extraída, puede encontrar la aplicación Katalon Studio. Abre Katalon Studio haciendo doble clic en Katalon Studio, o ejecútalo en tu Terminal.`cd ./katalon`

### Activación de Katalon Studio

1. Abre Katalon Studio.
2. Inicia sesión con tu cuenta de Katalon.
3. Si no tienes una cuenta, puedes registrarte en [Katalon TestOps](https://analytics.katalon.com/).

Para más detalles, consulta la [documentación oficial de Katalon Studio](https://docs.katalon.com/katalon-studio/get-started/install-katalon-studio).

## Ejemplos de uso

Este repositorio contiene ejemplos de uso de Katalon y JMeter para diferentes escenarios de testing. Explora las carpetas y archivos para más información.


