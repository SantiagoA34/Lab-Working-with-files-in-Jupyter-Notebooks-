<center><h1>Evaluación Aplicativa</h1></center>

## Nombres: 
    
* Santiago Alarcón
* Alex San Martín
* Nicolás Irusta

### Objetivos:
El objetivo de este trabajo es comprender y conocer los siguientes aspectos de las distribuciones:
* __Contexto histórico:__ Sus pioneros y fundamentos matemáticos.
* __Aplicaciones y usos:__ Aplicaciones en áreas como economía, finanzas, el mundo contemporáneo en general, etc.
* __Parámetros de ajuste:__ Sus interpretaciones e influencias en las distribuciones.
* __Momentos centrales:__ Los 4 momentos centrales 
* __Gráficar:__ CDF y PDF con distintos parámetros para evidenciar variaciones.
* __Comprender la relación de las distribuciones con el aprendizaje de la estadística inferencial.__



#### Distribuciones usadas:
* Distribución Polya
* Distribución Gamma
* Distribución Beta
* Distribución Hipergeométrica


### Orígen:
* #### Polya:

Es un modelo discreto  conocida como distribución contagio. Mide la aleatoriedad del contagio de enfermedades y de extensión y propagación de cualquier tipo de información relacionada un bien o servicio. Su origen se remonta hasta 1923, donde Friedrich Eggenberger y George Pólya lograron un avance matemático en la teoría de los refuerzos. Esta distribución influyó en áreas importantes de la estadística como la estadística Bayesiana. 

La Polya puede verse como una extensión de la binomial y, evidentemente, de la Bernoulli, pero con refuerzos. Los refuerzos se refieren a que se aumenta la probabilidad de que algo vuelva a ocurrir cada vez que sucede. Entonces, se aumenta un mismo elemento en una “urna” para que la siguiente vez 2ue se elija un elemento de forma al azar, el o los determinados elementos que se sacaron previamente y se añadieron a la urna tengan una mayor probabilidad de salir.

El procedimiento de devolver la bola a la urna con c boas más del mismo color es el refuerzo en el procedimiento y esto se repite n veces:$$
〖(x)〗_n=x(x+1)(x+2)….(x+n-1)
$$

Con estos productos se llega a obtener la forma general de la distribución:
$$
P(X = k) = \binom{n}{k} \frac{\left( \frac{a}{c} \right)_k \left( \frac{b}{c} \right)_{n-k}}{\left( \frac{a}{c} + \frac{b}{c} \right)_n}
$$

Esto,
$$
\binom{n}{k}
$$
Indica de cuántas maneras distintas se pueden obtener k bolas en un total de n extracciones.
$$
\frac{a}{c}
$$
Muestra cómo cambia la probabilidad a medida que se agregan más bolas del mismo color cada vez que se repite ese resultado.

* #### Gamma:

La función gamma, por otro lado, fue descubierta en 1729, cuando el matemático Leonard Euler intentaba generalizar los valores factoriales de enteros positivos a reales y números complejos. En este caso, esta distribución está relacionada con la distribución normal,  exponencial, poisson y la  chi-cuadrado. 

Básicamente, la distribución es útil para modelar los tiempos que transcurren entre distintos eventos.
Gamma se denota como Γ.

El tiempo entre eventos en un proceso de Poisson sigue la siguiente forma:
$$f_{\text{exp}}(x) = \lambda e^{-\lambda x}, \quad \text{donde } x \geq 0$$

Si se suman k tiempos de un evento a otro, se obtiene la distribución gamma:
$$f(x; \alpha, \lambda) = \frac{\lambda^\alpha x^{\alpha-1} e^{-\lambda x}}{\Gamma(\alpha)}, \quad \text{donde } x \geq 0$$



* #### Beta: 

Su origen se remonta a 1837, cuando Leonhard Euler definió la función Beta como una integral especial. La distribución Beta tomó forma gracias al trabajo de Ronald Fisher. Representa los valores posibles de probabilidad y se considera una distribución de probabilidad continua definida por dos parámetros positivos. Es un tipo de distribución que se utiliza para representar los resultados o el comportamiento aleatorio en proporciones o porcentajes.

 Sigue una fórmula dentro del rango de $$[0,1]$$. 
 
 La función se define como:
$$B(\alpha, \beta) = \int_0^1 u^{\alpha-1} (1-u)^{\beta-1} \, du, \quad \text{donde } 0 < x < 1$$

α y β son los escalares reales positivos de la distribucion.

La distribución se ve de la siguiente manera en su forma desarrollada:
$$f(x; \alpha, \beta) = \frac{1}{B(\alpha, \beta)} x^{\alpha-1} (1-x)^{\beta-1}, \quad \text{donde } 0 < x < 1$$

* #### Hipergeométrica:

La hipergeométrica, a un inicio, era asociada a una función para obtener el área de una hipérbola. Esta fue introducida por John Wallis, pero Sorensen y Fisher la incorporaron a estadística y probabilidades en 1950. Su propósito es extraer muestras sin reemplazos de poblaciones finitas y divididas. Como otras distribuciones previamente vistas, tiene relación con la binomial y la Bernoulli ya que modela la probabilidad de obtener un número específico de éxitos cuando se extraen n elementos sin reemplazos poblaciones finitas. 

El proceso consta de n pruebas, separadas o separables de entre un conjunto de N pruebas posibles. Cada una de las pruebas puede dar solo dos resultados mutuamente excluyentes.

De K disponibles, se eligen k de la siguiente manera:
$$\binom{K}{k}$$

La forma de elegir fracasos se elige en base a N-K para hallar el n-k restante y hallar el tamaño de la muestra:

$$\binom{N-K}{n-k}$$

El número total que existe para formar una muestra de n elementos del N total se ve asi: 

$$\binom{N}{n}$$

Asimismo, se llega a obtener la distribucion con forma:
$$P(X = k) = \frac{\binom{K}{k} \binom{N-K}{n-k}}{\binom{N}{n}}$$




### Usos y Aplicaciones:
##### Distribución Polya:
La distribución de Polya es una generalización de la distribución binomial negativa. Esta nos permite modelar fenómenos donde la historia previa influye en el comportamiento futuro, y se utiliza en múltiples campos como:

- **Epidemiología**:  
  Modela la propagación de enfermedades contagiosas, donde la probabilidad de contagio aumenta con cada nuevo caso, conocido como el *efecto contagio*.

  __Por ejemplo:__ La propagación del COVID-19, donde un caso positivo incrementa significativamente la probabilidad de nuevos contagios. Cuando un miembro de una familia se contagia, la probabilidad de que el resto de integrantes se contagie incrementa significativamente.

