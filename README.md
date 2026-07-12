[README.md](https://github.com/user-attachments/files/29943587/README.md)
# isr-dgii-2026
Tarea flujo de control parte 2
# Cálculo de ISR (Impuesto Sobre la Renta) - República Dominicana

Programa en C++ que lee el sueldo bruto mensual de un empleado y calcula el
Impuesto Sobre la Renta (ISR) que corresponde retener, según la escala
salarial vigente publicada por la DGII (Dirección General de Impuestos
Internos) para el año fiscal 2026.

## Integrantes

| Nombre | Matrícula |
|---|---|
| Keury Alexander López Castro | 2025-1868 |
| Pedro Junior Edubique Hernández | 2025-1422 |
| Fausto Junior Moreno Santana | 2025-1582 |

**Materia:** Lógica de Programación — Sección INF-011-1
Profesor(a): Gamalier Reyes Del Carmen
**Universidad:** Universidad Central del Este (UCE)

## Descripción

El programa solicita al usuario el sueldo bruto mensual de un empleado y,
usando la escala progresiva del ISR vigente para el año 2026 (Resolución
DGII No. DDG-AR1-2026-00001, con base legal en el Art. 296 del Código
Tributario, Ley 11-92), calcula cuánto se le debería retener de ISR cada mes.

### Escala de ISR aplicada (montos anuales)

| Renta anual (RD$) | Tasa aplicada |
|---|---|
| 0.01 — 416,220.00 | Exento (0%) |
| 416,220.01 — 624,329.00 | 15% sobre el excedente de RD$416,220.00 |
| 624,329.01 — 867,123.00 | RD$31,216.00 + 20% sobre el excedente de RD$624,329.00 |
| Más de 867,123.00 | RD$79,776.00 + 25% sobre el excedente de RD$867,123.00 |

Esta escala no se ha ajustado por inflación desde el año 2018, tal y como
lo confirma la propia DGII para el ejercicio fiscal 2026.

### Lógica del programa

1. Se lee el sueldo bruto **mensual** ingresado por el usuario.
2. Se anualiza (sueldo mensual × 12), ya que la escala de la DGII es anual.
3. Se ubica el tramo correspondiente y se calcula el ISR anual.
4. El ISR anual se divide entre 12 para obtener la retención mensual.
5. Si el sueldo anualizado no supera el mínimo exento (RD$416,220.00), se
   muestra **0 (N/A)**, indicando que no aplica ninguna retención.

## Cómo compilar y ejecutar

```bash
g++ -o calculo_isr calculo_isr.cpp
./calculo_isr
```

## Ejemplos de ejecución

### Escenario 1: Sueldo exento (no aplica ISR)

Sueldo mensual: RD$30,000.00 (RD$360,000.00 anual, por debajo del mínimo exento)

_(Captura de pantalla aquí)_

### Escenario 2: Sueldo en el tramo del 20%

Sueldo mensual: RD$60,000.00 (RD$720,000.00 anual)

_(Captura de pantalla aquí)_

### Escenario 3: Sueldo en el tramo del 25%

Sueldo mensual: RD$120,000.00 (RD$1,440,000.00 anual)

_(Captura de pantalla aquí)_

## Fuente de la escala

- DGII — Resolución No. DDG-AR1-2026-00001, escala del ISR para personas
  físicas vigente durante el año fiscal 2026.
- Código Tributario de la República Dominicana (Ley 11-92), Art. 296.
<img width="1489" height="805" alt="image" src="https://github.com/user-attachments/assets/6119488f-973f-4298-bece-a96e802a36e4" />
<img width="1474" height="601" alt="image" src="https://github.com/user-attachments/assets/37bc2356-8b99-4dfe-a057-0ed6b630fedb" />
<img width="1141" height="337" alt="image" src="https://github.com/user-attachments/assets/e017ddaf-4b1a-4bb3-9876-e1c38b90996d" />
<img width="1677" height="591" alt="image" src="https://github.com/user-attachments/assets/90ce2437-5af8-4b32-9ca7-54d518fd009e" />
<img width="985" height="388" alt="image" src="https://github.com/user-attachments/assets/c1287b75-d34a-4d04-844b-4f7be712b3c4" />
<img width="1714" height="658" alt="image" src="https://github.com/user-attachments/assets/8e7c0415-08b5-4f9a-8698-4061a9717465" />
<img width="1717" height="657" alt="image" src="https://github.com/user-attachments/assets/da1d339f-1719-4562-8750-f6f45783799b" />







