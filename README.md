# CALCULADORAEDAD
# Calculadora de Edad — LPR 5° 3° A-B (1° Cuatrimestre 2026)

Actividad de revisión integral de lógica y algoritmos. El proyecto implementa,
en **Python** y en **C++**, un programa que calcula la edad exacta de una
persona a partir de su fecha de nacimiento, validando que la fecha ingresada
exista realmente en el calendario (control de años bisiestos y de la
cantidad de días de cada mes).

## Objetivo

Comparar la implementación de un mismo algoritmo en un lenguaje de tipado
dinámico e interpretado (Python) frente a un lenguaje de tipado estático y
compilado (C++), reforzando los conceptos de:

- Condicionales y operadores lógicos.
- Funciones / validación de datos (filtro de consistencia).
- Manejo de errores de entrada.
- Diferencias de declaración de variables entre ambos lenguajes.

## Estructura del proyecto

```
/CALCULADORAEDAD/
├── .gitignore
├── README.md
├── LICENSE
├── Docs/
│   └── InformeProyectoCalculadoraEdad.pdf
├── Proyecto_CPP/
│   └── CalculadoraEdad.cpp
└── Proyecto_Python/
    └── CalculadoraEdad.py
```

## Cómo ejecutar

### Python
```bash
cd Proyecto_Python
python3 CalculadoraEdad.py
```

### C++
```bash
cd Proyecto_CPP
g++ CalculadoraEdad.cpp -o CalculadoraEdad
./CalculadoraEdad
```

En ambos casos se debe ingresar el día, mes y año de nacimiento cuando el
programa lo solicite.

## Lógica principal

- `es_bisiesto` / `esBisiesto`: determina si un año es bisiesto con la regla
  `(anio % 4 == 0 y anio % 100 != 0) o (anio % 400 == 0)`.
- `es_fecha_valida` / `esFechaValida`: filtro de consistencia que rechaza
  fechas imposibles (mes fuera de 1-12, día fuera de rango según el mes,
  29 de febrero en año no bisiesto, etc.).
- Cálculo de edad: se resta el año de nacimiento al año actual y se ajusta
  restando 1 si la persona todavía no cumplió años en el mes/día actual.

## Autor

**Lucas Del Pino, Ulises Ferrari, Maximo Orue y Federico Mattia** — LPR 5° 3° A-B
