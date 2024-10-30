# Sistemas Eléctricos

Los sistemas eléctricos se podría describir como el flujo de corriente eléctrica a traves de un circuito de material conductor, es decir, que sis propiedades químicas de como la eléctronegatividad permita el flujo de electrónes a traves de su camino; existen diferentes magnitudes de tensión y cargas donde se utilizan diferentes elementos que integren un circuito pues no es lo mismo hacer refencia a una subestación que distribuye energía eléctrica en una planta a una bateria que alimenta un circuito con pulsador y resistencia para encender un led; estos elementos conectados entre si controlan y administran energía eléctrica de forma que pueden distribuirla y controlarla en diferentes formas y aplicaciones.

>🔑 *Estabilidad de Voltaje:* Cómo el sistema mantiene niveles de voltaje dentro de un rango aceptable frente a fluctuaciones en la demanda o generación.

>🔑 *Frecuencia de operación:* Las redes eléctricas deben operar a una frecuencia constante (por ejemplo, 50 o 60 Hz), y las variaciones pueden causar problemas en la operación de equipos.

>🔑 *Flujos de potencia:* Analiza cómo se distribuye la energía en una red y se optimiza para minimizar pérdidas y maximizar la eficiencia.

>🔑 *Control Automático y sistemas de contingencia:* Los sistemas eléctricos cuentan con dispositivos de control automático para ajustar voltaje, frecuencia y flujo de potencia en tiempo real, asegurando estabilidad en caso de fallos o picos de demanda.

>🔑 *Dinamicas de la generación:* Evalúa cómo el sistema reacciona ante cambios en la generación de energía (por ejemplo, variabilidad en la producción de fuentes renovables) y en la demanda (por ejemplo, consumo industrial o doméstico).


# 1. Circuito RLC

Las redes RLC son circuitos eléctricos compuestos por tres elementos básicos:

1. **Resistor (R)**: Limita el flujo de corriente y disipa energía en forma de calor.
2. **Inductor (L)**: Almacena energía en un campo magnético cuando la corriente fluye a través de él y se opone a cambios rápidos de corriente.
3. **Capacitor (C)**: Almacena energía en un campo eléctrico y se opone a cambios rápidos en el voltaje.

## Tipos de Circuitos RLC

Las redes RLC pueden ser configuradas en serie o en paralelo, con propiedades diferentes en cada caso:

**RLC en Serie**: Los componentes R, L y C están conectados uno tras otro. En esta configuración, la corriente que pasa por cada elemento es la misma. La impedancia total se calcula sumando las impedancias individuales:

  
  $$Z = R + j\omega L - \frac{j}{\omega C}$$

donde $$\omega$$ es la frecuencia angular $$\omega = 2\pi f$$.

**RLC en Paralelo**: Los componentes R, L y C están conectados en paralelo. En esta configuración, el voltaje a través de cada componente es el mismo, pero la corriente se divide. La admitancia total se calcula como la suma de las admitancias individuales:


$$Y = \frac{1}{R} + j\omega C - \frac{j}{\omega L}$$

## Comportamiento Dinámico y Frecuencia de Resonancia

Un aspecto importante de las redes RLC es su frecuencia de resonancia $$(f_0\)$$, que ocurre cuando la impedancia total es puramente resistiva (sin parte imaginaria). Esto sucede cuando la reactancia inductiva y capacitiva se cancelan entre sí:


$$f_0 = \frac{1}{2 \pi \sqrt{LC}}$$


En esta frecuencia, el circuito responde con una amplitud máxima en la corriente o voltaje, dependiendo de la configuración.

## Aplicaciones

Las redes RLC se utilizan en sistemas eléctricos como convertidores de onda, en circuitos para regular señales de voltaje con una resistencia variable, son usados en la eléctronica análoga ya obsoleta de la mayoria de los eléctrodomesticos y articulos eléctronicos de los años 90s, y son usados aún en circuitos más modernos de carga de dispositivos móviles y en los mismos dispositivos moviles que integran en sus circuitos lazos cerrados de circuitos RLC


# 2. Leyes Fundamentales de circuitos RLC

El comportamiento de las redes RLC está gobernado por varias leyes y principios fundamentales de la electricidad.

## Leyes de Kirchhoff

1. **Ley de Corrientes de Kirchhoff (LCK)**: La suma de las corrientes que entran y salen de un nodo es cero. Esto se expresa como:

  $$ \sum I_{\text{entrada}} = \sum I_{\text{salida}}$$

