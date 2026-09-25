# Clase 4: Clasificación Hidráulica, Efectos de Pared y Precipitación Diferencial

En esta sección se revisan las desviaciones de la sedimentación libre ideal debido a límites físicos del recipiente (**efecto de pared**) y se analiza la teoría de **clasificación hidráulica y sedimentación diferencial** para mezclas binarias de partículas.

---

## 1. Efecto de la Pared sobre la Sedimentación Libre

Cuando el diámetro de una partícula ($D_P$) no es despreciable frente al diámetro de la columna o recipiente ($D_W$), la presencia de las paredes rígidas genera una restricción al flujo ascendente de fluido desplazado. Esto incrementa la fricción y disminuye la velocidad terminal real de sedimentación ($v_t$).

Para corregir esta desviación cuando $D_P / D_W > 0.05$, se multiplica la velocidad terminal teórica por un factor de corrección empírico ($k_W$):

$$v_{t,\text{real}} = v_t \cdot k_W$$

### Factores de Corrección según el Régimen Hidrodinámico

* **Régimen Laminar (Ley de Stokes):**
  $$k_W = \frac{1}{1 + 2.1 \left( \frac{D_P}{D_W} \right)}$$

* **Régimen de Transición y Turbulento:**
  $$k_W' = \frac{1 - \left( \frac{D_P}{D_W} \right)^2}{\sqrt{1 + \left( \frac{D_P}{D_W} \right)^4}}$$

---

## 2. Clasificación Hidráulica y Precipitación Diferencial

La **clasificación** es la separación de partículas en fracciones según su velocidad de precipitación dentro de un fluido. En el procesado de bioproductos y sólidos se utilizan dos métodos principales:

### A. Métodos de Hundimiento y Flotación
Utilizan un fluido o medio con densidad intermedia ($\rho$) entre el sólido pesado ($\rho_{PA}$) y el ligero ($\rho_{PB}$):

$$\rho_{PB} < \rho < \rho_{PA}$$

* Las partículas ligeras ascienden hacia la superficie.
* Las partículas pesadas sedimentan en el fondo.
* **Ventaja:** La separación es independiente del tamaño de partícula y se basa únicamente en las densidades relativas. Se suelen usar **seudolíquidos** (suspensiones acuosas estables de sólidos finos de alta densidad).

### B. Métodos de Precipitación Diferencial
Ocurren en un líquido cuya densidad es menor a la de ambos sólidos ($\rho < \rho_{PB} < \rho_{PA}$). Ambas sustancias sedimentan, pero a velocidades diferentes.

Si el intervalo de tamaños de la mezcla es amplio (de $D_{P1}$ a $D_{P4}$), se presenta un traslape o solapamiento: las partículas pesadas pequeñas precipitan a la misma velocidad que las partículas ligeras grandes.

Aquí tienes el código en Markdown puro listo para que lo copies, lo pegues directamente en el archivo `README.md` de tu carpeta del repositorio de GitHub y se renderice sin ningún problema con las fórmulas matematicas y tablas:

```



```

Velocidad Terminal (vt)
^
|          / Material A (Pesado, rho_PA)
|         /
vt_max|--------/-----/ Material B (Ligero, rho_PB)
|       /|    /|
|      / |   / |
vt_min|-----/- |  /  |
|    /|  | /   |
+---+-+--+-+---+---> Diámetro de Partícula (Dp)
Dp1 Dp2 Dp3 Dp4

```

```

## 3. Relación de Diámetros Equivalentes

Al igualar las velocidades terminales de dos materiales distintos ($v_{tA} = v_{tB}$), se establece la relación entre los diámetros de las partículas de $A$ y $B$ que sedimentan juntas:

$$\frac{D_{PA}}{D_{PB}} = \left( \frac{\rho_{PB} - \rho}{\rho_{PA} - \rho} \right)^n \left( \frac{C_{DA}}{C_{DB}} \right)^{1/2}$$

El exponente $n$ depende del régimen hidrodinámico en el que opera el equipo:

| Régimen Hidrodinámico | Exponente $n$ | Relación de Diámetros Equivalentes |
| :--- | :--- | :--- |
| **Laminar (Stokes)** | $n = 0.5$ | $\frac{D_{PA}}{D_{PB}} = \left( \frac{\rho_{PB} - \rho}{\rho_{PA} - \rho} \right)^{0.5}$ |
| **Transición** | $0.5 < n < 1.0$ | $\frac{D_{PA}}{D_{PB}} = \left( \frac{\rho_{PB} - \rho}{\rho_{PA} - \rho} \right)^n$ |
| **Turbulento (Newton)** | $n = 1.0$ | $\frac{D_{PA}}{D_{PB}} = \left( \frac{\rho_{PB} - \rho}{\rho_{PA} - \rho} \right)^{1.0}$ |

---

## 4. Ejercicios Resueltos

