# DATASHEET — Antena de parche circular para la banda ISM de 2,4 GHz

**Antena microstrip de disco, alimentada por sonda coaxial (SMA), sobre FR-4**

Proyecto Integrador · Antenas y Radiopropagación  · Universidad de Pamplona ·

Autor: Cristian Andrey Mendoza Gamboa

## Descripción

Antena plana de parche circular que opera en el modo dominante TM₁₁ y radia de forma perpendicular al disco con polarización lineal. Está diseñada para la banda ISM de 2,4 GHz (uso libre sin licencia, como Wi-Fi y Bluetooth). Se fabricó en dos versiones con la misma geometría: **A** (grabado químico con ácido) y **B** (fresado CNC).

## Características principales

- Banda de operación: 2,400 – 2,4835 GHz
- Impedancia nominal de 50 Ω, conector SMA hembra de panel
- Polarización lineal
- Perfil delgado (≈ 1,67 mm) y bajo costo, sobre FR-4 estándar
- Plano de masa de 70 × 70 mm

## Especificaciones eléctricas

| Parámetro | Condición | Simulado | Medido A (ácido) | Medido B (CNC) |
| --- | --- | --- | --- | --- |
| Frecuencia de resonancia | Mínimo de S11 | 2,40 GHz | 2,408GHz | 2,451GHz |
| S11 en resonancia | Z₀ = 50 Ω | ≈ −28 dB | ≈ -35 dB | −23,70 dB |
| VSWR en resonancia | Z₀ = 50 Ω | ≈ 1,08 | 1,031 | 1,142 |
| Impedancia de entrada | A 2,4 GHz | ≈ 53,6 − j1,8 Ω | 48,36 + j0,849 Ω | 44,06 − j1,486 Ω |
| Ancho de banda (VSWR < 2) | S11 < −9,54 dB | ≈ 20 MHz (estimación analítica) | 20Mhz | 20Mhz |
| Impedancia nominal | — | 50 Ω | 50 Ω | 50 Ω |
| Potencia de entrada de prueba | Nivel del VNA | 0 dBm | 0 dBm | 0 dBm |

## Características de radiación

| Parámetro | Valor | Fuente |
| --- | --- | --- |
| Ganancia máxima | 2,69 dBi a 2,4 GHz | Simulación MATLAB |
| Dirección de máxima radiación | Perpendicular al disco (broadside) | Simulación MATLAB |
| Polarización | Lineal, orientada según el eje de la sonda (eje x) | Modo TM₁₁ |

La ganancia, el patrón y la directividad se obtienen por simulación; no se midieron en cámara anecoica.

## Especificaciones mecánicas

| Parámetro | Valor |
| --- | --- |
| Radio del disco (a) | 16,85 mm |
| Diámetro del disco | 33,70 mm |
| Placa (sustrato + plano de masa) | 70 × 70 mm |
| Posición de la sonda | 6,41 mm desde el centro del disco, sobre el eje x |
| Coordenadas del centro del disco (origen en una esquina) | (35,00; 35,00) mm |
| Coordenadas del orificio de alimentación | (41,41; 35,00) mm |
| Espesor total (sustrato + 2 capas de cobre) | ≈ 1,67 mm |

## Materiales

| Elemento | Especificación |
| --- | --- |
| Sustrato | FR-4 doble cara, εr ≈ 4,4, tan δ ≈ 0,02, espesor 1,6 mm |
| Cobre | 35 µm (1 oz/ft²), disco en la cara superior y plano de masa continuo en la inferior |
| Conector | SMA hembra de panel, 50 Ω, pin central soldado al disco a través del sustrato |
| Cuerpo y dieléctrico del conector | Latón con acabado niquelado o dorado, dieléctrico PTFE |

## Enlace de referencia (ecuación de Friis)

Para dos antenas iguales separadas 1,25 m (10 λ) con 0 dBm transmitidos, la pérdida de espacio libre a 2,4 GHz es L = 32,44 + 20 log(2400) + 20 log(0,00125) ≈ 42,0 dB. Con la ganancia simulada de 2,69 dBi por antena, la potencia recibida esperada es Pr = 0 + 2,69 + 2,69 − 42,0 ≈ **−36,6 dBm**.

## Notas

1. Los valores simulados provienen del modelo patchMicrostripCircular de MATLAB Antenna Toolbox (Corte 1). Las columnas medidas se completan con las medidas del VNA.
2. La frecuencia de resonancia es muy sensible a la fabricación: 0,1 mm de error en el radio desplaza la resonancia ≈ 14 MHz.
3. La permitividad real del FR-4 (4,3 a 4,6) puede mover la resonancia entre ≈ −53 MHz y ≈ +28 MHz respecto a la de diseño (εr = 4,4).
4. Medir en espacio libre, lejos de objetos metálicos y de la mano, y calibrar el VNA (Open, Short, Load) en el extremo del cable.
