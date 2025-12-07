# Notas Personales - Simulación de Entrevista Laboral en TI

## 📚 Parte 1: Investigación

### ¿Cuáles son los tipos de entrevistas más comunes en el área de TI?

**1. Entrevista Técnica**
- **Objetivo:** Evaluar conocimientos específicos en programación, arquitectura, algoritmos, estructuras de datos
- **Formato:** Coding challenges en vivo, preguntas sobre tecnologías, resolución de problemas en tiempo real
- **Plataformas comunes:** LeetCode, HackerRank, CoderPad, o en whiteboard presencial
- **Ejemplo:** "Implementa una función que detecte si una cadena es un palíndromo con complejidad O(n)"

**2. Entrevista por Competencias (Behavioral)**
- **Objetivo:** Evaluar soft skills, trabajo en equipo, resolución de conflictos, adaptabilidad
- **Formato:** Preguntas basadas en experiencias pasadas usando método STAR
- **Temas comunes:** Liderazgo, comunicación, manejo de presión, aprendizaje continuo
- **Ejemplo:** "Cuéntame sobre una vez que tuviste que aprender una tecnología nueva bajo presión"

**3. Entrevista de Cultura Organizacional (Culture Fit)**
- **Objetivo:** Determinar alineación con valores, misión y forma de trabajo de la empresa
- **Formato:** Conversación sobre motivaciones, estilo de trabajo, objetivos profesionales
- **Evalúa:** Valores personales, estilo de comunicación, expectativas laborales
- **Ejemplo:** "¿Prefieres trabajar de forma autónoma o en equipo? ¿Por qué?"

**4. Entrevista de Sistema de Diseño (System Design)**
- **Objetivo:** Evaluar capacidad de arquitectura de sistemas escalables (para roles senior)
- **Formato:** Diseñar sistemas completos en whiteboard (ej. Twitter, Netflix, Uber)
- **Evalúa:** Escalabilidad, trade-offs, bases de datos, caching, microservicios
- **Ejemplo:** "Diseña un sistema de notificaciones en tiempo real para 10 millones de usuarios"

**5. Entrevista de Portafolio/Proyecto**
- **Objetivo:** Revisar proyectos reales del candidato
- **Formato:** Presentación de código, demos, explicación de decisiones técnicas
- **Evalúa:** Calidad del código, buenas prácticas, capacidad de explicar decisiones
- **Ejemplo:** "Muéstrame tu proyecto más complejo y explica los desafíos que enfrentaste"

**6. Entrevista con el Equipo Técnico (Pair Programming)**
- **Objetivo:** Ver cómo trabajas en colaboración real
- **Formato:** Programar juntos resolviendo un problema
- **Evalúa:** Comunicación, receptividad a feedback, pensamiento colaborativo
- **Ejemplo:** "Vamos a refactorizar esta función juntos, ¿qué mejorarías?"

---

### 3 Preguntas Frecuentes en Entrevistas Técnicas para Desarrollador Full Stack

**1. "¿Cuál es la diferencia entre var, let y const en JavaScript? ¿Cuándo usarías cada uno?"**

**Respuesta:**
- `var`: scope de función, hoisting completo, permite redeclaración (legacy)
- `let`: scope de bloque, no permite redeclaración, mutable
- `const`: scope de bloque, no permite reasignación (pero objetos/arrays son mutables)

**Uso recomendado:**
- `const` por defecto (inmutabilidad)
- `let` cuando necesites reasignar
- `var` evitarlo (ES5 legacy)

**Ejemplo:**
```javascript
const API_URL = "https://api.com"; // No cambiará
let counter = 0; // Cambiará
counter++;
```

**2. "Explica cómo funciona el Event Loop en Node.js y qué son las promesas"**

**Respuesta:**
El Event Loop es el mecanismo que permite a Node.js realizar operaciones no bloqueantes a pesar de ser single-threaded.

**Fases del Event Loop:**
1. Timers (setTimeout, setInterval)
2. I/O Callbacks
3. Idle, prepare
4. Poll (espera eventos nuevos)
5. Check (setImmediate)
6. Close callbacks

**Promesas:** Objetos que representan el resultado futuro de una operación asíncrona.
Estados: pending → fulfilled/rejected

**Ejemplo práctico:**
```javascript
// Mal: Callback hell
getData(function(a) {
  getMoreData(a, function(b) {
    getEvenMore(b, function(c) {
      console.log(c);
    });
  });
});

// Bien: Promesas
getData()
  .then(a => getMoreData(a))
  .then(b => getEvenMore(b))
  .then(c => console.log(c))
  .catch(error => console.error(error));

// Mejor: Async/await
async function fetchData() {
  try {
    const a = await getData();
    const b = await getMoreData(a);
    const c = await getEvenMore(b);
    console.log(c);
  } catch (error) {
    console.error(error);
  }
}
```

