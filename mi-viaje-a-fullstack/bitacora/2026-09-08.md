# Sistema de Bitácora Diaria (Git) + Guía de Portafolio Atractivo

Complemento del roadmap full stack: cómo llevar orden de tu estudio día a día y cómo construir un portafolio que llame la atención de reclutadores.

---

## PARTE 1: Bitácora diaria con Git

### Paso 1: Crea el repositorio

```
mi-viaje-a-fullstack/
├── README.md
├── bitacora/
│   ├── 2026-09/
│   │   ├── 2026-09-08.md
│   │   ├── 2026-09-09.md
│   │   └── ...
│   └── 2026-10/
├── problemas-resueltos/
│   ├── javascript/
│   ├── react/
│   ├── nodejs/
│   └── sql/
└── ejercicios/
```

- `bitacora/`: una entrada por día, organizada por mes.
- `problemas-resueltos/`: errores importantes que te costó resolver, organizados por tema (esto se vuelve oro cuando te topas con el mismo error meses después).
- `ejercicios/`: código suelto de práctica que no es un "proyecto" formal.

### Paso 2: Plantilla para cada entrada diaria

Guarda esto como `bitacora/plantilla.md` y cópialo cada día:

```markdown
# Día N — YYYY-MM-DD

## ⏱️ Tiempo estudiado
X horas

## 📚 Qué estudié / practiqué
- Tema 1
- Tema 2

## 🐛 Problema(s) que encontré
**Problema:** Descripción breve del error o duda.
**Contexto:** Qué estaba intentando hacer.

## ✅ Cómo lo resolví
Explicación de la solución (o "sigue pendiente" si no lo resolviste).
Si fue algo importante, cópialo también a `problemas-resueltos/[tema]/nombre-descriptivo.md`.

## 💡 Algo que aprendí y no quiero olvidar
Una idea clave del día, en tus propias palabras (esto refuerza la memoria).

## 🎯 Plan para mañana
- [ ] Tarea 1
- [ ] Tarea 2
```

### Paso 3: Plantilla para "problema resuelto" (tu base de conocimiento personal)

Guarda cada error importante en `problemas-resueltos/[tema]/`, ejemplo `problemas-resueltos/react/useeffect-loop-infinito.md`:

```markdown
# useEffect entra en loop infinito

**Fecha:** 2026-09-08
**Contexto:** Estaba haciendo fetch de datos dentro de un useEffect.

## Síntoma
El componente hacía la petición a la API una y otra vez sin parar.

## Causa
No incluí el array de dependencias `[]`, así que el efecto se ejecutaba en cada render.

## Solución
Agregar `[]` como segundo argumento para que solo corra al montar el componente.

## Cómo lo reconozco la próxima vez
Si veo múltiples requests repetidas en la pestaña Network, reviso primero las dependencias del useEffect.
```

Este archivo vale más que mil tutoriales: es tu propio manual de errores, en tu idioma, con tu contexto.

### Paso 4: Ritmo de commits

- **Un commit al final de cada sesión de estudio**, aunque solo hayas actualizado la bitácora.
- Mensajes de commit descriptivos, no genéricos:
  - ❌ "actualización"
  - ✅ `"Día 12: bitácora + resuelto bug de scope en closures"`
- Para código de ejercicios/proyectos: commits pequeños y frecuentes por cada funcionalidad que agregas, no un solo commit gigante.
- Usa ramas (`feature/nombre-funcionalidad`) desde que empieces con proyectos medianos en la Fase 2 en adelante, aunque trabajes solo — te acostumbra a un flujo profesional.

### Paso 5: Revisión semanal

Cada domingo (o el día que definas), revisa tu semana:
- ¿Cuántos días estudiaste?
- ¿Qué problema te costó más?
- ¿Qué necesitas repasar antes de avanzar?

Anótalo en un archivo `bitacora/resumen-semanal.md`. Esto te sirve también como material real para contar en entrevistas ("¿cómo aprendes cosas nuevas?").

---

## PARTE 2: Cómo hacer tu portafolio llamativo

### 1. El README de cada proyecto vende tanto como el código

Reclutadores y devs entran primero al README, no al código. Cada proyecto debe tener:
- **Nombre + una frase clara** de qué hace (no "mi proyecto de React", sino "App de gestión de gastos personales con gráficas en tiempo real").
- **GIF o captura de pantalla** de la app funcionando (esto es lo que más engancha).
- **Link a la demo en vivo** (deployada) — un proyecto sin link funcional pierde muchísimo valor.
- **Stack tecnológico usado** (badges/íconos ayudan visualmente).
- **Qué problema resolviste técnicamente** (1-2 líneas): ej. "implementé paginación infinita" o "optimicé la carga de imágenes con lazy loading".
- Cómo correrlo localmente (instrucciones claras).

### 2. Calidad sobre cantidad

- 3-4 proyectos muy pulidos y funcionales valen mucho más que 10 a medias.
- Al menos 1 proyecto debe ser full stack completo (frontend + backend + base de datos + auth + deploy).
- Evita clones genéricos sin ningún toque propio (todo mundo tiene un clon de Netflix); agrégale algo tuyo — una funcionalidad extra, un diseño distinto, un caso de uso real que te interese.

### 3. Sitio de portafolio propio

- Constrúyelo tú mismo (es tu primer gran proyecto de React/HTML-CSS) en vez de usar una plantilla genérica.
- Debe incluir: quién eres, proyectos con links a demo + repo, stack, cómo contactarte (email, LinkedIn, GitHub).
- Cuida el detalle visual: tipografía, espaciado, un color de acento — no necesita ser complejo, pero sí verse cuidado.

### 4. GitHub como carta de presentación

- README de perfil (el especial que aparece en tu perfil de GitHub) con una breve intro sobre ti y en qué estás trabajando actualmente.
- Contribuciones constantes (tu bitácora diaria ayuda mucho a esto, se ve en el gráfico de actividad).
- Repos con nombres descriptivos, no "proyecto-final-v2-definitivo".
- Pinea (fija) tus mejores 4-6 repos en la parte superior de tu perfil.

### 5. Documenta tu proceso públicamente (opcional pero muy efectivo)

- Publica avances cortos en LinkedIn o X: "Hoy aprendí X, así lo resolví" — esto genera visibilidad y a veces oportunidades llegan solas.
- Escribir 1 post explicando cómo resolviste un problema técnico interesante demuestra que entiendes lo que haces, no solo que copias código.

### 6. Detalles que marcan diferencia en entrevistas

- Poder explicar **por qué** tomaste ciertas decisiones técnicas en tus proyectos (no solo qué hiciste).
- Tener listo un "elevator pitch" de 30 segundos sobre tu proyecto estrella.
- Mostrar que sabes debuggear en vivo (por eso tu bitácora de problemas resueltos es tan valiosa — te entrena para explicar tu proceso de pensamiento).

---

## Checklist rápido antes de aplicar a trabajos

- [ ] Repositorio de bitácora activo con commits regulares
- [ ] Al menos 3-4 proyectos con README completo (descripción, capturas, demo, stack)
- [ ] Al menos 1 proyecto full stack deployado y funcional
- [ ] Sitio de portafolio propio, deployado
- [ ] Perfil de GitHub cuidado (README de perfil, repos pineados)
- [ ] Perfil de LinkedIn actualizado con proyectos
- [ ] Puedes explicar cualquiera de tus proyectos en voz alta sin ver el código