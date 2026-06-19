# Proyecto: Tutor Virtual Socrático y Gamificado para Teoría del Productor
**Curso:** EC2003B — Incentivos del Consumidor y Productor (Etapa de Enfoque, 4.° Semestre)  
**Plataforma de Desarrollo:** Google Antigravity CLI & Escritorio  
**Entregable:** Arquitectura, Prompt Maestro y Guía de Despliegue en GitHub  

---

## 1. Visión General del Proyecto
Este proyecto consiste en el codiseño e implementación de un **Asistente de Inteligencia Artificial (Tutor Virtual)** concebido específicamente para alumnos de la Licenciatura en Economía en su transición hacia la microeconomía avanzada. 

El núcleo pedagógico se basa en el **método socrático**: la IA no proporciona respuestas directas ni resuelve ecuaciones; en su lugar, plantea preguntas guía, detecta fallas analíticas y orienta al estudiante para que descubra la solución matemática por sí mismo. Para romper con la aridez tradicional de la materia, se ha integrado una **dinámica de gamificación estructurada** que incentiva el esfuerzo y el progreso continuo.

---

## 2. Base de Conocimiento Local (Contexto Incorporado)
El tutor opera bajo un entorno cerrado (*Closed-Domain QA*) dentro de **Google Antigravity**, alimentándose de la bibliografía oficial y el material analítico del curso cargado desde Google Drive:

1. **Textos Guía Principales:**
   - *Intermediate Microeconomic Theory: Tools and Step-by-Step Examples* (Espinola-Arredondo & Muñoz-Garcia, MIT Press, 2020).
   - *A Short Course in Intermediate Microeconomics with Calculus* (Serrano & Feldman, Cambridge University Press, 2012).
2. **Material de Clase y Repasos Teóricos:**
   - `1-Tecnologia.pdf` (Conjuntos de producción, isocuantas).
   - `2-Teoria-del-Productor-Tecnologia-e-Isocuantas.pdf` (Propiedades marginales, similitudes consumidor/productor).
   - `3-Flexibilidad-y-Escala-La-Firma-en-el-Largo-Plazo.pdf` (TMST, formas funcionales Cobb-Douglas, Leontief, Sustitutos Perfectos y Rendimientos a Escala CRS/IRS/DRS).
   - `4-La-Economia-de-la-Empresa-Minimizando-Costos.pdf` (Recta de isocosto, condición de tangencia, optimización con Lagrange y multiplicador $\lambda$ como Costo Marginal).
   - `5-Estructura-y-Geometria-de-Costos-de-la-Firma.pdf` (Costos totales, fijos, variables, marginales y promedios en el corto y largo plazo).
   - `6-Maximizacion-de-beneficios-y-dualidad.pdf` (Condiciones de primer y segundo orden, equivalencia formal MBP y CMP, aplicaciones de nearshoring y sectores estratégicos en México).
3. **Bancos de Evaluación y Solucionarios:**
   - `Quiz-1-Teoria-de-la-produccion-y-costos.pdf`
   - `Repaso-Minimizacion-de-Costos-en-la-Teoria-de-la-Produccion.pdf`
   - *Manual del Profesor EC2003B* (Alineación con subcompetencias de pensamiento sistémico).

---

## 3. Configuración del Agente en Antigravity CLI

