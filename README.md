# 🔍 Pen Drives y Escáneres

## 💾 I. El Pen Drive (Unidad de Almacenamiento Flash)

<img width="750" height="750" alt="image" src="https://github.com/user-attachments/assets/64e16606-dd18-4193-ac33-0963c202e08a" />

### 1. Definición Técnica
Un **Pen Drive** es un dispositivo de almacenamiento masivo que utiliza **memoria flash tipo NAND** para retener datos. A diferencia de los discos duros mecánicos (HDD), no posee partes móviles, lo que lo clasifica como un dispositivo de **estado sólido (SSD)** en miniatura.

Utiliza el estándar **USB (Universal Serial Bus)** para comunicarse con otros sistemas, permitiendo la lectura y escritura de datos mediante impulsos eléctricos que atrapan electrones en celdas de transistores de puerta flotante.



### 2. Componentes Internos
* **Conector USB Macho:** Provee la interfaz física de conexión.
* **Controlador de Almacenamiento:** El "cerebro" que gestiona la comunicación y el desgaste de la memoria.
* **Chip de Memoria Flash NAND:** Donde se guardan físicamente los bits.
* **Oscilador de Cristal:** Controla el flujo de datos mediante una señal de reloj.

### 3. Evolución y Velocidades
| Estándar | Nombre Comercial | Velocidad Teórica | Uso Recomendado |
| :--- | :--- | :--- | :--- |
| **USB 2.0** | High Speed | 480 Mbps | Teclados, ratones, documentos pequeños. |
| **USB 3.0/3.1** | SuperSpeed | 5 - 10 Gbps | Transferencia de archivos multimedia y copias de seguridad. |
| **USB 4.0** | Next Gen | Hasta 40 Gbps | Edición de video en tiempo real y estaciones de trabajo. |

### 4. Usos Avanzados
* **Sistemas Live (Booteo):** Instalar sistemas operativos (Linux, Windows) desde el USB.
* **Encriptación de Datos:** Uso de unidades con cifrado por hardware (AES-256) para seguridad bancaria o gubernamental.
* **ReadyBoost:** Uso de la memoria flash para ayudar a la memoria RAM en sistemas antiguos.

# 🛠️ Dispositivos BadUSB (Keystroke Injection)

Guía rápida sobre herramientas de hardware hacking para inyección de pulsaciones de teclas.

---

## 1. ¿Qué es un BadUSB?
A diferencia de un pendrive normal, un **BadUSB** es un dispositivo que se anuncia ante el sistema operativo como un **teclado (HID)**. Debido a que las computadoras confían intrínsecamente en los teclados, el dispositivo puede "teclear" comandos maliciosos a una velocidad increíble.

> [!CAUTION]
> **Diferencia Crítica:** No confundir con **Docker**. Docker es para contenedores de software; BadUSB es hardware para acceso físico inicial.

---

## 2. Tipos de Hardware Comunes

| Dispositivo | Descripción | Nivel de Precio |
| :--- | :--- | :--- |
| **USB Rubber Ducky** | El estándar de Hak5. Usa MicroSD y Ducky Script. | $$$ |
| **Digispark (ATtiny85)** | Microcontrolador económico programable con Arduino IDE. | $ |
| **Flipper Zero** | Herramienta multiusos con función BadUSB integrada. | $$$$ |
| **Raspberry Pi Pico** | Muy potente, emula teclado/ratón con CircuitPython. | $$ |



---

## 3. Mecanismo de Funcionamiento

1. **Identificación:** El PC lo reconoce como un dispositivo de interfaz humana (HID).
2. **Payload (Carga útil):** El script con instrucciones predefinidas.
3. **Ejecución:** Al conectarse, el USB "escribe" el script automáticamente saltándose restricciones visuales por su velocidad.

---


## 📑 II. El Escáner (Digitalizador de Imágenes)

<img width="500" height="271" alt="image" src="https://github.com/user-attachments/assets/dbb7fd02-2719-4b7f-be92-9161aa0d5d1c" />