**3. "¿Cómo optimizarías las consultas SQL en una aplicación con millones de registros?"**

**Respuesta estructurada:**

**Diagnóstico:**
- Usar `EXPLAIN ANALYZE` para ver el query plan
- Identificar table scans completos
- Revisar logs de slow queries

**Optimizaciones:**

1. **Índices estratégicos:**
```sql
-- Antes: Full table scan
SELECT * FROM users WHERE email = 'user@example.com';

-- Después: Con índice
CREATE INDEX idx_users_email ON users(email);
```

2. **Evitar SELECT *:**
```sql
-- Mal
SELECT * FROM users WHERE active = true;

-- Bien
SELECT id, name, email FROM users WHERE active = true;
```

3. **Joins eficientes:**
```sql
-- Usar INNER JOIN en lugar de subqueries
-- Índices en columnas de join
-- LIMIT para paginar resultados
```

4. **Caché de queries frecuentes con Redis**

5. **Particionamiento de tablas grandes**

6. **Connection pooling para reducir overhead**

---

### ¿Qué buscan evaluar los reclutadores en una entrevista de cultura organizacional?

**1. Alineación con Valores de la Empresa**
- ¿Compartes los principios fundamentales de la organización?
- Ejemplo: Si la empresa valora innovación, ¿muestras curiosidad y aprendizaje continuo?
- **Cómo demostrarlo:** Investigar valores en su web y conectarlos con tus experiencias

**2. Estilo de Trabajo y Colaboración**
- ¿Prefieres autonomía o supervisión cercana?
- ¿Cómo manejas feedback?
- ¿Trabajas mejor en equipo o solo?
- **Señal positiva:** Mostrar flexibilidad y adaptabilidad

**3. Motivación y Objetivos a Largo Plazo**
- ¿Por qué quieres trabajar aquí específicamente?
- ¿Qué buscas en tu carrera profesional?
- ¿Te motiva el producto/servicio de la empresa?
- **Red flag:** Respuestas genéricas como "quiero aprender" sin especificar qué

**4. Capacidad de Adaptación al Cambio**
- ¿Cómo reaccionas ante pivotes o cambios de prioridades?
- ¿Te sientes cómodo con ambigüedad?
- **Especialmente importante en startups**

**5. Comunicación y Resolución de Conflictos**
- ¿Cómo manejas desacuerdos con compañeros?
- ¿Das y recibes feedback constructivamente?
- ¿Comunicas proactivamente problemas?

**6. Balance Vida-Trabajo y Bienestar**
- ¿Qué necesitas para ser productivo?
- ¿Cómo manejas el estrés?
- ¿Qué esperas del ambiente laboral?

**7. Ownership y Responsabilidad**
- ¿Tomas iniciativa sin que te lo pidan?
- ¿Asumes responsabilidad por errores?
- ¿Tienes mentalidad de "dueño" del producto?

**Consejos para destacar:**
- Investiga la cultura en Glassdoor, LinkedIn, blog de la empresa
- Conecta tus valores personales con los de la empresa (con ejemplos)
- Haz preguntas sobre la cultura: "¿Cómo celebran los logros del equipo?"
- Sé auténtico: el culture fit es mutuo, no finjas ser alguien que no eres

---

## 📝 Parte 2: Preparación del Discurso

### 1. Cuéntame sobre ti

**Mi respuesta (90 segundos):**

> "Hola, soy Carlos, desarrollador full stack con experiencia en JavaScript, Node.js y PostgreSQL. Mi camino en tech comenzó hace 3 años cuando completé un bootcamp intensivo donde construimos aplicaciones desde cero, trabajando en equipo bajo metodologías ágiles.
>
> Durante mi formación, me especialicé en desarrollo frontend con JavaScript y Vue.js, pero también adquirí experiencia sólida en backend con Java, Spring Boot y bases de datos SQL. Uno de mis proyectos más significativos fue para Tecprosalud: un sistema interno que permite a médicos llevar consultas médicas a lugares remotos. Trabajé en toda la stack, desde el frontend con Vue.js hasta la integración con APIs REST en el backend con Spring Boot y PostgreSQL.
>
> Lo que más me motiva del desarrollo es resolver problemas reales con tecnología. Me apasiona escribir código limpio, aplicar patrones de diseño y aprender constantemente nuevas herramientas. Estoy buscando un rol donde pueda aportar mi experiencia técnica mientras sigo creciendo profesionalmente en un equipo que valore la calidad y la colaboración."

