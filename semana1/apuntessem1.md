# 📘 Resumen – Semana 1: Ecuaciones Paramétricas y Longitud de Arco

## 📌 1. Introducción a las Ecuaciones Paramétricas

En el sistema de coordenadas cartesianas, una curva suele representarse como \(y = f(x)\). Sin embargo, muchas curvas —como las trayectorias de movimiento— se describen mejor mediante **ecuaciones paramétricas**, donde las coordenadas \(x\) e \(y\) se expresan en función de un tercer parámetro \(t\) (generalmente el tiempo o un ángulo).

Una curva paramétrica en el plano se define como:
\[
c(t) = \big(x(t),\ y(t)\big), \quad t \in I
\]
donde \(I\) es un intervalo real.

---

## 📌 2. Parametrización de Curvas Conocidas

### Circunferencia centrada en el origen (radio \(R\)):
\[
x = R\cos\theta,\quad y = R\sin\theta, \quad \theta \in [0, 2\pi)
\]
El parámetro \(\theta\) representa el ángulo polar. Si \(\theta\) recorre \([0, 2\pi)\), la circunferencia se recorre una vez en sentido antihorario.

### Circunferencia con centro \((a,b)\):
\[
x = a + R\cos\theta,\quad y = b + R\sin\theta
\]
Esta forma traslada el centro de la circunferencia desde el origen al punto \((a,b)\).

---

### Ejemplo 1 – Elipse:
La elipse \(\left(\frac{x}{a}\right)^2 + \left(\frac{y}{b}\right)^2 = 1\) se parametriza como:
\[
c(t) = (a\cos t,\ b\sin t), \quad t \in [0, 2\pi)
\]
Nótese que si \(a = b = R\), recuperamos la parametrización de la circunferencia.

---

### Ejemplo 2 – Cicloide (radio 1):
La cicloide es la curva trazada por un punto fijo en el borde de una rueda que rueda sin deslizar sobre una recta. Para una rueda de radio \(1\), las ecuaciones son:
\[
x(t) = t - \sin t,\quad y(t) = 1 - \cos t
\]
donde \(t\) es el ángulo de rotación (en radianes) desde la posición inicial.

---

## 📌 3. Recta Tangente a Curvas Paramétricas

Para una curva \(c(t) = (x(t), y(t))\) con \(x(t)\) e \(y(t)\) derivables, la **pendiente de la recta tangente** en el punto correspondiente a \(t\) viene dada por:
\[
\frac{dy}{dx} = \frac{y'(t)}{x'(t)}, \quad \text{siempre que } x'(t) \neq 0
\]
Esta expresión se obtiene aplicando la regla de la cadena: \(\frac{dy}{dt} = \frac{dy}{dx} \cdot \frac{dx}{dt}\).

### Tangente horizontal:
Ocurre cuando \(\frac{dy}{dx} = 0\), es decir, cuando \(y'(t) = 0\) y \(x'(t) \neq 0\).

---

### Ejemplo 3 – Tangente en \(t = 3\):
Dada \(c(t) = (t^2+1,\ t^3-4t)\):
- Derivadas: \(x'(t) = 2t,\ y'(t) = 3t^2 - 4\)
- Pendiente en \(t=3\):
  \[
  \frac{dy}{dx} = \frac{3(3)^2 - 4}{2(3)} = \frac{23}{6}
  \]
- Ecuación de la recta tangente (usando la forma punto-pendiente):  
  \[
  y - y(3) = m\,(x - x(3))
  \]
  Con \(x(3)=10,\ y(3)=15\):
  \[
  y - 15 = \frac{23}{6}(x - 10)
  \]

---

