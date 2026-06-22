# Sesión 4: Redes, Computación y Farmacología Dimensional

**Curso:** Psicopatología Dimensional: De Categorías a Sistemas
**Instructor:** Javier Flores
**Duración:** 50 min | **Audiencia:** R1 Psiquiatría
**Bloque:** 1 — Fundamentos (cierra el bloque)
**Estructura:** Objetivo · Contenido · Caso · Conclusiones

---

## Objetivo

Jaflo, el objetivo de esta sesión es que al salir del aula un R1 pueda hacer, por primera vez en el curso, una formulación dimensional completa de un paciente — no con un marco, sino con el toolkit entero integrado.

Hemos construido tres sesiones de componentes. Hoy los ensamblamos y agregamos las dos lentes que faltan (cómo se conectan los síntomas y cómo elegir el fármaco) más la primera herramienta de prescripción del curso. Es la primera sesión que alcanza Bloom 5-6 (Evaluar/Crear): las sesiones 1-3 pedían ubicar y mapear; la 4 pide formular.

**Learning Objectives en lenguaje natural:**

- **K1 — Network Theory:** Explicar por qué los trastornos no son listas de síntomas sino redes causalmente conectadas, y usar el vocabulario de nodos, edges, centralidad, bridge symptoms e histéresis para explicar comorbilidad y persistencia. Dos ventajas mínimas sobre el modelo categórico.
- **K2 — Computational Psychiatry:** Describir qué es un prediction error y un prior bayesiano (nivel conceptual, sin matemática), y explicar cómo un mismo mecanismo produce síntomas distintos en psicosis, ansiedad y depresión.
- **K3 — Psicofarmacología de precisión:** Describir el marco de prescripción por dominio dimensional (NbN2) y comparar dos decisiones farmacológicas bajo lógica de precisión vs lógica categórica.
- **A1 — Formular:** Integrar al menos 3 frameworks del bloque (HiTOP, RDoC, exposoma, staging, network, psicofarmacología de precisión) en una formulación dimensional preliminar de María.
- **A2 — Planificar:** Proponer un plan de intervención que combine target de red (síntoma central), dominio farmacológico (NbN2) y proporcionalidad de staging.

**Progresión respecto a sesiones previas:**

| Sesión | Framework | Pregunta clínica | Nivel máximo |
|--------|-----------|------------------|-------------|
| 1 | HiTOP | ¿Dónde está en el mapa? | Bloom 4 |
| 2 | RDoC | ¿Qué sistema falla? | Bloom 4 |
| 3 | Exposoma + Staging | ¿Por qué llegó ahí? ¿Qué tan lejos? | Bloom 4 |
| **4** | **Networks + Comp. Psych + psicofarmacología de precisión** | **¿Cómo se conecta? ¿Qué fármaco, por qué?** | **Bloom 6** |

**María en 30 segundos — ¿dónde estamos?**

María ha sido el caso hilo conductor del bloque. En sesión 1 la ubicamos en HiTOP: distress alto, fear moderado, detachment moderado, p elevado. En sesión 2 mapeamos sus sistemas RDoC: Negative Valence alta (rumiación, fear), Positive Valence baja (anhedonia), Arousal alterado (insomnio), Social Processes disminuidos (evitación). En sesión 3 organizamos su exposoma en 3 dominios y le asignamos Stage 2, P1, E1. Hoy cerramos su arco: ¿cómo se conectan sus síntomas y qué fármaco elegimos?

> **Pregunta para los R1:** "Si ya saben dónde está el paciente (HiTOP), qué sistema falla (RDoC), por qué llegó ahí (exposoma) y qué tan lejos ha ido (staging)... ¿qué les falta para hacer una formulación completa?"
>
> **Respuesta esperada:** Les falta entender cómo los síntomas se conectan entre sí (la estructura interna del cuadro) y cómo elegir el tratamiento farmacológico con la misma lógica dimensional.

---

## Contenido

Tres bloques conceptuales. Cada uno agrega una lente al toolkit y se conecta con el siguiente.

### Bloque 1 — Network Theory: los síntomas son una red, no una lista (K1)

#### El problema con las listas de síntomas

> **"El DSM trata los síntomas como ítems intercambiables de un checklist. 5 de 9 criterios = depresión mayor. Pero ¿son intercambiables insomnio y culpa? ¿Anhedonia y pérdida de peso?"**

**Dato de apertura:** Fried & Nesse (2015) analizaron 3,703 pacientes con depresión mayor del estudio STAR*D. Encontraron **1,030 perfiles sintomáticos únicos** — un promedio de 3.6 pacientes por perfil. La mayoría de los perfiles (48.6%) fueron reportados por una sola persona.

Si hay 1,030 formas distintas de tener "depresión mayor", ¿realmente estamos hablando de una enfermedad? Network Theory propone que no — que lo que llamamos depresión es un patrón de conexiones entre síntomas, no una entidad que causa los síntomas.

#### ¿Qué es Network Theory?

La Network Theory of Mental Disorders (Borsboom, 2017; Borsboom & Cramer, 2013) propone que los trastornos mentales no son entidades latentes que "causan" síntomas, sino **redes emergentes de síntomas causalmente conectados** a través de mecanismos biológicos, psicológicos y sociales.

**Vocabulario clave — presentar con visual:**

| Concepto | Definición | Analogía |
|----------|-----------|----------|
| **Nodos** | Síntomas individuales (insomnio, rumiación, fatiga, anhedonia...) | Ciudades en un mapa |
| **Edges (aristas)** | Conexiones causales o asociativas entre síntomas | Carreteras entre ciudades |
| **Centralidad** | Cuántas y cuán fuertes conexiones tiene un síntoma | La ciudad con más carreteras — el hub del aeropuerto |
| **Bridge symptoms** | Síntomas que conectan clusters de dos trastornos distintos | El puente entre dos islas — explica la comorbilidad |
| **Activación de red** | Un evento externo activa un síntoma, que propaga activación a sus vecinos | Un incendio que se propaga por las carreteras |
| **Histéresis** | La red activada no se desactiva al remover el disparador — el trastorno persiste | El incendio sigue aunque la chispa ya se apagó |

#### Ejemplo: la red de depresión

```
Evento vital negativo (pérdida, estrés)
       |
       v
  [INSOMNIO] ────── [Fatiga] ────── [Concentración ↓]
       |                                    |
       v                                    v
  [Rumiación] ◄───► [Ánimo depresivo] ───► [Anhedonia]
       |                                    |
       v                                    v
  [Culpa]          [Aislamiento social] ──► [Ideación suicida]
```