- **Fiabilidad**:  
  Describe los fallos en sistemas donde un componente averiado incrementa la probabilidad de fallos posteriores.

  __Por ejemplo:__ La propagación de fallos en el motor de un auto. Las baterias de vehiculos cuando alcanzan su vida útil y empiezan a tener un mal funcionamiento a veces expulsan un liquido, este, al secarse se convierte en como un moho que se mantiene en la bateria. A largo plazo puede contagiar a otras partes del vehículo, estropeando diferentes piezas.

- **Finanzas**:  
  Aplicada en modelos de riesgo operacional para eventos raros con dependencia temporal, como fraudes en cadena.

  __Por ejemplo:__ Cuando en diferentes países, por lo general en Estados Unidos, las personas son descubiertas realizando cobros de sus seguros vehiculares fraudulentos. Al inspeccionar más, la probabilidad de encontrar otro caso similar incrementa.
  
- **Economía**:  
  Se usa para describir procesos de adopción tecnológica y de consumo, donde los primeros usuarios influyen en las decisiones de los siguientes.

  __Por ejemplo:__ Ante el lanzamiento de la nueva vagoneta de Toyota, la 4Runner 2025. Siendo de una nueva generación, los primeros en adquirirlas influyen e incrementan la pisibilidad de adopción global del vehículo.

##### Distribución Gamma:

La distribución Gamma es continua y modela el tiempo hasta que ocurren “k” eventos en un proceso de Poisson. Se aplica en diversas áreas:

- **Ingeniería**:  
  Modela tiempos de vida de componentes electrónicos y tiempos de espera hasta múltiples fallos en sistemas.

  __Por ejemplo:__ Siguiendo con el ejemplo de Toyota. Mide la vida útil de los componentes de los vehículos comercializados y de este modo, contabilizar las fallas críticas antes del mantenimiento preventivo cada cierto kilometraje.

- **Meteorología**:  
  Describe la distribución de precipitaciones acumuladas en un periodo de tiempo.

  __Por ejemplo:__ En el fenómeno de "El Ñino", por lo general en zonas como El Pacífico.

- **Finanzas**:  
  Se utiliza en modelos de riesgo operativo y de crédito, como el tiempo hasta enfrentar una pérdida significativa.

  __Por ejemplo:__ Modela el tiempo hasta una posible quiebra de un negocio que podría ser un restaurante de sushi. Se consideran factores de riesgo acumulados, como podría ser estar en un déficit debido al incremento en su costo de producción.

- **Economía**:  
  Aplica en el análisis de tiempos de recuperación económica, duración del desempleo y crisis financieras, donde los eventos no ocurren a una tasa constante.

  __Por ejemplo:__ En el caso de recesiones económicas, como la de 2009, de este modo midiendo el tiempo entre eventos graves económicos.

##### Distribución Beta

La distribución Beta es versátil y usada ampliamente en estadística aplicada. Su dominio está restringido a \([0,1]\), por lo que es ideal para modelar proporciones, tasas y probabilidades. Se emplea en:

- **Estadística Bayesiana**:                           
  Utilizada para actualizar probabilidades en el testeo de vacunas, como en los ensayos de de la vacuna Pfizer para el COVID 19.
  
- **Economía**:  
  Modela distribución de riqueza relativa, participación de mercado y proporción de gasto en rubros.

  __Por ejemplo:__ En el caso de Netflix, Disney+ y Amazon Prime. Modela la participación de mercado que estas plataformas de streaming tienen.

- **Finanzas**:  
  Se incorpora en modelos de optimización de portafolios y en tasas de retorno ajustadas dentro de límites específicos

  __Por ejemplo:__ Se usa en optimización de portafolios de inversión, de este modo, se asignan pesos a activos como acciones de Apple u otra empresa según el riesgo o retorno esperado.

- **Biología**:  
  Describe la variabilidad en tasas de crecimiento relativas

  __Por ejemplo:__ La proporción de nutrientes absorbidos por plantas. Ayuda a la modelación de la proporción de nitrógeno en las plantas de maíz para estudios agrícolas.

##### Distribución Hipergeométrica

La distribución hipergeométrica describe la probabilidad de extraer un número específico de éxitos de una población finita **sin reemplazo**. Se diferencia de la binomial en que cada extracción afecta la siguiente. Se aplica en:

- **Control de Calidad**:  
  Evaluación de productos sin reemplazo.

  __Por ejemplo:__ Siguiendo con el ejemplo de Toyota y la 4Runner. Estos tienen sus auditorías internas donde seleccionan muestras de 4Runners y detectan si existe algún defecto en estas unidades sin devolverlos a la producción.

- **Auditorías y Políticas Públicas**:  
  Análisis de subconjuntos específicos de poblaciones cerradas.

  __Por ejemplo:__ En una auditoría en Estados Unidos llamada Medicaid. Se analizaron subconjuntos de expedientes médicos seleccionados sin reemplazo.

- **Genética y Ecología**:  
  Estudios de características heredadas y poblaciones limitadas.

  __Por ejemplo:__ Se han realizado estudios de la diversidad genética de los pandas con la finalidad de analizar sus muestras limitadas de ADN.

- **Economía**:  
  Modelos de selección sin reemplazo, votaciones económicas, presupuestos públicos cerrados o asignaciones de recursos no renovables.

  __Por ejemplo:__ Hubo un caso en México donde se buscaba apoyar a agricultores, donde se podían otorgar unos subsidios limitados a cierta cantidad limitada de productorees. En este caso, aleatoriamente, se seleccionan diferentes muestras para analizar si son intentos de fraude o verídicos. Se modela la probabilidad de encontrar cierto número de intentos de fraude dentro de la muestra.

- **Finanzas**:  
  Modelado del número de activos que fallan simultáneamente en una cartera cerrada.

  __Por ejemplo:__ En una cartera fija de x bonos de distintas empresas, se busca la probabilidad de que al seleccionar 10 bonos al azar, al menos 3 estén en situación de impago. Ya que, cada bono seleccionado afecta a los siguientes, su modelación con esta distribución es pertinente. 



### Parámetros de Ajuste:
Los parámetros de ajustes varían dependiendo de las distrbuciones. Estos definen la forma y posición de la distribución para que se ajuste de la mejor manera a los datos, representando los datos realisticamente. 