### Ejemplo 4 – Puntos con tangente horizontal:
Resolviendo \(y'(t) = 0\):
\[
3t^2 - 4 = 0 \quad \Rightarrow \quad t = \pm\frac{2}{\sqrt{3}}
\]
- Puntos correspondientes:
  \[
  c\left(\frac{2}{\sqrt{3}}\right) = \left(\frac{7}{3},\ -\frac{16}{3\sqrt{3}}\right)
  \]
  \[
  c\left(-\frac{2}{\sqrt{3}}\right) = \left(\frac{7}{3},\ \frac{16}{3\sqrt{3}}\right)
  \]

---

## 📌 4. Longitud de Arco

Si una curva paramétrica \(c(t) = (x(t), y(t))\) tiene derivadas continuas en \([a,b]\), su **longitud de arco** desde \(t=a\) hasta \(t=b\) es:
\[
s = \int_a^b \sqrt{x'(t)^2 + y'(t)^2}\, dt
\]
Esta fórmula surge de aproximar la curva por segmentos rectos y tomar el límite cuando la partición se hace infinitamente fina (integral de la norma del vector velocidad).

---

### Ejemplo 5 – Circunferencia (radio \(R\)):
\[
x = R\cos\theta,\ y = R\sin\theta, \quad \theta \in [0, 2\pi)
\]
\[
x'(\theta)^2 + y'(\theta)^2 = (-R\sin\theta)^2 + (R\cos\theta)^2 = R^2(\sin^2\theta + \cos^2\theta) = R^2
\]
\[
s = \int_0^{2\pi} \sqrt{R^2}\, d\theta = \int_0^{2\pi} R\, d\theta = 2\pi R
\]
Que coincide con la fórmula conocida de la circunferencia.

---

### Ejemplo 6 – Arco de cicloide (radio 2):
\[
x(t) = 2(t-\sin t),\ y(t) = 2(1-\cos t)
\]
\[
x'(t) = 2(1-\cos t),\ y'(t) = 2\sin t
\]
\[
x'(t)^2 + y'(t)^2 = 4(1-\cos t)^2 + 4\sin^2 t = 8 - 8\cos t = 16\sin^2\frac{t}{2}
\]
\[
s = \int_0^{2\pi} \sqrt{16\sin^2\frac{t}{2}}\, dt = \int_0^{2\pi} 4\left|\sin\frac{t}{2}\right| dt = 8\int_0^{\pi} \sin u\, du = 16
\]
donde se usó la sustitución \(u = t/2\) y la identidad trigonométrica \(1-\cos t = 2\sin^2(t/2)\).

---

## 📌 5. Celeridad (Rapidez)

La **celeridad** (magnitud de la velocidad) a lo largo de una curva paramétrica es la derivada de la longitud de arco respecto al parámetro:
\[
\frac{ds}{dt} = \sqrt{x'(t)^2 + y'(t)^2}
\]
Esta cantidad siempre es no negativa y representa qué tan rápido se recorre la curva.

---

### Ejemplo 7 – Celeridad en la cicloide (radio 4):
Para \(c(t) = (4t-4\sin t,\ 4-4\cos t)\):
\[
\frac{ds}{dt} = \sqrt{(4-4\cos t)^2 + (4\sin t)^2} = 8\left|\sin\frac{t}{2}\right|
\]
En los puntos donde la tangente es horizontal (\(t = (2k-1)\pi\)), la celeridad es:
\[
\frac{ds}{dt} = 8\left|\sin\frac{(2k-1)\pi}{2}\right| = 8
\]

---

## 📌 6. Área de Superficie de Revolución (Introducción)

Si una curva \(c(t) = (x(t), y(t))\) con \(y(t) \geq 0\) se gira alrededor del eje \(x\), el **área de la superficie generada** entre \(t=a\) y \(t=b\) es:
\[
S = 2\pi \int_a^b y(t) \sqrt{x'(t)^2 + y'(t)^2}\, dt
\]
Esta fórmula será desarrollada con más detalle en semanas posteriores.

---

> 📖 *Este resumen cubre los conceptos fundamentales de la Semana 1, sentando las bases para el estudio de curvas en el espacio, funciones vectoriales y aplicaciones en ingeniería.*
