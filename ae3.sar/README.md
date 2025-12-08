# Técnica SAR - Construcción de Historia Profesional

## 🎯 Objetivo

Aplicar la técnica SAR (Situación–Acción–Resultado) para construir una historia profesional breve, concreta y auténtica que puedas usar en entrevistas laborales o conversaciones profesionales del sector tecnológico.

---

## 💡 En qué se enfoca este ejerciciocio

No se trata de aprender la técnica —ya lo hiciste—, sino de convertir una experiencia real en una historia lista para contar: una respuesta clara, humana y convincente que muestre tu valor profesional y tu manera de pensar.

> **"No cuentes lo que hiciste: contá cómo hiciste que algo cambiara."**

---

## 🧭 Parte 1: Elige una experiencia significativaiva

Piensa en una situación de tu vida profesional, académica o del bootcamp que refleje tu crecimiento o tus competencias. Puede ser:

- Resolver un problema técnico o de equipo
- Liderar una mejora o idea
- Aprender bajo presión
- Afrontar un error y transformarlo en aprendizaje

> 💡 **Tip:** Elige una historia que se alinee con el tipo de rol que estás buscando hoy.

---

## ✍️ Parte 2: Redacta tu historia con la técnica SARSAR

Usa esta plantilla práctica:

| Etapa | Preguntas guía | Tu historia |
|-------|----------------|-------------|
| **S – Situación** | ¿Dónde ocurrió? ¿Qué desafío había? | "Durante el proyecto final del bootcamp, el equipo tenía dificultades para integrar el backend con el frontend…" |
| **A – Acción** | ¿Qué hiciste? ¿Qué habilidades aplicaste? | "Propuse dividir tareas, documenté la API y organicé revisiones semanales para mantener el avance…" |
| **R – Resultado** | ¿Qué lograste o aprendiste? | "Logramos entregar a tiempo y la aplicación fue elegida para demo final. Aprendí a comunicar mejor con equipos distribuidos." |

> 💡 **Consejo:** Mantén la historia breve (menos de 2 minutos al contarla).

---

## 🤖 Parte 3: Refina tu historia con ChatGPTGPT

ChatGPT puede ayudarte a mejorar la claridad, el impacto y el lenguaje de tu historia.

**Prompt sugerido:**

> "Tengo una historia profesional para entrevista laboral. Escuchala y ayúdame a mejorarla según la técnica SAR. Indicame si transmite logro, claridad y autenticidad."

**Opciones de práctica:**

1. **Modo texto:** Pegá tu historia y pídele sugerencias de redacción o tono
2. **Modo voz:** Activa micrófono y cuéntala en voz alta para practicar fluidez y naturalidad
3. **Modo simulador:** "Actúa como un reclutador de tecnología y hazme una pregunta relacionada con mi historia"

> 💡 **Objetivo:** lograr una historia que suene natural, tenga foco en resultados y te deje tranquilo/a de poder contarla en cualquier entrevista.

---

## 🗣️ Parte 4: Feedback y reflexiónión

Lee o cuenta tu historia a un compañero/a o mentor/a y pide feedback sobre tres aspectos:

- ¿Es clara y creíble?
- ¿Refleja tus habilidades técnicas o blandas?
- ¿Deja una impresión positiva o aprendizaje?

**Finalmente, escribe una breve reflexión (5 líneas):**

> "Qué aprendí al construir esta historia y cómo la puedo usar para comunicar mi valor profesional."

---

## ✅ Evaluaciónión

| Criterio | Descripción | Puntos |
|----------|-------------|--------|
| Estructura SAR | Historia coherente, con situación, acción y resultado claros | 4 |
| Impacto y autenticidad | Refleja habilidades reales y propósito profesional | 3 |
| Práctica y mejora | Evidencia de iteración con IA o feedback recibido | 3 |
| **Total** | | **10 pts** |

---

## 🚀 Cierre

Una historia bien contada no solo responde una pregunta: construye tu credibilidad profesional.

Preparar 2 o 3 historias SAR antes de cada entrevista te da seguridad, coherencia y conexión con quien te escucha.

> **"Los hechos muestran tu experiencia. Las historias revelan tu potencial."**

---

