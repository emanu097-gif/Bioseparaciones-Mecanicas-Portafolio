# Memoria de Cálculo: Ejercicios Resueltos de Sedimentación y Bioseparaciones

En esta sección se documenta la resolución analítica paso a paso de los problemas numéricos abordados en clase sobre velocidad terminal, criterio $K$ y sedimentación frenada.

---

## Ejercicio 1: Velocidad Terminal de Partículas de Polvo en Aire

### Enunciado
Calcule la velocidad terminal de precipitación de partículas de polvo con diámetro de $60\,\mu\text{m}$ en aire a $293.15\,\text{K}$ ($20\,^\circ\text{C}$) y $101.3\,\text{kPa}$. Las partículas de polvo pueden considerarse esféricas con una densidad de $1,280\,\text{kg/m}^3$.

### Datos
* Diámetro de partícula ($D_P$): $60\,\mu\text{m} = 60 \times 10^{-6}\,\text{m}$
* Densidad de la partícula ($\rho_P$): $1,280\,\text{kg/m}^3$
* Densidad del aire ($\rho$): $1.204\,\text{kg/m}^3$
* Viscosidad del aire ($\mu$): $1.81 \times 10^{-5}\,\text{Pa}\cdot\text{s}$
* Aceleración de la gravedad ($g$): $9.81\,\text{m/s}^2$

### 1. Evaluación del Criterio $K$
$$K = D_P \left[ \frac{g \cdot \rho \cdot (\rho_P - \rho)}{\mu^2} \right]^{1/3}$$

$$K = (60 \times 10^{-6}) \left[ \frac{(9.81)(1.204)(1280 - 1.204)}{(1.81 \times 10^{-5})^2} \right]^{1/3} = 2.18$$

* **Diagnóstico de régimen:** Como $K = 2.18 < 2.6$, la sedimentación se desarrolla en **Régimen Laminar** (Ley de Stokes).

### 2. Cálculo de la Velocidad Terminal ($v_t$)
$$v_t = \frac{g \cdot D_P^2 \cdot (\rho_P - \rho)}{18 \cdot \mu}$$

$$v_t = \frac{(9.81)(60 \times 10^{-6})^2 (1280 - 1.204)}{18 (1.81 \times 10^{-5})} = 0.138\,\text{m/s}$$

* **Resultado:** $v_t = 0.138\,\text{m/s}$

---

## Ejercicio 2: Velocidad Terminal de Gotas de Aceite en Aire

### Enunciado
Se desea precipitar gotas de aceite con diámetro de $20\,\mu\text{m}$ suspendidas en aire a una temperatura de $25\,^\circ\text{C}$ y $101.3\,\text{kPa}$ de presión. La densidad del aceite es $900\,\text{kg/m}^3$. Calcule la velocidad terminal de precipitación de las gotas.

### Datos
* Diámetro de la gota ($D_P$): $20\,\mu\text{m} = 20 \times 10^{-6}\,\text{m}$
* Densidad del aceite ($\rho_P$): $900\,\text{kg/m}^3$
* Densidad del aire ($\rho$): $1.19\,\text{kg/m}^3$
* Viscosidad del aire ($\mu$): $1.85 \times 10^{-5}\,\text{Pa}\cdot\text{s}$
* Aceleración de la gravedad ($g$): $9.81\,\text{m/s}^2$

### 1. Evaluación del Criterio $K$
$$K = D_P \left[ \frac{g \cdot \rho \cdot (\rho_P - \rho)}{\mu^2} \right]^{1/3}$$

$$K = (20 \times 10^{-6}) \left[ \frac{(9.81)(1.19)(900 - 1.19)}{(1.85 \times 10^{-5})^2} \right]^{1/3} = 0.62$$

* **Diagnóstico de régimen:** Como $K = 0.62 < 2.6$, el proceso se rige por la **Ley de Stokes**.

### 2. Cálculo de la Velocidad Terminal ($v_t$)
$$v_t = \frac{g \cdot D_P^2 \cdot (\rho_P - \rho)}{18 \cdot \mu}$$

$$v_t = \frac{(9.81)(20 \times 10^{-6})^2 (900 - 1.19)}{18 (1.85 \times 10^{-5})} = 0.01051\,\text{m/s}$$

* **Resultado:** $v_t = 0.01051\,\text{m/s}$

---

## Ejercicio 3: Sedimentación Frenada de Esferas de Vidrio en Agua (Método 1)

### Enunciado
Calcule la velocidad de precipitación de esferas de vidrio con diámetro $D_P = 1.554 \times 10^{-4}\,\text{m}$ en agua a $20\,^\circ\text{C}$. La suspensión contiene $60\%$ de sólidos en peso ($X_S = 0.60$). La densidad de las esferas de vidrio es $\rho_P = 2,467\,\text{kg/m}^3$.