- **Paso 1 — Activación:** María pierde a su compañero de trabajo (evento). Esto activa insomnio (empieza a dormir 4-5 horas).
- **Paso 2 — Propagación:** El insomnio activa fatiga → la fatiga activa problemas de concentración → la rumiación aumenta → el ánimo baja → la anhedonia aparece.
- **Paso 3 — Feedback loops:** Rumiación ↔ Ánimo depresivo se refuerzan mutuamente. Insomnio ↔ Rumiación se refuerzan (no puede dormir porque rumia, rumia porque no puede dormir).
- **Paso 4 — Histéresis:** Después de 6 meses, aunque María se adapte a la pérdida, la red ya es auto-sostenida. El disparador desapareció, pero el trastorno persiste — los loops se mantienen activos por la fuerza de las conexiones internas.

> **Punto pedagógico:** "¿Por qué la depresión no se resuelve cuando el estresor desaparece? El modelo categórico no tiene buena respuesta. Network Theory sí: histéresis. Las conexiones entre síntomas se volvieron lo suficientemente fuertes para auto-sostenerse."

#### Centralidad: no todos los síntomas pesan igual

**Hallazgo empírico (Robinaugh et al., 2020, *Psychological Medicine*):** En una revisión de 363 artículos, la fatiga/baja energía es "quizás el síntoma de depresión más consistentemente central" en los estudios de red.

**Tipos de centralidad (nivel conceptual, no técnico):**

| Tipo | Pregunta que responde | Analogía |
|------|----------------------|----------|
| **Strength** | ¿Cuántas conexiones fuertes tiene este síntoma? | ¿Cuántos vuelos directos salen de esta ciudad? |
| **Betweenness** | ¿Cuántos caminos pasan por este síntoma? | ¿Es ciudad de tránsito obligado? |
| **Closeness** | ¿Qué tan cerca está de todos los demás síntomas? | ¿Qué tan rápido llego desde aquí a cualquier otra ciudad? |
| **Bridge expected influence** | ¿Cuánto conecta este síntoma con síntomas de *otro* trastorno? | ¿Es el puente entre dos islas? |

**Implicación terapéutica directa:** Si el insomnio es un nodo de alta centralidad en la red de María, tratar el insomnio primero podría desactivar cascadas: mejor sueño → menos fatiga → menos rumiación → mejor ánimo. Es una hipótesis de targets basada en estructura de red.

#### Bridge symptoms: por qué los trastornos vienen en paquete

> **"¿Por qué depresión y ansiedad son tan comórbidos? El modelo categórico dice 'dos enfermedades que coinciden'. Network Theory dice: hay síntomas puente que los conectan."**

**Ejemplo (Jones, Ma & McNally, 2021, *Multivariate Behavioral Research*):**

```
CLUSTER DEPRESIÓN          BRIDGE SYMPTOMS         CLUSTER ANSIEDAD
                           
[Ánimo depresivo]                                  [Preocupación]
[Anhedonia]              ← [Insomnio] →            [Tensión]
[Culpa]                  ← [Fatiga] →              [Irritabilidad]
[Ideación suicida]       ← [Concentración ↓] →     [Inquietud]
```

Insomnio, fatiga y problemas de concentración aparecen en criterios de *ambos* trastornos. No son comorbilidad — son **el puente** por el que la activación de un cluster se propaga al otro.

> **Conexión con HiTOP (sesión 1):** "¿Recuerdan que HiTOP explica la comorbilidad por factores latentes compartidos (distress, fear)? Network Theory ofrece una explicación complementaria pero distinta: la comorbilidad no es un factor latente sino conexiones directas entre síntomas de ambos clusters."

#### Limitaciones — honestidad epistémica

**Ser transparente con los R1 (Forbes et al., 2019, *World Psychiatry*):**

- Los hallazgos de centralidad son **poco replicables**: en 8 estudios de TEPT, el 88% de los síntomas mostraron alta centralidad en solo un estudio.
- Las métricas de centralidad fueron desarrolladas para redes sociales — su aplicabilidad a redes psicológicas es cuestionable (Bringmann et al., 2019).
- No hay evidencia robusta de que tratar síntomas centrales produzca mejores outcomes que otras estrategias (Castro et al., 2019: evidencia moderada).

> **Mensaje equilibrado:** "Network Theory es un modelo poderoso para *pensar* sobre la estructura de la psicopatología — comorbilidad, persistencia, heterogeneidad. Pero las herramientas empíricas aún no están maduras para guiar tratamiento individual. Úsenla como lente conceptual, no como GPS clínico."

---

### Bloque 2 — Computational Psychiatry: el cerebro como máquina de predicción (K2)

#### La idea central en una frase

> **"El cerebro no espera pasivamente a que el mundo le envíe información. Constantemente predice lo que va a pasar — y cuando la predicción falla, eso es un prediction error. Los trastornos mentales son formas específicas de que esa maquinaria de predicción falle."**

#### Prediction error: el concepto

**Analogía del GPS interno:**

"El cerebro funciona como un GPS que constantemente predice cuál será la próxima calle. Si tomas un giro esperado, el GPS no hace nada — la predicción se confirmó. Si tomas un giro inesperado, el GPS genera un *error de recalculación* y actualiza la ruta."

```
Predicción (lo que el cerebro espera)
       ↕ comparación
Señal real (lo que los sentidos captan)
       ↓
PREDICTION ERROR = señal real − predicción
       ↓
Si PE es grande → actualizar el modelo (aprendizaje)
Si PE es pequeño → mantener el modelo (confirmación)
```

**Tres componentes clave:**

1. **Priors (creencias previas):** Lo que el cerebro espera basado en experiencia previa. Son predicciones top-down.
2. **Evidencia sensorial:** Lo que los sentidos captan. Es información bottom-up.
3. **Precisión (confidence):** Cada fuente de información tiene un "volumen" — cuánta confianza se le asigna. El cerebro pondera priors vs. evidencia según la precisión de cada uno.

> **Analogía de los dos volúmenes:** "Imaginen que la percepción tiene dos controles de volumen: uno para 'lo que espero' (prior) y otro para 'lo que mis sentidos captan' (evidencia). En una persona sana, ambos están balanceados. En psicopatología, uno está al máximo y el otro al mínimo."

#### Prediction error alterado → síntomas específicos

**Presentar como tabla comparativa — la misma maquinaria, distinto patrón de falla:**

| Trastorno | ¿Qué falla? | Resultado clínico | Analogía |
|-----------|------------|-------------------|----------|
| **Psicosis** | El volumen del prior está al máximo, la evidencia sensorial al mínimo. El cerebro genera prediction errors masivos ante estímulos neutros (aberrant salience) | Ideas de referencia, delirios, alucinaciones — el cerebro "ve significado" donde no lo hay | El GPS recalcula frenéticamente en una calle perfectamente normal |
| **Ansiedad** | El prior de amenaza tiene precisión excesiva (hyperprecise threat priors). El cerebro sobreestima la probabilidad de peligro | Hipervigilancia, arousal excesivo, evitación — el filtro de spam está demasiado sensible | El filtro de spam marca todo como "posible amenaza" |
| **Depresión** | Los priors negativos tienen precisión excesiva. Los prediction errors positivos (buenas noticias) se atenúan (cognitive immunization) | Rumiación, desesperanza, anhedonia — el modelo pesimista es inmune a la evidencia contraria | El autocomplete del teléfono solo sugiere finales negativos |

