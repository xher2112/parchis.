README 

---

## Funcionalidades

- Tablero con 68 casillas externas y 8 internas por jugador
- Turnos por jugador con lanzamiento de dados y selección de fichas
- Reglas implementadas:
  - Salida con 5
  - Captura de fichas enemigas (bonificación de 20 pasos)
  - Movimientos extra por captura o entrada a la vía interna
  - Bloqueo con dos fichas del mismo color
  - Penalización por tres pares consecutivos
  - Entrada a vía interna y meta solo con número exacto
- Interfaz gráfica con:
  - Tablero visual
  - Clics para seleccionar dados y fichas
  - Panel informativo
  - Botones de "Lanzar dados" y "Terminar turno"

---

## Requisitos

- Python 3.6 o superior
- Biblioteca Pygame

Instalación de dependencias:
```bash
pip install pygame
```

---

## Cómo Ejecutar

1. Descarga el archivo `parques.py` o clona este repositorio.
2. Ejecuta el juego con el siguiente comando:
```bash
python parques.py
```

---

## Controles

- Clic izquierdo: seleccionar ficha o dado
- Botón "Lanzar dados": iniciar el turno
- Botón "Terminar turno": pasar al siguiente jugador

---

## Estructura del Código

### Parámetros iniciales
Define colores, tamaños, casillas y constantes visuales.

### Clases
- `Ficha`: representa una pieza del jugador.
- `Jugador`: administra las fichas, salidas y entradas, y los estados del turno.

### Inicialización
Se crean los jugadores con sus salidas y entradas específicas:
```python
jugadores = [
    Jugador("Rojo", "red", salida=0, entrada_hogar=67),
    Jugador("Azul", "blue", salida=17, entrada_hogar=16),
    Jugador("Verde", "green", salida=34, entrada_hogar=33),
    Jugador("Amarillo", "yellow", salida=51, entrada_hogar=50),
]
```

### Lógica del Juego
Contiene funciones para:
- Detectar bloqueos
- Verificar caminos
- Controlar movimientos según reglas

### Interfaz Gráfica
La clase `InterfazParquesPygame` se encarga de:
- Dibujar tablero y dados
- Controlar clics
- Ejecutar el bucle principal del juego

---

## Reglas Programadas

- Sacar ficha: se requiere un 5
- Captura: casillas inseguras permiten capturas con bonificación
- Bloqueo: dos fichas del mismo color bloquean el paso
- Tres dobles: penaliza enviando la última ficha movida a la cárcel
- Exactitud: necesaria para ingresar a la vía interna o a la meta
- Extra movimientos: al capturar o ingresar a vía interna
- Victoria: gana quien lleve primero sus 4 fichas a la meta

---

## Autor

Desarrollado como proyecto personal para practicar programación con Python y Pygame.  
Sugerencias, mejoras o forks son bienvenidos.

