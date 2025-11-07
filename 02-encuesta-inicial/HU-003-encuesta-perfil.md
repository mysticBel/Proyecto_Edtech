# HU-003: Encuesta Inicial de Evaluación de Perfil del Alumno

## 📋 METADATOS
- **ID**: HU-003
- **Épica**: Personalización y Adaptación
- **Prioridad**: CRÍTICA
- **Estimación**: 8 Story Points
- **Sprint**: 2
- **Stakeholders**: Alumnos, Profesores, Psicopedagogos, Director Académico
- **Fecha Creación**: 2025-11-06

---

## 🎯 ANÁLISIS INICIAL MULTI-PERSPECTIVA

### Perspectiva del Usuario
**¿Quién?** Alumno nuevo de primaria (8-12 años) realizando primera evaluación  
**¿Qué?** Encuesta diagnóstica gamificada de 15-20 preguntas en 10-15 minutos  
**¿Por qué?** Para identificar su perfil de aprendizaje, conocimientos previos y áreas de mejora, permitiendo adaptación del contenido

**Ambigüedades detectadas**:
- ¿La encuesta es obligatoria o opcional?
- ¿Se puede pausar y retomar en otro momento?
- ¿Qué dimensiones evalúa (cognitivo, emocional, estilos de aprendizaje)?
- ¿Los resultados son visibles para el alumno inmediatamente?

### Perspectiva Técnica
**Implementable**: ✅ Sí con IA  
**Restricciones**:
- Algoritmo de machine learning para clasificación de perfiles (Random Forest/Neural Network)
- Base de datos de preguntas categorizadas por dimensión
- Adaptive testing: siguientes preguntas dependen de respuestas previas
- Almacenamiento de respuestas para análisis longitudinal

### Perspectiva de Negocio
**Valor medible**:
- Incremento 45% en engagement por contenido personalizado
- Reducción 35% en frustración de alumnos con contenido inadecuado
- Mejora 30% en rendimiento académico en primeros 3 meses
- 100% de alumnos perfilados en primera semana

---

## 🔄 GENERACIÓN DE ALTERNATIVAS

### VERSIÓN A - ENFOQUE CENTRADO EN USUARIO (UX)

**Como** alumno nuevo en la plataforma  
**Quiero** completar una encuesta interactiva y visualmente atractiva de 15 preguntas  
**Para** que el sistema conozca cómo aprendo mejor y me recomiende contenido adecuado a mi nivel

#### Criterios de Aceptación UX:
1. **DADO** que soy un alumno nuevo  
   **CUANDO** inicio la encuesta  
   **ENTONCES** veo una introducción gamificada: "¡Vamos a conocerte mejor! Responde estas preguntas divertidas"

2. **DADO** que estoy respondiendo  
   **CUANDO** contesto cada pregunta  
   **ENTONCES** veo progreso visual (8 de 15) y animaciones de refuerzo positivo

3. **DADO** que completo la encuesta  
   **CUANDO** envío la última respuesta  
   **ENTONCES** veo mi perfil de aprendizaje con ilustraciones atractivas ("Eres un Explorador Visual")

4. **DADO** que quiero pausar  
   **CUANDO** hago clic en "Pausa"  
   **ENTONCES** puedo retomar desde donde quedé por hasta 7 días

5. **DADO** que uso tablet/móvil  
   **CUANDO** accedo a la encuesta  
   **ENTONCES** la interfaz se adapta con botones grandes y navegación táctil

---

### VERSIÓN B - ENFOQUE TÉCNICO EFICIENTE

**Como** sistema de personalización  
**Quiero** implementar Computer Adaptive Testing (CAT) con algoritmo de machine learning  
**Para** determinar el perfil óptimo del alumno con mínimas preguntas y máxima precisión (>85%)

#### Criterios de Aceptación Técnicos:
1. **DADO** que se implementa algoritmo CAT  
   **CUANDO** el alumno responde pregunta N  
   **ENTONCES** se selecciona pregunta N+1 usando Item Response Theory para maximizar información

2. **DADO** que se clasifican respuestas  
   **CUANDO** se procesan todas las respuestas  
   **ENTONCES** el algoritmo Random Forest clasifica en 8 perfiles con confianza ≥80%

3. **DADO** que se detecta perfil  
   **CUANDO** la encuesta termina  
   **ENTONCES** se genera vector de características: [visual, auditivo, kinestésico, lógico, social, verbal, musical, naturalista]