#### Psicosis como aberrant salience

**Modelo de Kapur (2003, *American Journal of Psychiatry*):** Un estado hiperdopaminérgico desregulado genera asignación aberrante de saliencia — estímulos ordinarios se vuelven extraordinariamente significativos.

- **Delirios:** El esfuerzo cognitivo por darle sentido narrativo a estas experiencias aberrantemente salientes. "El cerebro intenta explicar por qué todo parece significativo."
- **Alucinaciones:** La experiencia directa de la saliencia aberrante de representaciones internas. El volumen del prior está tan alto que el cerebro "escucha" lo que espera, no lo que hay.

**Evidencia experimental (Powers, Mathys & Corlett, 2017, *Science*):** Demostraron que alucinaciones inducidas por condicionamiento Pavloviano resultan del overweighting de priors perceptuales. Personas propensas a alucinaciones sobreponderan sus predicciones sobre la evidencia sensorial.

> **Conexión con Tomás (sesión 3):** "¿Recuerdan a Tomás, 16 años, que decía 'siento que la gente me mira raro pero probablemente es mi imaginación'? En lenguaje computacional: su sistema de saliencia genera prediction errors leves ante estímulos sociales neutros — pero su insight está preservado: reconoce que la predicción puede ser errónea. Eso es Stage 1b: el sistema está perturbado pero no ha tomado el control."

#### Depresión como priors pesimistas immunizados

**Modelo de Kube et al. (2020, *Biological Psychiatry*):** La depresión involucra priors negativos con precisión excesiva + atenuación de prediction errors positivos.

- La persona espera predominantemente resultados negativos.
- Cuando ocurre algo bueno, el sistema "inmuniza cognitivamente": "fue suerte", "no durará", "no cuenta".
- El prior pesimista no se actualiza porque los prediction errors positivos se descuentan.

> **Implicación clínica:** "Esto explica por qué el feedback positivo no funciona fácilmente en depresión. No es que el paciente 'no quiera' mejorar — es que su maquinaria de predicción está calibrada para descartar la evidencia positiva. La terapia cognitiva, vista desde aquí, es un intento de recalibrar la precisión de los priors."

#### Ansiedad como priors de amenaza hiperprecisos

**Modelo de Paulus & Stein (2006, *Biological Psychiatry*):** La ansiedad involucra una señal de predicción interoceptiva alterada — detección aumentada de la diferencia entre el estado corporal observado y el esperado.

> **Analogía del termostato:** "Un termostato predice la temperatura y ajusta. En ansiedad, el termostato está miscalibrado: predice que el cuerpo está en peligro, detecta discrepancias exageradas, y dispara alarmas desproporcionadas. La ínsula anterior es ese termostato."

#### El puente clave: cada neuromodulador controla un parámetro del algoritmo

> **Punto pedagógico:** "No necesitan la matemática. Necesitan el mapa: cada neuromodulador es una *perilla* del algoritmo de predicción. Cuando prescriben, están ajustando perillas específicas."

**Tabla — El mapa neuromodulador → parámetro computacional:**

| Neuromodulador | Parámetro que controla | Cuando se rompe | Ejemplo clínico |
|---|---|---|---|
| **Dopamina** (fásica) | Prediction error de recompensa (RPE), saliencia | Aberrant salience → psicosis; RPE atenuado → anhedonia | Antipsicóticos D2 bajan saliencia; estimulantes suben signal-to-noise |
| **Serotonina** | Priors aversivos, asimetría recompensa/castigo, plasticidad | Priors negativos rígidos → depresión; sesgo aversivo → ansiedad | ISRSs corrigen asimetría de aprendizaje; psicodélicos (5-HT2A) relajan priors de alto nivel |
| **Acetilcolina** | Precisión de evidencia sensorial (*expected uncertainty*) | Precisión sensorial baja → el prior domina → psicosis | KarXT (xanomeline-trospium) restaura precisión sensorial sin bloquear D2 |
| **Noradrenalina** | Incertidumbre inesperada, volatilidad, reset | Sobreestimación de volatilidad → ansiedad crónica | Guanfacina/atomoxetina recalibran estimación de volatilidad |
| **Glutamato/GABA** | Ganancia cortical (balance E/I), plasticidad | Ganancia E/I alterada → cognición, plasticidad | Ketamina abre ventana de plasticidad para reescribir priors negativos |

(Fuentes: Schultz, Dayan & Yu, Mathys, Adams, Corlett, Browning, Powers)

> **"Cuando un paciente dice 'todo me parece amenazante', el mapa les dice: sobreestimación de volatilidad → noradrenalina. Cuando dice 'nada me importa', el mapa dice: RPE positivo atenuado → dopamina. Cuando dice 'la gente me mira raro', dice: aberrant salience → dopamina, o precisión sensorial baja → acetilcolina. El neuromodulador les señala el fármaco."**

#### Reencuadre clínico: de "qué diagnóstico" a "qué parámetro"

> "El reencuadre que propone Computational Psychiatry es radical: cambiar la pregunta de '¿qué diagnóstico tiene?' por '¿qué parámetro inferencial está roto y qué neuromodulador lo controla?'. Los fármacos no son 'antidepresivos' o 'antipsicóticos' — son intervenciones sobre el algoritmo inferencial."

Esto conecta directamente con el bloque siguiente: NbN2 y farmacología por dominio.

---

### Bloque 3 — Psicofarmacología de precisión: prescribir por dominio, no por diagnóstico (K3)

#### El problema que la precision psychiatry resuelve

> **"Si un paciente con 'depresión mayor' tiene anhedonia severa y un paciente con 'esquizofrenia' también tiene anhedonia severa... ¿por qué le damos ISRS a uno y antipsicótico al otro? ¿No sería más lógico tratar la anhedonia — el síntoma dimensional compartido — con la misma lógica farmacológica?"**

**El absurdo del modelo categórico:**

| Paciente | Diagnóstico | Síntoma dimensional | Prescripción categórica | Lógica |
|----------|------------|---------------------|------------------------|--------|
| Ana | TDM | Anhedonia severa | Sertralina (ISRS) | "Es depresión → antidepresivo" |
| Pedro | Esquizofrenia | Anhedonia severa | Risperidona | "Es esquizofrenia → antipsicótico" |

Ambos tienen el mismo síntoma dimensional (anhedonia = Positive Valence ↓), pero reciben fármacos distintos porque la etiqueta categórica es distinta. La risperidona, además, puede *empeorar* la anhedonia vía bloqueo D2 en el circuito de recompensa.