### **Ejercicio 1: Clasificación de Sílice y Galena en Régimen Laminar**

**Enunciado:**  
Se desea separar una mezcla de partículas de sílice (B) y galena (A) con tamaños entre $5.21 \times 10^{-6}\text{ m}$ y $2.50 \times 10^{-5}\text{ m}$ por clasificación hidráulica en agua a $20\,^\circ\text{C}$ ($\rho = 998.2\text{ kg/m}^3$, $\mu = 1.002 \times 10^{-3}\text{ Pa}\cdot\text{s}$).
* Densidad de la galena ($\rho_{PA}$): $7,500\text{ kg/m}^3$
* Densidad de la sílice ($\rho_{PB}$): $2,650\text{ kg/m}^3$

Asumiendo partículas esféricas en régimen laminar, determine las fracciones de producto resultantes.

#### **Desarrollo:**

1. **Relación de diámetros equidistantes ($n = 0.5$):**
   $$\frac{D_{PA}}{D_{PB}} = \left( \frac{2650 - 998.2}{7500 - 998.2} \right)^{0.5} = \left( \frac{1651.8}{6501.8} \right)^{0.5} = \mathbf{0.504}$$

2. **Cálculo de diámetros límite de mezcla:**
   * Diámetro de galena que iguala a la sílice más pequeña ($D_{P1} = 5.21 \times 10^{-6}\text{ m}$):
     $$D_{PA}' = 0.504 \cdot (5.21 \times 10^{-6}\text{ m}) = \mathbf{2.626 \times 10^{-6}\text{ m}}$$
   * Diámetro de sílice que iguala a la galena más grande ($D_{P4} = 2.50 \times 10^{-5}\text{ m}$):
     $$D_{PB}' = \frac{2.50 \times 10^{-5}\text{ m}}{0.504} = \mathbf{4.960 \times 10^{-5}\text{ m}}$$

3. **Fracciones Obtenidas:**
   * **Fracción 1 (Galena pura):** Partículas de galena desde $1.26 \times 10^{-5}\text{ m}$ hasta $2.50 \times 10^{-5}\text{ m}$.
   * **Fracción 2 (Mezcla binaria):** Galena ($5.21 \times 10^{-6}\text{ m}$ a $1.26 \times 10^{-5}\text{ m}$) y Sílice ($1.03 \times 10^{-5}\text{ m}$ a $2.50 \times 10^{-5}\text{ m}$).
   * **Fracción 3 (Sílice pura):** Partículas de sílice desde $5.21 \times 10^{-6}\text{ m}$ hasta $1.03 \times 10^{-5}\text{ m}$.

---

### **Ejercicio 2: Clasificador Hidráulico con Esfericidad ($\psi = 0.806$)**

**Enunciado:**  
Una mezcla de sílice ($2,650\text{ kg/m}^3$) y galena ($7,500\text{ kg/m}^3$) con tamaños entre $0.008\text{ cm}$ y $0.07\text{ cm}$ se separa en un clasificador. Las partículas poseen una esfericidad $\psi = 0.806$.
* **a)** Determine la velocidad ascendente del agua para obtener un producto de galena pura en el fondo.
* **b)** Calcule el rango de tamaño de la galena pura obtenida.

#### **Desarrollo:**

1. **Inciso a (Velocidad del fluido):**  
   Para evitar que la sílice precipite al fondo, la velocidad del agua debe igualar la velocidad terminal de la partícula de sílice más grande ($D_{PB,\text{max}} = 0.07\text{ cm} = 7 \times 10^{-4}\text{ m}$).  
   
   Evaluando el criterio $K$ para la partícula de $7 \times 10^{-4}\text{ m}$:
   $$K = D_P \cdot \left[ \frac{g \cdot \rho \cdot (\rho_{PB} - \rho)}{\mu^2} \right]^{1/3} \approx 13.56$$

   Dado que $2.6 \le K \le 68.9$, el sistema opera en **Régimen de Transición**. Aplicando el método gráfico/correlación ajustada por esfericidad $\psi = 0.806$:

   $$v_{\text{agua}} = v_{t,\text{sílice max}} \approx \mathbf{0.046 \text{ m/s}} \quad (4.6 \text{ cm/s})$$

2. **Inciso b (Rango del producto puro):**  
   El tamaño mínimo de galena que sedimenta a esta velocidad se calcula con la relación de transición ($n \approx 0.6$):
   $$\frac{D_{PA}^*}{D_{PB,\text{max}}} = \left( \frac{1651.8}{6501.8} \right)^{0.6} \approx 0.438$$

   $$D_{PA}^* = 0.438 \cdot (0.07\text{ cm}) = \mathbf{0.0307 \text{ cm}}$$

   **Resultado:** El producto de galena pura abarca diámetros desde **$0.0307\text{ cm}$ hasta $0.0700\text{ cm}$**.

```