### 1. Definición Técnica
El **Escáner** es un periférico de entrada que utiliza la **optoelectrónica** para convertir información analógica (papel, fotografías, objetos 3D) en un mapa de bits digital. Este proceso se basa en la captura de la luz reflejada mediante sensores fotosensibles.



### 2. El Proceso de Digitalización
1.  **Iluminación:** Una fuente de luz (LED o Xenón) barre el documento.
2.  **Reflexión:** La luz rebota en el papel y es dirigida mediante espejos hacia un sensor.
3.  **Conversión:** El sensor (**CCD** o **CIS**) transforma la intensidad de la luz en señales eléctricas.
4.  **Procesamiento:** Un conversor Analógico-Digital (ADC) traduce esas señales en píxeles.

### 3. Tipos y Aplicaciones
* **Escáner de Cama Plana:** El estándar para documentos de oficina y fotos.
* **Escáner de Tambor:** Utilizado en la industria de impresión de alta gama por su extrema resolución.
* **Escáner de Gran Formato:** Para planos de arquitectura e ingeniería.
* **Escáner 3D:** Utiliza láseres para mapear la geometría de objetos físicos para su posterior impresión 3D o diseño CAD.

### 4. Conceptos de Calidad
* **DPI (Puntos por pulgada):** Define la nitidez. Un escaneo estándar usa 300 DPI, mientras que uno fotográfico profesional supera los 1200 DPI.
* **Profundidad de Color:** Medida en bits; determina cuántos millones de colores puede reconocer el dispositivo.
* **OCR (Reconocimiento Óptico de Caracteres):** Software que analiza la imagen escaneada para identificar letras y convertirlas en texto editable (Word/PDF).

---

## 🔄 III. Integración en el Flujo de Trabajo

La combinación de ambos dispositivos crea un ciclo de gestión documental eficiente:

1.  **Captura (Input):** El escáner digitaliza un archivo físico, eliminando la necesidad de papel.
2.  **Procesamiento:** El ordenador optimiza el archivo (compresión, corrección de color).
3.  **Distribución (Output/Storage):** El **Pen Drive** actúa como el vehículo físico que permite trasladar esa información a entornos "Air-gapped" (sin conexión a red) o entregas físicas seguras.

> **Dato Curioso:** Un pen drive de 64GB puede almacenar aproximadamente 2 millones de documentos escaneados en formato PDF estándar.

---


## 🛠️ Buenas Prácticas y Mantenimiento

* **Para el Pen Drive:** Siempre usar la opción "Expulsar de forma segura" para evitar la corrupción de la tabla de archivos (FAT32/NTFS).
* **Para el Escáner:** Limpiar el cristal con paños de microfibra y evitar productos abrasivos que puedan rayar la superficie, lo que causaría líneas permanentes en los escaneos.

---

## 🎯 III. Conclusiones

Tras analizar ambos dispositivos, se pueden extraer las siguientes conclusiones:

1.  **Sinergia Digital:** El escáner y el pen drive forman un ecosistema cerrado de "captura y transporte". Mientras uno digitaliza la realidad, el otro la hace móvil y accesible fuera de la red.
2.  **Obsolescencia del Papel:** La evolución de los escáneres con tecnología **OCR** ha permitido que las empresas migren a oficinas "sin papel", mejorando la eficiencia y la ecología.
3.  **Fiabilidad:** La transición de soportes ópticos (CD/DVD) a memorias flash (Pen Drives) ha aumentado drásticamente la durabilidad de la información almacenada frente a daños físicos.
4.  **Seguridad:** En la era de la nube, el uso combinado de estos periféricos sigue siendo la forma más segura de transferir información confidencial en entornos "Air-gapped" (sin conexión a internet) para evitar ciberataques.

---

## 📚 Fuentes y Referencias

La información presentada en este repositorio ha sido recopilada y verificada a través de las siguientes fuentes técnicas:

* **USB Implementers Forum (USB-IF)**
* **IEEE (Institute of Electrical and Electronics Engineers)**
* **TWAIN Working Group** 
* **Especificaciones de Fabricantes** 
   
**Creado por Antonio Montaño Herrera**