2. **Ley de Voltajes de Kirchhoff (LVK)**: La suma de las caídas de voltaje alrededor de cualquier lazo cerrado es cero. Esto se representa como:

   
   $$\sum V = 0$$

## Ley de Ohm

La ley de Ohm establece la relación entre voltaje $$(V\)$$, corriente $$(I\)$$ y resistencia $$(R\)$$:


$$V = IR$$

## 2. Comportamiento de los Capacitores (Carga y Descarga)

La carga y descarga de un capacitor en una red RLC son fenómenos transitorios:

Durante la carga:

  
  $$V_C(t) = V_0 \left(1 - e^{-\frac{t}{RC}}\right)$$

Durante la descarga:

  
  $$V_C(t) = V_0 e^{-\frac{t}{RC}}$$

## Comportamiento de los Inductores (Carga y Descarga)

La carga y descarga de un inductor se describen con las ecuaciones:

Durante la carga:

  
  $$I_L(t) = I_0 \left(1 - e^{-\frac{tR}{L}}\right)$$

Durante la descarga:


  $$I_L(t) = I_0 e^{-\frac{tR}{L}}$$

## Ecuación Diferencial de un Circuito RLC

Para un circuito RLC en serie, la ecuación diferencial que modela su comportamiento es:


$$L \frac{d^2q}{dt^2} + R \frac{dq}{dt} + \frac{q}{C} = 0$$

donde $$(q\)$$ es la carga en el capacitor.


## 3. Amplificadores Operacionales

Los amplificadores operacionales tienen una gran ganancia de voltaje y pueden realizar funciones como amplificación, filtrado, integración y diferenciación.

## Principios Básicos del Amplificador Operacional

- **Entrada no inversora $$(+\)$$**: Incrementa el voltaje de salida si el voltaje en esta entrada aumenta.
- **Entrada inversora $$(-\)$$**: Incrementa el voltaje de salida en sentido opuesto si el voltaje en esta entrada aumenta.

### Configuraciones Comunes de Amplificadores Operacionales

### 3.1. Amplificador Inversor

   
   $$V_{\text{out}} = -\frac{R_f}{R_{\text{in}}} V_{\text{in}}$$

### 3.2. Amplificador No Inversor

   
   $$V_{\text{out}} = \left(1 + \frac{R_f}{R_{\text{in}}}\right) V_{\text{in}}$$

### 3.3. Sumador Inversor

   
   $$V_{\text{out}} = -\left(\frac{R_f}{R_1} V_1 + \frac{R_f}{R_2} V_2 + \cdots\right)$$

### 3.4. Integrador

   $$V_{\text{out}} = -\frac{1}{RC} \int V_{\text{in}} \, dt$$

### 3.5. Diferenciador

   
   $$V_{\text{out}} = -RC \frac{dV_{\text{in}}}{dt}$$

## Aplicaciones de los Amplificadores Operacionales

Los amplificadores operacionales se utilizan ampliamente en las industrias colombianas, especialmente en sectores como telecomunicaciones, manufactura y energía. En telecomunicaciones, permiten mejorar la calidad de las señales y reducir el ruido en la transmisión. En manufactura, son esenciales para el control de sensores y dispositivos de precisión en máquinas automatizadas. Además, en el sector energético, ayudan en la regulación de corriente y voltaje en sistemas de potencia, optimizando la eficiencia y estabilidad de redes eléctricas y dispositivos de medición y protección.


## Conclusiones

Los amplificadores operacionales y sistemas eléctricos en Colombia han sido fundamentales para la estabilidad y eficiencia en telecomunicaciones, control de sensores y energía. La integración de amplificadores en dispositivos móviles y sistemas de control automático optimiza el consumo de energía y mejora el procesamiento de señales, fomentando la precisión y automatización en diversas industrias.

## Referencias
>Maxwell, D. (2022). Aplicaciones modernas de amplificadores operacionales en sistemas industriales. IEEE Transactions on Industrial Electronics.
>Texas Instruments. (2023). Op Amps: Applications in Energy and Telecommunications. Texas Instruments Technical Library.
>Analog Devices. (2023). Trends in Operational Amplifiers Reflect Advancing Electronics Industry. Analog Devices. Disponible en Analog Devices
>Smith, A. (2022). Uso de amplificadores en la industria electrónica. Journal of Applied Electronics.
