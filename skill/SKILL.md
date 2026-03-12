---
name: market-research-insurance
description: >
  Skill especializado para ejecutar estudios de mercado del sector asegurador mexicano.
  Úsalo cuando el proyecto implique analizar ramos de seguros (GMM, Autos, Daños, Vida),
  comparar oferta de valor entre competidores, evaluar brechas de portafolio de una aseguradora
  específica, o profundizar en Responsabilidad Civil con sus subramos. Activar también cuando
  se necesite triangular datos de CNSF, AMIS u otras fuentes regulatorias con información
  comercial de productos.
---

# Skill: Estudio de Mercado — Sector Asegurador México

## Propósito

Guía paso a paso para producir análisis de mercado rigurosos y accionables en el sector
asegurador, con énfasis en la estructura de productos, competencia, y evaluación de brechas
de portafolio para una aseguradora específica (en este proyecto: Sura).

---

## Workflow Principal

### FASE 1 — Recolección de datos por ramo

Para cada ramo a analizar, ejecuta este ciclo:

1. **Datos macro del ramo** (fuentes: CNSF, AMIS)
   - Prima directa emitida total del ramo (últimos 3 años)
   - Participación de mercado de top 5-8 aseguradoras
   - Siniestralidad promedio del sector
   - Tasa de crecimiento YoY

2. **Mapeo de oferta de valor** (fuentes: páginas web de aseguradoras)
   - Coberturas básicas vs. adicionales
   - Exclusiones relevantes
   - Límites y sublímites típicos
   - Deducibles estándar del mercado
   - Diferenciadores de producto

3. **Canales y distribución**
   - Agentes independientes / brokers
   - Directo / digital
   - Bancaseguros
   - Corporativo / especializado

4. **Tendencias y emergentes**
   - Nuevas coberturas en desarrollo
   - Regulación reciente (CNSF circular específica)
   - Comportamiento post-pandemia si aplica

---

### FASE 2 — Análisis profundo Daños + RC

Para el ramo de Daños, sigue este desglose adicional:

#### 2A. Subramos de Daños (nivel medio de detalle)
Para cada subramo (Incendio, Terremoto, Transporte, Crédito, Agrícola, Misceláneos):
- Tamaño relativo dentro del ramo Daños
- Principales jugadores especializados
- Características técnicas del producto

#### 2B. Responsabilidad Civil (MÁXIMO DETALLE)

Para **cada línea de RC**, documenta:

```
Nombre del subramo RC
├── Descripción técnica del riesgo cubierto
├── Marco legal en México (si aplica)
├── Tamaño de mercado estimado
├── Aseguradoras que lo ofrecen en MX
│   ├── Nacionales (GNP, Sura, Mapfre, AXA...)
│   └── Especializadas (Chubb, AIG, Zurich, Lloyd's...)
├── Rangos de suma asegurada típicos
├── Primas referenciales (si disponibles)
├── Cliente objetivo
├── Nivel de madurez del mercado MX vs. internacional
│   (Emergente / En desarrollo / Maduro)
└── Tendencias específicas
```

**Líneas de RC a cubrir:**
- RC General / Operaciones
- RC Profesional (Errors & Omissions)
- RC Directores y Funcionarios (D&O)
- RC Producto / Responsabilidad por Producto
- RC Ambiental / Contaminación
- RC Cyber / Riesgos Digitales
- RC Construcción (CAR) y Montaje (EAR)
- RC Transporte (Carga y Flota)
- RC Patronal

---

### FASE 3 — Gap Analysis de Sura

Construye una tabla para cada ramo con este formato:

| Producto / Subramo | ¿Sura lo tiene? | Observaciones | Fuente |
|-------------------|-----------------|---------------|--------|
| RC General | ✅ Sí | Ofrecido vía corredor | sura.com.mx |
| D&O PyMEs | ⚠️ Limitado | Solo grandes empresas | ... |
| RC Cyber | ❌ No detectado | Sin evidencia en sitio | ... |

**Escala:**
- ✅ **Tiene producto**: Evidencia clara en canales oficiales
- ⚠️ **Tiene pero limitado**: Existe pero con restricciones (segmento, suma asegurada, canal)
- ❌ **No detectado**: Sin evidencia pública al momento del análisis
- 🔍 **Requiere verificación**: Dato incierto, necesita validación directa

---

### FASE 4 — Síntesis y Entregables

1. Consolida `analisis/*.md` en `outputs/estudio-mercado-completo.md`
2. Extrae hallazgos clave en `outputs/resumen-ejecutivo.md` (máx. 2 páginas)
3. Actualiza `referencias/fuentes.md` con todas las fuentes usadas

---

## Criterios de Calidad

| Criterio | Estándar |
|----------|---------|
| Datos de mercado | Fuente + año visible en cada cifra |
| Análisis de Sura | Verificado en fuente oficial (sura.com.mx o comunicado) |
| RC subramos | Todos los 9 subramos cubiertos con estructura completa |
| Resumen ejecutivo | Autocontenido, orientado a decisiones de portafolio |

---

## Fuentes Prioritarias (URLs de referencia)

```
CNSF Estadísticas:    https://www.gob.mx/cnsf
AMIS Estadísticas:    https://www.amis.com.mx/portal/estadisticas
Sura México:          https://www.sura.com.mx
GNP Seguros:          https://www.gnp.com.mx
Mapfre México:        https://www.mapfre.com.mx
AXA México:           https://axa.mx
Chubb México:         https://www.chubb.com/mx-es
AIG México:           https://www.aig.com.mx
Zurich México:        https://www.zurich.com.mx
Swiss Re Institute:   https://www.swissre.com/institute
```

---

## Glosario Rápido

| Término | Definición |
|---------|-----------|
| RC | Responsabilidad Civil — cobertura por daños a terceros |
| D&O | Directors & Officers — RC de directivos por decisiones gerenciales |
| E&O | Errors & Omissions — RC Profesional |
| CAR | Contractor's All Risk — RC en construcción |
| EAR | Erection All Risk — RC en montaje industrial |
| Prima directa | Monto cobrado al asegurado antes de reaseguro |
| Siniestralidad | Relación siniestros pagados / primas devengadas |
| Sublímite | Límite específico dentro de la suma asegurada general |

*Para el glosario completo, consultar `referencias/glosario-seguros.md`*
