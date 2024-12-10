# Katalon-Y-JMeter
Repositorio que contiene pasos de instalación y configuración de las aplicaciones testing Katalon y JMeter

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
   Para instalar Appium, necesita Java. Por lo tanto, asegúrese de que Java esté instalado ingresando el siguiente comando:
   ```sh
   java --version
   ```
   - **Instalación via npm (Node Package Manager)**
   ```sh
   npm install -g appium
   ```
   - **Instalación de *uiautomator2***
   ```sh
   appium driver install uiautomator2
   ```     
   - **Verificación de Instalación**
   ```sh
   appium --version
   ```
   - Verificar si aparece el driver *uiatomator2*
   ```sh
   appium driver list --installed
   ``` 
3. Android Studio (funcionara como emulador de un dispositovo movil)

   - **Descargar:**
      * Ingresa a https://developer.android.com/studio
      * Descarga la última versión para tu sistema operativo
   
   - **Instalación:**
      * Ejecuta el instalador de Android Studio
      * Sigue el asistente de instalación
      * Durante la instalación, asegúrate de marcar las opciones:
         - Android SDK Build-Tools
         - Android SDK Platform-Tools
         - Android Emulator
         - Android Emulator hypervisor driver
        

   - **Configuración de Variables de Entorno**
      * **Variables Android:**
         - ANDROID_HOME: Ruta al SDK de Android
         - Ejemplo en Windows:
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
         - *Nota: Se recomienda agregar al PATH tanto del sistema como del usuario*
   - **Emuladores y Dispositivos**
      * Crear Dispositivo Virtual (AVD) en Android Studio:
         - Abre Android Studio
         - Selecciona "Tools" > "Virtual Device Manager"
         - Haz clic en "Create Virtual Device"
           
         <img src="https://github.com/user-attachments/assets/c5116664-b67a-4a2c-8b3a-2486a9acd98d" width="200" height="auto">
      * Configurar una apk de prueba
        - Incicializar el dispotivo creado en el paso anterior y instalar el apk de prueba: **APIDemos.apk**
        - Abrir Katalon Studio y seleccionar crear un nuevo proyecto
        - En las opciones que se despliegan, colocar el nombre, el tipo de dispositivo en donde se realizaran las pruebas en este caso *movil* y la ruta donde quiere que se guarde el proyecto
        - En la barra de opciones existe el siguiente icono:
           <img src="https://github.com/user-attachments/assets/fa7e24f1-5123-4ac7-ae70-03534a49666d" width="50" height="auto">
          Presionamos y seleccionamos *Android Devices*
        - Si al iniciar nos pregunta si queremos descargar recursos para Android SDK le damos que sí.
        - Devemos vizualizar el nombre del emulador creado en *Device Name*. En *Application File* colocar el apk con la dirección en donde se encuentré en el directorio
        - Presionamos el boton *Start*, y tendriamos la herramienta lista para los casos de prueba

## Instalación de JMeter

Estos son los pasos detallados para instalar, configurar y usar **Apache JMeter** para pruebas de rendimiento y carga. Abarca los requisitos del sistema, las instrucciones de instalación y un ejemplo de creación y ejecución de un plan de prueba básico.

---

### 1. Requisitos del sistema

Para instalar y usar JMeter, asegúrese de que su sistema cumpla con los siguientes requisitos:

#### Hardware
- **RAM**: Mínimo 2 GB (se recomiendan 4 GB o más para pruebas grandes).
- **Espacio en disco**: Al menos 500 MB libres.

#### Software
- **Sistema operativo**: Compatible con Windows, macOS y Linux.
- **Java**: Java Development Kit (JDK) versión 8 o superior.
- [Descargar JDK](https://www.oracle.com/java/technologies/javase-downloads.html).

---

### 2. Instalación de JMeter

#### Paso 1: Descargar Apache JMeter
1. Visita el sitio web oficial de JMeter: [https://jmeter.apache.org/](https://jmeter.apache.org/).
2. Descarga la última versión **binaria** estable como archivo ZIP.

#### Paso 2: Instalar JMeter
1. Extrae el archivo ZIP en tu directorio preferido (por ejemplo, `C:\apache-jmeter` o `/usr/local/apache-jmeter`).
2. Navega hasta la carpeta extraída para verificar su estructura:
- `bin`: Contiene scripts para iniciar JMeter.
- `lib`: Contiene bibliotecas y complementos.

---

### 3. Configuración de JMeter

#### Paso 1: Configurar Java
1. Verificar la instalación de Java:
```bash
java -version
```
2. Si Java no está instalado, descargue e instale el JDK.
3. Configure la variable de entorno JAVA_HOME:
- Windows:
   * Vaya a "Este equipo > Propiedades > Configuración avanzada del sistema > Variables de entorno".
   * Agregue:
   * Nombre: JAVA_HOME
   * Valor: Ruta a la carpeta JDK (p. ej., C:\Program Files\Java\jdk-17.
- Linux/macOS: Agregue a .bashrc o .zshrc:
   ```bash
   export JAVA_HOME=/path/to/jdk
   export PATH=$JAVA_HOME/bin:$PATH
   ```
   * Reinicie la terminal o el símbolo del sistema.
#### Paso 2: Inicie JMeter
1. Navegue a la carpeta bin en el directorio en el que descargo JMeter.
- Ejecute:
   * Windows: Haga doble clic en **ApacheJMeter.bat**.
   * Linux/macOS: Ejecute ./jmeter en la terminal
