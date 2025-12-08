# Notas Personales - Preparación para Entrevistas

## Comprensión del Material

### Conceptos Clave Aprendidos

**1. La entrevista es un diálogo bidireccional**
- No se trata de "aprobar" sino de demostrar encaje mutuo
- La empresa evalúa si puedes resolver sus problemas
- Tú evalúas si el entorno se alinea con tus objetivos profesionales

**2. Preparación estratégica vs. memorización**
- Analizar el puesto antes de la entrevista (tecnologías, cultura, desafíos)
- Mapear experiencias concretas a las habilidades requeridas
- Practicar la estructura, no las respuestas palabra por palabra

**3. La técnica STAR es fundamental**
- **S**ituación: contexto específico
- **T**area: tu responsabilidad
- **A**cción: qué hiciste concretamente
- **R**esultado: impacto medible

**4. Comunicación no verbal importa tanto como el contenido**
- En presencial: postura, contacto visual, energía
- En virtual: iluminación, encuadre, mirada a cámara
- Tono de voz: entusiasmo controlado, claridad, pausas estratégicas

---

## Sugerencias y Consejos Personales

### Antes de la Entrevista

**Investiga profundamente la empresa**
- Lee su blog técnico, revisa sus repos en GitHub si son open source
- Identifica qué stack usan y prepara ejemplos con tecnologías similares
- Busca entrevistas o artículos de sus developers en Medium, YouTube, etc.

**Prepara tu "arsenal de historias"**
- 3-4 proyectos que domines completamente
- 2-3 desafíos técnicos superados con aprendizajes claros
- 1-2 ejemplos de trabajo en equipo o liderazgo técnico

**Practica en voz alta**
- No leas, habla naturalmente
- Grábate y escucha: detecta muletillas ("eh", "o sea", "básicamente")
- Cronometra: respuestas de 60-90 segundos son ideales

### Durante la Entrevista

**Escucha activamente**
- Parafrasea la pregunta si no está clara: "Entiendo que me preguntas sobre..."
- Toma 2-3 segundos para pensar antes de responder
- Está bien decir "no lo sé, pero así lo investigaría..."

**Sé específico, no genérico**
- **Mal:** "Soy una persona proactiva"
- **Bien:** "En mi último proyecto, noté que las pruebas E2E eran lentas. Propuse migrar de Selenium a Playwright, documenté el proceso y redujimos el tiempo de CI de 15 a 7 minutos"

**Piensa en voz alta (entrevistas técnicas)**
- Explica tu razonamiento mientras codeas
- Menciona trade-offs: "Esta solución es O(n²) pero optimizable a O(n) con un HashMap"
- Si te atascas, verbaliza: "Creo que puedo resolver esto con recursión, déjame intentar..."

### Después de la Entrevista

**Autoevaluación inmediata**
- Anota preguntas que no esperabas
- Identifica respuestas mejorables
- Revisa conceptos técnicos que no dominaste

**Follow-up profesional**
- Email de agradecimiento en 24h (breve, específico)
- Menciona algo concreto de la conversación
- Reafirma interés sin ser insistente

---

## Las Tres Preguntas para la Grabación

### 1. Pregunta Personal: "Háblame de ti y por qué te interesa este puesto"

**Respuesta modelo (90 segundos):**

> "Hola, soy Carlos, desarrollador full stack con experiencia en JavaScript, Node.js y PostgreSQL. Mi camino en tech comenzó 3 años cuando completé un bootcamp intensivo donde construimos aplicaciones desde cero, trabajando en equipo bajo metodologías ágiles.
>
> Durante mi formación, me especialicé en desarrollo frontend, pero también adquirí experiencia sólida en backend con Express y bases de datos SQL. Uno de mis proyectos destacados en los que he trabajado fue un sistema interno para la empresa Tecprosalud: una aplicación que ofrece servicios a médicos que desean llevar consultas médicas a lugares remotos o donde el alcance de centros médicos no es equitativo, acercando la posibilidad de realizar exámenes, diagnósticos y consultas. En este, trabajé en el frontend con Javascript y Vuejs y el backend con Java más Springboot y Postgresql.
>
> Lo que me atrae de este puesto es la oportunidad de trabajar con Javascript en un entorno donde puedo seguir aprendiendo. Me motiva especialmente la cultura de la empresa, su vocación por el buen mentoring, y creo que mi experiencia en la aplicación de patrones de desarrollo a soluciones específicas puede aportar valor desde el inicio. Estoy buscando un rol donde pueda crecer técnicamente mientras contribuyo a proyectos con impacto real."

**Por qué funciona:**
- Estructura clara: quién eres → qué has hecho → por qué este puesto
- Datos concretos (tecnologías, métricas)
- Conecta experiencia con necesidades de la empresa
- Muestra motivación genuina, no genérica

---

### 2. Pregunta Técnica: "Explica cómo optimizarías el rendimiento de una aplicación web lenta"

**Respuesta modelo (120 segundos):**