> **"La precision psychiatry invierte la lógica: primero identifica el dominio dimensional afectado y el parámetro computacional roto, luego elige el fármaco por mecanismo de acción sobre ese dominio."**

#### NbN2: el lenguaje de la precision psychiatry

La **Neuroscience-based Nomenclature** (NbN/NbN2; Zohar, Stahl, Nutt et al., 2015; Lancet Psychiatry 2026) desplaza la taxonomía por indicación — "antidepresivo", "antipsicótico", "ansiolítico" — porque estas etiquetas mezclan historia comercial, síntomas tratados y supuestos diagnósticos DSM.

**NbN2 define cada fármaco por dos ejes:**

1. **Dominio farmacológico:** el sistema neurotransmisor/molécula que modifica (serotonina, dopamina, glutamato, GABA, acetilcolina, noradrenalina, opioides, orexina, histamina, litio-mimético, melatonina...)
2. **Modo de acción:** la interacción primaria — agonismo, agonismo parcial, antagonismo, inhibición de recaptación, PAM (modulador alostérico positivo), bloqueador de canal, inhibición enzimática...

**Ejemplos que cambian la forma de pensar:**

| Nombre clásico | Problema clínico | NbN2: Dominio + Modo de acción |
|---------------|-----------------|-------------------------------|
| "Antidepresivo" (sertralina) | Trata OCD, TEPT, pánico, ansiedad. ¿Es "antidepresivo" en OCD? | **Serotonina, SERT reuptake inhibitor** |
| "Antipsicótico" (quetiapina 25mg) | A 25mg es hipnótico H1/α1. A 600mg es D2/5-HT2A. | **Multimodal dose-dependent** (concepto DDDP: *different dosage, different pharmacology*) |
| "Antipsicótico" (aripiprazol) | Es agonista parcial D2, no antagonista. Puede activar o estabilizar según tono DA. | **Dopamina, D2 receptor partial agonist + 5-HT1A partial agonist** |
| "Antipsicótico" (xanomeline-trospium/Cobenfy) | Sin bloqueo D2. Primer mecanismo colinérgico aprobado para esquizofrenia (FDA 2024). | **Acetilcolina, M1/M4 receptor agonist + peripheral muscarinic antagonist** |
| "Estabilizador del ánimo" | Categoría sin base farmacológica. Litio, valproato y lamotrigina tienen mecanismos completamente distintos. | Litio: **modulador de señalización intracelular**. Lamotrigina: **bloqueador de canal Na+/modulador de liberación de glutamato** |

> **Punto para R1:** "Quetiapina a 25mg no es el mismo fármaco clínico que quetiapina a 600mg. Aripiprazol no es un 'antipsicótico débil' — es un agonista parcial que estabiliza dopamina en ambas direcciones. Cobenfy es un antipsicótico sin D2. El nombre NbN2 les dice *qué hace el fármaco*, no para qué diagnóstico se inventó."

#### El concepto DDDP: *Different Dosage, Different Pharmacology*

**Publicado recientemente en Lancet Psychiatry (2026):** el reconocimiento formal de que la dosis transforma el fármaco.

| Fármaco | Dosis baja | Dosis alta |
|---------|-----------|-----------|
| **Quetiapina** | H1/α1 → sedación/hipnótico | D2/5-HT2A + norquetiapina (NET/5-HT1A) → antipsicótico/antidepresivo |
| **Aripiprazol** | Agonismo parcial D2 predominante → activación/augmentation | Mayor ocupancia D2 → estabilización antipsicótica |
| **Trazodona** | 5-HT2A antagonismo + H1/α1 → hipnótico | SERT inhibition + 5-HT2A → antidepresivo |

> "La próxima vez que alguien les diga 'quetiapina es un antipsicótico', pregunten: ¿a qué dosis?"

#### Las 5 preguntas antes de prescribir

**Este es el algoritmo que van a usar en todo el curso:**

Antes de elegir un psicofármaco, formulen 5 preguntas explícitas:

1. **¿Qué dominio RDoC explica la discapacidad actual?** — No el diagnóstico nominal, sino el dominio funcional alterado.
2. **¿Qué circuito/parámetro computacional está desregulado?** — ¿Aberrant salience? ¿Priors negativos rígidos? ¿Volatilidad sobreestimada? ¿Signal-to-noise bajo?
3. **¿Qué receptor/transportador/canal modula ese circuito con la menor carga colateral?** — NbN2: dominio farmacológico + modo de acción.
4. **¿Qué evidencia clínica existe para ese fenotipo y en qué población?** — No toda plausibilidad mecanística se traduce en eficacia.
5. **¿Qué marcador temprano indicará que el mecanismo fue comprometido o falló?** — Monitoreo por dimensión, no por score total.

> **"Esta secuencia reduce tres sesgos: escalada por inercia, polifarmacia por síntoma aislado y cambio lateral dentro de la misma clase histórica."**

#### Tabla de referencia: dominio RDoC → parámetro computacional → lever farmacológico

**Esta tabla integra las 3 herramientas de hoy — se usará en cada bloque del curso:**

| Dominio RDoC | Parámetro computacional | Neuromodulador lever | Fármacos NbN2 | Bloque |
|---|---|---|---|---|
| **Negative Valence (Fear)** | Priors de amenaza hiperprecisos; sobreestimación de volatilidad | 5-HT, NE, GABA | SERT inhibitors; α2A agonists (guanfacina); GABA-A PAMs (corto plazo) | B2, S7 |
| **Negative Valence (Distress)** | Priors negativos rígidos; PE positivos atenuados (cognitive immunization) | 5-HT, NE, Glu | SERT/NET inhibitors; NMDA antagonists (ketamina/esketamina); 5-HT2A agonists (psilocibina, investigacional) | B3, S10 |
| **Positive Valence** | RPE atenuado; bajo vigor motivacional | DA, opioides, Glu | NDRI (bupropión); D2/D3 partial agonists (cariprazina); estimulantes si ADHD | B4, S12 |
| **Arousal/Regulatory** | Ganancia E/I alterada; ritmo circadiano | Li, GABA, orexina, histamina | Li (modulador intracelular); GABA-A neuroesteroides (zuranolona); DORAs (suvorexant) | B5, S14 |
| **Cognitive Systems** | Precisión sensorial baja; signal-to-noise reducido | DA, ACh, Glu | D2 partial agonists; M1/M4 agonists (KarXT/Cobenfy); vortioxetina (multimodal 5-HT) | B6, S16 |
| **Disinhibited Ext.** | MF domina sobre MB; signal-to-noise DA/NE | NE, DA | NET inhibitors (atomoxetina); DA/NE reuptake inhibitors (estimulantes); opioid antagonists (naltrexona) | B7, S18 |
| **Antagonistic Ext.** | Regulación social; mentalización | Estabilización afectiva | Mood stabilizers baja dosis; NO "fármaco para personalidad" | B8, S20 |

