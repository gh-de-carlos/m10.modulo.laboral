# 📝 Tarea: Simulando una Entrevista Laboral en TI

**En parejas o grupos, simulen una entrevista**

---

## 🎯 Objetivo de aprendizaje

Conocer y practicar los diferentes tipos de entrevistas laborales utilizadas en la industria TI, diferenciando entre preguntas técnicas, conductuales y de ajuste cultural, con el fin de mejorar la preparación y desempeño del candidato.

---

## 🧠 Instrucciones

### Parte 1: Investigación

Investiga los siguientes aspectos y responde en un documento (1 página):

1. **¿Cuáles son los tipos de entrevistas más comunes en el área de TI?**
   - Ejemplos: técnica, por competencias, cultural, etc.

2. **Menciona 3 preguntas frecuentes en entrevistas técnicas para tu perfil**
   - Ejemplos de perfiles: Desarrollador, QA, Data, etc.

3. **¿Qué buscan evaluar los reclutadores en una entrevista de cultura organizacional?**

---

### Parte 2: Preparación del discurso

Redacta tus respuestas personales para las siguientes preguntas típicas de entrevista:

1. **Cuéntame sobre ti.**

2. **¿Cuál ha sido el mayor desafío técnico que has enfrentado?**

3. **¿Cómo manejas el trabajo bajo presión?**

4. **¿Por qué te gustaría trabajar en nuestra empresa?**

5. **¿Tienes experiencia trabajando en equipos ágiles?**

---

### Parte 3: Simulación de entrevista (opcional, ideal si es una clase práctica)

- En parejas o grupos, simulen una entrevista TI (uno hace de reclutador, otro de candidato).
- Graben un video corto (3-5 minutos) o presenten un roleplay en clase.
- La entrevista debe incluir al menos **3 preguntas técnicas** y **2 conductuales**.

---

## Desarrollo

### Parte 1: Investigación

#### 1. ¿Cuáles son los tipos de entrevistas más comunes en el área de TI?

**a) Entrevista Técnica**
- Evalúa conocimientos específicos en programación, algoritmos, estructuras de datos y tecnologías
- Formato: coding challenges en vivo, preguntas sobre arquitectura, resolución de problemas
- Ejemplo: "Implementa una función que detecte palíndromos con complejidad O(n)"

**b) Entrevista por Competencias (Behavioral)**
- Evalúa soft skills: trabajo en equipo, resolución de conflictos, liderazgo, adaptabilidad
- Utiliza el método STAR (Situación, Tarea, Acción, Resultado)
- Ejemplo: "Cuéntame sobre una vez que aprendiste una tecnología nueva bajo presión"

**c) Entrevista de Cultura Organizacional (Culture Fit)**
- Determina alineación con valores, misión y estilo de trabajo de la empresa
- Evalúa motivaciones, objetivos profesionales y compatibilidad con el equipo
- Ejemplo: "¿Prefieres trabajar de forma autónoma o colaborativa? ¿Por qué?"

**d) Entrevista de Diseño de Sistemas (System Design)**
- Para roles senior: evalúa capacidad de arquitectura de sistemas escalables
- Se diseñan sistemas completos considerando escalabilidad, trade-offs, microservicios
- Ejemplo: "Diseña un sistema de notificaciones para 10 millones de usuarios"

**e) Entrevista de Portafolio/Proyecto**
- Revisión de proyectos reales del candidato
- Evalúa calidad del código, buenas prácticas y capacidad de explicar decisiones técnicas
- Ejemplo: "Explica los desafíos técnicos de tu proyecto más complejo"

**f) Pair Programming**
- Programar en colaboración para evaluar comunicación y trabajo en equipo
- Se observa receptividad a feedback y pensamiento colaborativo
- Ejemplo: "Refactoricemos esta función juntos"

---

#### 2. 3 Preguntas frecuentes en entrevistas técnicas para Desarrollador Full Stack

**Pregunta 1: "¿Cuál es la diferencia entre var, let y const en JavaScript?"**

**Respuesta:**
- `var`: scope de función, permite redeclaración, hoisting completo (legacy ES5)
- `let`: scope de bloque, no permite redeclaración, es mutable
- `const`: scope de bloque, no permite reasignación (aunque objetos/arrays internos son mutables)

**Uso recomendado:** `const` por defecto para inmutabilidad, `let` cuando necesites reasignar, evitar `var`.

```javascript
const API_URL = "https://api.com"; // No cambiará
let counter = 0; // Necesita reasignación
counter++;
```

---

**Pregunta 2: "Explica el Event Loop en Node.js y cómo funcionan las promesas"**