**Estructura:**
- Quién soy + stack técnico (15s)
- Qué he hecho + proyecto destacado (45s)
- Qué busco + motivación (30s)

---

### 2. ¿Cuál ha sido el mayor desafío técnico que has enfrentado?

**Mi respuesta (usando STAR):**

> **Situación:** Durante el desarrollo del sistema para Tecprosalud, teníamos que integrar múltiples servicios externos (APIs de laboratorios, sistemas de citas, pagos) con tiempos de respuesta muy variables, lo que causaba timeouts y mala experiencia de usuario.
>
> **Tarea:** Mi responsabilidad era rediseñar la arquitectura de integración para que fuera resiliente y no bloqueara la interfaz mientras esperábamos respuestas de servicios lentos.
>
> **Acción:** 
> - Implementé un patrón de procesamiento asíncrono con colas de mensajes
> - Agregué circuit breakers para servicios externos con Resilience4j
> - Configuré timeouts agresivos y reintentos exponenciales
> - Añadí caché con Redis para respuestas frecuentes
> - Implementé polling en el frontend en lugar de espera síncrona
>
> **Resultado:** Redujimos los timeouts de un 15% de las peticiones a menos del 1%. El tiempo de respuesta percibido por usuarios mejoró de 8 segundos a 2 segundos. Además, documenté el patrón para que el equipo lo aplicara en otras integraciones. Aprendí mucho sobre sistemas distribuidos y la importancia de diseñar para el fallo.

**Por qué funciona:**
- Demuestra conocimiento técnico específico (circuit breakers, caching, async)
- Muestra impacto medible (métricas concretas)
- Incluye aprendizaje y transferencia de conocimiento

---

### 3. ¿Cómo manejas el trabajo bajo presión?

**Mi respuesta:**

> "Bajo presión, me enfoco en tres cosas: priorización, comunicación y mantener la calidad mínima necesaria.
>
> **Priorización:** Primero identifico qué es crítico vs. importante. Uso la matriz de Eisenhower: urgente/importante. Si tengo un bug en producción y una feature nueva, el bug va primero sin duda.
>
> **Comunicación proactiva:** Informo temprano si veo que no llegaré a un deadline. Prefiero renegociar plazos o scope antes que entregar algo mal hecho. Por ejemplo, en un sprint ajustado, propuse entregar la feature core sin los 'nice-to-have', y entregar esos después. El equipo lo agradeció porque teníamos algo funcional a tiempo.
>
> **Calidad sobre velocidad:** Incluso bajo presión, mantengo estándares mínimos: tests para lógica crítica, code review aunque sea rápido, y documentación básica. Sé que los atajos de hoy son deuda técnica mañana.
>
> **Manejo personal:** Cuando siento que la presión me supera, tomo breaks cortos, salgo a caminar 5 minutos. También soy honesto con el equipo si necesito ayuda. El trabajo en equipo existe para momentos difíciles."

**Por qué funciona:**
- Método estructurado (no improvisar bajo presión)
- Demuestra madurez profesional
- Incluye ejemplo real
- Reconoce límites (pedir ayuda no es debilidad)

---

### 4. ¿Por qué te gustaría trabajar en nuestra empresa?

> ⚠️ **Nota:** Esta respuesta debe personalizarse según la empresa. Aquí hay un template:

**Estructura recomendada:**

> "Me atrae [EMPRESA] por tres razones principales:
>
> **1. El producto/misión:** [Describe qué hace la empresa y por qué te importa]
> Ejemplo: 'Me apasiona cómo están democratizando el acceso a servicios financieros en Latinoamérica. Vengo de una familia donde el acceso bancario siempre fue un desafío, así que este problema me toca personalmente.'
>
> **2. El stack tecnológico y cultura de ingeniería:** [Menciona tecnologías específicas]
> Ejemplo: 'He leído en su blog técnico sobre cómo usan microservicios con Kubernetes y eso se alinea con lo que quiero aprender. También valoro que hagan code reviews rigurosos y tengan sprints de refactoring, eso habla de madurez técnica.'
>
> **3. Oportunidad de crecimiento:** [Conecta tus objetivos con la empresa]
> Ejemplo: 'Quiero evolucionar de junior a mid-level, y veo que tienen un programa de mentoring estructurado y tech talks internas. Además, [nombre de persona] mencionó en LinkedIn que crecieron de junior a tech lead en 2 años, eso me inspira.'"

