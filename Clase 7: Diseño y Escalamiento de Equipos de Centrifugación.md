#Diseño y Escalamiento de Equipos de Centrifugación

Para diseñar y operar equipos centrífugos (como las centrífugas tubulares), el objetivo es lograr que el tiempo de sedimentación de las partículas sea menor o igual al tiempo de residencia del fluido dentro de la cámara, el cual es impuesto por el gasto volumétrico[cite: 7]. 

Para lograrlo, debemos considerar variables clave del proceso[cite: 6]:
* **Del fluido y la partícula:** Propiedades del caldo, tamaño de partícula, densidad del caldo y de la partícula, y viscosidad del líquido[cite: 6].
* **Del equipo:** Velocidad de rotación, radios de giro, gasto o flujo de alimentación, y tiempo de residencia[cite: 6].

---

## Centrífugas Tubulares

### 1. Tiempo de Residencia ($t_r$)
La velocidad del fluido en sentido axial ($v_z$) se relaciona con el gasto volumétrico ($Q$) y el área transversal de flujo ($A$)[cite: 9]:
$$v_z = \frac{dz}{dt} = \frac{Q}{A}$$

Para un tazón cilíndrico, el área transversal es $A = \pi (R_o^2 - R_1^2)$[cite: 9]. Integrando la velocidad a lo largo de la altura $L$ del tazón, el tiempo de residencia queda como[cite: 10]:
$$t_r = \frac{\pi(R_o^2 - R_1^2)L}{Q}$$

### 2. Sedimentación al 100% y Gasto Volumétrico
Para que se recupere el 100% de las partículas, integramos la velocidad radial desde el radio interno ($R_1$) hasta el externo ($R_o$)[cite: 12]. El tiempo de sedimentación ($t_s$) se define como[cite: 13]:
$$t_s = \frac{18\mu}{d_p^2 \Delta\rho \omega^2} \ln\left(\frac{R_o}{R_1}\right) = \frac{g}{v_g \omega^2} \ln\left(\frac{R_o}{R_1}\right)$$

Al relacionar este tiempo con la capacidad de flujo, el gasto volumétrico de corte para retener el 100% de una partícula con velocidad terminal de caída libre $v_g$ es[cite: 14]:
$$Q = v_g \left[ \left(\frac{\pi\omega^2 L}{g}\right) \left(\frac{R_o^2 - R_1^2}{\ln(R_o/R_1)}\right) \right]$$
Donde $v_g = \frac{d_p^2 \Delta\rho g}{18\mu}$[cite: 14].

### 3. Sedimentación al 50% (Punto de Corte Práctico)
En bioseparaciones, es común diseñar para remover el 50% de las partículas de un tamaño de corte específico[cite: 15]. Las partículas se distribuyen uniformemente, por lo que la mitad de la masa estará dividida por un radio medio $R_{50}$[cite: 16]:
$$R_{50} = \left(\frac{R_o^2 + R_1^2}{2}\right)^{1/2}$$

El tiempo de sedimentación para este 50% de recuperación es[cite: 18]:
$$t_s^{50} = \frac{g}{v_g \omega^2} \ln\left[ \frac{R_o}{\left(\frac{R_o^2 + R_1^2}{2}\right)^{1/2}} \right]$$

El caudal volumétrico asociado a esta sedimentación parcial es[cite: 19]:
$$Q_{50} = 2v_g \left[ \left(\frac{\pi\omega^2 L}{g}\right) \left(\frac{R_o^2 - R_1^2}{\ln\left(\frac{2R_o^2}{R_o^2 + R_1^2}\right)}\right) \right]$$

---

## 💿 Centrífugas de Discos

En estos equipos, el caudal total se divide entre el número de discos ($n$), de forma que $Q_n = \frac{Q}{n}$[cite: 22]. El perfil de velocidad entre los discos es parabólico y el modelo del equipo nos da la siguiente relación para el 100% de sedimentación[cite: 23, 25]:
$$Q = v_g \left[ \frac{2\pi n \omega^2}{3g} (R_o^3 - R_1^3) \cot \theta \right]$$

---

## Escalamiento: El Factor Sigma ($\Sigma$)

El valor Sigma ($\Sigma$) representa el área equivalente de un sedimentador gravitacional que tendría la misma capacidad que la centrífuga[cite: 20]. Es la variable maestra para comparar y escalar equipos porque agrupa toda la geometría y la cinemática de la máquina:
$$Q = v_g \Sigma$$
$$Q_{50} = 2 v_g \Sigma$$

**Fórmulas del Factor Sigma para Tubulares:**
* **Para 100%:** $\Sigma = \left(\frac{\pi\omega^2 L}{g}\right) \left[ \frac{R_o^2 - R_1^2}{\ln(R_o/R_1)} \right]$[cite: 20]
* **Para 50%:** $\Sigma = \left(\frac{\pi\omega^2 L}{g}\right) \left[ \frac{R_o^2 - R_1^2}{\ln\left(\frac{2R_o^2}{R_o^2 + R_1^2}\right)} \right]$[cite: 21]

**Ley de Escalamiento:**
Si pasamos de un equipo a otro manteniendo la misma suspensión, la relación de capacidades es directa:
$$\frac{Q_1}{\Sigma_1} = \frac{Q_2}{\Sigma_2}$$

### Valores Típicos de Sigma ($\Sigma$ en m²)
| Tipo de Centrífuga | Rango de Factor $\Sigma$ |
| :--- | :--- |
| Intermitente | 20 - 200 |
| Decantadora | 150 - 2,500 |
| Tubular | 2,000 - 3,000 |
| Discos | 400 - 120,000 |

---

## Tiempo Equivalente ($Gt$)

Otra forma de transpolar parámetros entre diferentes centrífugas (especialmente de laboratorio) es usando la constante del producto del efecto centrífugo ($G$) y el tiempo de corrida ($t$)[cite: 28]:
$$G_1 t_1 = G_2 t_2$$

**Valores típicos de $Gt$ para organelos celulares[cite: 28]:**
* **Núcleo:** $G = 600$, $t = 5$ min $\rightarrow Gt = 3,000$ min
* **Mitocondria:** $G = 15,000$, $t = 5$ min $\rightarrow Gt = 75,000$ min
* **Ribosomas:** $G = 100,000$, $t = 60$ min $\rightarrow Gt = 6,000,000$ min