##### Distribución Polya: $$
P[X = k] = \binom{n}{k} \cdot \frac{M^{(k,c)} (N-M)^{(n-k,c)}}{N^{(n,c)}}
$$ 
Existen 4 parámetros para esta distribución
<table style="width:100%; border: 2px solid black; border-collapse: collapse; font-size: 16px;">
  <thead>
    <tr style="background-color: #800020; color: white;">
      <th style="padding:10px; border: 2px solid black;">Parámetro</th>
      <th style="padding:10px; border: 2px solid black;">Descripción</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:10px; border: 2px solid black;"><b>N</b></td>
      <td style="padding:10px; border: 2px solid black;">
        Número total de pruebas.
      </td>
    </tr>
    <tr>
      <td style="padding:10px; border: 2px solid black;"><b>M / p</b></td>
      <td style="padding:10px; border: 2px solid black;">
        Muestra la probabilidad inicial de obtener un resultado en el primer intento.
      </td>
    </tr>
    <tr>
      <td style="padding:10px; border: 2px solid black;"><b>n</b></td>
      <td style="padding:10px; border: 2px solid black;">
        Número de pruebas realizadas.
      </td>
    </tr>
    <tr>
      <td style="padding:10px; border: 2px solid black;"><b>c</b></td>
      <td style="padding:10px; border: 2px solid black;">
        Factor de contagio: cómo cambian las probabilidades según resultados anteriores.
      </td>
    </tr>
  </tbody>
</table>

Si "c" es positivo, la probabilidad de obtener el mismo resultado es mayor, si fuera negativo, la probabilidad de obtener el mismo resultado reduce.
En el caso que tome resultados negativos se tiene que cumplir la siguiente condición: 
$$
-N + c(n-1) > 1
$$ 
De igual manera para obtener los resultados sin dificultad M y N-M  deben ser divisibles por c y cumplir con: 
$$
\max\left(0, n + \frac{N-M}{c}\right) \leq k \leq \min\left(n, \frac{-M}{c}\right)
$$

Casos particulares en función al valor de "c":
|Parámetros|Representación|
|----------|--------------|
|
$$
c > 0
$$|Un éxito o un fracaso incrementa la probabilidad de éxito o fracaso|
|
$$
c = 0
$$|Son sucesos independientes|
|
$$
c < 0
$$|El éxito disminuye la probabilidad de volver a tener éxito, aplica lo mismo para el fracaso|

##### Distribución Gamma: $$
f(x) = \frac{1}{\Gamma(k) b^k} x^{k-1} e^{-x/b}, \quad x \in (0, \infty)$$
Existen 2 parámetros:
<table style="width:100%; border: 2px solid black; border-collapse: collapse;">
  <thead>
    <tr style="background-color: #800020; color: white;">
      <th style="padding:10px; border: 2px solid black;">Shapek \(k\)</th>
      <th style="padding:10px; border: 2px solid black;">Scaleb \(b\)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:10px; border: 2px solid black;">
        Este es el parámetro de forma. Mide la forma de la distribución.<br><br>
        Si $$k < 1$$ <b>Es fuertemente asimétrica.</b><br><br>
        Si $$k = 1$$ <b>La distribución se convierte en una exponencial.</b><br><br>
        Si $$k > 1$$ <b>Es más simétrica.</b><br><br>
        Mientras más alto sea el valor de \(k\), más se parece a una distribución normal.
      </td>
      <td style="padding:10px; border: 2px solid black;">
        Este es el parámetro de escala. Puede estirar o comprimir la distribución en el eje \(x\) afectando la dispersión.<br><br>
        Mientras mayor sea \(b\), mayor será la dispersión.<br><br>
        Mientras menor sea \(b\), mayor será la concentración.
      </td>
    </tr>
  </tbody>
</table>

##### Distribución Beta:
$$f(x) = \frac{1}{B(a,b)} \, x^{a-1} (1-x)^{b-1}, \quad x \in (0,1)$$

En este caso, existen 2 parámetros de igual forma:
<style>
  table.custom-table {
    width: 100%;
    border-collapse: collapse;
    text-align: center;
    font-family: Arial, sans-serif;
  }
  table.custom-table th {
    background-color: #800000; /* Guindo */
    color: white;
    padding: 10px;
    border: 2px solid #800000;
  }
  table.custom-table td {
    padding: 10px;
    border: 2px solid #800000;
  }
  table.custom-table tbody tr:hover {
    background-color: #f2f2f2; /* Color suave al pasar el mouse */
  }
</style>

<table class="custom-table">
  <thead>
    <tr>
      <th>(a)</th>
      <th>(b)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        Este es el parámetro izquierdo. <br><br>
        Es uno de los exponentes de la variable aleatoria en la distribución beta. <br><br>
        Controla junto a \( b \) la forma de la distribución.
      </td>
      <td>
        Este es el parámetro derecho. <br><br>
        También es un exponente de la variable aleatoria en la distribución beta. <br><br>
        Trabaja con \( a \) para moldear la forma de la distribución.
      </td>
    </tr>
  </tbody>
</table>


##### Distribución Hipergeométrica:
$$P(X = x) = \frac{\binom{n}{x} \binom{N-k}{n-x}}{\binom{N}{n}}$$

<table border="1" style="border-collapse: collapse; text-align: center;">
  <tr style="background-color: #800000; color: white;">
    <th>Parámetro</th>
    <th>Descripción</th>
  </tr>
  <tr>
    <td><b>N</b></td>
    <td>Tamaño de la población</td>
  </tr>
  <tr>
    <td><b>K</b></td>
    <td>Número de éxitos</td>
  </tr>
  <tr>
    <td><b>n</b></td>
    <td>Tamaño de la muestra</td>
  </tr>
</table>

### Momentos Centrales:
#### ¿Que es un momento central?
Es una medida que captura el grado en el que una variable aleatoria se desvía de su media.  Los momentos centrales brindan información significativa sobre la distribución de los puntos alrededor de la media, lo que ayuda a comprender los conjuntos de datos de manera integral.
Existen 4 momentos centrales: 
<table style="border-collapse: collapse; width: 100%;">
  <thead>
    <tr style="background-color: #800000; color: white;">
      <th style="padding: 8px; border: 1px solid #ddd;">Momento Central</th>
      <th style="padding: 8px; border: 1px solid #ddd;">Definición</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 8px; border: 1px solid #ddd;">E[X]</td>
      <td style="padding: 8px; border: 1px solid #ddd;">Es el valor esperado, el promedio esperado de todas las pruebas.</td>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #ddd;">Var[X]</td>
      <td style="padding: 8px; border: 1px solid #ddd;">La varianza mide la dispersión de los datos respecto a su media o valor esperado.</td>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #ddd;">Asimetría (Skewness)</td>
      <td style="padding: 8px; border: 1px solid #ddd;">Mide la asimetría con respecto de la media.</td>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #ddd;">Curtosis</td>
      <td style="padding: 8px; border: 1px solid #ddd;">Describe la forma de las colas y el pico.</td>
    </tr>
  </tbody>