**Red flags a evitar:**
- ❌ "Porque es una empresa grande/famosa"
- ❌ "Por el salario" (aunque sea cierto, no lo digas así)
- ❌ "Para ganar experiencia" (muy genérico)
- ❌ Respuestas que aplican a cualquier empresa

---

### 5. ¿Tienes experiencia trabajando en equipos ágiles?

**Mi respuesta:**

> "Sí, he trabajado con Scrum en varios proyectos. En mi bootcamp y en proyectos freelance, aplicamos ceremonias ágiles adaptadas al tamaño del equipo.
>
> **Experiencia concreta:**
> - **Daily standups:** Sincronización diaria de 15 minutos para compartir progreso, blockers y plan del día
> - **Sprint planning:** Definimos user stories, estimamos con planning poker, priorizamos backlog
> - **Sprint review:** Demostramos features completados al product owner y stakeholders
> - **Retrospectivas:** Mi parte favorita. Analizamos qué salió bien, qué mejorar, y definimos acciones concretas
>
> **Herramientas:** Jira para tracking, Slack para comunicación, GitHub para code review
>
> **Aprendizajes:**
> - La importancia de definir bien el 'Definition of Done'
> - Que las estimaciones mejoran con el tiempo (velocity se estabiliza después de 3-4 sprints)
> - Que las retrospectivas solo funcionan si realmente implementas cambios
>
> **Si no tuvieran experiencia:**
> 'No he trabajado formalmente en Scrum, pero estoy familiarizado con los conceptos: iteraciones cortas, entregas incrementales, feedback continuo. He usado Kanban para proyectos personales y entiendo la filosofía ágil de adaptabilidad. Estoy ansioso por aprender la implementación formal en un equipo profesional.'"

**Por qué funciona:**
- Demuestra conocimiento práctico, no teórico
- Menciona herramientas específicas
- Incluye reflexión sobre el proceso
- Proporciona alternativa si no tienes experiencia

---

## 🎬 Parte 3: Guía para la Simulación de Entrevista

### Roles y Responsabilidades

**👔 Si eres el RECLUTADOR:**

**Preparación:**
- Elige 3 preguntas técnicas y 2 conductuales (del listado abajo)
- Ten una rúbrica mental de qué buscar en cada respuesta
- Investiga brevemente el perfil del candidato (CV ficticio)

**Durante la entrevista:**
- Crea un ambiente profesional pero amigable
- Toma notas visibles (simula interés)
- Haz preguntas de seguimiento: "¿Puedes profundizar en...?"
- Observa lenguaje corporal, claridad, estructura de respuestas

**Feedback a dar:**
- ✅ Qué hizo bien (estructura, ejemplos concretos)
- 🔄 Qué podría mejorar (muletillas, vaguedad, falta de métricas)
- 💡 Cómo sonaría la respuesta "ideal"

---

**💼 Si eres el CANDIDATO:**

**Preparación:**
- Revisa tus respuestas de la Parte 2
- Prepara 2-3 preguntas para hacerle al reclutador al final
- Ten ejemplos de proyectos listos para mencionar

**Durante la entrevista:**
- Toma 2-3 segundos para pensar antes de responder
- Usa estructura STAR para preguntas conductuales
- Sé específico: menciona tecnologías, métricas, aprendizajes
- Mantén contacto visual (si es presencial) o mira a la cámara (si es virtual)

**Feedback a solicitar:**
- "¿Mi respuesta fue clara?"
- "¿Faltó algún detalle técnico que esperabas?"
- "¿Qué nota darías a mi comunicación del 1-10?"

---

### 📋 Banco de Preguntas para la Simulación

#### 3 Preguntas Técnicas Sugeridas:

1. **"Explica la diferencia entre autenticación y autorización. ¿Cómo las implementarías en una API REST?"**
   - *Busca:* Conocimiento de seguridad, JWT, OAuth, roles

2. **"¿Qué es el patrón MVC y cuáles son sus ventajas? ¿Lo has usado en algún proyecto?"**
   - *Busca:* Arquitectura de software, experiencia práctica

3. **"¿Cómo debuguearías una aplicación que funciona en local pero falla en producción?"**
   - *Busca:* Metodología de troubleshooting, conocimiento de herramientas (logs, monitoring)

#### 2 Preguntas Conductuales Sugeridas:

1. **"Cuéntame sobre una vez que tuviste que aprender una tecnología nueva rápidamente."**
   - *Busca:* Capacidad de aprendizaje, autodidactismo, gestión del tiempo