> **"Noten que la tabla ahora tiene una columna de parámetro computacional. El dominio RDoC les dice QUÉ sistema. El parámetro computacional les dice POR QUÉ falla. El neuromodulador les dice CON QUÉ intervenir. NbN2 les dice CÓMO nombrarlo."**

#### Ejemplo contrastado: mismo diagnóstico, distinto perfil → distinto fármaco

**Caso A — Elena:**
- Diagnóstico DSM: Depresión Mayor Recurrente (F32.1)
- **Perfil dimensional:** Negative Valence (distress) ↑↑↑, Positive Valence normal
- **Parámetro computacional:** Priors negativos rígidos con precisión excesiva; sesgo aversivo de aprendizaje
- Síntoma dominante: rumiación intensa, llanto, desesperanza
- **NbN2:** Target = serotonina (modular asimetría recompensa/castigo). Fármaco = **sertralina: serotonin, SERT reuptake inhibitor**
- Si TRD: considerar **esketamina: glutamate, NMDA receptor antagonist** (burst de plasticidad para reescribir priors negativos)

**Caso B — Diego:**
- Diagnóstico DSM: Depresión Mayor Recurrente (F32.1) — mismo diagnóstico que Elena
- **Perfil dimensional:** Negative Valence normal, Positive Valence ↓↓↓, Arousal ↓
- **Parámetro computacional:** RPE positivo atenuado; bajo vigor motivacional (circuito VTA-NAcc)
- Síntoma dominante: anhedonia profunda, hipersomnia, apatía, fatiga motivacional
- **NbN2:** Target = dopamina/norepinefrina (restaurar RPE positivo y vigor). Fármaco = **bupropión: norepinephrine/dopamine, reuptake inhibitor**
- Si bipolaridad subumbral: considerar **cariprazina: dopamine, D3-preferring D2/D3 receptor partial agonist**

> **"Mismo F32.1, distinto fármaco. ¿Por qué? Porque el dominio, el parámetro computacional y el neuromodulador son distintos. Elena tiene priors negativos rígidos → necesita recalibrar serotonina. Diego tiene RPE positivo atenuado → necesita activación dopaminérgica. Un ISRS en Diego podría empeorar su anhedonia. NbN2 les dice esto; la etiqueta F32.1 no."**

#### Error frecuente: confundir clase con mecanismo

> "Los errores más caros que van a ver en su residencia vienen de confundir la clase histórica con el mecanismo real."

| Error | Por qué es error |
|-------|-----------------|
| "Antipsicótico" = todos iguales | Risperidona (D2 antagonista fuerte), aripiprazol (D2 partial agonist) y Cobenfy (M1/M4 agonista sin D2) tienen mecanismos radicalmente distintos |
| Subir ISRS si no responde → otro ISRS | Si la no-respuesta es por anhedonia (Positive Valence), otro ISRS repite el error. Cambiar de dominio farmacológico |
| Quetiapina 25mg para insomnio = "tomar antipsicótico" | A esa dosis es H1/α1 antagonist, no antipsicótico. Pero la carga metabólica H1 crónica sí existe |
| "Necesita ansiolítico" → benzodiazepina crónica | BZD es GABA-A PAM agudo; no recalibra priors de amenaza. ISRS/SNRI sí recalibran aprendizaje aversivo a largo plazo |

#### Convergencia: Network + Computational + NbN2 + Staging

> "Ahora combinen las herramientas de hoy:"

1. **Network Theory** les dice cuál es el nodo central (el target terapéutico prioritario).
2. **Computational Psychiatry** les dice cuál es el parámetro de predicción alterado y qué neuromodulador lo controla.
3. **NbN2** les dice cómo nombrar el fármaco por dominio farmacológico y modo de acción.
4. **Staging** les dice si es momento de usar fármaco o si intervención no-farmacológica es suficiente.

> **Ejemplo rápido con María:**
> - Network: insomnio es nodo central; rumiación es bridge symptom
> - Computational: priors pesimistas con precisión excesiva (5-HT); PE positivos atenuados (DA)
> - NbN2: Negative Valence (distress) → **sertralina: serotonin, SERT reuptake inhibitor**. Si anhedonia persiste → considerar **bupropión: NE/DA, reuptake inhibitor**
> - Staging: Stage 2, primer episodio completo → sí amerita farmacoterapia, proporcional
> - 5 preguntas: (1) NegVal + PosVal; (2) priors negativos rígidos + RPE atenuado; (3) SERT > NDRI; (4) evidencia sólida ISRS primera línea TDM; (5) monitorear anhedonia (SHAPS), rumiación y sueño por separado

---

## Caso

Jaflo, aquí María deja de ser ejemplo ilustrativo y se vuelve el primer paciente del curso al que se le aplica el toolkit entero. Es el cierre de su arco como caso hilo conductor del Bloque 1.

### La red de síntomas de María

Apliquemos Network Theory a María. Presentar la red esquemática:

```
                    [Exposoma: ACEs, padre alcohólico, bullying]
                                      |
                                      v
[Insomnio] ◄───────────────► [Rumiación] ◄────► [Ánimo depresivo]
     |                             |                     |
     v                             v                     v
[Fatiga] ──────────────► [Concentración ↓]        [Anhedonia]
                                                        |
                                                        v
                                                [Aislamiento social]
                                                        |
                                                        v
                                              [Evitación situaciones]
```

- **Nodo central candidato:** Insomnio (alta conectividad: conecta con rumiación, fatiga, concentración, y es hub transdiagnóstico RDoC de sesión 2).
- **Bridge symptom:** Rumiación conecta Negative Valence (cluster depresivo) con Cognitive Systems (concentración, toma de decisiones) — puente entre dimensiones HiTOP.
- **Feedback loops:** Rumiación ↔ Ánimo depresivo; Insomnio ↔ Rumiación; Anhedonia ↔ Aislamiento social.
- **Implicación terapéutica:** Si atacamos insomnio + rumiación como targets prioritarios, podríamos desactivar cascadas en múltiples dominios simultáneamente.

> **Conexión con RDoC (sesión 2):** "¿Recuerdan que en sesión 2 dijimos que el insomnio aparece en >80% de trastornos psiquiátricos y es el nodo transdiagnóstico RDoC más importante? Network Theory les da el vocabulario para explicar por qué: es un nodo de alta centralidad que conecta múltiples clusters."

### El patrón computacional de María

En lenguaje de Computational Psychiatry:

