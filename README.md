# 💻🚀 Cómo CREAR un USB BOOTEABLE con RUFUS Paso a Paso (Guía Completa) 🔧✨

En esta guía, te explico **cómo crear un USB booteable utilizando Rufus** de manera sencilla. Asegúrate de que tu USB esté en buen estado, y si no tienes uno disponible, también puedes usar un **disco externo** o una partición de tu disco duro. ¡Sigue estos pasos y tendrás tu dispositivo booteable listo en minutos!

### Paso 1: DESCARGAR la aplicación RUFUS
1. Visita el [sitio oficial de Rufus](https://rufus.ie/) para descargar la última versión de la aplicación.
2. Descarga el ejecutable que no requiere instalación (`Rufus Portable`).

> [!TIP]
> Todas las versiones de **Rufus** son portátiles, lo que significa que no requieren instalación y puedes ejecutarlas directamente desde tu equipo. Sin embargo, si descargas la versión que tiene una **"P"** al final del nombre del archivo (por ejemplo, **rufus-4.5p**), estarás obteniendo una especie de **versión Insider**. Esta versión te permite probar opciones experimentales que no están disponibles en las versiones regulares.

### Paso 2: EJECUTAR la aplicación RUFUS
1. Abre la aplicación descargada (no requiere instalación).
2. Al abrir Rufus por primera vez, aparecerá un cuadro de **política de actualización**. Aquí puedes optar por permitir que Rufus verifique automáticamente actualizaciones futuras:
   - Elige **Sí** para permitir que Rufus busque actualizaciones.
   - Rufus también puede descargar directamente la **ISO de Windows** desde la aplicación si lo necesitas.

> [!IMPORTANT]
> Asegúrate de estar conectado a Internet para que Rufus pueda verificar actualizaciones y descargar la ISO en caso de ser necesario.

### Paso 3: SELECCIONAR el dispositivo USB o DISCO EXTERNO
1. En la opción **Dispositivo**, selecciona la unidad USB que quieres convertir en booteable. Si no tienes un USB disponible, también puedes usar un **disco externo** o una **partición** del disco duro de tu PC.
   - Asegúrate de seleccionar la unidad correcta, ya que los datos de la unidad serán eliminados.

#### Requisitos para el uso de un DISCO EXTERNO o PARTICIÓN:
- **Disco Externo**: Debe tener suficiente espacio libre (al menos 8 GB) y estar formateado en **NTFS** o **FAT32**.
- **Partición del Disco**: Debe ser una partición vacía con al menos 8 GB de espacio libre, y debe estar formateada en **NTFS** o **FAT32**. Lo ideal es que sea una partición independiente del sistema operativo.

> [!NOTE]
> Si no cuentas con un USB, puedes usar un disco externo o partición siempre y cuando cumplan con los requisitos de espacio y formato.

### Paso 4: VERIFICAR el estado del USB o DISCO EXTERNO
Es recomendable que el **USB** o **disco externo** que vayas a usar esté en buen estado. Para verificar el estado de tu dispositivo, puedes usar herramientas como **[H2testw](https://h2testw.org/)**, **[CrystalDiskInfo](https://crystalmark.info/en/software/crystaldiskinfo/)**, o la herramienta de **NirSoft** llamada **[USBDeview](https://www.nirsoft.net/utils/usb_devices_view.html)**:
- **[H2testw](https://h2testw.org/)**: Verifica si tu USB tiene sectores dañados.
- **[CrystalDiskInfo](https://crystalmark.info/en/software/crystaldiskinfo/)**: Comprobar el estado de salud de tu disco duro.
- **[USBDeview (NirSoft)](https://www.nirsoft.net/utils/usb_devices_view.html)**: Verifica el estado de tus dispositivos USB actuales y antiguos, asegurándote de que el USB funciona correctamente antes de crear la unidad booteable.

> [!WARNING]
> Es muy importante verificar el estado del USB o disco externo antes de proceder. Si el dispositivo tiene errores, es posible que el proceso de creación de la unidad booteable falle o no funcione correctamente.

### Paso 5: Configuración de ARRANQUE en RUFUS
1. En la opción **Elección de arranque**, deja la opción predeterminada: **Disco o imagen de ISO (Elija por favor)**.
2. Haz clic en el botón **Seleccionar** para buscar el archivo **ISO** del sistema operativo que has descargado (por ejemplo, Windows 10 o Linux).

> [!NOTE]
> Al hacer clic en **Seleccionar**, aparecerá una **flecha** junto a la opción. Si la presionas, verás la opción **Descargar**, la cual te permitirá obtener la imagen ISO directamente desde los **enlaces oficiales de Microsoft**. Al elegir descargar, se abrirá una ventana en la que podrás **configurar la imagen de Windows** que deseas descargar (por ejemplo, elegir la edición y versión de Windows).

#### Verificar la ISO con SHA:
- Al lado del botón **Seleccionar** hay un **icono de un círculo**, que te permite realizar un **Benchmark** o verificación de la imagen ISO seleccionada. Rufus calculará el **hash SHA-1 o SHA-256** de la ISO, lo cual es útil para comprobar la integridad de la imagen y asegurarte de que es auténtica.

#### Opciones de arranque explicadas:
- **Disco o imagen de ISO (Elija por favor)**: Te permite seleccionar un archivo ISO que contiene un sistema operativo (Windows, Linux, etc.).
- **MS-DOS**: Rufus creará un USB con el sistema operativo MS-DOS, útil para ejecutar programas antiguos o hacer actualizaciones de firmware.
- **FreeDOS**: Alternativa libre a MS-DOS, usado para tareas como actualizaciones de BIOS o ejecutar programas DOS.

> [!TIP]
> Asegúrate de haber descargado la imagen ISO correcta para el sistema operativo que deseas instalar o ejecutar.

### Paso 6: OPCIONES DE IMAGEN (solo para ISOs de Windows)
Si seleccionas una imagen ISO de **Windows**, Rufus mostrará una opción adicional llamada **Opciones de imagen**. Esta opción tiene dos modalidades:

- **Instalación estándar de Windows**: Esta opción crea un USB booteable para instalar Windows como lo harías normalmente. Se utiliza en instalaciones limpias o actualizaciones de sistemas operativos.
  
> [!TIP]
> Elige esta opción si deseas hacer una instalación completa de Windows en una PC.

- **Windows To Go**: Esta opción permite crear un USB con una versión portátil de Windows que se puede ejecutar directamente desde la unidad USB, sin necesidad de instalar el sistema operativo en el disco duro de la PC. Es ideal si necesitas llevar tu entorno de Windows contigo y ejecutarlo en cualquier computadora compatible.

#### Requisitos para Windows To Go:
- Un **USB** o **disco externo** con al menos **32 GB de espacio**.
- El dispositivo de almacenamiento debe ser de alta velocidad, preferiblemente un **USB 3.0** o superior para un rendimiento adecuado.
- Solo funciona con **versiones empresariales de Windows** (Windows 8, 8.1 y 10 Enterprise), aunque Rufus permite utilizar otras versiones no oficialmente soportadas.
  
> [!NOTE]
> **Windows To Go** no está diseñado para instalarse en discos duros y no se actualiza como una instalación estándar de Windows.

> [!IMPORTANT]
> Para la mayoría de los usuarios, es recomendable seleccionar **Instalación estándar de Windows**, ya que te permitirá instalar Windows en una PC de la manera tradicional.

### Paso 7: SELECCIONAR el ESQUEMA de partición y SISTEMA de destino
1. **Esquema de partición**: Selecciona el esquema correcto según tu equipo:
   - **GPT**: Para sistemas modernos con UEFI.
   - **MBR**: Para sistemas más antiguos con BIOS.
2. **Sistema de destino**: Selecciona:
   - **UEFI (sin CSM)**: Para equipos modernos.
   - **BIOS o UEFI-CSM**: Para sistemas más antiguos.

### Paso 8: Configuración avanzada de FORMATO y PROPIEDADES de la unidad
1. **Propiedades avanzadas de la unidad**: Ajusta las opciones avanzadas solo si es necesario.
2. **Etiqueta de volumen**: Cambia el nombre de la unidad si lo prefieres.
3. **Sistema de archivos**: Usa **NTFS** para Windows o **FAT32** si necesitas compatibilidad adicional.
4. **Tamaño del clúster**: Deja la opción en **predeterminado**, a menos que se indique lo contrario.

> [!IMPORTANT]
> No modifiques las opciones avanzadas de formato a menos que tengas conocimientos específicos. Las configuraciones predeterminadas funcionan bien para la mayoría de los usuarios.

### Paso 9: Iniciar la CREACIÓN del USB BOOTEABLE
1. Verifica en la sección de **Estado** que todo está listo.
2. Haz clic en **Empezar**. 

#### Configuración adicional de Windows:
- Cuando hagas clic en **Empezar**, aparecerá una ventana que te permitirá configurar opciones avanzadas de instalación de Windows, como:
  - **Deshabilitar la telemetría**.
  - **Omitir BitLocker**.
  - Entre otras opciones. Si no necesitas modificar estas configuraciones, puedes dejarlas por defecto.
  
  Después de confirmar tus preferencias, aparecerá un mensaje que te pedirá **formatear el USB**. Haz clic en **Sí** para continuar, y comenzará el proceso de creación del USB booteable.

#### Configuración adicional para Linux:
- Si estás creando un USB booteable de **Linux**, al presionar **Empezar**, aparecerá una ventana llamada **Imagen ISO Hybrid** con dos opciones:
  - **Escribir en imagen ISO (Recomendada)**: Elige esta opción.
  - **Escribir en imagen DD**: Solo si lo requiere la imagen.
  
> [!IMPORTANT]
> Una vez seleccionada la opción, aparecerá una ventana para confirmar la descarga de **linuxsys**. Presiona **Sí** para descargar los archivos adicionales y luego comenzará la instalación.

### Paso 10: Arrancar desde el USB BOOTEABLE
1. Una vez finalizado el proceso, reinicia tu computadora.
2. Para iniciar desde el USB booteable:
   - Presiona **F8** (o la tecla correspondiente) durante el arranque para abrir el **menú de arranque**.
   - Selecciona la unidad USB que acabas de crear.

   - Si no ves la opción del USB, entra en la **BIOS**:
     - Reinicia la PC y presiona la tecla para acceder a la **BIOS** (generalmente F2, Esc o Supr).
     - Ve a la **Configuración de arranque** y selecciona el **USB booteable** como la **unidad principal** para que el sistema arranque automáticamente desde esa unidad.

> [!NOTE]
> La tecla para acceder a la BIOS o el menú de arranque puede variar según la marca de tu equipo, así que consulta la documentación de tu computadora si no sabes cuál es.

### ¡Todo Listo!
Una vez que tu PC arranque desde el **USB booteable** o **disco externo**, podrás instalar el sistema operativo sin problemas.

- **[Ver todas las versiones de Rufus](https://rufus.ie/downloads/)**: Consulta todas las versiones lanzadas de Rufus y descarga la que necesites.
- **[Repositorio en GitHub](https://github.com/pbatard/rufus)**: Consulta el repositorio oficial de Rufus para más información y actualizaciones.

---

## Licencia

 Este proyecto se encuentra bajo la licencia [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Consulta el archivo `LICENSE` para más detalles.

© 2024 tweakstech
