# Blog de Evidencias: Bioseparaciones Mecánicas

## Unidad 1: Introducción a las Bioseparaciones y Bioprocesos Industriales

### 1. Contexto Industrial y Clasificación de las Operaciones
* **Upstream:** Preparación de medios, esterilización e inoculación en el biorreactor.
* **Downstream (Bioseparaciones):** Recuperación, aislamiento, purificación y formulación del bioproducto.
* **Ubicación del Producto:**
  * *Intracelular:* Requiere ruptura celular (homogeneización/lisis) + separación de restos celulares.
  * *Extracelular:* Requiere separación celular directa del caldo agotado.

### 2. Generaciones de Bioprocesos
| Característica | 1ª Generación | 2ª Generación | 3ª Generación |
| :--- | :--- | :--- | :--- |
| **Período** | Previo a 1975 | 1975 – 1985 | 1985 – Presente |
| **Células** | No recombinantes | Recombinantes (*E. coli*, levaduras) | Recombinantes / Mamífero |
| **Productos** | Solventes, antibióticos | Insulina, hGH | mAbs, EPO, Factor VIII |
| **Pureza / Valor**| Alta / Bajo | Muy Alta / Alto | Extremadamente Alta / Muy Alto |

### 3. Impacto Financiero y Secuencia de Operaciones
El downstream representa entre el **20% y el 80% del costo directo de producción** debido a bajas concentraciones iniciales, termolabilidad y requerimientos regulatorios de alta pureza.

**Secuencia Operativa:**
1. Generación y separación de partículas (Sedimentación, centrifugación, filtración).
2. Aislamiento del producto (Extracción, adsorción, ultrafiltración).
3. Purificación (Cromatografía de alta resolución, cristalización).
4. Acabado (Secado, liofilización).

---

## Unidad 2: Sedimentación y Clarificación — Fundamentos e Hidrodinámica

### 1. Conceptos Básicos y Balance de Fuerzas
* **Espesamiento:** Maximiza la concentración de sólidos en el fondo.
* **Clarificación:** Maximiza la limpieza del efluente líquido superior.

**Balance de Fuerzas sobre una esfera en caída:**
$$F_A = F_G - F_B - F_D = 0$$

* **Fuerza Gravitacional:** $F_G = V_P \cdot \rho_P \cdot g$
* **Fuerza Boyante:** $F_B = V_P \cdot \rho \cdot g$
* **Fuerza de Arrastre:** $F_D = C_D \cdot \frac{v^2}{2} \cdot \rho \cdot A_P$

### 2. Velocidad Terminal y Ley de Stokes
Despejando para la velocidad terminal constante ($v_t$):
$$v_t = \sqrt{ \frac{4 \cdot g \cdot D_P \cdot (\rho_P - \rho)}{3 \cdot C_D \cdot \rho} }$$

* **Régimen Laminar ($Re_P < 1$):** $C_D = 24 / Re_P$
  $$\text{Ley de Stokes: } v_t = \frac{g \cdot D_P^2 \cdot (\rho_P - \rho)}{18 \cdot \mu}$$
* **Régimen Turbulento ($1000 < Re_P < 2\times10^5$):** $C_D \approx 0.44$

### 3. Criterio Adimensional K
$$K = D_P \cdot \left[ \frac{g \cdot \rho \cdot (\rho_P - \rho)}{\mu^2} \right]^{1/3}$$
* $K < 2.6$: Régimen Laminar (Ley de Stokes).
* $2.6 \le K \le 68.9$: Régimen de Transición.
* $68.9 < K < 2360$: Régimen Turbulento.

---

## Unidad 3: Métodos Gráficos y Sedimentación Frenada

### 1. Método Gráfico para $v_t$
Se grafica la recta de pendiente $-2$ en escala logarítmica:
$$\log(C_D) = -2 \cdot \log(Re_P) + \log\left( \frac{4 \cdot g \cdot D_P^3 \cdot \rho \cdot (\rho_P - \rho)}{3 \cdot \mu^2} \right)$$
La intersección con la curva de esfericidad determina el par ordenado $(Re_P, C_D)$ para calcular $v_t$.

### 2. Sedimentación Frenada (Hindered Settling)
Para suspensiones concentradas donde las partículas interfieren entre sí:
* **Fracción de Líquido:** $\epsilon = \frac{V_L}{V_L + V_S}$
* **Densidad de Suspensión:** $\rho_m = \epsilon \cdot \rho + (1 - \epsilon) \cdot \rho_P$
* **Viscosidad de Suspensión:** $\mu_m = \frac{\mu}{\psi_P} \quad \text{con} \quad \psi_P = \frac{1}{10^{1.82(1-\epsilon)}}$

**Velocidad Frenada Corregida (Ley de Stokes Modificada):**
$$v_t = \frac{g \cdot D_P^2 \cdot (\rho_P - \rho)}{18 \cdot \mu} \cdot (\epsilon^2 \cdot \psi_P)$$

### 3. Partículas Finas y Efecto Browniano
En partículas $< 0.1\,\mu\text{m}$, el movimiento browniano supera la gravedad, requiriendo el uso de **centrifugación** para lograr la separación.
