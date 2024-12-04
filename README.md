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

    Antes de instalar, asegúrate de configurar el entorno necesario para Katalon Studio.

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

1. Registrate en [Katalon TestOps](https://analytics.katalon.com/)
1. Abre Katalon Studio.
2. Inicia sesión con tu cuenta de Katalon.

Para más detalles, consulta la [documentación oficial de Katalon Studio](https://docs.katalon.com/katalon-studio/get-started/install-katalon-studio).

### Requisitos para Pruebas de Aplicaciones Móviles

Si bien ya con los pasos anteriores podriamos usar Katalon para aplicaciones web, en esta oportunidad tambien se va a usar la herramieta para aplicaciones moviles,
es por ello que se necesita los siguientes requisitos:

1. **NodeJs**
   - **Versión Recomendada:** Node.js 12.x o superior
   - **Descargar e Instalar:**
      * Visita el sitio web oficial de Node.js: https://nodejs.org/ 
      * Selecciona la versión LTS (Long Term Support)
      * Sigue el asistente de instalación para tu sistema operativo
   - **Verificación de Instalación:**
      ```sh
      node --version
      npm --version
      ```
2. **APPIUM**
   
   Katalon utiliza la biblioteca de código abierto Appium. Entonces, después de instalar con éxito node.js, el siguiente paso es instalar Appium.
   Para instalar Appium, necesita Java. Por lo tanto, asegúrese de que Java esté instalado en el servidor ingresando el siguiente comando:
   ```sh
   java --version
   ```
   - **Instalación via npm (Node Package Manager)**
   ```sh
   npm install -g appium
   ```
   - **Verificación de Instalación**
   ````sh
   appium --version
   ```
3. Android Studio (funcionara como emulador de un dispositovo movil)

   - **Descargar:**
      * Ingresa a https://developer.android.com/studio
      * Descarga la última versión para tu sistema operativo
   
   - **Instalación:**
      * Ejecuta el instalador de Android Studio
      * Sigue el asistente de instalación
      * Durante la instalación, asegúrate de marcar las opciones:
         Android SDK
         Android SDK Platform
         Android Virtual Device (AVD)

   - **Configuración de Variables de Entorno**
      * **Variables Android:**
         ANDROID_HOME: Ruta al SDK de Android
         Ejemplo en Windows:
         ```sh
         Variable: ANDROID_HOME
         Valor: C:\Users\[TuNombre]\AppData\Local\Android\Sdk
         ```
      * **Agregar al PATH:**
         ```sh
         %ANDROID_HOME%\platform-tools
         %ANDROID_HOME%\tools
         %ANDROID_HOME%\tools\bin
         ```
   - **Emuladores y Dispositivos**
      * Crear Dispositivo Virtual (AVD) en Android Studio:
         - Abre Android Studio
         - Selecciona "Tools" > "AVD Manager"
         - Haz clic en "Create Virtual Device"
         - Elige un dispositivo y una imagen del sistema
         - Configura las características del dispositivo virtual

## Creación y ejecución de un caso de prueba de Android en Katalon Studio

Este repositorio contiene ejemplos de uso de Katalon y JMeter para diferentes escenarios de testing. Explora las carpetas y archivos para más información.