4. **DADO** que se almacenan datos  
   **CUANDO** se guardan respuestas  
   **ENTONCES** se mantiene trazabilidad para análisis longitudinal y re-calibración del modelo

5. **DADO** que se busca precisión  
   **CUANDO** hay incertidumbre en clasificación  
   **ENTONCES** se agregan 2-3 preguntas adicionales dirigidas hasta alcanzar confianza ≥80%

---

### VERSIÓN C - ENFOQUE DE VALOR DE NEGOCIO

**Como** institución educativa  
**Quiero** una herramienta de diagnóstico que genere insights accionables para profesores  
**Para** personalizar enseñanza desde día 1 y mejorar resultados de aprendizaje en 30%

#### Criterios de Aceptación de Negocio:
1. **DADO** que se completa diagnóstico  
   **CUANDO** se genera perfil del alumno  
   **ENTONCES** se crean recomendaciones automáticas para el profesor: "María aprende mejor con diagramas y ejemplos concretos"

2. **DADO** que se busca retorno de inversión  
   **CUANDO** se implementa personalización  
   **ENTONCES** se trackean KPIs: tiempo en plataforma, ejercicios completados, satisfacción, calificaciones

3. **DADO** que se necesita validación  
   **CUANDO** psicopedagogos revisan perfiles  
   **ENTONCES** >90% de perfiles son considerados "precisos" según criterio experto

4. **DADO** que hay diferentes contextos  
   **CUANDO** se usa en distintas materias  
   **ENTONCES** el perfil se aplica exitosamente en matemáticas, ciencias, lengua con mejoras medibles

5. **DADO** que se busca escala  
   **CUANDO** 500+ alumnos usan el sistema  
   **ENTONCES** se demuestra ROI positivo: +30% rendimiento, -25% tiempo de tutoría individual

**KPIs**:
- Precisión de perfiles: >85% validada por expertos
- Mejora en engagement: +45% tiempo en plataforma
- Satisfacción: >8/10 en encuestas de alumnos y profesores

---

## 🎯 VERSIÓN FINAL SINTETIZADA

**Matriz de Decisión**:
- Valor de negocio (30%): Versión C = 9/10
- Factibilidad técnica (25%): Versión B = 7/10 (CAT es complejo)
- Experiencia de usuario (25%): Versión A = 9/10
- Esfuerzo de implementación (20%): Versión A = 8/10
**Puntuación final**: 8.25/10

**Decisión**: Implementar enfoque híbrido: UX de Versión A + técnica simplificada de B + KPIs de C

---

## 📝 HISTORIA REFINADA FINAL

**Como** alumno de primaria (8-12 años) recién registrado en la plataforma  
**Quiero** completar una encuesta interactiva de 15-18 preguntas gamificadas en 10-15 minutos  
**Para** que el sistema identifique mi perfil de aprendizaje (visual, auditivo, kinestésico, lógico) con 85% de precisión y personalice automáticamente mis contenidos educativos

---

## ✅ CRITERIOS DE ACEPTACIÓN DETALLADOS (FINAL)

### Escenario 1: Inicio de Encuesta con Onboarding Gamificado
**DADO** que soy un alumno de 10 años recién registrado "Luis Martínez"  
**Y** es mi primer acceso a la plataforma  
**CUANDO** el sistema detecta que no tengo perfil completado  
**ENTONCES**:
- Veo modal de bienvenida: "¡Hola Luis! Antes de empezar, vamos a conocerte mejor 🎯"
- Se explica con iconos: "Responde 15 preguntas divertidas para que te recomendemos las mejores actividades"
- Estimación de tiempo: "Te tomará solo 10-15 minutos"
- Botones: [Empezar ahora] [Hacerlo más tarde]
- Si elijo "más tarde" → Recordatorio suave cada 3 días por 2 semanas

### Escenario 2: Flujo de Preguntas Adaptativas
**DADO** que inicio la encuesta  
**CUANDO** respondo las primeras 5 preguntas base sobre estilos de aprendizaje  
**ENTONCES**:
- **Pregunta 1** (Visual): "¿Cómo prefieres que te expliquen algo nuevo?"
  - A) Con diagramas y dibujos 🎨
  - B) Con palabras y explicaciones 📖
  - C) Haciéndolo yo mismo 🔧
- **Pregunta 2** (Lógica): "¿Qué te gusta más?"
  - A) Resolver acertijos y puzzles 🧩
  - B) Leer historias y cuentos 📚
  - C) Hacer experimentos 🔬
