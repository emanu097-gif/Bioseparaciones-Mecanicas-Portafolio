#Centrifugación en el Procesamiento de Bioproductos

Cuando lidiamos con caldos biológicos que son una pesadilla para filtrar, o cuando generar demasiados desechos contaminantes no es una opción, la centrifugación entra al quite como una de nuestras operaciones unitarias principales. 

Básicamente, aprovechamos el movimiento giratorio para separar sustancias basándonos en su diferencia de densidad. 

## 🦠 ¿Para qué la usamos en biotecnología?

* **Recuperación de células:** Separación de la biomasa directamente del caldo de cultivo.
* **Limpieza celular:** Remoción de debris (desechos celulares) después de procesos de rompimiento celular.
* **Aislamiento de proteínas y productos insolubles:** Súper útil para separar precipitados proteicos o cuerpos de inclusión. 
  * *Nota técnica:* Los cuerpos de inclusión suelen ser partículas muy densas (1.3 a 1.5 g/mL) y pequeñitas (0.3 a 1 µm) que podemos aislar mediante centrifugación en dos o tres etapas, apoyándonos con agua de lavado y detergentes.

## ⚙️ Fundamentos: Teoría de la Sedimentación

Toda la base física detrás de esto (y que nos sirve para dimensionar equipos) viene de la teoría de sedimentación, gobernada por la Ley de Stokes. 

Para partículas que tardarían una eternidad en decantar por simple gravedad en un tanque, el equipo centrífugo genera velocidades de rotación altísimas que multiplican el efecto de la diferencia de densidades entre el sólido y el líquido. Podemos asumir que los caldos biológicos, al ser suspensiones diluidas, se comportan bajo esta ley.

### 1. Sedimentación por gravedad (Caída libre)
Bajo la Ley de Stokes clásica, la velocidad terminal o de caída ($v_t$) es proporcional al cuadrado del diámetro de la partícula y a la diferencia de densidades:

$$v_t = \frac{g D_P^2 (\rho_P - \rho)}{18\mu}$$

Donde:
* $v_t$ = Velocidad de sedimentación gravitacional (m/s)
* $g$ = Aceleración de la gravedad (9.81 m/s²)
* $D_P$ = Diámetro de la partícula (m)
* $\rho_P$ = Densidad de la partícula (kg/m³)
* $\rho$ = Densidad del fluido (kg/m³)
* $\mu$ = Viscosidad dinámica del fluido (Pa·s)

### 2. Sedimentación Centrífuga
En una centrífuga, cambiamos la aceleración de la gravedad ($g$) por la aceleración centrífuga ($\omega^2 r$), lo que dispara la magnitud de las fuerzas de precipitación y nos permite atrapar partículas muchísimo más pequeñas. La velocidad de sedimentación centrífuga ($v_\omega$) queda así:

$$v_\omega = \frac{d_p^2 \Delta\rho \omega^2 r}{18\mu}$$

Donde:
* $v_\omega$ = Velocidad de sedimentación centrífuga (m/s)
* $d_p$ = Diámetro de la partícula (m)
* $\Delta\rho$ = Diferencia de densidades $\rho_P - \rho$ (kg/m³)
* $\omega$ = Velocidad angular (rad/s)
* $r$ = Radio de giro o distancia desde el eje de rotación (m)

---

## 🔬 Clasificación de Equipos

A nivel laboratorio, solemos trabajar con rotores de ángulo fijo o de cestas oscilantes (swing-bucket), usando tubos estándar como los Eppendorf (1.5 mL) o Falcon (50 mL) de fondo cónico o redondo. 

Pero cuando escalamos a nivel industrial, la clasificación se divide según su principio de operación. Aquí tienes el mapa mental de los equipos:

```text
Centrífugas Industriales
│
├── Filtrantes
│
└── Sedimentadoras
    ├── Tubular
    ├── Cámara múltiple
    ├── Tazón sólido
    ├── Decantadoras
    └── Discos