**Respuesta:**
El Event Loop permite operaciones no bloqueantes en Node.js a pesar de ser single-threaded. Procesa callbacks de operaciones asíncronas en fases: timers, I/O callbacks, poll, check, close callbacks.

Las **promesas** representan el resultado futuro de una operación asíncrona. Estados: pending → fulfilled/rejected.

```javascript
// Evolución de código asíncrono
// Callback hell ❌
getData(function(a) {
  getMore(a, function(b) {
    console.log(b);
  });
});

// Promesas ✅
getData()
  .then(a => getMore(a))
  .then(b => console.log(b))
  .catch(err => console.error(err));

// Async/await ✅✅
async function fetchData() {
  try {
    const a = await getData();
    const b = await getMore(a);
    console.log(b);
  } catch (error) {
    console.error(error);
  }
}
```

---

**Pregunta 3: "¿Cómo optimizarías consultas SQL en una aplicación con millones de registros?"**

**Respuesta:**

**Diagnóstico primero:**
- Usar `EXPLAIN ANALYZE` para identificar cuellos de botella
- Revisar slow query logs
- Detectar full table scans

**Optimizaciones:**

1. **Índices estratégicos:**
```sql
CREATE INDEX idx_users_email ON users(email);
```

2. **Evitar SELECT *:**
```sql
-- Mal
SELECT * FROM users WHERE active = true;

-- Bien
SELECT id, name, email FROM users WHERE active = true;
```

3. **Joins eficientes con índices en columnas de join**

4. **Paginación con LIMIT/OFFSET**

5. **Caché con Redis para queries frecuentes**

6. **Connection pooling para reducir overhead**

7. **Particionamiento de tablas grandes por fecha o región**

---

#### 3. ¿Qué buscan evaluar los reclutadores en una entrevista de cultura organizacional?

**a) Alineación con valores de la empresa**
- ¿Compartes los principios fundamentales (innovación, colaboración, transparencia)?
- Investigan si tus valores personales son compatibles con la cultura

**b) Estilo de trabajo y colaboración**
- Preferencia por autonomía vs. supervisión
- Capacidad de dar y recibir feedback
- Trabajo en equipo vs. individual

**c) Motivación y objetivos a largo plazo**
- Por qué esta empresa específicamente (no respuestas genéricas)
- Qué buscas en tu carrera profesional
- Interés genuino en el producto/servicio

**d) Capacidad de adaptación al cambio**
- Cómo reaccionas ante pivotes o cambios de prioridades
- Comodidad con ambigüedad (especialmente en startups)

**e) Comunicación y resolución de conflictos**
- Manejo de desacuerdos con compañeros
- Comunicación proactiva de problemas
- Madurez emocional

**f) Balance vida-trabajo**
- Qué necesitas para ser productivo
- Manejo del estrés
- Expectativas del ambiente laboral

**g) Ownership y responsabilidad**
- Iniciativa sin supervisión constante
- Asumir responsabilidad por errores
- Mentalidad de "dueño" del producto

**Cómo prepararse:**
- Investigar la cultura en Glassdoor, LinkedIn, blog de la empresa
- Conectar valores personales con ejemplos concretos de tu experiencia
- Preparar preguntas sobre la cultura: "¿Cómo celebran logros del equipo?"
- Ser auténtico: el culture fit es bidireccional

---

### Parte 2: Preparación del Discurso

#### 1. Cuéntame sobre ti

Hola, soy Carlos, desarrollador full stack con experiencia en JavaScript, Node.js y PostgreSQL. Mi camino en tecnología comenzó hace 3 años cuando completé un bootcamp intensivo donde construimos aplicaciones desde cero, trabajando en equipo bajo metodologías ágiles.

Durante mi formación, me especialicé en desarrollo frontend con JavaScript y Vue.js, pero también adquirí experiencia sólida en backend con Java, Spring Boot y bases de datos SQL. Uno de mis proyectos más significativos fue para Tecprosalud: un sistema interno que permite a médicos llevar consultas médicas a lugares remotos donde el acceso a centros médicos no es equitativo. Trabajé en toda la stack: frontend con Vue.js e integración de APIs REST en el backend con Spring Boot y PostgreSQL.

Lo que más me motiva del desarrollo es resolver problemas reales con tecnología. Me apasiona escribir código limpio, aplicar patrones de diseño y aprender constantemente nuevas herramientas. Estoy buscando un rol donde pueda aportar mi experiencia técnica mientras sigo creciendo profesionalmente en un equipo que valore la calidad y la colaboración.

---

