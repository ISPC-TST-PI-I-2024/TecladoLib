# TecladoLib

## Descripción

**TecladoLib** es una librería para el control y manejo de un teclado matricial 4x3 utilizando un ESP32. Esta librería permite una fácil integración del teclado en proyectos de Arduino y proporciona funciones sencillas para leer las teclas presionadas y realizar acciones en consecuencia.

## Características

- Soporte para teclados matriciales 4x3.
- Configuración flexible de pines.
- Fácil integración con proyectos basados en ESP32.
- Lectura eficiente de teclas presionadas, con soporte para todas las combinaciones de filas y columnas.
- Ejemplos incluidos para facilitar la puesta en marcha.

## Instalación

Para instalar esta librería en tu proyecto de PlatformIO:

1. Clona o descarga este repositorio en la carpeta `lib` de tu proyecto de PlatformIO.
2. Asegúrate de que los archivos `teclado.h` y `teclado.cpp` están ubicados en `lib/TecladoLib/src/`.
3. Incluye la librería en tu código con:
   ```cpp
   #include <teclado.h>
   ```
 ## Uso
**Inicialización**  
Para utilizar la librería, primero debes crear un objeto de la clase `Teclado` y configurar los pines de las filas y columnas del teclado. Por ejemplo:
```cpp
#include <Arduino.h>
#include "teclado.h"

// Configura los pines de las filas y columnas
Teclado teclado(34, 35, 32, 33, 25, 26, 27);

void setup() {
    Serial.begin(115200);
    teclado.iniciar();  // Inicializa el teclado
}

void loop() {
    char tecla = teclado.leerTecla();  // Lee la tecla presionada
    if (tecla) {  // Si se presionó una tecla
        Serial.print("Tecla presionada: ");
        Serial.println(tecla);
    }
}  
```
## Ejemplos  
Ejemplos adicionales se pueden encontrar en la carpeta examples, que demuestran cómo utilizar la librería en diferentes escenarios.  

## Documentación  
Para más detalles sobre la librería y su funcionamiento interno, consulta la documentación disponible en la carpeta docs. Aquí encontrarás:  

- [] README.md: Este archivo, que proporciona una visión general de la librería.  
- [] USAGE.md: Instrucciones detalladas y ejemplos de uso.  
- [] TECHNICAL_DETAILS.md: Detalles técnicos sobre la implementación y funcionamiento interno de la librería.  

## Contribución
Contribuciones a TecladoLib son bienvenidas. Si deseas agregar nuevas funcionalidades, mejorar el código existente o corregir errores, por favor, sigue estos pasos:

- Haz un fork del repositorio.
- Crea una rama para tu nueva característica (git checkout -b feature/nueva-caracteristica).
- Realiza tus cambios y haz commit (git commit -am 'Agrega nueva característica').
- Haz push de la rama (git push origin feature/nueva-caracteristica).
- Abre un Pull Request.  

## Licencia  
Este proyecto está licenciado bajo la Licencia MIT. Para más detalles, consulta el archivo LICENSE.

## Autores  
TecladoLib ha sido desarrollada por @Gona79. Para contacto o consultas, puedes escribir a gv@gonaiot.com