## Desarrollo

### Parte 1: Experiencia Seleccionada

**Experiencia elegida:** Integración de servicios externos en el proyecto Tecprosalud - Manejo de timeouts y mejora de experiencia de usuario

Esta experiencia refleja competencias técnicas clave (arquitectura de sistemas, manejo de APIs, optimización) y habilidades blandas (resolución de problemas, toma de decisiones, documentación) que son relevantes para roles de Desarrollador Full Stack.

---

### Parte 2: Historia SAR - Versión Inicial

| Etapa | Preguntas guía | Mi historia |
|-------|----------------|-------------|
| **S – Situación** | ¿Dónde ocurrió? ¿Qué desafío había? | Durante mi colaboración en el proyecto Tecprosalud, una aplicación que lleva servicios médicos a zonas remotas de Chile, nos enfrentábamos a un problema crítico: la integración con múltiples APIs externas (laboratorios, sistemas de citas, pagos) generaba timeouts frecuentes debido a tiempos de respuesta variables. Esto provocaba que el 15% de las peticiones fallaran y los médicos tenían que esperar hasta 8 segundos para realizar acciones básicas, afectando gravemente la experiencia de usuario. |
| **A – Acción** | ¿Qué hiciste? ¿Qué habilidades aplicaste? | Analicé el problema y propuse rediseñar la arquitectura de integración. Implementé un patrón de procesamiento asíncrono con colas de mensajes para no bloquear la interfaz. Agregué circuit breakers usando Resilience4j para manejar servicios caídos, configuré timeouts agresivos con reintentos exponenciales, y añadí caché con Redis para respuestas frecuentes. En el frontend con Vue.js, cambié de espera síncrona a polling, mostrando feedback visual al usuario. Documenté todo el proceso para que el equipo pudiera aplicar estos patrones en futuras integraciones. |
| **R – Resultado** | ¿Qué lograste o aprendiste? | Redujimos los timeouts del 15% a menos del 1% de las peticiones. El tiempo de respuesta percibido por los usuarios bajó de 8 segundos a 2 segundos. La aplicación se volvió resiliente ante caídas de servicios externos. Además, el equipo adoptó estos patrones como estándar. Personalmente, aprendí mucho sobre sistemas distribuidos, la importancia de diseñar para el fallo, y cómo comunicar decisiones técnicas complejas al equipo de forma clara. |

**Tiempo estimado de narración:** ~90 segundos

---

### Parte 3: Refinamiento con IA

#### Iteración 1: Feedback de IA sobre versión inicial

**Prompt usado:** "Tengo una historia profesional para entrevista laboral usando técnica SAR. Escúchala y ayúdame a mejorarla. Indícame si transmite logro, claridad y autenticidad."

**Feedback recibido (simulado como IA partner):**

> **Análisis de tu historia SAR:**
>
> **Fortalezas:**
> - ✅ Estructura SAR clara y completa
> - ✅ Métricas concretas (15% a 1%, 8s a 2s) que demuestran impacto
> - ✅ Tecnologías específicas mencionadas (Vue.js, Resilience4j, Redis)
> - ✅ Muestra tanto habilidades técnicas como de documentación/comunicación
> - ✅ Contexto social relevante (servicios médicos en zonas remotas)
>
> **Áreas de mejora:**
> - La sección de Situación es un poco larga. Podrías acortar los detalles técnicos iniciales.
> - En Acción, mencionar "circuit breakers" y "Resilience4j" puede ser muy técnico para algunos reclutadores. Considera simplificar o agregar contexto breve.
> - El Resultado podría enfatizar más el impacto en el negocio/usuarios (médicos pudiendo atender más pacientes) además de las métricas técnicas.
>
> **Sugerencia de tono:** La historia es auténtica y profesional. Para hacerla más conversacional, podrías comenzar con "En Tecprosalud trabajábamos en..." en lugar de "Durante mi colaboración...". Esto la hace más directa.

#### Iteración 2: Historia SAR Mejorada

