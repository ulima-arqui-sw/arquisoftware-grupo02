# Tema / alumno

Ingeniería del caos / Javier Olazábal

# Desarrollo conceptual 

La **Ingeniería del Caos** (Chaos Engineering) es una disciplina dentro del ámbito de las pruebas de software que se centra en probar y mejorar la resiliencia de un sistema mediante la introducción controlada de caos. El objetivo es descubrir y abordar debilidades y fallos en un sistema antes de que se conviertan en problemas graves en entornos de producción real.

## Conceptos clave de la Ingeniería del Caos:

1.  **Resiliencia**: La capacidad de un sistema para resistir, recuperarse y adaptarse a fallos o perturbaciones sin interrupciones significativas.

2. **Experimentación controlada**: Introducción deliberada de fallos y caos en un sistema de manera controlada y monitorizada.

3. **Hipótesis y validación**: Formulación de hipótesis sobre cómo podría fallar un sistema y validación de esas hipótesis a través de experimentos.

4. **Monitoreo constante**: Observación continua del sistema durante los experimentos para evaluar el impacto y la efectividad de las estrategias de resiliencia.

## Herramientas de Ingeniería del Caos:

1. **Chaos Monkey (Simian Army)**:
Desarrollado por Netflix, Chaos Monkey es una herramienta que provoca aleatoriamente fallos en instancias de producción para asegurarse de que los ingenieros están construyendo sistemas que pueden resistir fallos.

2. **Gremlin**:
Gremlin es una plataforma que permite a los equipos de ingeniería llevar a cabo experimentos de caos de manera controlada. Permite inyectar fallos en diferentes capas de la infraestructura, como la red, el sistema operativo o las aplicaciones.

3. **Pumba**:
Es una herramienta de código abierto que permite introducir caos en contenedores Docker. Puede simular pérdida de red, latencia, y otros escenarios para evaluar la resiliencia de las aplicaciones en entornos de contenedores.

4. **Chaos Toolkit**:
Ofrece un enfoque más generalizado para la Ingeniería del Caos, permitiendo a los ingenieros definir y ejecutar experimentos de caos en sus sistemas. Es extensible y puede integrarse con otras herramientas y servicios.

## Escenarios de uso

La ingeniería del caos se puede aplicar en diferentes escenarios, como:

1. **Pruebas de resiliencia**: La ingeniería del caos se puede utilizar para probar la resiliencia de un sistema, introduciendo fallos en el sistema y observando cómo responde. Esto permite a los ingenieros identificar y abordar debilidades y fallos antes de que se conviertan en problemas graves en entornos de producción real.
2. **Pruebas de recuperación ante desastres**: La ingeniería del caos se puede utilizar para probar la capacidad de un sistema para recuperarse de fallos y desastres. Esto permite a los ingenieros identificar y abordar debilidades y fallos en los planes de recuperación ante desastres.
3. **Pruebas de seguridad**: La ingeniería del caos se puede utilizar para probar la seguridad de un sistema, introduciendo fallos en el sistema y observando cómo responde. Esto permite a los ingenieros identificar y abordar debilidades y fallos en la seguridad antes de que se conviertan en problemas graves en entornos de producción real.
4. **Pruebas de carga**: La ingeniería del caos se puede utilizar para probar la capacidad de un sistema para manejar cargas de trabajo pesadas, introduciendo cargas de trabajo en el sistema y observando cómo responde. Esto permite a los ingenieros identificar y abordar debilidades y fallos antes de que se conviertan en problemas graves en entornos de producción real.
5. **Pruebas de escalabilidad**: La ingeniería del caos se puede utilizar para probar la capacidad de un sistema para escalar, introduciendo cargas de trabajo en el sistema y observando cómo responde. Esto permite a los ingenieros identificar y abordar debilidades y fallos antes de que se conviertan en problemas graves en entornos de producción real.
6. **Pruebas de disponibilidad**: La ingeniería del caos se puede utilizar para probar la disponibilidad de un sistema, introduciendo fallos en el sistema y observando cómo responde. Esto permite a los ingenieros identificar y abordar debilidades y fallos antes de que se conviertan en problemas graves en entornos de producción real.
7. **Pruebas de rendimiento**: La ingeniería del caos se puede utilizar para probar el rendimiento de un sistema, introduciendo cargas de trabajo en el sistema y observando cómo responde. Esto permite a los ingenieros identificar y abordar debilidades y fallos antes de que se conviertan en problemas graves en entornos de producción real.
8. **Pruebas de tolerancia a fallos**: La ingeniería del caos se puede utilizar para probar la tolerancia a fallos de un sistema, introduciendo fallos en el sistema y observando cómo responde. Esto permite a los ingenieros identificar y abordar debilidades y fallos antes de que se conviertan en problemas graves en entornos de producción real.

## Primeros pasos 
### 1. instalar chaospy
```bash
pip install chaospy
```
### 2. Crear archivo *payment_app.py*

```python
# archivo: payment_app.py

import random

def procesar_pago(monto, chaos_factor):
    exito = random.random() < chaos_factor
    if exito:
        return f"Pago exitoso: ${monto}"
    else:
        return "Error en el procesamiento de pago"
```
### 3. Crear archivo *chaos_payment_demo.py*

```python
# archivo: chaos_payment_demo.py

import chaospy
from payment_app import procesar_pago

def introducir_caos(monto):
    # Configurar un experimento de caos
    dist = chaospy.Normal(0, 1)  
    samples = dist.sample(10)  

    resultados = []
    for sample in samples:
        resultado = procesar_pago(monto,sample)
        resultados.append(resultado)

    return resultados

if __name__ == "__main__":
    monto_de_pago = 50.0

    print("Resultado sin caos:")
    print(procesar_pago(monto_de_pago,1))

    print("\nResultados con caos:")
    resultados_caos = introducir_caos(monto_de_pago)
    for resultado in resultados_caos:
        print(resultado)
```
### 4. Ejecutar el archivo *test_payment_app.py*

```bash
    python chaos_payment_demo.py
```

# Demo 

[video de la demo](https://drive.google.com/file/d/1JYzVgGGuZkWam_LhkBjbjbiwhOJdrmfo/view?usp=sharing)