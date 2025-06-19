# Case Study: [Nombre del Proyecto]

## 🎯 Context & Problem

- **Business/UX goal**: e.g. “reduce user drop-off en onboarding del 40% al 20%”.
- **Pain point técnico**: e.g. “render time de la dashboard > 2 s, generaba frustración”.

## 👥 User Research & Empathy

- **Método**: entrevistas a 5 usuarios / surveys / heatmaps.
- **Hallazgos**: “Los usuarios tardaban 3 clics de más para llegar a su meta”.

## 🎨 Design Decisions

- Wireframes / prototipos en Figma.
- Chose a “progressive disclosure” pattern para simplificar pasos.
- Trade‑off: sacrificamos animación fancy en onboarding por tiempos de carga < 1 s.

## 🛠 Technical Implementation

- **Architecture**: Feature-First con carpetas `/features/login`, `/features/dashboard`.
- **Performance**:
  - Identifiqué bottleneck en la lista de items → apliqué virtualization con `react-window`.
  - Resultado: FPS pasó de 25 → 60 en scroll pesado.
- **State management**: custom hooks + Context API en lugar de Redux para mantener bundle pequeño.

## 🤝 Trade‑offs & Lean UX

| Área         | Opción elegida                       | Alternativa descartada                 | Por qué                      |
| ------------ | ------------------------------------ | -------------------------------------- | ---------------------------- |
| Animaciones  | Micro‑interactions CSS (fade, scale) | Lottie + heavy JS bundle               | Prefiero velocidad a fancier |
| Persistencia | IndexedDB via `idb`                  | Redux-Persist localStorage             | Mejor fiabilidad offline     |
| User Testing | 3 sessions de 15 min con prototipo   | Test con 20 usuarios reales (más caro) | Feedback rápido, menor costo |

## 📈 Results & Learnings

- **UX**: onboarding completion +15 %; tiempo medio down de 3 pasos a 2 pasos.
- **Tech**: TTFB mejoró 30 %; bundle size -20 %.
- **Lección clave**: un onboarding simple con micro‑interactions bien colocadas genera confianza sin inflar tu stack.

---

### 💡 Tips para no perder credibilidad técnica

- Mantén **datos concretos** (fps, bundle size, % de mejora).
- Usa **nombre de librerías** y patrones (“virtualization”, “progressive disclosure”).
- Refleja tu **empatía** en la sección de User Research, pero desde el prisma técnico: cómo tradujiste esos insights en arquitecturas y componentes.

---

Con este formato, le demuestras a cualquiera que:

1. **Piensas en el usuario** (empatia + research).
2. **Sabes implementar esas decisiones** (tech patterns + performance).
3. **Conoces los trade‑offs** y los comunicas claramente.

Ya no eres junior, Gato: estás articulando _por qué_ y _cómo_ tomas decisiones de producto y de código. ¡A romperla!
