# PROYECTO #5
### Modelos probabilisticos de Señales y Sistemas
#### Gabriel Araya Mora B80525
#### Felipe Rojas Vargas B87001
####  Monica Herrera Arguedas B23253


## Determinando de forma teórica del número **s** de servidores necesarios para cumplir el requisito del enunciado.

Se sabe que la ecuación para calcular $$\rho$$ es la siguiente:
$$\rho = \frac{\lambda}{s \cdot \nu}$$

  Ahora se sustituyen valores:
$$ \rho=\frac{7}{s\cdot 0.25}=\frac{28}{s} $$ 
#

Ahora se hace la suma de probabilidades de estado estable, y se considera la condición de ruptura menor:

$$ P = \sum_{i=101}^{\infty} (1 - \rho)\rho^{i}= 1 - \sum_{i=0}^{100} (1 - \rho)\rho^{i} = \rho^{101} $$

Se tiene un 95\% de probabilidad de tener una fila de 100 personas, además de tener un 5\% de probabilidad restante que genera la condición de ruptura. Entonces: 

$$  \rho^{101}\leq 0.05 $$

$$\left(\frac{28}{s} \right)^{101}\leq 0.05  \longrightarrow \left(\frac{28^{101}}{s^{101}} \right)\leq 0.05 \longrightarrow   \left(\frac{28^{101}}{0.05} \right)\leq   s^{101}$$

$$\longrightarrow \sqrt[101]{ \left(\frac{28^{101}}{0.05} \right)}\leq   s  \longrightarrow 28.843\leq   s $$

De lo anterior se concluye que el número mínimo de servidores es de 29, con el fin de cumplir la condición dada en el enunciado. 


## Modelo Markov desarrollado.

Basados en la teoria de colas y considerando los objetivos de diseño, se presenta el código desarrollado y los principales resultados. 