- **Sistema selecciona siguientes preguntas** basado en tendencias detectadas:
  - Si respuestas indican perfil Visual → Más preguntas sobre preferencias visuales
  - Si indican Kinestésico → Preguntas sobre actividades prácticas
- **Barra de progreso** visible: "5 de 15 completadas" con animación

### Escenario 3: Evaluación de Conocimientos Previos por Materia
**DADO** que he respondido preguntas de estilo de aprendizaje  
**CUANDO** el sistema evalúa mis conocimientos previos  
**ENTONCES**:
- **Matemáticas** (3 preguntas adaptativas):
  - Nivel 1: "¿Cuánto es 5 + 3?" → Si acierto → "¿Cuánto es 12 × 4?"
  - Si fallo → Pregunta más fácil → "¿Cuántos dedos tienes en total?"
- **Ciencias** (2 preguntas):
  - "¿Qué necesitan las plantas para crecer?"
  - "¿Por qué llueve?"
- **Lectura** (2 preguntas):
  - Leer párrafo corto de 50 palabras y responder comprensión
- **Cada pregunta tiene tiempo límite de 60 segundos** (evita overthinking)
- **Respuestas registran**: tiempo_respuesta, nivel_dificultad, confianza_estimada

### Escenario 4: Detección Automática de Perfil con Machine Learning
**DADO** que he completado 15 preguntas  
**CUANDO** el algoritmo procesa mis respuestas  
**ENTONCES**:
- **Backend ejecuta algoritmo Random Forest**:
  ```python
  features = [
      visual_score,      # 0.8 (alta preferencia visual)
      auditory_score,    # 0.3 (baja preferencia auditiva)
      kinesthetic_score, # 0.6 (media preferencia kinestésica)
      logical_score,     # 0.7 (alta capacidad lógica)
      math_level,        # 6 (nivel 6to grado)
      reading_level,     # 5 (nivel 5to grado)
      confidence_level   # 0.85 (alta confianza general)
  ]
  
  predicted_profile = model.predict(features)
  confidence = model.predict_proba(features).max()
  ```
- **Si confianza ≥ 80%** → Perfil asignado
- **Si confianza < 80%** → Se agregan 3 preguntas dirigidas para clarificar
- **Resultado**: "Perfil: Visual-Lógico" con confianza 87%

### Escenario 5: Presentación de Resultados Gamificada
**DADO** que mi perfil ha sido determinado como "Explorador Visual-Lógico"  
**CUANDO** veo los resultados  
**ENTONCES**:
- **Animación de revelación** con confetti y sonido de logro
- **Avatar personalizado**: Robot con lentes (visual) y calculadora (lógico)
- **Descripción amigable**: "¡Eres un Explorador Visual-Lógico! 🤖🔍"
  - "Te encantan los diagramas, gráficos y resolver problemas paso a paso"
  - "Aprendes mejor cuando ves ejemplos visuales y patrones"
- **Fortalezas identificadas**:
  - ✅ Matemáticas: Nivel 6to grado
  - ✅ Pensamiento lógico: Muy desarrollado
  - ✅ Memoria visual: Excelente
- **Áreas de crecimiento**:
  - 🎯 Lectura comprensiva: Nivel 5to grado
  - 🎯 Expresión oral: Por desarrollar
- **Recomendaciones personalizadas**:
  - "Te recomendamos empezar con ejercicios de geometría visual"
  - "Los videos explicativos con diagramas son perfectos para ti"

### Escenario 6: Casos de Incertidumbre - Preguntas Adicionales
**DADO** que mis respuestas son ambiguas (ej: 50% Visual, 45% Auditivo, 5% Kinestésico)  
**CUANDO** el algoritmo no puede decidir con confianza ≥80%  
**ENTONCES**:
- Sistema muestra: "¡Casi terminamos! Solo 3 preguntas más para conocerte mejor" 🎯
- **Preguntas dirigidas** para diferenciar:
  - "Cuando estudias, ¿qué te ayuda más?"
    - A) Hacer mapas mentales y esquemas
    - B) Leer en voz alta y escuchar explicaciones
    - C) Tomar notas a mano mientras leo
- Cada respuesta **incrementa peso** del estilo correspondiente
- Al finalizar → Nueva clasificación con confianza mejorada