### Datos
* Diámetro de partícula ($D_P$): $1.554 \times 10^{-4}\,\text{m}$
* Densidad de las esferas ($\rho_P$): $2,467\,\text{kg/m}^3$
* Densidad del agua a $20\,^\circ\text{C}$ ($\rho$): $998\,\text{kg/m}^3$
* Viscosidad del agua ($\mu$): $1.002 \times 10^{-3}\,\text{kg/m}\cdot\text{s}$
* Fracción masiva de sólidos ($X_S$): $0.60$

### 1. Determinación del Coeficiente de Arrastre ($C_D$) y Reynolds ($Re$)
$$C_D = \left[ \frac{4 \cdot g \cdot D_P^3 \cdot \rho \cdot (\rho_P - \rho)}{3 \cdot \mu^2} \right] = \frac{4 (9.81) (1.554 \times 10^{-4})^3 (998) (2467 - 998)}{3 (1.002 \times 10^{-3})^2} = 71.67$$

A partir del método gráfico logarítmico, se asume un valor de $Re = 2$:

$$v_t = \frac{Re \cdot \mu}{\rho \cdot D_P} = \frac{(2)(1.002 \times 10^{-3})}{(998)(1.554 \times 10^{-4})} = 0.0129\,\text{m/s}$$

### 2. Fracción de Volumen del Líquido ($\epsilon$) y Viscosidad Efectiva
Tomando la base de cálculo de densidad de suspensión ($V = \frac{m}{\rho}$):
$$\epsilon = \frac{\frac{40}{998}}{\frac{40}{998} + \frac{60}{2467}} = 0.6223$$

$$\psi_P = \frac{1}{10^{1.82(1 - \epsilon)}} = \frac{1}{10^{1.82(1 - 0.622)}} = 0.2051$$

### 3. Corrección por Sedimentación Frenada ($v_{tf}$)
$$v_{tf} = v_t \cdot (\epsilon^2 \cdot \psi_P) = (0.0129\,\text{m/s}) \cdot (0.622^2 \times 0.2051) = 1.0172 \times 10^{-3}\,\text{m/s}$$

* **Resultado:** $v_{tf} = 1.0172 \times 10^{-3}\,\text{m/s}$

---

## Ejercicio 4: Sedimentación Frenada de Esfalerita en Tetracloruro de Carbono

### Enunciado
Partículas de esfalerita con densidad de $4,000\,\text{kg/m}^3$ se asientan por la fuerza de gravedad en tetracloruro de carbono a $20\,^\circ\text{C}$, cuya densidad y viscosidad son de $1,594\,\text{kg/m}^3$ y $1.03\,\text{cP}$, respectivamente. El diámetro de las partículas de esfalerita es $0.1\,\text{mm}$. La fracción en volumen del tetracloruro es de $0.80$ ($\epsilon = 0.80$). Determine la velocidad de asentamiento de la esfalerita.

### Datos
* Densidad de la esfalerita ($\rho_P$): $4,000\,\text{kg/m}^3$
* Densidad del fluido ($\rho$): $1,594\,\text{kg/m}^3$
* Viscosidad del fluido ($\mu$): $1.03\,\text{cP} = 1.03 \times 10^{-3}\,\text{kg/m}\cdot\text{s}$
* Diámetro de partícula ($D_P$): $0.1\,\text{mm} = 1 \times 10^{-4}\,\text{m}$
* Fracción de volumen del líquido ($\epsilon$): $0.80$

### 1. Coeficiente de Arrastre Auxiliar ($C_D$) y Reynolds ($Re$)
$$C_D = \frac{4(9.81)(1 \times 10^{-4})^3 (1594)(4000 - 1594)}{3(1.03 \times 10^{-3})^2} = 47.93$$

Para $Re = 2$:
$$v_t = \frac{(2)(1.03 \times 10^{-3})}{(1594)(1 \times 10^{-4})} = 0.0129\,\text{m/s}$$

### 2. Factor de Corrección por Porosidad ($\psi_P$)
$$\psi_P = \frac{1}{10^{1.82(1 - \epsilon)}} = \frac{1}{10^{1.82(1 - 0.80)}} = 0.4325$$

### 3. Cálculo de la Velocidad Frenada ($v_{tf}$)
$$v_{tf} = (0.0129\,\text{m/s}) \cdot (0.80^2 \times 0.4325) = 3.5969 \times 10^{-3}\,\text{m/s}$$

* **Resultado:** $v_{tf} = 3.5969 \times 10^{-3}\,\text{m/s}$
