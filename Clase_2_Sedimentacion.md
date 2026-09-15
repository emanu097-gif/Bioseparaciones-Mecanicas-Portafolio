# Clase 2: Sedimentación y Clarificación — Fundamentos e Hidrodinámica

## 1. Definición y Principios de la Operación Unitaria
La **sedimentación** es una operación unitaria mecánica en la que se aprovecha la fuerza de gravedad para separar componentes dispersos con densidades heterogéneas dentro de un fluido (sea líquido o gas).

### Clasificación de los Sistemas Dispersos
* **Suspensiones:** Sistemas donde partículas sólidas insolubles se encuentran dispersas en una fase líquida continua.
* **Emulsiones:** Dispersiones formadas por gotas de un líquido inmiscible dentro de otro líquido.

### Clasificación Operativa según el Propósito del Proceso
1. **Espesamiento (Thickening):** Modalidad cuyo objetivo principal es aumentar la concentración de la fase sólida dispersa, generando un lodo concentrado en la salida inferior del equipo.
2. **Clarificación (Clarification):** Modalidad enfocada en retirar bajas concentraciones de partículas sólidas suspendidas con el fin de obtener un efluente líquido remanente limpio o clarificado.

---

## 2. Variables de Proceso y Equipamiento
El desempeño e hidrodinámica de la sedimentación gravitacional están regulados por:
* La diferencia de densidades entre la partícula dispersa y el fluido continuo ($\rho_P - \rho$).
* El tamaño medio y distribución del diámetro de partícula ($D_P$).
* La viscosidad dinámica del fluido portador ($\mu$).
* La geometría de las partículas (las formas esféricas precipitan a mayor velocidad que geometrías discoidales, cilíndricas o laminares).
* La concentración de la fase dispersa (mecanismo de caída libre frente a caída frenada).
* La adición de agentes floculantes (sustancias que promueven el aglomerado de partículas incrementando su diámetro efectivo).

### Taxonomía General de Equipos de Sedimentación
* **Sistemas por Gravedad:**
  * *Sistemas Frenados:* Cribas fijas, cribas y mesas móviles, sedimentadores de placas inclinadas (lamella) y celdas de flotación.
  * *Sistemas Libres:* Elutriadores, sedimentadores de operación continua/intermitente y espesadores industriales.
* **Sistemas Centrífugos:**
  * *Pared Estacionaria:* Hidrociclones.
  * *Pared Rotatoria:* Centrífugas de discos, decantadores de rodillo (*scroll decanter*), centrífugas tubulares y centrífugas de cámaras múltiples.
* **Sistemas Electrostáticos:** Precipitadores y sedimentadores electrostáticos.

---

## 3. Balance de Fuerzas e Hidrodinámica de Caída

### Balance sobre una Partícula Rígida Esférica
Para una partícula esférica de diámetro $D_P$, masa $m$ y densidad $\rho_P$ que desciende dentro de un fluido con densidad $\rho$ y viscosidad $\mu$, intervienen tres fuerzas principales:

1. **Fuerza Gravitacional ($F_G$):** Actúa hacia abajo impulsando la caída.
   $$F_G = m \cdot g = V_P \cdot \rho_P \cdot g$$

2. **Fuerza Boyante o de Flotación ($F_B$):** Actúa hacia arriba en oposición a la gravedad (Principio de Arquímedes).
   $$F_B = V_P \cdot \rho \cdot g = \frac{m \cdot \rho \cdot g}{\rho_P}$$

3. **Fuerza de Arrastre o Resistencia ($F_D$):** Fuerza de fricción hidrodinámica ejercida por el fluido opuesta a la dirección del movimiento.
   $$F_D = C_D \cdot \left(\frac{v^2}{2}\right) \cdot \rho \cdot A_P$$
   Donde $C_D$ representa el coeficiente de arrastre adimensional y $A_P$ es el área proyectada de la partícula perpendiculares al flujo ($\frac{\pi D_P^2}{4}$ en esferas).