### Escenario 7: Guardado de Progreso y Reanudación
**DADO** que estoy en pregunta 8 de 15  
**Y** necesito pausar la encuesta  
**CUANDO** hago clic en "Pausar"  
**ENTONCES**:
- Mensaje: "¿Quieres pausar? Podrás continuar desde aquí cuando vuelvas"
- Botones: [Sí, pausar] [No, continuar]
- Si pauso → Se guarda estado en localStorage y BD:
  ```json
  {
    "user_id": 12345,
    "survey_session_id": "uuid-abc-123",
    "current_question": 8,
    "answers": [{"q1": "A", "timestamp": "..."}, ...],
    "started_at": "2025-11-06T10:30:00Z",
    "paused_at": "2025-11-06T10:37:00Z"
  }
  ```
- **Al regresar** → Modal: "¡Hola Luis! Continuemos desde donde quedaste (pregunta 8 de 15)"
- **Si no retoma en 7 días** → Email recordatorio suave

### Escenario 8: Validación por Psicopedagogos (Proceso Posterior)
**DADO** que mi perfil "Visual-Lógico" ha sido asignado  
**CUANDO** el sistema ejecuta validación de calidad  
**ENTONCES**:
- **10% de perfiles aleatorios** son marcados para revisión humana
- Psicopedagogo "Dr. García" recibe notificación:
  - "Revisar perfil de Luis Martínez (8 años, Visual-Lógico, confianza 87%)"
  - Panel muestra: respuestas originales, justificación del algoritmo, perfil asignado
- **Dr. García puede**:
  - ✅ Aprobar perfil ("Parece correcto")
  - ⚠️ Sugerir ajustes ("Más kinestésico de lo detectado")
  - ❌ Rechazar ("Perfil incorrecto, re-evaluar")
- **Si hay ajustes** → Se actualiza perfil y se notifica al profesor
- **Métricas agregadas** → "Precisión del algoritmo: 89% según validaciones humanas"

---

## 🔗 DEPENDENCIAS IDENTIFICADAS

### Dependencias Técnicas
1. **Machine Learning Pipeline**
   - Dataset de entrenamiento con 1000+ respuestas etiquetadas por psicopedagogos
   - Modelo Random Forest o XGBoost para clasificación de perfiles
   - Pipeline de pre-procesamiento de respuestas

2. **Base de Datos**
   - Tabla `assessment_questions` con categoría, dificultad, tipo
   - Tabla `student_responses` con timestamp, confidence, tiempo_respuesta
   - Tabla `learning_profiles` con vectores de características

3. **APIs Internas**
   - GET /api/v1/assessment/start (inicia encuesta)
   - POST /api/v1/assessment/answer (registra respuesta)
   - GET /api/v1/assessment/next-question (algoritmo adaptativo)
   - POST /api/v1/assessment/complete (finaliza y calcula perfil)

### Dependencias de Negocio
1. **Pre-requisitos**
   - Validación pedagógica de preguntas por equipo de psicopedagogos
   - Definición de 8 perfiles de aprendizaje (VARK + Inteligencias Múltiples)
   - Criterios de edad apropiados para primaria (8-12 años)

2. **Procesos**
   - Workflow de revisión de perfiles por especialistas
   - Proceso de re-evaluación cada 6 meses
   - Capacitación de profesores en interpretación de perfiles

### Dependencias de Datos
1. **Fuentes de Datos**
   - Investigación psicopedagógica sobre estilos de aprendizaje en primaria
   - Benchmarks de conocimientos por grado (matemáticas, lectura, ciencias)
   - Datos de validación cruzada con test psicológicos estándar

2. **Transformaciones**
   - Normalización de respuestas por edad (8 años vs 12 años)
   - Pesos adaptativos según contexto cultural/regional
   - Algoritmo de decaimiento de confianza en perfil (actualización semestral)

---

## ⚠️ RIESGOS Y MITIGACIONES

### Riesgo 1: Perfiles Inexactos por Sesgo de Algoritmo
**Descripción**: Algoritmo ML genera perfiles incorrectos, especialmente para minorías  
**Probabilidad**: Media | **Impacto**: Alto  
**Mitigación**:
- **Dataset balanceado**: Incluir respuestas de diferentes contextos socioeconómicos
- **Validación cruzada**: 10% de perfiles revisados por psicopedagogos
- **A/B Testing**: Comparar algoritmo vs evaluación humana en grupo control
- **Métricas de equidad**: Analizar precisión por género, edad, región
- **Re-entrenamiento**: Modelo actualizado cada trimestre con nuevos datos
- **Meta**: >85% precisión validada por expertos

