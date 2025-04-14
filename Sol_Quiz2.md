
# ✅ Solución al problema del tanque cilíndrico (con $c = 1$)

## **Datos del problema**

- Tanque: **cilindro vertical**
- Altura inicial del agua: $H = 20 \, \text{m}$
- Radio del tanque: $R = 2 \, \text{m}$  
  → Área de la base: $A = \pi R^2 = 4\pi \, \text{m}^2$
- Radio del orificio: $r = 0.03 \, \text{m}$  
  → Área del orificio: $a = \pi r^2 = 0.0009\pi \, \text{m}^2$
- Coeficiente de descarga: $c = 1$
- Gravedad: $g = 9.8 \, \text{m/s}^2$

---

## **a) Ecuación diferencial y condición inicial**

La ecuación que rige el vaciado según la **ley de Torricelli** es:

$$
\frac{dV}{dt} = -c a \sqrt{2gh}
$$

Como el volumen del cilindro es $V = A h$, se tiene:

$$
A \frac{dh}{dt} = -c a \sqrt{2gh} \quad \Rightarrow \quad \frac{dh}{dt} = -\frac{c a}{A} \sqrt{2g h}
$$

Sustituyendo los valores conocidos:

$$
\frac{dh}{dt} = -\frac{1 \cdot 0.0009\pi}{4\pi} \sqrt{2 \cdot 9.8 \cdot h}
= -\frac{0.0009}{4} \sqrt{19.6 h}
= -0.000225 \sqrt{19.6 h}
$$

**Condición inicial:**  
$$
h(0) = 20
$$

---

## **b) ¿Toma el mismo tiempo vaciar la mitad superior que la mitad inferior?**

**No.**  
El flujo de salida depende de $\sqrt{h}$, por lo que al principio el caudal es más alto, y disminuye con la altura. Por tanto:

> **La primera mitad del volumen se vacía más rápido que la segunda.**

---

## **c) ¿Cuánto tiempo tarda en llegar a $\frac{1}{4}$ de la altura inicial?**

Queremos hallar el tiempo $t$ tal que $h(t) = 5$.

Partimos de:

$$
\frac{dh}{dt} = -0.000225 \sqrt{19.6 h}
$$

Separando variables:

$$
\frac{1}{\sqrt{h}} \, dh = -0.000225 \sqrt{19.6} \, dt
\Rightarrow \int_{20}^{5} \frac{1}{\sqrt{h}} \, dh = -0.0009961 \int_{0}^{t} dt
$$

Cálculo numérico:

$$
\sqrt{19.6} \approx 4.4272 \quad \Rightarrow \quad k = 0.000225 \cdot 4.4272 \approx 0.0009961
$$

$$
2(\sqrt{5} - \sqrt{20}) = -0.0009961 \cdot t
\Rightarrow 2(2.236 - 4.472) = -0.0009961 \cdot t
\Rightarrow -4.472 = -0.0009961 \cdot t
$$

$$
t \approx \frac{4.472}{0.0009961} \approx \boxed{4490.7 \, \text{segundos}} \approx \boxed{1 \, \text{hora y 15 minutos}}
$$

---

## 🧮 **Resumen de fórmula generalizada para este caso**

$$
\boxed{
\frac{dh}{dt} = -\left(\frac{c \cdot a}{A}\right) \sqrt{2g h}
}
\quad \text{con } h(0) = H
$$