2. **"Describe una situación donde no estuviste de acuerdo con una decisión técnica del equipo."**
   - *Busca:* Comunicación, manejo de conflictos, humildad técnica

---

### 🎥 Checklist para la Grabación (3-5 minutos)

**Antes:**
- [ ] Setup técnico probado (cámara, audio, luz)
- [ ] Fondo neutral y sin distracciones
- [ ] Ambos tienen claro su rol
- [ ] Preguntas seleccionadas (3 técnicas + 2 conductuales)
- [ ] Timer listo (no exceder 5 minutos)

**Estructura del video:**
```
[0:00-0:15] Introducción
  Reclutador: "Hola [nombre], gracias por venir. Cuéntame un poco sobre ti."

[0:15-2:00] Pregunta Personal + 1 Técnica
  - "Háblame de ti" (30-45s)
  - Primera pregunta técnica (60-90s)

[2:00-3:30] Pregunta Técnica + 1 Conductual
  - Segunda pregunta técnica (60s)
  - Primera pregunta conductual (60-90s)

[3:30-4:45] Pregunta final + Preguntas del candidato
  - Última pregunta conductual o técnica (45s)
  - Candidato pregunta algo (30s)

[4:45-5:00] Cierre
  Reclutador: "Muchas gracias, estaremos en contacto."
```

**Después:**
- [ ] Cambien roles y repitan (si tienen tiempo)
- [ ] Den feedback mutuamente usando la rúbrica abajo
- [ ] Identifiquen 2-3 mejoras concretas cada uno

---

### 📊 Rúbrica de Evaluación

**Para el Candidato:**

| Aspecto | 1-2 (Necesita mejorar) | 3-4 (Bien) | 5 (Excelente) |
|---------|------------------------|------------|---------------|
| **Claridad** | Respuestas confusas, divaga | Respuestas comprensibles | Respuestas concisas y estructuradas |
| **Especificidad** | Muy genérico, sin ejemplos | Algunos ejemplos concretos | Ejemplos detallados con métricas |
| **Conocimiento técnico** | Dudas o errores | Conocimiento sólido básico | Demuestra profundidad y matices |
| **Comunicación no verbal** | Nervioso, sin contacto visual | Relajado, profesional | Confiado, lenguaje corporal positivo |
| **Estructura (STAR)** | Sin estructura clara | Usa STAR parcialmente | STAR impecable con impacto |

**Para el Reclutador:**

| Aspecto | 1-2 (Necesita mejorar) | 3-4 (Bien) | 5 (Excelente) |
|---------|------------------------|------------|---------------|
| **Preguntas claras** | Confusas o mal formuladas | Claras y relevantes | Progresivas, indagan profundidad |
| **Escucha activa** | Interrumpe, no escucha | Atento, toma notas | Hace seguimiento inteligente |
| **Ambiente** | Intimidante o muy casual | Profesional | Balance perfecto profesional/amigable |
| **Feedback** | Vago o inexistente | Feedback útil | Feedback específico y accionable |

---

## ✅ Entregables Finales

### Documento de Investigación (1 página)
- [ ] Tipos de entrevistas en TI explicados
- [ ] 3 preguntas técnicas con respuestas preparadas
- [ ] Evaluación de reclutadores en culture fit explicada

### Respuestas Preparadas (Parte 2)
- [ ] "Cuéntame sobre ti" (60-90s escrito)
- [ ] "Mayor desafío técnico" con STAR
- [ ] "Trabajo bajo presión" con ejemplos
- [ ] "Por qué esta empresa" (template adaptable)
- [ ] "Experiencia en ágil" con detalles

### Video de Simulación (3-5 minutos)
- [ ] Grabación con ambos roles visibles
- [ ] Mínimo 3 preguntas técnicas
- [ ] Mínimo 2 preguntas conductuales
- [ ] Calidad de audio/video aceptable
- [ ] Intercambio profesional (saludo, cierre)

---

## 🚀 Reflexión Final

**Claves para una simulación exitosa:**

1. **Tómalo en serio:** Aunque sea práctica, simula realismo. Te prepara para la real.

2. **El feedback es oro:** La mejor práctica incluye retroalimentación específica.

3. **Itera:** Graba múltiples versiones si puedes. La primera nunca es la mejor.

4. **Estudia las preguntas difíciles:** No solo respondas, entiende QUÉ evalúan.

5. **El reclutador también aprende:** Ver qué buscar en candidatos te hace mejor entrevistado.

**Recuerda:** Las entrevistas son habilidades que se entrenan. Cada simulación te acerca más a conseguir el trabajo que buscas. ¡Éxito! 🎯