</table>

Una vez definidos estos conceptos, pasemos con los momentos centrales de las distribuciones.
##### Distribución Polya:
1. $$
E[X] = np
$$
2. $$
\text{Var}(X) = \mu_2 = \frac{npq(N + nc)}{N + c}
$$ 
3.  $$
\text{Asimetría (Skewness)} = \mu_3 = \frac{\mu_2 (q - p)(N + 2nc)}{N + 2c}
$$
4. $$
\text{Curtosis} = \mu_4 = \frac{(N+nc)\left(N^2 + 3Nc(n-1) + c^2(n-1)(3n-5)\right)pq(1-6pq)}{(N+c)^2 \cdot (npq(N+nc))} - 3
$$

##### Distribución Gamma:
1. $$ E[X] = bk$$
2. $$ Var[X] = b^2 k$$
3. $$\text{Asimetría} = \frac{2}{\sqrt{k}}$$
4. $$\text{Curtosis} = 3 + \frac{6}{k}$$

##### Distribución Beta
1. $$E[X] = \frac{a}{a+b}$$
2. $$\text{Var}[X] = \frac{ab}{(a+b)^2 (a+b+1)}$$
3. $$\text{Asimetría (Skewness)} = \frac{2(b-a) \sqrt{a+b+1}}{(a+b+2) \sqrt{ab}}$$
4. $$\text{Curtosis} = \frac{3a^3b + 3ab^3 + 6a^2b^2 + 13a^2b + 13ab^2 + 14ab + a^2 + b^2 + a^3 + b^3}{ab(a+b+2)(a+b+3)}$$

##### Distribución Hipergeométrica:
1. $$E[X] = np$$
2. $$\text{Var}[X] = npq \cdot \frac{N-n}{N-1}$$
3. $$\text{Asimetría} = \frac{(N-2k) \sqrt{N-1} (N-2n)}{(N-2) \sqrt{nk(N-k)(N-n)}}$$
4. $$\text{Curtosis} = \frac{N^2 (N-1)(N(N+1) - 6n(N-n)) - 6nK(N-K)(N-Nn+1)}{nK(N-K)(N-n)(N-2)(N-3)}$$

### Funciones y Gráficos:

__Distribución Polya:__

Los parámetros para la distribución son los siguientes:

__Parámetros de Gráficas 1 y 2 (PDF y CDF)__
* n = 30 ---> (Tamaño de la muestra)
* a = ---> 5 ("Éxitos" iniciales relacionado a M)
* b = ---> 10 ("Fracasos" iniciales relacionados a N-M)

__Parámetros de Gráficas 3 y 4 (PDF y CDF)__
* n = 35
* a = 10
* b = 15

__Parámetros de Gráficas 5 y 6 (PDF y CDF)__
* n = 40
* a = 15
* b = 20

__Parámetros de Gráficas 7 y 8 (PDF y CDF)__
* n = 45
* a = 20
* b = 25 

__Parámetros de Gráficas 9 y 10 (PDF y CDF)__
* n = 50
* a = 25
* b = 30

* ### Gráficas 1 y 2:


```python
# Instalación de las librerias necesarias
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import betabinom

# Parámetros
n = 30
a = 5
b = 10

# Valores de k
k = np.arange(0, n + 1)

# PDF y CDF
pdf = betabinom.pmf(k, n, a, b)
cdf = betabinom.cdf(k, n, a, b)

# Gráficas
fig, ax = plt.subplots(1, 2, figsize=(14, 5))

# PDF
ax[0].vlines(k, 0, pdf, colors='royalblue', lw=3)
ax[0].plot(k, pdf, 'o', color='navy')
ax[0].set_title('Distribución de Polya (PDF)', fontsize=16)
ax[0].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[0].set_ylabel('P[X = k]', fontsize=14)
ax[0].grid(alpha=0.3)

# CDF
ax[1].plot(k, cdf, marker='o', color='crimson')
ax[1].set_title('Distribución de Polya (CDF)', fontsize=16)
ax[1].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[1].set_ylabel('P[X ≤ k]', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_28_0.png)
    


* ### Gráficas 3 y 4:


```python
n = 35
a = 10
b = 15

