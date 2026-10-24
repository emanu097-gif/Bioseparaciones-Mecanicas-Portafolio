#Teoría y Fundamentos de Centrifugación

Los separadores centrífugos operan bajo el principio de rotación de un objeto en torno a un eje central a una distancia radial constante. Al girar un recipiente cilíndrico, se desarrolla una fuerza igual y opuesta hacia las paredes del tazón (fuerza centrífuga), la cual causa que las partículas sedimenten a través de la fase líquida o se filtren a través de un lecho.

## ⚙️ Clasificación Operativa

La centrifugación se puede perfilar de acuerdo con la velocidad del rotor y el objetivo del proceso:

* **Por velocidad de rotación:**
  * **Baja velocidad:** $<10,000$ rpm.
  * **Alta velocidad:** $10,000 - 20,000$ rpm.
  * **Ultracentrifugación:** $>20,000$ rpm.
* **Por propósito:**
  * **Analítico:** Determinar propiedades físicas de las partículas en sedimentación.
  * **Preparativo:** Aislar partículas, células o moléculas de interés biológico.

---

## Modalidades de Separación según el Medio

### 1. Centrifugación Diferencial
La suspensión se somete a rotación y el destino de cada partícula depende estrictamente de su tamaño, forma y densidad. 
* Las partículas más grandes y densas sedimentan más rápido.
* Tras la corrida, obtenemos dos fases claras: un "pellet" (sedimento en el fondo) y un sobrenadante líquido.

### 2. Centrifugación en Gradiente de Densidad
Se emplea un medio continuo que varía su densidad a lo largo del tubo de la centrífuga (usualmente en rotores basculantes). Este gradiente puede ser *preformado* (mezclando soluciones escalonadas o continuas de sacarosa, por ejemplo) o *autoformado* (ultracentrifugando una sal como CsCl hasta que forma su propio gradiente).

Se subdivide en dos tipos fundamentales:

| Característica | Centrifugación Zonal | Centrifugación Isopícnica |
| :--- | :--- | :--- |
| **Mecanismo** | Separa por tamaño y forma (clasificación por velocidades de sedimentación). | Separa exclusivamente por densidad de la partícula[cite: 2]. |
| **Equilibrio** | No alcanza el equilibrio termodinámico de sedimentación[cite: 2]. | Sí alcanza el equilibrio de sedimentación[cite: 2]. |
| **Velocidad** | Más rápida[cite: 2]. | Lenta (requiere tiempo para alcanzar el equilibrio)[cite: 2]. |
| **Comportamiento** | Las partículas forman bandas discretas según qué tan rápido viajan por el tubo[cite: 2]. | Las partículas se estabilizan en la zona exacta donde la densidad del medio iguala la suya[cite: 2]. |

---

##Modelado Matemático y Ecuaciones de Diseño

El diseño y escalamiento de centrífugas (especialmente las de tazón cilíndrico tubular) requiere analizar la trayectoria de las partículas.

```text
Esquema de Centrífuga Tubular (Vista Transversal)
|-------------------------------------|
|               |  (Fase líquida)     |
|   Núcleo      |                     | 
|   de aire     |--> R                | L (Altura del tazón)
|               |                     |
|       r1      |       r2            |
|  (Interfase)  |  (Pared del tazón)  |
+-------------------------------------+
        ^ Eje de rotación (z)

### 1. Velocidad de Sedimentación Radial ($v_r$)
La velocidad a la que una partícula se mueve hacia la pared está dada por la ley de sedimentación adaptada al campo centrífugo:

$$v_r = \frac{dr}{dt} = \frac{d_p^2 \Delta\rho \omega^2 r}{18\mu}$$

### 2. Factor G o Efecto Centrífugo (RCF)
Es la relación entre la velocidad de sedimentación centrífuga y la gravitacional, muy útil para caracterizar equipos:

$$G = \frac{\omega^2 r}{g}$$

En la práctica, la Fuerza Centrífuga Relativa (RCF) se calcula directamente con las revoluciones por minuto (RPM) y el radio $r$ del rotor:

$$RCF = 1.118 \times 10^{-3} \times r \times (RPM)^2$$

### 3. Diámetro Crítico de Partícula ($D_{pc}$)
Se define como el diámetro de la partícula que viaja exactamente la mitad de la capa líquida $\frac{r_2 - r_1}{2}$ durante el tiempo de residencia disponible.
* Si la partícula tiene un diámetro mayor a $D_{pc}$, precipitará predominantemente en la pared del equipo.
* Las partículas más pequeñas saldrán arrastradas con el líquido.

A una velocidad de flujo crítico ($q_c$), la ecuación de diseño del equipo es:

$$q_c = \frac{\omega^2(\rho_p - \rho)D_{pc}^2}{18\mu \ln\left[\frac{2r_2}{r_1 + r_2}\right]} V$$

Donde el volumen de líquido ($V$) contenido en el tazón de altura $b$ es:

$$V = \pi b (r_2^2 - r_1^2)$$

### 4. Caudal, Tiempo de Residencia y Trayectoria
Para una partícula cualquiera de diámetro $D_p$, el caudal $q$ se relaciona geométricamente como:

$$q = \frac{\omega^2(\rho_p - \rho)D_p^2}{18\mu \ln(r_2/r_1)} V$$

El tiempo de residencia ($t_r$ o $\theta$) es simplemente la relación entre el volumen de retención y el caudal volumétrico $Q$:

$$t_r = \theta = \frac{V}{Q}$$

Si integramos la trayectoria, podemos calcular la distancia radial ($x$) recorrida por una partícula de tamaño $D_p$ en el tiempo disponible:

$$x = \frac{r \omega^2 (\rho_s - \rho)D_p^2}{18\mu} \cdot \frac{V}{Q}$$

$$\ln\left(\frac{r_2}{r_1}\right) = \frac{\omega^2(\rho_s - \rho)D_p^2}{18\mu} \theta = \frac{\omega^2(\rho_s - \rho)D_p^2}{18\mu} \cdot \frac{V}{Q}$$

También podemos estimar un diámetro de partícula de corte modificado ($D_p'$) basado en la geometría y operación:

$$D_p' = \sqrt{\frac{9\mu Q}{(\rho_s - \rho)\omega^2 V} \cdot \frac{r_2 - r_1}{r}}$$