### Riesgo 2: Resistencia de Alumnos a Completar Encuesta
**Descripción**: Alumnos abandonan encuesta por aburrimiento o duración excesiva  
**Probabilidad**: Alta | **Impacto**: Alto  
**Mitigación**:
- **Gamificación**: Avatares, puntos, animaciones de progreso
- **Duración optimizada**: Máximo 15 preguntas, 10-15 minutos
- **Preguntas atractivas**: Visuales, contextualizadas, edad-apropiadas
- **Puntos de pausa**: Guardar progreso, reanudar later
- **Incentivos**: "Desbloquea tu primer avatar al completar"
- **Meta**: >90% tasa de completitud

### Riesgo 3: Sobreinterpretación de Resultados por Profesores
**Descripción**: Profesores usan perfiles como etiquetas rígidas limitando potencial  
**Probabilidad**: Media | **Impacto**: Alto  
**Mitigación**:
- **Capacitación**: Workshop "Perfiles como guía, no como límites"
- **Documentación clara**: "Luis tiene tendencia visual, pero puede aprender de otras formas"
- **Actualizaciones periódicas**: Re-evaluación cada 6 meses
- **Múltiples dimensiones**: Mostrar perfil como espectro, no categoría única
- **Alertas**: "Los perfiles son orientativos y pueden cambiar"
- **Meta**: <5% de quejas por "encasillamiento"

### Riesgo 4: Problemas de Privacidad con Datos Psicológicos
**Descripción**: Datos sensibles sobre perfiles cognitivos mal manejados  
**Probabilidad**: Baja | **Impacto**: Crítico  
**Mitigación**:
- **Anonimización**: Respuestas sin identificadores directos
- **Consentimiento explícito**: Padres aprueban evaluación psicopedagógica
- **Acceso limitado**: Solo profesores asignados ven perfil completo
- **Retención limitada**: Datos eliminados al finalizar etapa educativa
- **Cifrado**: Toda comunicación y almacenamiento encriptado
- **Auditoría legal**: Revisión GDPR/FERPA compliance

### Riesgo 5: Dependencia Excesiva de Tecnología vs Observación Humana
**Descripción**: Sistema automatizado reemplaza observación pedagógica natural  
**Probabilidad**: Media | **Impacto**: Medio  
**Mitigación**:
- **Herramienta complementaria**: "El perfil es un punto de partida, no la verdad absoluta"
- **Observación docente**: Campo para que profesor añada observaciones propias
- **Flexibilidad**: Profesor puede ajustar perfil basado en experiencia en aula
- **Validación continua**: Comparar predicciones vs resultados reales
- **Balance**: 70% algoritmo + 30% criterio docente

---

## 📊 ESTIMACIÓN Y ESFUERZO

### Breakdown de Tareas (8 Story Points = ~64 horas)

1. **Diseño de Banco de Preguntas** (8h)
   - Creación de 50+ preguntas validadas por psicopedagogos
   - Categorización por dimensión (visual, auditivo, kinestésico, lógico)
   - Adaptación de lenguaje para edades 8-12 años

2. **Frontend - Interfaz de Encuesta Gamificada** (12h)
   - UI responsive con animaciones y progreso visual
   - Componentes: preguntas múltiple opción, barra progreso, avatares
   - Lógica de guardado local y reanudación

3. **Backend - Lógica Adaptativa** (10h)
   - Algoritmo de selección de siguiente pregunta
   - Endpoint para registro de respuestas con timestamps
   - Sistema de pausa y reanudación de sesiones

4. **Machine Learning - Clasificación de Perfiles** (12h)
   - Dataset sintético inicial de 1000 respuestas
   - Entrenamiento de modelo Random Forest
   - Pipeline de predicción con confianza
   - Validación cruzada y métricas de precisión

5. **Backend - Gestión de Perfiles** (6h)
   - CRUD de perfiles de aprendizaje
   - Sistema de versionado (perfil evoluciona)
   - APIs para consulta por profesor/alumno

6. **Gamificación y UX** (4h)
   - Sistema de avatares según perfil
   - Animaciones de logro y refuerzo positivo
   - Personalización de mensajes por edad

7. **Testing y Validación** (8h)
   - Unit tests del algoritmo de clasificación
   - Integration tests del flujo completo
   - User testing con grupo de 20 alumnos reales
   - Validación con psicopedagogos