k = np.arange(0, n + 1)
pdf = betabinom.pmf(k, n, a, b)
cdf = betabinom.cdf(k, n, a, b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

# Gráfica PDF
ax[0].vlines(k, 0, pdf, colors='royalblue', lw=3)
ax[0].plot(k, pdf, 'o', color='navy')
ax[0].set_title('Distribución de Polya (PDF)', fontsize=16)
ax[0].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[0].set_ylabel('P(X = k)', fontsize=14)
ax[0].grid(alpha=0.3)

# Gráfica CDF
ax[1].plot(k, cdf, marker='o', color='crimson')
ax[1].set_title('Distribución de Polya (CDF)', fontsize=16)
ax[1].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[1].set_ylabel('P(X ≤ k)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_30_0.png)
    


* ### Gráficas 5 y 6:


```python
n = 40
a = 15
b = 20

k = np.arange(0, n + 1)
pdf = betabinom.pmf(k, n, a, b)
cdf = betabinom.cdf(k, n, a, b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

# Gráfica PDF
ax[0].vlines(k, 0, pdf, colors='royalblue', lw=3)
ax[0].plot(k, pdf, 'o', color='navy')
ax[0].set_title('Distribución de Polya (PDF)', fontsize=16)
ax[0].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[0].set_ylabel('P(X = k)', fontsize=14)
ax[0].grid(alpha=0.3)

# Gráfica CDF
ax[1].plot(k, cdf, marker='o', color='crimson')
ax[1].set_title('Distribución de Polya (CDF)', fontsize=16)
ax[1].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[1].set_ylabel('P(X ≤ k)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_32_0.png)
    


* ### Gráficas 7 y 8:


```python
n = 45
a = 20
b = 25

k = np.arange(0, n + 1)
pdf = betabinom.pmf(k, n, a, b)
cdf = betabinom.cdf(k, n, a, b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

# Gráfica PDF
ax[0].vlines(k, 0, pdf, colors='royalblue', lw=3)
ax[0].plot(k, pdf, 'o', color='navy')
ax[0].set_title('Distribución de Polya (PDF)', fontsize=16)
ax[0].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[0].set_ylabel('P(X = k)', fontsize=14)
ax[0].grid(alpha=0.3)

# Gráfica CDF
ax[1].plot(k, cdf, marker='o', color='crimson')
ax[1].set_title('Distribución de Polya (CDF)', fontsize=16)
ax[1].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[1].set_ylabel('P(X ≤ k)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_34_0.png)
    


* ### Gráficas 9 y 10:


```python
n = 50
a = 25
b = 30

k = np.arange(0, n + 1)
pdf = betabinom.pmf(k, n, a, b)
cdf = betabinom.cdf(k, n, a, b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

# Gráfica PDF
ax[0].vlines(k, 0, pdf, colors='royalblue', lw=3)
ax[0].plot(k, pdf, 'o', color='navy')
ax[0].set_title('Distribución de Polya (PDF)', fontsize=16)
ax[0].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[0].set_ylabel('P(X = k)', fontsize=14)
ax[0].grid(alpha=0.3)

# Gráfica CDF
ax[1].plot(k, cdf, marker='o', color='crimson')
ax[1].set_title('Distribución de Polya (CDF)', fontsize=16)
ax[1].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[1].set_ylabel('P(X ≤ k)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_36_0.png)
    


__Distribución Gamma:__

Los parámetros para la distribución son los siguientes:

__Parámetros para Gráficas 11 y 12 (PDF y CDF)__
* k = 5
* b = 5

__Parámetros para Gráficas 13 y 14 (PDF y CDF)__
* k = 10 
* b = 10

__Parámetros para Gráficas 15 y 16 (PDF y CDF)__
* k = 15
* b = 15

__Parámetros para Gráficas 17 y 18 (PDF y CDF)__
* k = 20
* b = 20

__Parámetros para Gráficas 19 y 20 (PDF y CDF)__
* k = 25 
* b = 25

* ### Gráficas 11 y 12:


```python
#Instalación de librerias
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import gamma

k = 5
b = 5

x = np.linspace(0, 100, 1000)
pdf = gamma.pdf(x, a=k, scale=b)
cdf = gamma.cdf(x, a=k, scale=b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

# PDF
ax[0].plot(x, pdf, color='royalblue')
ax[0].set_title('Distribución Gamma (PDF)', fontsize=16)
ax[0].set_xlabel('x', fontsize=14)
ax[0].set_ylabel('f(x)', fontsize=14)
ax[0].grid(alpha=0.3)

# CDF
ax[1].plot(x, cdf, color='crimson')
ax[1].set_title('Distribución Gamma (CDF)', fontsize=16)
ax[1].set_xlabel('x', fontsize=14)
ax[1].set_ylabel('F(x)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_39_0.png)
    


* ### Gráficas 13 y 14:


```python
k = 10
b = 10
x = np.linspace(0, 200, 1000)
pdf = gamma.pdf(x, a=k, scale=b)
cdf = gamma.cdf(x, a=k, scale=b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

ax[0].plot(x, pdf, color='royalblue')
ax[0].set_title('Distribución Gamma (PDF)', fontsize=16)
ax[0].set_xlabel('x', fontsize=14)
ax[0].set_ylabel('f(x)', fontsize=14)
ax[0].grid(alpha=0.3)

ax[1].plot(x, cdf, color='crimson')
ax[1].set_title('Distribución Gamma (CDF)', fontsize=16)
ax[1].set_xlabel('x', fontsize=14)
ax[1].set_ylabel('F(x)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_41_0.png)
    


* ### Gráficas 15 y 16:


```python
k = 15
b = 15
x = np.linspace(0, 300, 1000)
pdf = gamma.pdf(x, a=k, scale=b)
cdf = gamma.cdf(x, a=k, scale=b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

ax[0].plot(x, pdf, color='royalblue')
ax[0].set_title('Distribución Gamma (PDF)', fontsize=16)
ax[0].set_xlabel('x', fontsize=14)
ax[0].set_ylabel('f(x)', fontsize=14)
ax[0].grid(alpha=0.3)

ax[1].plot(x, cdf, color='crimson')
ax[1].set_title('Distribución Gamma (CDF)', fontsize=16)
ax[1].set_xlabel('x', fontsize=14)
ax[1].set_ylabel('F(x)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_43_0.png)
    


* ### Gráfica 17 y 18:


```python
k = 20
b = 20
x = np.linspace(0, 400, 1000)
pdf = gamma.pdf(x, a=k, scale=b)
cdf = gamma.cdf(x, a=k, scale=b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

ax[0].plot(x, pdf, color='royalblue')
ax[0].set_title('Distribución Gamma (PDF)', fontsize=16)
ax[0].set_xlabel('x', fontsize=14)
ax[0].set_ylabel('f(x)', fontsize=14)
ax[0].grid(alpha=0.3)

ax[1].plot(x, cdf, color='crimson')
ax[1].set_title('Distribución Gamma (CDF)', fontsize=16)
ax[1].set_xlabel('x', fontsize=14)
ax[1].set_ylabel('F(x)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_45_0.png)
    


* ### Gráficas 19 y 20:


```python
k = 25
b = 25
x = np.linspace(0, 500, 1000)
pdf = gamma.pdf(x, a=k, scale=b)
cdf = gamma.cdf(x, a=k, scale=b)

fig, ax = plt.subplots(1, 2, figsize=(14, 5))

ax[0].plot(x, pdf, color='royalblue')
ax[0].set_title('Distribución Gamma (PDF)', fontsize=16)
ax[0].set_xlabel('x', fontsize=14)
ax[0].set_ylabel('f(x)', fontsize=14)
ax[0].grid(alpha=0.3)

ax[1].plot(x, cdf, color='crimson')
ax[1].set_title('Distribución Gamma (CDF)', fontsize=16)
ax[1].set_xlabel('x', fontsize=14)
ax[1].set_ylabel('F(x)', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_47_0.png)
    


__Distribución Beta:__

Los parámetros para la distribución son los siguientes:

__Parámetros para Gráficas 21 y 22 (PDF y CDF)__
* a = 2
* b = 5

__Parámetros para Gráficas 23 y 24 (PDF y CDF)__
* a = 7 
* b = 10

__Parámetros para Gráficas 25 y 26 (PDF y CDF)__
* a = 12
* b = 15

__Parámetros para Gráficas 27 y 28 (PDF y CDF)__
* a = 17
* b = 20

__Parámetros para Gráficas 29 y 30 (PDF y CDF)__
* a = 22 
* b = 25

* ### Gráficas 21 y 22:


```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import beta

a, b = 2, 5
x = np.linspace(0, 1, 1000)
pdf = beta.pdf(x, a, b)
cdf = beta.cdf(x, a, b)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].plot(x, pdf, 'b-', label=f'PDF Beta({a},{b})')
axs[0].set_title('Beta PDF')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Density')
axs[0].legend()

axs[1].plot(x, cdf, 'r-', label=f'CDF Beta({a},{b})')
axs[1].set_title('Beta CDF')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Cumulative Probability')
axs[1].legend()

plt.tight_layout()
plt.show()
```


    
![png](output_50_0.png)
    


* ### Gráficas 23 y 24:


```python
a, b = 7, 10
x = np.linspace(0, 1, 1000)
pdf = beta.pdf(x, a, b)
cdf = beta.cdf(x, a, b)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].plot(x, pdf, 'b-', label=f'PDF Beta({a},{b})')
axs[0].set_title('Beta PDF')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Density')
axs[0].legend()

axs[1].plot(x, cdf, 'r-', label=f'CDF Beta({a},{b})')
axs[1].set_title('Beta CDF')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Cumulative Probability')
axs[1].legend()

plt.tight_layout()
plt.show()
```


    
![png](output_52_0.png)
    


* ### Gráficas 25 y 26:


```python
a, b = 12, 15
x = np.linspace(0, 1, 1000)
pdf = beta.pdf(x, a, b)
cdf = beta.cdf(x, a, b)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].plot(x, pdf, 'b-', label=f'PDF Beta({a},{b})')
axs[0].set_title('Beta PDF')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Density')
axs[0].legend()

axs[1].plot(x, cdf, 'r-', label=f'CDF Beta({a},{b})')
axs[1].set_title('Beta CDF')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Cumulative Probability')
axs[1].legend()

plt.tight_layout()
plt.show()
```


    
![png](output_54_0.png)
    


* ### Gráficas 27 y 28:


```python
a, b = 17, 20
x = np.linspace(0, 1, 1000)
pdf = beta.pdf(x, a, b)
cdf = beta.cdf(x, a, b)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].plot(x, pdf, 'b-', label=f'PDF Beta({a},{b})')
axs[0].set_title('Beta PDF')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Density')
axs[0].legend()

axs[1].plot(x, cdf, 'r-', label=f'CDF Beta({a},{b})')
axs[1].set_title('Beta CDF')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Cumulative Probability')
axs[1].legend()

plt.tight_layout()
plt.show()
```


    
![png](output_56_0.png)
    


* ### Gráficas 29 y 30:


```python
a, b = 22, 25
x = np.linspace(0, 1, 1000)
pdf = beta.pdf(x, a, b)
cdf = beta.cdf(x, a, b)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].plot(x, pdf, 'b-', label=f'PDF Beta({a},{b})')
axs[0].set_title('Beta PDF')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Density')
axs[0].legend()

axs[1].plot(x, cdf, 'r-', label=f'CDF Beta({a},{b})')
axs[1].set_title('Beta CDF')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Cumulative Probability')
axs[1].legend()

plt.tight_layout()
plt.show()
```


    
![png](output_58_0.png)
    


__Distribución Hipergeométrica:__

Los parámetros para la distribución son los siguientes:

__Parámetros para Gráficas 31 y 32 (PDF y CDF)__
* N = 30
* k = 10
* n = 15

__Parámetros para Gráficas 33 y 34 (PDF y CDF)__
* N = 35 
* k = 15
* n = 20

__Parámetros para Gráficas 35 y 36 (PDF y CDF)__
* N = 40
* k = 20
* n = 25

__Parámetros para Gráficas 37 y 38 (PDF y CDF)__
* N = 45 
* k = 25
* n = 30

__Parámetros para Gráficas 39 y 40 (PDF y CDF)__
* N = 50 
* k = 30
* n = 35

* ### Gráficas 31 y 32:


```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import hypergeom

N, k, n = 30, 10, 5
x = np.arange(0, n+1)
pmf = hypergeom.pmf(x, N, k, n)
cdf = hypergeom.cdf(x, N, k, n)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].stem(x, pmf, basefmt=" ")
axs[0].set_title(f'Hipergeométrica PMF (N={N}, k={k}, n={n})')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Probabilidad')

axs[1].step(x, cdf, where='post')
axs[1].set_title(f'Hipergeométrica CDF (N={N}, k={k}, n={n})')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Probabilidad acumulada')

plt.tight_layout()
plt.show()
```


    
![png](output_61_0.png)
    


* ### Gráficas 33 y 34:


```python
N, k, n = 35, 15, 10
x = np.arange(0, n+1)
pmf = hypergeom.pmf(x, N, k, n)
cdf = hypergeom.cdf(x, N, k, n)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].stem(x, pmf, basefmt=" ")
axs[0].set_title(f'Hipergeométrica PMF (N={N}, k={k}, n={n})')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Probabilidad')

axs[1].step(x, cdf, where='post')
axs[1].set_title(f'Hipergeométrica CDF (N={N}, k={k}, n={n})')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Probabilidad acumulada')

plt.tight_layout()
plt.show()
```


    
![png](output_63_0.png)
    


* ### Gráficas 35 y 36:


```python
N, k, n = 40, 20, 15
x = np.arange(0, n+1)
pmf = hypergeom.pmf(x, N, k, n)
cdf = hypergeom.cdf(x, N, k, n)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].stem(x, pmf, basefmt=" ")
axs[0].set_title(f'Hipergeométrica PMF (N={N}, k={k}, n={n})')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Probabilidad')

axs[1].step(x, cdf, where='post')
axs[1].set_title(f'Hipergeométrica CDF (N={N}, k={k}, n={n})')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Probabilidad acumulada')

plt.tight_layout()
plt.show()
```


    
![png](output_65_0.png)
    


* ### Gráficas 37 y 38:


```python
N, k, n = 45, 25, 20
x = np.arange(0, n+1)
pmf = hypergeom.pmf(x, N, k, n)
cdf = hypergeom.cdf(x, N, k, n)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].stem(x, pmf, basefmt=" ")
axs[0].set_title(f'Hipergeométrica PMF (N={N}, k={k}, n={n})')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Probabilidad')

axs[1].step(x, cdf, where='post')
axs[1].set_title(f'Hipergeométrica CDF (N={N}, k={k}, n={n})')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Probabilidad acumulada')

plt.tight_layout()
plt.show()
```


    
![png](output_67_0.png)
    


* ### Gráficas 39 y 40:


```python
N, k, n = 50, 30, 25
x = np.arange(0, n+1)
pmf = hypergeom.pmf(x, N, k, n)
cdf = hypergeom.cdf(x, N, k, n)

fig, axs = plt.subplots(1, 2, figsize=(12, 5))
axs[0].stem(x, pmf, basefmt=" ")
axs[0].set_title(f'Hipergeométrica PMF (N={N}, k={k}, n={n})')
axs[0].set_xlabel('x')
axs[0].set_ylabel('Probabilidad')

axs[1].step(x, cdf, where='post')
axs[1].set_title(f'Hipergeométrica CDF (N={N}, k={k}, n={n})')
axs[1].set_xlabel('x')
axs[1].set_ylabel('Probabilidad acumulada')

plt.tight_layout()
plt.show()
```


    
![png](output_69_0.png)
    


### Aplicaciones (Extra)

Existen diferentes usos para estas distribuciones como se planteó y profundizó anteriormente. Sin embargo, un ejemplo extra bastante interesante que trata un tema bastante importante en la actualidad fue planteado. Los vehículos eléctricos. Y para analizar este tema se usará la _Distribución Polya_.

La adopción de los vehículos eléctricos (EVs) se disparó los últimos años en múltiples países debido a muchos factores, entre estos están la preocupación por el medio ambiente, avances tecnológicos y políticas públicas que incentivan al uso de energías alternativas. 

__¿Porqué se usa la distribución polya?__

Esta distribución resulta muy útil para modelar cómo los consumidores, al adoptar un vehículo eléctrico influyen en otros a través de reseñas positivas, observaciones directas o testimonios personales. A medida que más personas compran un EV y se ven beneficiados por sus características como mejor costo operativo o un menor impacto ambiental, aumenta la probabilidad de que nuevos compradores se sumen, generando un efecto de contagio social.

Esto funcionó bastante bien en países como Estados Unidos, China, Noruega o Suiza, donde la infraestructura, el poder adquisitivo de los habitantes y la cultura tecnológica favorecen a esta adopción. Sin embargo, de acá surge una pregunta interesante. 

__¿Cómo se propagarían estos vehículos a un país menos desarrollado y con una fuerte crisis socioeconómica como lo es Bolivia?__ 
 
Es importante ser conscientes de la situación del país referente a este tipo de vehículos. Esta, puede volverse bastante compleja. Por un lado la crisis económica hace que muchos ciudadanos no puedan permitirse uno de estos vehículos, ya que a pesar de sus beneficios a largo plazo, su costo es bastante elevado. Además, la cultura automovilística del país es particular. Muchas personas llegan a desconfiar de tecnologías nuevas, y tienden a preferir vehículos tradicionales con motor de combustión naturalmente aspirados, creyendo que los EVs  son menos duraderos y más costosos de mantener. A esto se le suman otros factores que hacen difícil la adopción, como la escasa cantidad de puestos de carga en el país, lo que limita bastante la viabilidad de estos vehículos. 

Incluso para quienes están dispuestos a hacer el cambio. Además que muchos mecánicos locales no están capacitados ni dispuestos a recibir vehículos eléctricos, ya que son tecnologías poco conocidas y temen dañar el sistema eléctrico u otro componente debido a la falta de experiencia. Finalmente las condiciones geográficas y viales del país representan un desafío porque muchos caminos no están pensados para ciertos modelos que pueden ser más delicados o con una suspensión más baja de lo habitual.

Dado el contexto del país, con una población cerrada a nuevas tecnologías, escasa infraestructura de carga y poca formación técnica para mantener estos vehículos, la adopción de vehículos eléctricos puede modelarse como un proceso influenciado por decisiones previas. Es decir, cada vez que alguien compra un EV, puede aumentar o disminuir la probabilidad de que otros personas también compren uno, en función de la experiencia, visibilidad y comentarios que genere esa decisión.

Precisamente este comportamiento es el que permite analizar la distribución Polya, donde la probabilidad de un resultado (comprar un EV) cambia en función de las decisiones previas. Esta propiedad es ideal para simular fenómenos de contagio social, donde la adopción de un bien depende de cuántas personas lo han adoptado anteriormente.

Por este motivo y al ser un ejemplo bastante interesante para analizar se decidió ilustrar cómo sería un posible análisis de esta situación con datos similares a los reales y realizar una demostración de este suceso. _(Cabe mencionar que los datos que se utilizarán NO son datos oficiales ni mucho menos es un análisis existente, fueron datos seleccionados tomando la referencia de datos reales, ya que la finalidad del trabajo NO es demostrar un ejemplo con datos reales. Sino, más bien, es un ejemplo que estamos proporcionando por lo interesante y llamativo que es)_

Supongamos que estamos analizando una comunidad urbana pequeña en Bolivia, como una zona de clase media en la ciudad de Cochabamba. Donde podrían llegar a popularizarse los vehículos eléctricos si se dan las condiciones correctas.

#### Planteamiento del problema:

Queremos modelar la adopción de vehículos eléctricos entre 100 personas. Inicialmente, solo 5 personas tienen predisposición a adquirir uno por factores como poder adquisitivo, conocimiento del tema o conciencia ecológica.

Además, sabemos que:
* Las personas que ven a sus vecinos o conocidos usar un EV tienden a sentirse más seguras de hacer lo mismo.
* Cada nueva adopción genera una influencia positiva (refuerzo) sobre la comunidad, porque genera confianza, se comparten experiencias o se visibilizan los beneficios. (Esto en un corto plazo, ya que los vehículos eléctricos en Bolivia recién están penetrando el mercado y un gran porcentaje de estos no han presentado fallas en un lapso de 1 año aproximadamente).

#### Parámetros:

Por ello, los parámetros que emplearemos para esta Distribución Polya son los siguientes:

* N = 100 (Número total de personas).
* M = 5 (Número de personas que tienen predisposición inicial a comprar un EV).
* n = 20 (20 pruebas para analizar cómo avanza la adopción).
* c = 2 (valor positivo, evidenciando el efecto de contagio social).

#### Resolución:

* Es importante destacar que el ejercicio no da un valor específico de "k", por ello tomaremos el valor de k = 3
1. Primer paso - Cálculo de coeficiente binomial:
$$
\binom{20}{3} = \frac{20 \times 19 \times 18}{3 \times 2 \times 1} = 1140
$$

2. Segundo paso - Producto Generalizado:
$$
5^{(3,2)} = 5 \times (5+2) \times (5+2+2) = 5 \times 7 \times 9 = 315 
$$

3. Tercer paso - Segundo Producto Generalizado:
$$
(N - M)^{(n-k,c)} = (100 - 5)^{(20-3,2)} = 95^{(17,2)}
$$
$$
95^{(17,2)} = 95 \times 97 \times 99 \times \dots \times (95 + 2 \times 16) = 95 \times 97 \times 99 \times \cdots \times 127
$$
Son 17 términos, aumentando de 2 en 2.

4. Cuarto Paso - Producto Generalizado:
$$
N^{(n,c)} = 100^{(20,2)}
$$
$$
100^{(20,2)} = 100 \times 102 \times 104 \times \cdots \times 138
$$
De nuevo, son 20 términos, cada uno incrementando de 2 en 2.

5. Quinto paso - Unir todo:
$$
P(X=3) = 1140 \times \frac{315 \times 95^{(17,2)}}{100^{(20,2)}}
$$
$$
P(X=3) \approx 0.2397
$$

#### Observaciones:
* El valor de P(X = 3) es aproximadamente 23,97%
* Se puede interpretar que hay un 24% de probabilidad de que en 20 intentos, 3 compren un vehículo eléctrico.
* Este fue el ejemplo planteado para ver cómo funciona y se aplica la distribución de Polya en un ejemplo de la actualidad y en el contexto nacional boliviano.

#### Conclusión: 
Este resultado evidencia un efecto positivo de influencia social en la adopción temprana de nuevas tecnologías dentro del grupo analizado.

#### Momentos Centrales: 
_Paso previo:_
$$
p = \frac{N}{M} = \frac{100}{5} = 0.05
$$

$$
q = 1 - p = 0.95
$$

1. Esperanza:

$$
E[X] = 20 \times 0.05 = 1
$$

2. Varianza:

$$
\mu_2 = \frac{20 \times 0.05 \times 0.95 \times (100 + 20 \times 2)}{100 + 2}
$$

Simplificando:

$$
\mu_2 = \frac{20 \times 0.05 \times 0.95 \times 140}{102}
$$

$$
\mu_2 = \frac{1 \times 0.95 \times 140}{102}
$$

$$
\mu_2 = \frac{133}{102}
$$

$$
\mu_2 \approx 1.3039
$$

3. Asimetría:

$$
\mu_3 = \frac{1.3039 \times (0.95 - 0.05) \times (100 + 2 \times 20)}{100 + 4}
$$

Simplificando:

$$
\mu_3 = \frac{1.3039 \times 0.9 \times 140}{104}
$$

$$
\mu_3 = \frac{1.3039 \times 126}{104}
$$

$$
\mu_3 = \frac{164.0914}{104}
$$

$$
\mu_3 \approx 1.5778
$$

4. Curtosis: 
* Paso 1 - Cálculo de términos intermedios:
$$N + nc = 100 + 20 \times 2 = 140$$

$$N^2 = 100^2 = 10000$$

$$3Nc(n-1) = 3 \times 100 \times 2 \times 19 = 11400$$

$$c^2(n-1)(3n-5) = 4 \times 19 \times 55 = 4180$$

* Paso 2 - Suma de los términos:
$$N^2 + 3Nc(n-1) + c^2(n-1)(3n-5) = 10000 + 11400 + 4180 = 25580$$

* Paso 3 - cálculo de $$pq(1-6pq)$$

$$pq(1-6pq) = 0.05 \times 0.95 \times (1 - 6 \times 0.05 \times 0.95)$$

Primero calculamos esto:
$$6pq = 6 \times 0.05 \times 0.95 = 0.285$$

$$1 - 0.285 = 0.715$$

$$pq(0.715) = 0.05 \times 0.95 \times 0.715 = 0.03396$$

* Paso 4 - Sustitución en la fórmula de la Curtosis \( \mu_4 \)

La fórmula es:

$$
\mu_4 = \frac{(N+nc)(N^2 + 3Nc(n-1) + c^2(n-1)(3n-5))pq(1-6pq)}{(N+c)^2(npq(N+nc))}
$$

Sustituimos:

$$
\mu_4 = \frac{140 \times 25580 \times 0.03396}{(100+2)^2 \times (20 \times 0.05 \times 0.95 \times 140)}
$$

Simplificando:

$$
\mu_4 = \frac{140 \times 25580 \times 0.03396}{10404 \times (1 \times 0.95 \times 140)}
$$

$$
\mu_4 = \frac{140 \times 25580 \times 0.03396}{10404 \times 133}
$$

* Paso - Cálculo del numerador y denominador

Numerador:

$$
140 \times 25580 \times 0.03396 \approx 121376.5
$$

Denominador:

$$
10404 \times 133 \approx 1383732
$$

Paso 6 - Resultado final

$$
\mu_4 = \frac{121376.5}{1383732}
$$

$$
\mu_4 \approx 0.0877
$$

### Gráfica de la PDF y CDF del ejemplo:


```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.special as sp

# rising factorial mejorada usando scipy
def rising_factorial(x, n, c):
    return sp.poch(x / c, n) * (c ** n)

# Parámetros
n = 20    # número de extracciones
M = 5     # éxitos totales en la población
N = 100   # tamaño de la población total
c = 2     # incremento en el reemplazo

# Valores de k
k = np.arange(0, n + 1)

# PDF
pdf = sp.comb(n, k) * (rising_factorial(M, k, c) * rising_factorial(N - M, n - k, c)) / rising_factorial(N, n, c)

# CDF
cdf = np.cumsum(pdf)

# Graficar
fig, ax = plt.subplots(1, 2, figsize=(14, 5))

# PDF
ax[0].vlines(k, 0, pdf, colors='royalblue', lw=3)
ax[0].plot(k, pdf, 'o', color='navy')
ax[0].set_title('Distribución de Pólya Generalizada (PDF)', fontsize=16)
ax[0].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[0].set_ylabel('P[X = k]', fontsize=14)
ax[0].grid(alpha=0.3)

# CDF
ax[1].plot(k, cdf, marker='o', color='crimson')
ax[1].set_title('Distribución de Pólya Generalizada (CDF)', fontsize=16)
ax[1].set_xlabel('Número de éxitos (k)', fontsize=14)
ax[1].set_ylabel('P[X ≤ k]', fontsize=14)
ax[1].grid(alpha=0.3)

plt.tight_layout()
plt.show()
```


    
![png](output_78_0.png)
    


### Interpretación de las gráficas:
* ##### PDF - Función de Probabilidad:

Muestra la probabilidad de obtener exactamente k éxitos y tiene la forma esperada:

* Mayor probabilidad para pocos éxitos (0, 1, 2) porque M = 5 (pocos éxitos en la población).

* Luego la probabilidad baja muy rápido (lo cual era predescible en un modelo tipo Pólya generalizado).

* ##### CDF - Función de Distribución Acumulativa:

Muestra la probabilidad de obtener hasta k éxitos (acumulado).

Se observa que parte de ≈0.4 (porque la probabilidad de 0 éxitos no es tan baja) y sube muy rápido a 1.

Se observa de igual forma que casi toda la probabilidad está acumulada en los primeros 4-5 éxitos. Eso también es lógico porque con M pequeño, es raro tener muchos éxitos.


```python

```