| Etapa | Mi historia mejorada |
|-------|---------------------|
| **S – Situación** | En Tecprosalud, la aplicación que desarrollamos para llevar servicios médicos a zonas remotas de Chile tenía un problema crítico: las integraciones con APIs externas de laboratorios y sistemas de citas causaban timeouts frecuentes. El 15% de las peticiones fallaban y los médicos esperaban hasta 8 segundos para acciones básicas, lo que impactaba directamente su capacidad de atender pacientes. |
| **A – Acción** | Propuse rediseñar cómo manejábamos estas integraciones. Implementé procesamiento asíncrono para que la interfaz no se bloqueara mientras esperábamos respuestas externas. Agregué mecanismos de protección (circuit breakers) que detectaban cuando un servicio estaba caído y evitaban seguir intentando, configuré reintentos inteligentes, y usé caché con Redis para datos que no cambiaban frecuentemente. En el frontend con Vue.js, cambié la experiencia a mostrar progreso en tiempo real en lugar de una pantalla congelada. Documenté todo para que el equipo pudiera replicarlo. |
| **R – Resultado** | Los timeouts bajaron del 15% a menos del 1%. El tiempo de respuesta percibido se redujo de 8 a 2 segundos, y lo más importante: los médicos podían trabajar de forma fluida incluso cuando servicios externos tenían problemas. El equipo adoptó estos patrones como estándar para futuras integraciones. Aprendí mucho sobre sistemas distribuidos y diseño resiliente, y mejoré mi capacidad de comunicar decisiones técnicas complejas de forma clara. |

**Tiempo estimado:** ~75 segundos (más conciso)

#### Iteración 3: Práctica de entrega oral

**Prompt usado:** "Actúa como un reclutador de tecnología para un rol de Desarrollador Full Stack. Hazme una pregunta relacionada con mi historia SAR sobre Tecprosalud."

**Pregunta del reclutador (simulado):**

> "Interesante tu trabajo en Tecprosalud. Me gustaría profundizar: cuando mencionas que implementaste circuit breakers, ¿cómo decidiste los umbrales para activarlos? Y más importante, ¿cómo manejaste la comunicación con el equipo de producto cuando estos mecanismos bloqueaban solicitudes a servicios externos? Seguramente hubo casos donde el usuario veía un mensaje de error en lugar del resultado esperado."

**Mi respuesta preparada:**

> "Excelente pregunta. Para los umbrales del circuit breaker, empecé con valores conservadores basados en el comportamiento histórico de cada servicio: si fallaban 5 requests consecutivos o el 50% en una ventana de 30 segundos, el circuito se abría por 60 segundos. Estos valores los ajustamos iterativamente monitoreando en producción.
>
> Sobre la comunicación con producto, fue clave explicar el trade-off: antes, el usuario esperaba 8+ segundos y luego veía un error genérico. Ahora, con el circuit breaker, si un servicio está caído, le mostramos inmediatamente un mensaje claro: 'El sistema de laboratorio no está disponible temporalmente. Intenta en unos minutos o contáctanos.' Esto mejoró la percepción del usuario porque falla rápido con información útil, en lugar de dejarlo esperando sin saber qué pasa. El equipo de producto valoró mucho esta transparencia y la mejor experiencia resultante."

**Feedback de la práctica oral (IA):**

> Tu respuesta demuestra profundidad técnica equilibrada con pensamiento de producto. Tres fortalezas:
> 1. Diste números específicos (5 fallos, 50%, 30s, 60s) que muestran rigurosidad
> 2. Explicaste el "por qué" del negocio, no solo el "cómo" técnico
> 3. Mencionaste iteración y ajuste basado en datos reales
>
> Para mejorar: Tu respuesta fue completa pero un poco larga (~60 segundos). En entrevista real, considera empezar con el insight clave ("fallar rápido con información útil vs esperar sin saber qué pasa") y luego dar los detalles técnicos si preguntan más.

---

### Parte 4: Reflexión Personal

**¿Qué aprendí al construir esta historia y cómo la puedo usar para comunicar mi valor profesional?**

Al construir esta historia SAR, aprendí que las experiencias técnicas complejas se vuelven más poderosas cuando las conecto con impacto real en usuarios finales. Lo importante no es solo enumerar tecnologías (Resilience4j, Redis, Vue.js), sino explicar el problema que resolvían y el resultado medible que generaron. También descubrí que mencionar el contexto social del proyecto (servicios médicos en zonas remotas) añade significado y muestra que pienso más allá del código.

