# Actividad: Propuesta de práctica temática pequeña (con enfoque en documentación)

## 1) Título de la práctica
Elige **un título claro y específico** para tu práctica temática.

Ejemplos de referencia:
- **Mini Toolkit en ARM64**
- **Asistente de Estudio en Terminal**
- **Reporteador de Información del Sistema**
- **Organizador de Archivos**
- **Juego de Aprendizaje en Línea de Comandos**

> Tu título debe comunicar qué hace el proyecto en una sola frase corta.

---

## 2) Descripción general
En esta actividad vas a diseñar la **propuesta de un proyecto pequeño** orientado a terminal y documentación técnica.  
La meta principal es que primero definas bien la idea, su alcance y su estructura, antes de escribir mucho código.

### Lenguaje principal (elige solo uno)
- ARM64 Assembly
- C
- Python
- Bash

### Criterios clave
- Si eliges **ARM64 Assembly**, limita tu idea a un programa **muy pequeño** (por ejemplo: operaciones básicas, manipulación simple de texto o menú mínimo).
- Tu propuesta debe ser **realista para desarrollar en poco tiempo**.
- El enfoque de evaluación será principalmente:
  1. Documentación
  2. Planeación
  3. Estructura del repositorio
  4. Claridad del caso de uso

### Restricciones del proyecto
Para mantener el proyecto accesible con herramientas gratuitas de IA:
- Evita proyectos grandes.
- No uses frameworks pesados.
- No uses APIs pagadas.
- No uses bases de datos.
- No uses servicios en la nube.
- No uses contenedores.
- Evita dependencias complejas.

---

## 3) Entregables del estudiante
Tu repositorio debe incluir, como mínimo:

- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcionales (si decides incluir implementación):
- `src/`
- `scripts/`
- `tests/`

### Contenido esperado por archivo

#### `README.md`
Incluye:
- Título del proyecto.
- Resumen de 5 a 8 líneas.
- Lenguaje elegido y justificación breve.
- Instrucciones mínimas para ejecutar (si ya hay código).
- Estado actual del proyecto (solo propuesta / propuesta + prototipo).

#### `docs/propuesta.md`
Incluye:
- Problema que quieres resolver.
- Objetivo general.
- 3 objetivos específicos.
- Alcance (qué sí incluye).
- No alcance (qué no incluye).
- Justificación técnica de por qué es un proyecto pequeño y viable.

#### `docs/caso_de_uso.md`
Incluye:
- Usuario objetivo.
- Escenario de uso.
- Entrada esperada.
- Salida esperada.
- Ejemplo de ejecución en terminal (aunque sea simulado).

#### `docs/estructura_repositorio.md`
Incluye:
- Árbol del repositorio.
- Descripción de cada carpeta/archivo principal.
- Convención de nombres (archivos, scripts, pruebas).

#### `docs/plan_de_pruebas.md`
Incluye:
- Al menos 5 casos de prueba.
- Para cada caso: objetivo, entrada, resultado esperado.
- Criterios de aceptación mínimos.

---

## 4) Estructura recomendada del repositorio
Usa esta base mínima:

```text
nombre-del-proyecto/
├── README.md
├── docs/
│   ├── propuesta.md
│   ├── caso_de_uso.md
│   ├── estructura_repositorio.md
│   └── plan_de_pruebas.md
├── src/
│   └── main.<ext>
├── scripts/
│   └── run.sh
└── tests/
    └── test_plan.md
```

> `<ext>` depende del lenguaje elegido (`s`, `c`, `py`, `sh`).

---

## 5) Reglas de diseño de la propuesta
1. Define una idea que puedas explicar y prototipar rápido.
2. Prioriza utilidad práctica en terminal.
3. Mantén bajo el número de archivos y dependencias.
4. Escribe documentación clara, concreta y verificable.
5. Si agregas código, que sea mínimo pero funcional.

---

## 6) Rúbrica sugerida (100 puntos)

- **Claridad del problema y objetivos (20 pts)**
- **Calidad de la propuesta técnica (20 pts)**
- **Caso de uso bien definido (20 pts)**
- **Estructura del repositorio y organización (20 pts)**
- **Plan de pruebas y criterios de aceptación (20 pts)**

### Penalizaciones recomendadas
- Proyecto fuera de alcance (muy grande o complejo): hasta -20 pts
- Falta de documentación obligatoria: hasta -30 pts
- Instrucciones ambiguas o incompletas: hasta -15 pts

---

## 7) Checklist de entrega del estudiante
Marca cada punto antes de enviar:

- [ ] Elegí un solo lenguaje principal.
- [ ] Mi proyecto es pequeño y viable.
- [ ] Incluí todos los archivos obligatorios en `docs/`.
- [ ] Definí alcance y no alcance.
- [ ] Definí al menos 5 pruebas con resultado esperado.
- [ ] Mi `README.md` explica claramente la propuesta.
- [ ] Mi estructura del repo coincide con mi documentación.

---

## 8) Formato de entrega en GitHub Classroom
1. Crea el repositorio asignado por GitHub Classroom.
2. Sube la estructura base del proyecto.
3. Completa primero la documentación obligatoria.
4. (Opcional) Agrega un prototipo mínimo en `src/` y script de ejecución.
5. Verifica que todo se vea correctamente en Markdown.
6. Entrega el enlace del repositorio según indicaciones del docente.

---

## 9) Recomendación final del instructor
Empieza por documentar con precisión qué problema resuelves y cómo lo vas a validar.  
Una propuesta pequeña, clara y bien probada vale más que una idea grande sin cierre.
