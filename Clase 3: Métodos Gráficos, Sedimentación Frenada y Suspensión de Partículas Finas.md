# Clase 3: Métodos Gráficos, Sedimentación Frenada y Suspensión de Partículas Finas

## 1. Métodos Gráficos para la Determinación de la Velocidad Terminal ($v_t$)
Cuando el sistema no cumple con la Ley de Stokes o se encuentra en el régimen de transición ($2.6 \le K \le 68.9$), determinar la velocidad terminal por prueba y error resulta iterativo. Para agilizar el proceso, se utilizan ecuaciones de igualación logarítmica que relacionan el coeficiente de arrastre ($C_D$) y el número de Reynolds ($Re$).

### Caso A: Diámetro de Partícula ($D_P$) Conocido, Velocidad Terminal ($v_t$) Desconocida
Igualando las formas logarítmicas de la ecuación del coeficiente de arrastre y del número de Reynolds, se elimina la velocidad $v_t$, obteniendo la siguiente función lineal:

$$\log C_D = -2 \log Re + \log \left[ \frac{4 \cdot g \cdot D_P^3 \cdot \rho \cdot (\rho_P - \rho)}{3 \cdot \mu^2} \right]$$

* **Geometría de la recta:** En una gráfica $\log C_D$ vs $\log Re$, la ecuación representa una línea recta con **pendiente fija de $-2$**.
* **Punto de evaluación en $Re = 1$:** La recta pasa exactamente por el valor de ordenadas:
  $$C_D = \frac{4 \cdot g \cdot D_P^3 \cdot \rho \cdot (\rho_P - \rho)}{3 \cdot \mu^2}$$
* **Procedimiento:** Se traza la recta con pendiente $-2$ sobre la gráfica experimental de $C_D$ vs $Re$. El punto de intersección con la curva del factor de forma o esfericidad ($\psi$) de la partícula entrega el valor real del número de Reynolds ($Re$), a partir del cual se despeja directamente $v_t$.

### Caso B: Velocidad Terminal ($v_t$) Conocida, Diámetro de Partícula ($D_P$) Desconocido
Cuando se conoce la velocidad de asentamiento pero se requiere determinar el tamaño equivalente de la partícula, se aplica la relación logarítmica auxiliar:

$$\log C_D = \log Re + \log \left[ \frac{4 \cdot g \cdot (\rho_P - \rho) \cdot \mu}{3 \cdot \rho^2 \cdot v_t^3} \right]$$

* **Geometría de la recta:** En la gráfica logarítmica, representa una recta con **pendiente positiva fija de $+1$**.
* **Procedimiento:** La intersección con la curva de esfericidad ($\psi$) determina el número de Reynolds y, posteriormente, el diámetro de partícula $D_P$.

---

## 2. Coeficientes de Resistencia en Esferas No Rígidas (Gotas y Burbujas)
Cuando las partículas en suspensión son fluidos (gotas de líquido o burbujas de gas), el perfil de fricción se modifica debido a dos fenómenos hidrodinámicos:
1. **Circulación interna:** El flujo externo induce corrientes convectivas dentro de la gota o burbuja.
2. **Deformación geométrica:** Los esfuerzos de cizallamiento pueden alterar la esfericidad del cuerpo disperso.

### Comportamiento según el Número de Reynolds
* **Burbujas de aire en agua ($Re < 50$):** Presentan la misma curva de resistencia al flujo que las esferas rígidas.
* **Gotas líquidas en gases ($Re < 100$):** Su coeficiente de resistencia coincide con el de partículas esféricas rígidas.
* **Gotas pequeñas en líquidos inmiscibles ($Re \approx 10$):** Se comportan hidrodinámicamente como sólidos rígidos.
* **Gotas en líquidos ($10 < Re < 500$):** La circulación interna reduce el arrastre, logrando una velocidad terminal **mayor** que la de partículas sólidas equivalentes.

---

## 3. Precipitación Frenada (Hindered Settling)
En suspensiones concentradas, la elevada presencia de partículas genera interferencia mutua: los campos de velocidad se traslapan y el volumen de líquido desplazado genera una corriente ascendente significativa. La velocidad real de sedimentación resulta **menor** a la predicha por caída libre.

### Formulación Matemática y Factores de Corrección

#### 1. Viscosidad Efectiva de la Mezcla ($\mu_m$)
La viscosidad aparente del sistema $\mu_m$ es mayor que la del líquido puro $\mu$ y se corrige mediante un factor empírico adimensional $\psi_P$:

$$\mu_m = \frac{\mu}{\psi_P}$$

Donde el factor de corrección $\psi_P$ depende de la fracción de volumen del líquido ($\epsilon$):

$$\psi_P = \frac{1}{10^{1.82(1 - \epsilon)}}$$

La fracción de volumen de líquido ($\epsilon$) se calcula como:

$$\epsilon = \frac{V_L}{V_L + V_S}$$

#### 2. Densidad Efectiva de la Mezcla ($\rho_m$)
La densidad global de la suspensión engloba a la fase sólida y líquida:

$$\rho_m = \epsilon \cdot \rho + (1 - \epsilon) \cdot \rho_P$$

La diferencia efectiva de densidades resulta en:

$$\rho_P - \rho_m = \epsilon \cdot (\rho_P - \rho)$$

#### 3. Velocidad Terminal Frenada ($v_t$) en Régimen Laminar
Sustituyendo la viscosidad efectiva $\mu_m$ y la densidad modificada en la Ley de Stokes, se obtiene la expresión para flujo frenado:

$$v_t = \frac{g \cdot D_P^2 \cdot (\rho_P - \rho)}{18 \cdot \mu} \cdot (\epsilon^2 \cdot \psi_P)$$

#### 4. Número de Reynolds Modificado para Flux Frenado
$$Re = \frac{D_P \cdot v_t \cdot \rho_m}{\mu_m \cdot \epsilon} = \frac{D_P^3 \cdot g \cdot (\rho_P - \rho) \cdot \rho_m \cdot \epsilon \cdot \psi_P^2}{18 \cdot \mu^2}$$

*Condición de validez:* Si $Re < 1$, el asentamiento frenado ocurre dentro del intervalo de la Ley de Stokes.

---

## 4. Sedimentación en Suspensiones de Partículas Finas

### Correlación de Asentamiento Homogéneo
Para suspensiones homogéneas de partículas finas, la velocidad de asentamiento de la mezcla ($u_s$) se estima con la expresión:

$$u_s = u_t \cdot (\epsilon)^n$$

Donde $u_t$ es la velocidad terminal individual y $n$ es el exponente empírico de asentamiento.

### Efecto del Movimiento Browniano
En partículas muy pequeñas (escala micrométrica), las colisiones térmicas moleculares (movimiento browniano) contrarrestan la fuerza gravitacional:
* En partículas de pocos micrómetros, la velocidad de precipitación se reduce sustancialmente.
* En partículas menores a $0.1\,\mu\text{m}$, el movimiento browniano es predominante y la sedimentación gravitacional es nula.
* Para lograr la separación de estas suspensiones finas es técnicamente indispensable aplicar **fuerza centrífuga**.
