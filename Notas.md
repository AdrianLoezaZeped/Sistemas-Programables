# Sistemas Programables
Es un dispositovo electronico diseñado para controlar y automatizar procesos industriales
* Se basan en un software programable
* Facilidad de programacion
* Robuztez
* Flexibilidad
* Integridad

## PLC
Se desarollaron 1970, es una herramienta esencial que trabaja con micros utilizando logica boolena, por ejemplo se utiliza en los semanforos, hornos de microondas, alertas, sensor de movimiento.
Se pueden programar y reprogramar muy facilmente, son compactos y potentes

![MONOGRAFICO: Lenguajes de programación - Principios básicos de PLC |  Observatorio Tecnológico](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQRb_12VkocjMgk-QvllVoh_bk1Xu3T7oiVVw&s)

Diagrama de un PLC

Es importante saber el proceso de lo que se va realizar para poder trabajar en cualquier proceso para poder automatizar

## Arduino
Arduino es una plataforma de desarrollo basada en una placa electrónica de hardware libre que incorpora un microcontrolador re-programable y una serie de pines hembra. Estos permiten establecer conexiones entre el microcontrolador y los diferentes sensores y actuadores de una manera muy sencilla (principalmente con cables dupont).
Una placa electrónica es una PCB (“Printed Circuit Board”, “Placa de Circuito Impreso” en español). Las PCBs superficies planas fabricadas en un material no conductor, la cual costa de distintas capas de material conductor. Una PCB es la forma más compacta y estable de construir un circuito electrónico. Por lo tanto, la placa Arduino no es más que una PCB que implementa un determinado diseño de circuitería interna. De esta forma el usuario final no se debe preocupar por las conexiones eléctricas que necesita el microcontrolador para funcionar, y puede empezar directamente a desarrollar las diferentes aplicaciones electrónicas que necesite.
De 7 a 12 volts si no se quema 
## Sensores 
Es un dispositivo que detecta una variable para convertirlos en voltaje o corriente
* Deteccion de estimulos (Cambios de entorno)
* Conversion de energia (Senales electricas)
* Procesamiento (Acondicionadores de senal)

### Sensores Analogicos
Los sensores analógicos son dispositivos que miden magnitudes físicas, como la temperatura o la presión, y emiten una señal eléctrica continua que varía de forma proporcional a la cantidad que se está midiendo. A diferencia de los sensores digitales, que emiten valores discretos, los analógicos proporcionan un rango continuo de valores, lo que permite una medición detallada y sensible a los cambios en el entorno. 
### Sensores Digitales
Un sensor digital es un dispositivo electrónico o electroquímico que detecta un cambio en el entorno y lo convierte en una señal digital, es decir, en valores discretos (como ceros y unos) que pueden ser fácilmente procesados por microcontroladores y sistemas informáticos. A diferencia de los sensores analógicos, que entregan datos continuos, los sensores digitales proporcionan mediciones precisas y fiables en formato binario, con interfaces de comunicación estándar como I2C, SPI o UART para una fácil integración. 
Características principales
* Salida discreta y cuantizada:
Generan valores de salida finitos y cuantificados, usualmente en código binario, lo que los hace ideales para sistemas digitales. 
* Alta precisión y exactitud:
Ofrecen mediciones muy fiables y coherentes, lo que es crucial para aplicaciones donde la integridad de los datos es fundamental. 
* Procesamiento de señales digital:
Muchos sensores digitales incluyen funciones de procesamiento de señales directamente en su interior. 
* Compatibilidad con microcontroladores:
Son ideales para su uso con microcontroladores y sistemas digitales, facilitando su integración. 
* Interfaces de comunicación:
Suelen contar con interfaces de comunicación como I2C, SPI o UART, lo que permite conectarlos fácilmente a otros dispositivos digitales. 

## PWM
Controlar la cantidad de energia entregada a un dispositivo, como un LED. En arduino se utiliza prar regular el brillo del LED sin necesidad de cambiar el voltaje de la fuerza da alimentacion
Pines Activados para PWM(3,5,6,9,10,11)
### Ejemplo de encender 1 pin gradualmente
<img width="664" height="754" alt="image" src="https://github.com/user-attachments/assets/85f048d5-0848-4a78-af6c-503c588eb912" />

```
int led = 3;
int time = 1000;

int niveles[] = {0, 64, 128, 192, 255, 192, 128, 64, 0}; 

void setup() {
  pinMode(led, OUTPUT);
}

void loop() {
  for (int i = 0; i < 9; i++) {   
    analogWrite(led, niveles[i]);
    delay(time);
  }
}
```