#### 2. ¿Cuál ha sido el mayor desafío técnico que has enfrentado?

**Situación:** Durante el desarrollo del sistema para Tecprosalud, teníamos que integrar múltiples servicios externos (APIs de laboratorios, sistemas de citas, pagos) con tiempos de respuesta muy variables, causando timeouts y mala experiencia de usuario.

**Tarea:** Mi responsabilidad era rediseñar la arquitectura de integración para que fuera resiliente y no bloqueara la interfaz mientras esperábamos respuestas de servicios lentos.

**Acción:** 
- Implementé un patrón de procesamiento asíncrono con colas de mensajes
- Agregué circuit breakers para servicios externos con Resilience4j
- Configuré timeouts agresivos y reintentos exponenciales
- Añadí caché con Redis para respuestas frecuentes
- Implementé polling en el frontend en lugar de espera síncrona

**Resultado:** Redujimos los timeouts del 15% de las peticiones a menos del 1%. El tiempo de respuesta percibido por usuarios mejoró de 8 segundos a 2 segundos. Documenté el patrón para que el equipo lo aplicara en otras integraciones. Aprendí mucho sobre sistemas distribuidos y la importancia de diseñar para el fallo.

---

#### 3. ¿Cómo manejas el trabajo bajo presión?

Bajo presión me enfoco en tres aspectos fundamentales: priorización, comunicación y mantener calidad mínima.

**Priorización:** Identifico qué es crítico vs. importante usando la matriz de Eisenhower (urgente/importante). Si tengo un bug en producción y una feature nueva, el bug va primero sin duda.

**Comunicación proactiva:** Informo temprano si veo que no llegaré a un deadline. Prefiero renegociar plazos o scope antes que entregar algo mal hecho. En un sprint ajustado, propuse entregar la feature core sin los "nice-to-have", entregándolos después. El equipo lo valoró porque teníamos algo funcional a tiempo.

**Calidad sobre velocidad:** Incluso bajo presión, mantengo estándares mínimos: tests para lógica crítica, code review aunque sea rápido, y documentación básica. Los atajos de hoy son deuda técnica mañana.

**Manejo personal:** Cuando la presión me supera, tomo breaks cortos de 5 minutos. También soy honesto con el equipo si necesito ayuda. El trabajo en equipo existe para momentos difíciles.

---

#### 4. ¿Por qué te gustaría trabajar en nuestra empresa?

Me atrae esta empresa por tres razones principales:

**El producto/misión:** Me interesa el impacto que genera su tecnología [especificar según la empresa]. Resolver problemas reales para usuarios finales es lo que me motiva en el desarrollo de software.

**Stack tecnológico y cultura de ingeniería:** He investigado sobre su stack y veo que utilizan [tecnologías específicas de la empresa]. Esto se alinea con mi experiencia en JavaScript, Vue.js y Spring Boot, y también representa una oportunidad de seguir creciendo técnicamente. Valoro especialmente [mencionar algo específico: code reviews, documentación técnica, tech talks].

**Oportunidad de crecimiento:** Busco un ambiente donde pueda evolucionar profesionalmente de junior/mid-level mientras aporto valor desde el inicio. He leído sobre [mencionar programa de mentoring, proyectos interesantes, o cultura de aprendizaje] y eso me inspira a contribuir al equipo mientras desarrollo nuevas habilidades.

---

#### 5. ¿Tienes experiencia trabajando en equipos ágiles?

Sí, he trabajado con Scrum en varios proyectos. En mi bootcamp y proyectos posteriores, aplicamos ceremonias ágiles adaptadas al tamaño del equipo.

**Experiencia concreta:**
- **Daily standups:** Sincronización diaria de 15 minutos para compartir progreso, blockers y plan del día
- **Sprint planning:** Definimos user stories, estimamos con planning poker, priorizamos backlog
- **Sprint review:** Demostramos features completados al product owner y stakeholders
- **Retrospectivas:** Mi parte favorita. Analizamos qué salió bien, qué mejorar, y definimos acciones concretas para implementar

**Herramientas:** Jira para tracking, Slack para comunicación asíncrona, GitHub para code review y control de versiones.

**Aprendizajes clave:**
- La importancia de definir claramente el "Definition of Done"
- Las estimaciones mejoran con el tiempo (velocity se estabiliza después de 3-4 sprints)
- Las retrospectivas solo funcionan si realmente implementas los cambios acordados
- La comunicación constante es más valiosa que la documentación exhaustiva

He aprendido que la agilidad no es solo seguir ceremonias, sino mantener una mentalidad de mejora continua, entregas incrementales y adaptabilidad al cambio.