8. **Documentación** (4h)
   - Guía de interpretación para profesores
   - Manual técnico del algoritmo
   - Política de privacidad específica

**Variación estimada**: ±25% (48-80 horas) por complejidad del ML

---

## 🎯 VALIDATION CHECKLIST

- [x] **Historia cumple criterios INVEST**
  - ✅ Independent: Funciona después de registro (HU-002)
  - ✅ Negotiable: Número de preguntas y algoritmo adaptables
  - ✅ Valuable: +45% engagement, +30% rendimiento académico
  - ✅ Estimable: 8 SP = 64h con breakdown detallado
  - ⚠️ Small: Requiere 2 sprints por complejidad ML
  - ✅ Testable: 8 escenarios con métricas específicas

- [x] **Criterios de aceptación son testeables**
  - GIVEN/WHEN/THEN en todos los escenarios
  - Métricas: 15-18 preguntas, 10-15 min, >85% precisión
  - Casos límite: abandono, incertidumbre, pausa/reanudación

- [x] **Dependencias están documentadas**
  - Técnicas: ML pipeline, bases de datos, APIs
  - Negocio: validación psicopedagógica, capacitación docente
  - Datos: dataset de entrenamiento, benchmarks educativos

- [x] **Riesgos están identificados y mitigados**
  - 5 riesgos principales con mitigaciones específicas
  - Foco en precisión, abandono, sobreinterpretación, privacidad

- [x] **Estimación está dentro del rango esperado**
  - 8 SP justificados por complejidad ML + gamificación + validación

- [ ] **Stakeholders han validado la propuesta** (Pendiente: Psicopedagogos, Ética de IA)

---

## 📈 MÉTRICAS DE ÉXITO POST-IMPLEMENTACIÓN

### Métricas Técnicas
- **Precisión del algoritmo**: >85% validada por psicopedagogos
- **Tiempo de completitud**: 10-15 minutos (p50)
- **Tasa de abandono**: <10%
- **Disponibilidad del servicio**: >99.5%

### Métricas de Negocio
- **Alumnos perfilados**: 100% en primera semana
- **Mejora en engagement**: +45% tiempo en plataforma
- **Mejora en rendimiento**: +30% en evaluaciones (3 meses)
- **Satisfacción de profesores**: >8/10 en utilidad de perfiles

### Métricas de Usuario
- **Tasa de completitud**: >90%
- **Satisfacción con proceso**: >8/10
- **Re-evaluaciones voluntarias**: >60% cada 6 meses
- **Percepción de precisión**: >80% "el perfil me describe bien"

### Métricas de Calidad
- **Validación por expertos**: >90% perfiles considerados precisos
- **Actualizaciones de perfil**: <15% requieren corrección manual
- **Quejas por encasillamiento**: <5% de profesores/padres

---

## 📝 NOTAS ADICIONALES

### Marco Teórico Utilizado
- **VARK Model**: Visual, Auditory, Reading/Writing, Kinesthetic
- **Howard Gardner**: Inteligencias Múltiples (8 tipos)
- **David Kolb**: Estilos de Aprendizaje Experiencial
- **Item Response Theory**: Para testing adaptativo
- **Bloom's Taxonomy**: Para clasificación de conocimientos

### Consideraciones de Desarrollo
- **Framework ML**: Scikit-learn para prototipo, TensorFlow para producción
- **Almacenamiento**: PostgreSQL para respuestas, Redis para sesiones activas
- **Monitoreo**: Drift detection para degradación de modelo
- **Escalabilidad**: Diseño para 10K+ evaluaciones simultáneas

### Roadmap de Evolución
- **Fase 1**: Perfiles básicos (visual/auditivo/kinestésico/lógico)
- **Fase 2**: Inteligencias múltiples completas (8 dimensiones)
- **Fase 3**: Perfiles emocionales y motivacionales
- **Fase 4**: AI generativo para preguntas personalizadas

---

## 🔄 HISTORIAL DE CAMBIOS

| Fecha | Versión | Cambios | Autor |
|-------|---------|---------|-------|
| 2025-11-06 | 1.0 | Creación inicial con algoritmo ML | BA Team |

---

**Estado**: ✅ READY FOR PSYCHOPEDAGOGICAL REVIEW  
**Aprobado por**: [Pendiente]  
**Fecha de aprobación**: [Pendiente]