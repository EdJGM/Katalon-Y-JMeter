# JMeter
# Guía de Instalación de JMeter

Esta guía te ayudará a instalar Apache JMeter en tu sistema utilizando un archivo comprimido proporcionado para asegurar que todos tengan la misma versión. La ruta de instalación será `C:/JMeter`.

## Requisitos Previos

- Asegúrate de tener Java instalado en tu sistema. JMeter requiere Java para ejecutarse. Puedes descargar e instalar Java desde [aquí](https://www.oracle.com/java/technologies/javase-downloads.html).

## Pasos de Instalación

1. **Descargar el Archivo Comprimido de JMeter:**
    - Asegúrate de tener el archivo comprimido de JMeter que se ha proporcionado.

2. **Crear el Directorio de Instalación:**
    - Crea un directorio en `C:/` llamado `JMeter`. Puedes hacerlo manualmente o utilizando el siguiente comando en la terminal:
      ```sh
      mkdir C:/JMeter
      ```

3. **Extraer el Archivo Comprimido:**
    - Extrae el contenido del archivo comprimido de JMeter en el directorio `C:/JMeter`. Puedes utilizar herramientas como WinRAR, 7-Zip, o el comando de extracción de Windows.

4. **Configurar las Variables de Entorno:**
    - Añade la ruta `C:/JMeter/bin` a la variable de entorno `PATH` para que puedas ejecutar JMeter desde cualquier lugar en la línea de comandos.
      - En Windows 10:
         1. Abre el Panel de Control.
         2. Ve a Sistema y Seguridad > Sistema.
         3. Haz clic en "Configuración avanzada del sistema".
         4. En la pestaña "Opciones avanzadas", haz clic en "Variables de entorno".
         5. En "Variables del sistema", selecciona la variable `Path` y haz clic en "Editar".
         6. Añade `C:/JMeter/bin` al final de la lista y guarda los cambios.

5. **Verificar la Instalación:**
    - Abre una terminal y ejecuta el siguiente comando para verificar que JMeter se ha instalado correctamente:
      ```sh
      jmeter -v
      ```
    - Deberías ver la versión de JMeter y otra información relacionada.

## Ejecutar JMeter

- Para iniciar JMeter en modo GUI, simplemente ejecuta el siguiente comando en la terminal:
  ```sh
  jmeter
  ```

¡Y eso es todo! Ahora tienes Apache JMeter instalado y listo para usar en tu sistema.