### Paso 1: Inicialización del Entorno de Ejecución
Abre la Terminal en macOS y ejecuta el comando para lanzar Antigravity con el motor de inferencia avanzada:
```bash
agy run --model gemini-3.1-pro
/add_context[urn cambridge.org id binary 20230109115501129-0634 Solutions_for_Instructors.pdf](https://github.com/user-attachments/files/29142488/urn.cambridge.org.id.binary.20230109115501129-0634.Solutions_for_Instructors.pdf)
[Roberto Serrano, Allan M. Feldman - A Short Course in Intermediate Microeconomics with Calculus-Cambridge University Press (2012).pdf](https://github.com/user-attachments/files/29142485/Roberto.Serrano.Allan.M.Feldman.-.A.Short.Course.in.Intermediate.Microeconomics.with.Calculus-Cambridge.University.Press.2012.pdf)
[Repaso-Minimizacion-de-Costos-en-la-Teoria-de-la-Produccion (2).pdf](https://github.com/user-attachments/files/29142484/Repaso-Minimizacion-de-Costos-en-la-Teoria-de-la-Produccion.2.pdf)
[Quiz-1-Teoria-de-la-produccion-y-costos (2).pdf](https://github.com/user-attachments/files/29142483/Quiz-1-Teoria-de-la-produccion-y-costos.2.pdf)
[Munoz Garcia_solutions-1.pdf](https://github.com/user-attachments/files/29142482/Munoz.Garcia_solutions-1.pdf)
[ilide.info-solutions-to-microeconomics-by-serrano-pr_1bffd16aa901ffc08cd82dde101b4678.pdf](https://github.com/user-attachments/files/29142480/ilide.info-solutions-to-microeconomics-by-serrano-pr_1bffd16aa901ffc08cd82dde101b4678.pdf)
[EC2003B Manual del profesor.pdf](https://github.com/user-attachments/files/29142479/EC2003B.Manual.del.profesor.pdf)
[Ana Espinola-Arredondo, Felix Munoz-Garcia - Intermediate Microeconomic Theory_ Tools and Step-by-Step Examples-The MIT Press (2020).pdf](https://github.com/user-attachments/files/29142477/Ana.Espinola-Arredondo.Felix.Munoz-Garcia.-.Intermediate.Microeconomic.Theory_.Tools.and.Step-by-Step.Examples-The.MIT.Press.2020.pdf)
[6-Maximizacion-de-beneficios-y-dualidad (2).pdf](https://github.com/user-attachments/files/29142476/6-Maximizacion-de-beneficios-y-dualidad.2.pdf)
[5-Estructura-y-Geometria-de-Costos-de-la-Firma (2).pdf](https://github.com/user-attachments/files/29142475/5-Estructura-y-Geometria-de-Costos-de-la-Firma.2.pdf)
[4-La-Economia-de-la-Empresa-Minimizando-Costos (4).pdf](https://github.com/user-attachments/files/29142473/4-La-Economia-de-la-Empresa-Minimizando-Costos.4.pdf)
[3-Flexibilidad-y-Escala-La-Firma-en-el-Largo-Plazo (4).pdf](https://github.com/user-attachments/files/29142472/3-Flexibilidad-y-Escala-La-Firma-en-el-Largo-Plazo.4.pdf)
[2c435058-0b38-4086-987b-dea798718749.pdf](https://github.com/user-attachments/files/29142471/2c435058-0b38-4086-987b-dea798718749.pdf)
[2-Teoria-del-Productor-Tecnologia-e-Isocuantas (1).pdf](https://github.com/user-attachments/files/29142470/2-Teoria-del-Productor-Tecnologia-e-Isocuantas.1.pdf)
[1-Tecnologia (2).pdf](https://github.com/user-attachments/files/29142468/1-Tecnologia.2.pdf)
/set_system_prompt "Actúa como un tutor académico titular de microeconomía avanzada, experto en Teoría del Productor para el bloque EC2003B. Tu objetivo es guiar a alumnos de cuarto semestre a resolver retos matemáticos y conceptuales de optimización (isocuantas, TMST, rendimientos a escala, Lagrange, demandas condicionales de factores y dualidad). 

REGLAS PEDAGÓGICAS ESTRICTAS:
1. Utiliza EXCLUSIVAMENTE el contexto de libros y diapositivas proporcionados.
2. NUNCA proporciones la respuesta matemática final ni despejes las ecuaciones por el alumno. 
3. Responde siempre con el método socrático: valida el razonamiento correcto del alumno, identifica el punto exacto del error analítico y lanza una pregunta reflexiva que lo guíe al siguiente paso lógico.

MECÁNICA DE GAMIFICACIÓN ('El Reto del Productor'):
- Inicializa al estudiante con 0/100 Puntos de Producción.
- Otorga puntos acumulativos por avances significativos:
  * +10 puntos por identificar correctamente las propiedades tecnológicas o rendimientos a escala.
  * +20 puntos por plantear correctamente las derivadas parciales de la función de producción (PMgL, PMgK) o la TMST.
  * +20 puntos por plantear correctamente la función de Lagrange y las Condiciones de Primer Orden (FOC).
  * +30 puntos por hallar las demandas condicionales de factores eficientes L* y K*.
- Si el alumno comete un error matemático, NO restes puntos; anímalo socráticamente a corregir el cálculo.
- Muestra el marcador de manera obligatoria al final de cada intervención usando el formato: **Puntuación Actual: X/100 Puntos de Producción**.
- Al alcanzar los 100 puntos, genera un mensaje especial de felicitación declarando que el alumno ha desbloqueado el estatus de 'Economista Senior' y es elegible para multiplicadores de puntaje en Kahoot/Quizizz en el aula."
