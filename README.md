# Guía de Laboratorio: Puente Rectificador de Onda Completa con Diodos de Silicio

## Introducción

En este laboratorio, se analizará el comportamiento de un puente rectificador de onda completa utilizando cuatro diodos de silicio. Se determinará la forma de onda del voltaje de salida, se calcularán los valores promedio de voltaje, corriente y potencia en la resistencia de carga, y se analizará el efecto de un condensador en paralelo sobre el rizado del voltaje.

## Objetivos
1. Hallar analíticamente la forma de onda del voltaje de salida $\( v_o(t) \)$.
2. Calcular el voltaje promedio $\( V_o \)$, la corriente promedio $\( I_o \)$, y la potencia promedio $\( P \)$ en la resistencia de carga.
3. Determinar el rizado pico a pico del voltaje cuando se coloca un condensador de 47 µF en paralelo con la carga.

## Datos Iniciales
- **Señal de entrada**: 12 Vrms, frecuencia de 60 Hz
- **Resistencia de carga**: $\( R = 1 k\Omega \)$
- **Condensador en paralelo**: $\( C = 47 \mu F \)$

![image](https://github.com/user-attachments/assets/e6ce7c27-35e1-4a3a-a414-1158b7fa2d40)

---

## **Paso 1: Voltaje de Salida $\( v_o(t) \)$**

### Voltaje de Entrada $\( v_i(t) \)$:
- La señal de entrada es una onda senoidal de 12 Vrms y 60 Hz:
  ```math
  v_i(t) = 12 \cdot \sqrt{2} \cdot \sin(2\pi \cdot 60 \cdot t)
  ```
  
  Donde:
  ```math
  V_{peak} = 12 \cdot \sqrt{2} \approx 16.97 \, V
  ```

### Consideraciones del Puente Rectificador:
> [!TIP]
> - Los diodos de silicio presentan una caída de voltaje aproximada de 0.7 V.
> - En el puente rectificador, el voltaje de salida se obtiene restando la caída de voltaje de dos diodos:
  ```math
  v_o(t) \approx V_{peak} - 2 \cdot V_D = 16.97 \, V - 2 \cdot 0.7 \, V \approx 15.57 \, V_{peak}
  ```

### Forma de Onda de $\( v_o(t) \)$:
- La salida será una señal rectificada de onda completa, con un valor máximo de 15.57 V y una frecuencia de 120 Hz:
  ```math
  v_o(t) = |15.57 \cdot \sin(2\pi \cdot 120 \cdot t)|
  ```

---

## **Paso 2: Cálculos Promedios**

### Voltaje Promedio $\( V_o \)$:
El voltaje promedio en un rectificador de onda completa es:
```math
V_o = \frac{2 \cdot V_{peak}}{\pi}
```
Sustituyendo $\( V_{peak} = 15.57 \, V \)$:
```math
V_o = \frac{2 \cdot 15.57 \, V}{\pi} \approx 9.92 \, V
```

### Corriente Promedio $\( I_o \)$:
La corriente promedio se obtiene por la Ley de Ohm:
```math
I_o = \frac{V_o}{R}
```
Donde $\( R = 1 k\Omega \)$:
```math
I_o = \frac{9.92 \, V}{1 k\Omega} \approx 9.92 \, mA
```

### Potencia Promedio $\( P \)$:
La potencia promedio en la resistencia de carga es:
```math
P = V_o \cdot I_o = 9.92 \, V \cdot 9.92 \, mA \approx 98.4 \, mW
```

---

## **Paso 3: Cálculo del Rizado Pico a Pico**

Cuando se añade un condensador de 47 µF en paralelo con la carga, el rizado del voltaje puede calcularse con:
```math
V_{rizado(pp)} = \frac{I_o}{f \cdot C}
```
Donde:
- $\( I_o = 9.92 \, mA \)$
- $\( f = 120 \, Hz \)$
- $\( C = 47 \mu F \)$

> [!WARNING]
> - La frecuencia del rizado de voltaje es del doble de la señal  $\( V_o \)$.
> - De la ecuación para $V_{rizado(pp)}$, a mayor capacidad del condensador, menor rizado de voltaje (inversamente proporcional).

Sustituyendo los valores:
```math
V_{rizado(pp)} = \frac{9.92 \, mA}{120 \cdot 47 \mu F} \approx 1.76 \, V
```

---

## **Resumen de Resultados**

1. **Voltaje de salida promedio**: $\( V_o = 9.92 \, V \)$
2. **Corriente promedio**: $\( I_o = 9.92 \, mA \)$
3. **Potencia promedio**: $\( P = 98.4 \, mW \)$
4. **Rizado pico a pico** con $\( C = 47 \mu F \)$: $\( V_{rizado(pp)} \approx 1.76 \, V \)$

> [!TIP]
> Este análisis incluye los cálculos fundamentales para un puente rectificador de onda completa, con especial atención en la forma de onda del voltaje de salida, los valores promedios y el efecto de un condensador sobre el rizado.


## **¿Cómo es el comportamiento de la corriente en los diodos con el efecto del condensador sobre el rizado?**
1. Únicamente circula corriente por los diodos en el tiempo de carga del condensador de $\( C = 47 \mu F \)$.
2. El tiempo de carga se presenta entre el $\( V_{rizado(máximo)} =15.57 \, V \)$ y  $\( V_{rizado(mínimo)} = 13.89 \, V \)$. Es decir, el tiempo que tarda la senoidal en ir de $\(13.89 \, V \ )$ a $\(15.57 \, V \ )$.
3. Los diodos y el secundario del transformador presentan corrientes de pico repetitiva.
4. ¿Cómo calcular el pico de corriente por los diodos?