> "Excelente pregunta. Mi enfoque sería sistemático, empezando por diagnosticar antes de optimizar.
>
> **Primero, identificaría el cuello de botella** usando herramientas como Chrome DevTools, Lighthouse o New Relic. Analizaría:
> - Tiempos de carga de red (Waterfall en Network tab)
> - Renderizado y scripts bloqueantes (Performance tab)
> - Consultas a base de datos lentas (logs del backend)
>
> **Luego, aplicaría optimizaciones según el diagnóstico:**
>
> **En el frontend:**
> - Lazy loading de componentes y rutas con React.lazy() o dynamic imports
> - Code splitting para reducir el bundle inicial
> - Optimización de imágenes: WebP, srcset para responsive images, CDN
> - Implementar Service Workers para caché estratégico
> - Virtualización de listas largas con react-window
>
> **En el backend:**
> - Añadir índices en queries SQL frecuentes
> - Implementar caché con Redis para datos que no cambian constantemente
> - Paginación para reducir payload de respuestas
> - Comprimir respuestas con Gzip o Brotli
>
> **En la infraestructura:**
> - CDN para assets estáticos
> - HTTP/2 o HTTP/3 para multiplexing
> - Database connection pooling
>
> Por ejemplo, en un proyecto real redujimos el First Contentful Paint de 4s a 1.2s combinando code splitting, optimización de imágenes y añadiendo un índice en una tabla de usuarios que tenía 50k registros. Siempre mido el impacto antes y después con métricas concretas."

**Por qué funciona:**
- Metodología clara (diagnosticar → optimizar)
- Conocimiento de herramientas específicas
- Cubre múltiples capas (frontend, backend, infra)
- Incluye ejemplo real con métricas
- Demuestra pensamiento estructurado

---

### 3. Pregunta Conductual (STAR): "Cuéntame de una vez que tuviste que resolver un conflicto técnico en equipo"

**Respuesta modelo (90 segundos):**

> "Claro. Durante mi proyecto final del bootcamp trabajamos en una aplicación de e-commerce con un equipo de 5 personas.
>
> **Situación:** A mitad del sprint, surgió un desacuerdo sobre la arquitectura de estado. Dos compañeros querían usar Redux porque era 'el estándar', pero yo y otro developer propusimos Context API porque nuestra app era pequeña y Redux añadiría complejidad innecesaria.
>
> **Tarea:** Como éramos una democracia técnica sin líder formal, mi rol fue facilitar que tomáramos la mejor decisión basada en datos, no en opiniones.
>
> **Acción:** Propuse hacer un spike técnico de 2 horas. Cada equipo implementaría un feature crítico (carrito de compras) con su solución propuesta. Definimos criterios objetivos: líneas de código, tiempo de implementación, facilidad de testing y curva de aprendizaje para el equipo.
>
> Después de la demo, discutimos los resultados. Mi implementación con Context API fue más rápida (45 min vs 90 min), tenía menos boilerplate, y todos entendieron el código inmediatamente. Sin embargo, reconocí que Redux sería mejor si la app escalaba.
>
> **Resultado:** Decidimos usar Context API pero documentar cuándo migrar a Redux (más de 5 contextos o estado compartido complejo). Completamos el proyecto a tiempo, sin conflictos posteriores, y el equipo aprendió a resolver desacuerdos con experimentos rápidos en lugar de debates teóricos. Esta experiencia me enseñó que las mejores decisiones técnicas se basan en experimentar, no en dogmas."

**Por qué funciona:**
- Estructura STAR impecable
- Muestra habilidades técnicas (Redux, Context API)
- Demuestra soft skills: facilitación, toma de decisiones, humildad
- No villainiza a nadie, enfoque en solución
- Incluye aprendizaje aplicable

---

## Tips para la Grabación

### Configuración Técnica
- **Luz natural** de frente o ring light
- **Fondo neutro** sin distracciones
- **Encuadre:** de pecho para arriba, centrado
- **Audio claro:** auriculares con micrófono o grabadora de voz
- **Prueba antes:** revisa que video/audio se escuchen bien

### Durante la Grabación
- **Respiración profunda** antes de empezar cada pregunta
- **Sonríe naturalmente**, proyecta confianza (no arrogancia)
- **Mira a la cámara**, no a tu imagen en pantalla
- **Gestos moderados**, manos visibles
- **Pausa entre preguntas**, no grabes todo en una toma si necesitas descansar

### Estructura Recomendada
```
[Intro breve]
"Hola, soy [nombre]. A continuación responderé tres preguntas como parte de mi preparación para entrevistas técnicas."

[Pregunta 1 - Personal]
[Pausa de 2-3 segundos]

[Pregunta 2 - Técnica]
[Pausa de 2-3 segundos]

[Pregunta 3 - Conductual]

[Cierre opcional]
"Gracias por su atención. Quedo abierto a cualquier feedback."
```

---

## Checklist Pre-Grabación

- [X] He escrito las tres preguntas que responderé
- [X] Practiqué mis respuestas en voz alta (mínimo 2 veces)
- [X] Preparé ejemplos específicos con métricas/datos
- [X] Revisé que mi setup técnico funcione
- [X] Tengo agua cerca
- [X] He eliminado distracciones (notificaciones OFF)
- [X] Cronometré mis respuestas (60-120 segundos c/u)
- [X] Identifiqué muletillas a evitar
- [X] Estoy vestido apropiadamente
- [X] Tengo energía positiva y actitud abierta

---

## Reflexión Final

La mejor preparación combina:
1. **Conocimiento técnico sólido** (saber hacer el trabajo)
2. **Comunicación clara** (saber explicar lo que haces)
3. **Autoconocimiento** (entender tus fortalezas y áreas de mejora)
4. **Autenticidad** (ser tú mismo, no un personaje)

Las entrevistas son habilidades que se entrenan. Cada práctica te acerca más a tu objetivo laboral. ¡Éxito!