- **Prediction error alterado:** priors pesimistas con precisión excesiva → cognitive immunization (descuenta evidencia positiva).
- **Priors hiperprecisos:** en Negative Valence (todo será malo) + Positive Valence (nada valdrá la pena).
- **Conexión con exposoma:** la adversidad temprana (padre alcohólico, bullying, madre con depresión) puede haber calibrado los priors hacia amenaza/desesperanza — un prior aprendido en ventana crítica y ahora hiperpreciso.
- **Dial de precisión:** prior pesimista al máximo, evidencia positiva atenuada (mute).

> "El caso de María nos dice algo clínico: su rumiación no es 'carácter' ni 'queja' — es la expresión de un sistema de predicción que descarta evidencia positiva. Eso cambia la forma de abordar la psicoterapia: no es 'pensar positivo', es recalibrar la precisión del prior."

### El plan farmacológico de María

Aplicando las 5 preguntas antes de prescribir:

1. **¿Qué dominio RDoC explica la discapacidad?** Negative Valence (distress ↑) + Positive Valence (reward ↓).
2. **¿Qué parámetro computacional está desregulado?** Priors negativos rígidos (5-HT) + RPE positivo atenuado (DA).
3. **¿Qué receptor/transportador modula ese circuito?** Lever primario: SERT → **sertralina: serotonin, SERT reuptake inhibitor** (50-100mg). Si anhedonia persiste: agregar **bupropión: NE/DA, reuptake inhibitor**.
4. **¿Qué evidencia clínica existe?** ISRS primera línea TDM (NMA robusta). Bupropión para anhedonia residual (evidencia moderada).
5. **¿Qué marcador temprano indicará respuesta/falla?** SHAPS (anhedonia), diario de rumiación, ISI (sueño) — por separado, no solo PHQ-9 total.

**¿Proporcional al staging?** Sí — Stage 2 (primer episodio completo) amerita farmacoterapia + psicoterapia.

> "Noten que el plan no es 'dar un antidepresivo'. Es: atacar Negative Valence con serotonina (sertralina), monitorear Positive Valence por separado, y si la anhedonia no responde al SRI, agregar un NDRI (bupropión) en vez de escalar dentro de la misma clase. Esa es la diferencia entre prescripción categórica y precision psychiatry."

### Template de formulación dimensional (entregado en papel o proyectado)

---

**FORMULACIÓN DIMENSIONAL — TEMPLATE**
*Curso: Psicopatología Dimensional | Bloque 1: Fundamentos*

**Paciente:** ____________________

**1. PERFIL DIMENSIONAL (HiTOP — Sesión 1)**
- Espectro(s) afectado(s): ___
- Dimensiones elevadas: ___
- Factor p: bajo / moderado / elevado
- Comorbilidad esperada por perfil: ___

**2. SISTEMAS AFECTADOS (RDoC — Sesión 2)**
- Dominio(s) primario(s): ___
- Unidad de análisis relevante: circuito / fisiología / conducta / self-report
- Constructo(s) RDoC específico(s): ___

**3. EXPOSOMA (Sesión 3)**
- General externo: ___
- Específico externo: ___
- Interno (inferido): ___

**4. STAGING (Sesión 3)**
- Estadio: ___
- Modificador P: ___
- Modificador E: ___

**5. RED DE SÍNTOMAS (Network — Sesión 4)**
- Nodo(s) central(es): ___
- Bridge symptom(s): ___
- Feedback loop(s) identificado(s): ___

**6. PATRÓN COMPUTACIONAL (Sesión 4)**
- ¿Qué prediction error está alterado? ___
- ¿Priors hiperprecisos? ¿En qué dominio? ___

**7. PLAN FARMACOLÓGICO — 5 preguntas (Sesión 4)**
- P1. ¿Qué dominio RDoC explica la discapacidad? ___
- P2. ¿Qué parámetro computacional está desregulado? ___
- P3. ¿Qué receptor/transportador modula ese circuito? → Fármaco NbN2: ___
- P4. ¿Qué evidencia clínica existe para este fenotipo? ___
- P5. ¿Qué marcador temprano indicará respuesta/falla? ___
- ¿Proporcional al staging? ___

**8. PLAN INTEGRADO**
- Target de red prioritario: ___
- Intervención no-farmacológica: ___
- Intervención farmacológica (NbN2: dominio + modo de acción): ___
- Monitoreo dimensional: ¿qué dimensión mido para evaluar respuesta? ___

---

### Ejercicio integrador (32-47 min) — A1, A2

**Instrucciones (2 min):**

> "Ahora van a hacer lo que ningún checklist del DSM les permite: una formulación dimensional completa. Tienen el template en papel. Usen todo lo del bloque — mínimo 3 frameworks. Tienen 8 minutos individuales y luego discutimos."

**Trabajo individual (8 min):**

Los R1 completan el template con María. Facilitador circula el aula, haciendo preguntas de coaching:

- "¿Cuál es el nodo central de María? ¿Cómo lo saben?"
- "¿El SRI es para el distress o para la anhedonia? ¿Y si la anhedonia no responde?"
- "¿El staging les permite fármaco o no?"

### Guía del facilitador — Respuestas esperadas para María

**1. PERFIL DIMENSIONAL (HiTOP)**
- Espectros: Internalizing (subfactor distress ↑↑, subfactor fear ↑), Detachment ↑
- Dimensiones: distress alto, fear moderado, detachment moderado
- Factor p: elevado (afecta múltiples espectros)
- Comorbilidad esperada: alta — perfil transdiagnóstico con participación de 3 espectros

**2. SISTEMAS AFECTADOS (RDoC)**
- Dominios primarios: Negative Valence (sustained threat, loss), Positive Valence (reward responsiveness ↓)
- Secundarios: Arousal/Regulatory (sleep-wakefulness), Social Processes (affiliation ↓)
- Constructos: rumiación cruza Cognitive Systems y Negative Valence; insomnio cruza Arousal y todos los demás

**3. EXPOSOMA**
- General externo: padre alcohólico (modelado disfuncional + posible negligencia), madre con depresión (disponibilidad emocional reducida), bullying severo en secundaria (adversidad en ventana crítica adolescente)
- Específico externo: insomnio severo (3-4h/noche), atracones 2-3x/semana, abandonó ejercicio. Faltan datos: sustancias, contaminación, pantallas
- Interno: probable sensibilización HPA por adversidad temprana, inflamación → anhedonia (circuito IL-6 → dopamina ↓), desregulación circadiana

**4. STAGING**
- Estadio: 2 (primer episodio completo que cumple criterios)
- Modificador P: P1 (rumiación como indicador de posible deterioro cognitivo funcional)
- Modificador E: E1 (adversidad temprana + insomnio crónico + dieta disregulada)

**5. RED DE SÍNTOMAS**
- Nodos centrales: insomnio (alta conectividad con fatiga, rumiación, concentración), rumiación (conecta Negative Valence con Cognitive Systems)
- Bridge symptoms: rumiación (puente depresión-ansiedad), insomnio (puente Arousal-Negative Valence)
- Feedback loops: rumiación ↔ ánimo depresivo; insomnio ↔ rumiación; anhedonia ↔ aislamiento social

