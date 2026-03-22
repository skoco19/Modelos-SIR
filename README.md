# TFG-bifurcaciones-SIR

Simulaciones numéricas en Python para los modelos epidemiológicos SIR, SIRS y SEIR con análisis de bifurcaciones.  
Trabajo Fin de Grado en Ingeniería Matemática — CUNEF Universidad, curso 2025–2026.

**Autora:** Sofía Koutsourais Collado  
**Director:** Jamie Michael Taylor

---

## Descripción

Este repositorio contiene el código numérico desarrollado para el Trabajo Fin de Grado
*"Análisis de bifurcaciones en modelos epidemiológicos tipo SIR"*.


---

## Estructura del repositorio

```
TFG-bifurcaciones-SIR/
│
├── simulaciones_SIR_SIRS_SEIR.ipynb   # Script principal de simulación
│
├── figuras/                         # Figuras generadas 
│   ├── evolucion_temporal.png
│   ├── bifurcacion_SIRS.png
│   └── comparacion_modelos.png
│
└── README.md
```

---

## Modelos

| Modelo | Compartimentos | Característica principal |
|--------|---------------|--------------------------|
| SIR    | S, I, R       | Modelo base clásico |
| SIRS   | S, I, R       | Pérdida de inmunidad (delta > 0) |
| SEIR   | S, E, I, R    | Período de incubación (1/sigma) |

En los tres modelos el número reproductivo básico es R_0 = beta / gamma.

---

## Simulaciones

El script genera tres figuras:

1. **`evolucion_temporal`** — Evolución temporal de los tres modelos para R_0 = 0,8 y R_0 = 2,5.
2. **`bifurcacion_SIRS`** — Diagrama de bifurcación del modelo SIRS: fracción de infectados en equilibrio I* en función de R_0.
3. **`comparacion_modelos`** — Comparación de la dinámica de los tres modelos para R_0 = 2,5.

### Parámetros empleados

| Parámetro | Valor | Descripción |
|-----------|-------|-------------|
| gamma     | 0,1   | Tasa de recuperación (período infeccioso medio: 10 días) |
| sigma     | 0,2   | Tasa de progresión (período de incubación medio: 5 días, solo SEIR) |
| delta     | 0,05  | Tasa de pérdida de inmunidad (solo SIRS) |
| I(0)      | 0,01  | Fracción inicial de infectados |
| S(0)      | 0,99  | Fracción inicial de susceptibles |