Esta historia me permite comunicar múltiples competencias simultáneamente: capacidad técnica para arquitectura de sistemas, habilidades de resolución de problemas bajo presión, pensamiento orientado a resultados con métricas concretas, y capacidad de documentación/comunicación al equipo. Puedo adaptarla según la empresa: si es una startup, enfatizo la rapidez en implementar soluciones; si es una empresa grande, destaco los patrones reutilizables y la documentación; si valoran impacto social, resalto el contexto de salud en zonas remotas.

La práctica con IA me hizo consciente de ajustar el nivel técnico según mi audiencia: con un CTO puedo profundizar en circuit breakers y estrategias de retry; con un reclutador HR, me enfoco en el impacto de negocio y las soft skills. Finalmente, tener esta historia lista y practicada me da confianza: sé que puedo responder preguntas como "cuéntame de un desafío técnico que hayas enfrentado" o "describe una vez que mejoraste un sistema existente" con una narrativa clara, auténtica y que demuestra mi valor profesional más allá de mi CV.

---

### Historia SAR Adicional (Bonus)

**Situación alternativa para diferentes contextos de entrevista:**

#### Historia 2: Transición de carrera y aprendizaje autodidacta

**S – Situación:** Después de trabajar en retail y banca, decidí reconvertirme al desarrollo de software a los 30+ años sin tener experiencia técnica previa. Sabía que competía con developers más jóvenes con formación tradicional, y necesitaba demostrar que mi trayectoria diversa era una fortaleza, no una desventaja.

**A – Acción:** Me inscribí en tres bootcamps consecutivos de Talento Digital (JavaScript Full Stack, Frontend, Java Full Stack) para construir fundamentos sólidos rápidamente. Complementé con proyectos personales donde aplicaba lo aprendido inmediatamente. Cuando surgió la oportunidad de ser tutor de bootcamp, la tomé porque sabía que enseñar me obligaría a entender conceptos más profundamente. Simultáneamente, busqué colaborar en proyectos reales como el de Tecprosalud para ganar experiencia práctica mientras seguía aprendiendo.

**R – Resultado:** En menos de 3 años pasé de cero experiencia tech a trabajar como desarrollador Full Stack en un proyecto con impacto social, ser tutor ayudando a otros a aprender programación, y tener un stack sólido (Vue.js, React, Spring Boot, Node.js). Mi experiencia previa en comunicación y trabajo en equipo se convirtió en un diferenciador: puedo explicar conceptos técnicos con claridad, me adapto rápido a nuevos entornos, y valoro la colaboración. Aprendí que el desarrollo de software no es solo sobre código, sino sobre resolver problemas reales con tecnología.

**Uso:** Esta historia es perfecta para responder "¿por qué desarrollo de software?" o "cuéntame sobre tu carrera anterior" convirtiendo una potencial debilidad (no tener título CS tradicional) en una narrativa de determinación, aprendizaje continuo y perspectiva única.

---

### Tips para uso en entrevistas

**Cuándo usar cada historia:**

- **Historia Tecprosalud (técnica):** Preguntas sobre desafíos técnicos, trabajo con APIs, optimización de sistemas, arquitectura
- **Historia transición de carrera:** Preguntas sobre motivación, aprendizaje, por qué tech, cómo manejas cambios

**Adaptaciones según empresa:**

| Tipo de empresa | Énfasis en Tecprosalud |
|-----------------|------------------------|
| **Startup** | Rapidez de implementación, autonomía, impacto directo en producto |
| **Empresa grande** | Patrones reutilizables, documentación, escalabilidad, trabajo en equipo |
| **Sector salud/social** | Impacto en comunidades remotas, sensibilidad al contexto de usuarios |
| **Fintech** | Manejo de sistemas críticos, resilencia, timeouts, circuit breakers |

**Elementos a mantener siempre:**
- Métricas concretas (15% → 1%, 8s → 2s)
- Tecnologías específicas sin abrumar
- Impacto en usuarios/negocio, no solo logro técnico
- Aprendizaje personal al final
- Tono conversacional, no robótico