**6. PATRÓN COMPUTACIONAL**
- Prediction error alterado: priors pesimistas con precisión excesiva → cognitive immunization (descuenta evidence positiva)
- Priors hiperprecisos: en Negative Valence (todo será malo) + Positive Valence (nada valdrá la pena)
- Conexión con exposoma: adversidad temprana puede haber calibrado los priors hacia amenaza/desesperanza

**7. PLAN FARMACOLÓGICO — 5 preguntas**
- P1. Dominios: Negative Valence (distress ↑) + Positive Valence (reward ↓)
- P2. Parámetro: priors negativos rígidos (5-HT) + RPE positivo atenuado (DA)
- P3. Lever primario: SERT → **sertralina: serotonin, SERT reuptake inhibitor** (50-100mg). Si anhedonia persiste: agregar **bupropión: NE/DA, reuptake inhibitor**
- P4. Evidencia: ISRS primera línea TDM (NMA robusta). Bupropión para anhedonia residual (evidencia moderada)
- P5. Marcadores: SHAPS (anhedonia), rumiación (diario), ISI (sueño) — por separado, no solo PHQ-9 total
- Proporcional al staging: Sí — Stage 2 amerita farmacoterapia + psicoterapia

**8. PLAN INTEGRADO**
- Target de red prioritario: insomnio (nodo central) → higiene del sueño + considerar DORA si no responde (NbN2: orexin, OX1/OX2 receptor antagonist — no quetiapina crónica como "hipnótico")
- Intervención no-farmacológica: TCC para depresión (reestructuración cognitiva = recalibrar precisión de priors negativos) + activación conductual (restaurar RPE positivos via experiencia) + intervención sobre exposoma modificable (reactivar ejercicio, regularizar dieta)
- Intervención farmacológica: **Sertralina: serotonin, SERT reuptake inhibitor** para Negative Valence. Evaluar respuesta a 4-6 semanas midiendo dimensiones por separado. Si anhedonia persiste: **bupropión: NE/DA, reuptake inhibitor** para Positive Valence
- Monitoreo dimensional: SHAPS (anhedonia/Positive Valence), diario de rumiación (Negative Valence/Cognitive), ISI/actigrafía (Arousal/sueño) — no solo PHQ-9 total

### Plenario (5 min)

**Preguntas para el debate:**

> 1. "¿Qué ven en esta formulación que el DSM no les da?"

**Guiar hacia:** La formulación dimensional les muestra *dónde* está (HiTOP), *por qué* (exposoma), *qué sistema falla* (RDoC), *cómo se conectan los síntomas* (network), *qué mecanismo está roto* (computational), *qué tan lejos ha ido* (staging), y *qué fármaco actúa sobre qué dominio* (psicofarmacología de precisión). El DSM les da: F32.1.

> 2. "Si miden 'mejoría de depresión' con un score total del PHQ-9... ¿qué problema ven?"

**Guiar hacia:** Un score total puede mejorar por reducción de insomnio y fatiga mientras la anhedonia sigue igual o empeora. El monitoreo dimensional les pide medir cada dominio por separado: ¿mejoró el distress? ¿Mejoró el reward? ¿Mejoró el sueño? Si la anhedonia no responde al SRI, el score total puede enmascarar una no-respuesta en Positive Valence.

> 3. "¿Y si María estuviera en Stage 1b en vez de Stage 2? ¿Qué cambia?"

**Guiar hacia:** Stage 1b = no fármaco en primera línea. TCC + intervención sobre exposoma modificable + monitoreo. El staging determina la intensidad; psicofarmacología de precisión determina la dirección. No son lo mismo.

**Error de R1 que hay que corregir si aparece:**
- "Le daría antidepresivo + ansiolítico + hipnótico" → psicofarmacología de precisión no apila por diagnóstico; identifica dominios y usa el menor número de fármacos con la mayor cobertura de dominios.
- "La formulación dimensional es demasiado complicada para la práctica" → En la práctica, no escriben un documento de 8 secciones. Pero el *pensamiento* dimensional cambia sus decisiones aunque el formulario sea breve. Con el tiempo se vuelve automático.

---

## Conclusiones

Jaflo, el cierre del Bloque 1 tiene tres funciones: fijar el take-home, mapear lo construido y abrir el Bloque 2.

### Take-Home Message

> **"La formulación dimensional no es un modelo — es un toolkit. Cada herramienta ilumina un ángulo distinto del mismo paciente: HiTOP dice dónde está, RDoC dice qué sistema falla, exposoma dice por qué, staging dice cuánto intervenir, networks dice cómo se conectan los síntomas, computational dice qué mecanismo está roto, y psicofarmacología de precisión dice qué fármaco por qué razón."**

Estas **7 preguntas** son el esqueleto de todo el curso. A partir de la sesión 5, vamos a aplicar este toolkit dominio por dominio.

### Mapa completo del Bloque 1

```
Sesión 1: HiTOP         → ¿DÓNDE está en el mapa?               (estructura)
Sesión 2: RDoC          → ¿QUÉ sistema falla?                   (mecanismo)
Sesión 3: Exposoma      → ¿POR QUÉ llegó ahí?                   (riesgo)
          Staging       → ¿QUÉ TAN LEJOS ha ido?                (trayectoria)
Sesión 4: Networks      → ¿CÓMO SE CONECTAN los síntomas?       (estructura interna)
          Computational → ¿QUÉ MECANISMO de predicción falla?   (computación)
          psicofarmacología de precisión         → ¿QUÉ FÁRMACO, POR QUÉ DOMINIO?       (tratamiento)
```

> "Estas 7 preguntas son el esqueleto de todo el curso. A partir de la sesión 5, vamos a aplicar este toolkit dominio por dominio, empezando por Negative Valence — el sistema de amenaza."

### Preview Bloque 2: Negative Valence / Internalizing-Fear

El Bloque 2 tiene 3 sesiones: modelo (sesión 5), psicoterapia (sesión 6), y psicofarmacología de precisión (sesión 7). Vamos a entrar en el sistema de amenaza — acute threat, potential threat, sustained threat. Verán por qué fobias, pánico, ansiedad de separación y OCD son variantes dimensionales del mismo sistema, y cómo tratar cada una con la lógica que aprendieron hoy.

### Template de formulación: el deliverable

> "El template que usaron hoy se queda con ustedes. Lo van a usar en cada bloque del curso. Para la sesión final (sesión 21), cada uno presentará una formulación dimensional completa de un paciente real — este template es su herramienta."

### Tarea breve

"Dos opciones (elijan una):

1. Completen la formulación dimensional de un paciente real de su rotación usando el template de hoy (mínimo 3 de las 8 secciones).
2. Si ya hicieron la mini-historia exposómica de la sesión 3, agreguen las secciones de red, patrón computacional y psicofarmacología de precisión."