### Fuerza Resultante y Velocidad Terminal ($v_t$)
El comportamiento acelerado de la partícula se rige por:
$$m \cdot \frac{dv}{dt} = F_G - F_B - F_D = m \cdot g - \frac{m \cdot \rho \cdot g}{\rho_P} - C_D \cdot \left(\frac{v^2}{2}\right) \cdot \rho \cdot A_P$$

Dado que el período inicial de aceleración es insignificante (del orden de fracciones de segundo), la fuerza neta se iguala rápidamente a cero ($\frac{dv}{dt} = 0$), alcanzando la **velocidad terminal constante ($v_t$)**:

$$v_t = \sqrt{\frac{4 \cdot g \cdot D_P \cdot (\rho_P - \rho)}{3 \cdot C_D \cdot \rho}}$$

### Coeficiente de Arrastre ($C_D$) y Regímenes de Caída
El coeficiente de arrastre está determinado por el Número de Reynolds de la partícula ($Re = \frac{D_P \cdot v \cdot \rho}{\mu}$):

* **Régimen Laminar (Ley de Stokes: $Re < 1$):** Dominado por fuerzas viscosas. El coeficiente toma el valor de $C_D = \frac{24}{Re}$. Sustituyendo en la expresión general se obtiene la **Ley de Stokes**:
  $$v_t = \frac{g \cdot D_P^2 \cdot (\rho_P - \rho)}{18 \cdot \mu}$$

* **Régimen Turbulento (Ley de Newton: $1000 < Re < 2.0 \times 10^5$):** Dominado por fuerzas inerciales. El coeficiente permanece prácticamente constante en $C_D \approx 0.44$.

* **Efecto de Partículas Ultrafinas:** En partículas de diámetros submicrométricos, el movimiento browniano generado por colisiones térmicas moleculares supera a la fuerza de gravedad, impidiendo el asentamiento libre e imponiendo el uso de **fuerza centrífuga**.

---

## 4. Criterio Adimensional $K$
Para definir el régimen de caída aplicable cuando se desconoce la velocidad terminal $v_t$, se calcula el parámetro adimensional **Criterio $K$**:

$$K = D_P \cdot \left[ \frac{g \cdot \rho \cdot (\rho_P - \rho)}{\mu^2} \right]^{1/3}$$

### Criterios de Selección de Régimen:
* **$K < 2.6$:** El flujo es de tipo **laminar**. La velocidad terminal se calcula de forma directa con la **Ley de Stokes**.
* **$2.6 \le K \le 68.9$:** El flujo se ubica en la zona de **transición**. Requiere métodos de aproximación numérica iterativa o metodologías gráficas para determinar $C_D$ y $v_t$.
* **$68.9 < K < 2360$:** El flujo es de tipo **turbulento**. Se aplica la velocidad terminal bajo $C_D = 0.44$.

---

## 5. Dinámica de Sedimentación Batch (Ensayo de Columnas)
En una prueba intermitente de columna o probeta graduada con suspensión concentrada, se desarrollan cuatro regiones verticales a lo largo del tiempo
1. **Zona A:** Región superior con fluido clarificado libre de fase sólida.
2. **Zona B:** Región central que conserva la concentración de suspensión e identidad homogénea inicial.
3. **Zona C:** Región de transición caracterizada por un gradiente de concentración variable en tamaño y densidad.
4. **Zona D:** Región inferior compuesta por lodo acumulado en proceso de densificación.

### Punto Crítico de Sedimentación
El descenso de la interfase claro-suspensión es inicialmente constante. Al desaparecer la Zona B, se alcanza el **Punto Crítico (C)**, momento en el cual el mecanismo hidrodinámico de caída libre/frenada cesa y da paso a la **consolidación y compresión mecánica del lodo acumulado**, extendiendo considerablemente el tiempo necesario para lograr mayor clarificación.