---

## Referencias

### Network Theory — Papers base
1. Borsboom D. A network theory of mental disorders. *World Psychiatry*. 2017;16(1):5-13. doi:10.1002/wps.20375
2. Borsboom D, Cramer AOJ. Network analysis: An integrative approach to the structure of psychopathology. *Annu Rev Clin Psychol*. 2013;9:91-121. doi:10.1146/annurev-clinpsy-050212-185608
3. Cramer AOJ, Waldorp LJ, Van Der Maas HLJ, Borsboom D. Comorbidity: A network perspective. *Behav Brain Sci*. 2010;33(2-3):137-150. doi:10.1017/S0140525X09991567
4. Fried EI, van Borkulo CD, Cramer AOJ, et al. Mental disorders as networks of problems: A review of recent insights. *Soc Psychiatry Psychiatr Epidemiol*. 2017;52(1):1-10. doi:10.1007/s00127-016-1319-z
5. Fried EI, Nesse RM. Depression is not a consistent syndrome: An investigation of unique symptom patterns in the STAR*D study. *J Affect Disord*. 2015;172:96-102. doi:10.1016/j.jad.2014.10.010
6. Jones PJ, Ma R, McNally RJ. Bridge centrality: A network approach to understanding comorbidity. *Multivariate Behav Res*. 2021;56(2):353-367. doi:10.1080/00273171.2019.1614898
7. Robinaugh DJ, Hoekstra RHA, Toner ER, Borsboom D. The network approach to psychopathology: A review of the literature 2008-2018 and an agenda for future research. *Psychol Med*. 2020;50(3):353-366. doi:10.1017/S0033291719003404
8. McNally RJ. Network analysis of psychopathology: Controversies and challenges. *Annu Rev Clin Psychol*. 2021;17:31-53. doi:10.1146/annurev-clinpsy-081219-092850

### Network Theory — Limitaciones
9. Forbes MK, Wright AGC, Markon KE, Krueger RF. Evidence that psychopathology symptom networks have limited replicability. *J Abnorm Psychol*. 2017;126(7):969-988. doi:10.1037/abn0000276
10. Forbes MK, Wright AGC, Markon KE, Krueger RF. The network approach to psychopathology: promise versus reality. *World Psychiatry*. 2019;18(3):272-273. doi:10.1002/wps.20659
11. Bringmann LF, Elmer T, Epskamp S, et al. What do centrality measures measure in psychological networks? *J Abnorm Psychol*. 2019;128(8):892-903. doi:10.1037/abn0000446
12. Castro D, et al. Differential role of central and bridge symptoms in network deactivation. *Front Psychol*. 2019;10:2448. doi:10.3389/fpsyg.2019.02448

### Computational Psychiatry — Papers base
13. Kapur S. Psychosis as a state of aberrant salience. *Am J Psychiatry*. 2003;160(1):13-23
14. Corlett PR, Murray GK, Honey GD, et al. Disrupted prediction-error signal in psychosis: evidence for an associative account of delusions. *Brain*. 2007;130(9):2387-2400
15. Corlett PR, Honey GD, Fletcher PC. Prediction error, ketamine and psychosis: An updated model. *J Psychopharmacol*. 2016;30(7):592-603. doi:10.1177/0269881116650087
16. Corlett PR, Fraser KM. 20 Years of Aberrant Salience in Psychosis. *Am J Psychiatry*. 2025;182(9):819-829. doi:10.1176/appi.ajp.20240556
17. Powers AR, Mathys C, Corlett PR. Pavlovian conditioning-induced hallucinations result from overweighting of perceptual priors. *Science*. 2017;357(6351):596-600. doi:10.1126/science.aan3458
18. Kube T, Schwarting R, Rozenkrantz L, Glombiewski JA, Rief W. Distorted cognitive processes in major depression: A predictive processing perspective. *Biol Psychiatry*. 2020;87(5):388-398
19. Paulus MP, Stein MB. An insular view of anxiety. *Biol Psychiatry*. 2006;60(4):383-387
20. Friston KJ. The free-energy principle: a unified brain theory? *Nat Rev Neurosci*. 2010;11:127-138
21. Friston KJ, Stephan KE, Montague R, Dolan RJ. Computational psychiatry: the brain as a phantastic organ. *Lancet Psychiatry*. 2014;1(2):148-158
22. Huys QJM, Maia TV, Frank MJ. Computational psychiatry as a bridge from neuroscience to clinical applications. *Nat Neurosci*. 2016;19:404-413
23. Bennett D, Silverstein SM, Niv Y. The Two Cultures of Computational Psychiatry. *JAMA Psychiatry*. 2019;76(6):563-564
24. Adams RA, Stephan KE, Brown HR, Frith CD, Friston KJ. The computational anatomy of psychosis. *Front Psychiatry*. 2013;4:47. doi:10.3389/fpsyt.2013.00047

### Farmacología dimensional / psicofarmacología de precisión
25. Zohar J, Stahl S, Moller HJ, et al. A review of the current nomenclature for psychotropic agents and an introduction to the Neuroscience-based Nomenclature. *Eur Neuropsychopharmacol*. 2015;25(12):2318-2325. doi:10.1016/j.euroneuro.2015.08.019
26. Nutt DJ, Blier P. Neuroscience-based Nomenclature (NbN) for Clinical Psychopharmacology and Neuroscience. *Int J Neuropsychopharmacol*. 2016;19(8):pyw066. doi:10.1093/ijnp/pyw066
27. Stahl SM. *Stahl's Essential Psychopharmacology*. 5th ed. Cambridge University Press; 2021
28. Kas MJ, et al. A quantitative approach to neuropsychiatry: The why and the how. *Neurosci Biobehav Rev*. 2019;97:3-9
29. Bilderbeck AC, et al. Overview of psicofarmacología de precisión clinical implementation. *Neurosci Biobehav Rev*. 2019;97:87-93. doi:10.1016/j.neubiorev.2018.06.019

### Computational Psychiatry — Desarrollos recientes
30. Shaw AD, Sumner RL, Berndt LCS. Predictive coding and neurocomputational psychiatry. *Front Psychiatry*. 2025;16:1713833
31. Lin X, et al. Interpreting anxiety disorders from interoceptive computational models. *Brain Behav*. 2025;e71019. doi:10.1002/brb3.71019
32. Gilbert JR, Wusinich C, Zarate CA Jr. A predictive coding framework for understanding major depression. *Front Hum Neurosci*. 2022;16:787495. doi:10.3389/fnhum.2022.787495
33. Briganti G, Scutari M, Epskamp S, Borsboom D, et al. Network analysis: An overview for mental health research. *Int J Methods Psychiatr Res*. 2024;33(4):e2034. doi:10.1002/mpr.2034
