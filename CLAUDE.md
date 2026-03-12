# Estudio de Mercado — Sector Asegurador México
## CLAUDE.md — Instrucciones Maestras del Proyecto

---

## 🎯 Objetivo del Proyecto

Producir un estudio de mercado estructurado y accionable del sector asegurador mexicano, con análisis de oferta de valor por ramo, enfoque especial en Daños y Responsabilidad Civil, y evaluación de si Sura cuenta hoy con productos competitivos en cada segmento.

**Cliente interno:** Liderazgo de Operaciones — LCG  
**Uso previsto:** Análisis estratégico / insumo para propuesta de valor hacia clientes del sector asegurador  
**Idioma de entregables:** Español

---

## 🗂️ Estructura del Proyecto

```
estudio-mercado-seguros/
├── CLAUDE.md                    ← Este archivo (instrucciones maestras)
├── SKILL.md                     ← Skill específico para el estudio
├── datos-brutos/                ← Fuentes crudas: PDFs, páginas web, datos CNSF
│   ├── gmm/
│   ├── autos/
│   ├── danos/
│   │   ├── incendio/
│   │   ├── terremoto/
│   │   ├── responsabilidad-civil/
│   │   └── miscelaneos/
│   └── vida/
├── analisis/                    ← Análisis intermedios por ramo
│   ├── gmm.md
│   ├── autos.md
│   ├── danos.md                 ← Análisis principal detallado
│   ├── responsabilidad-civil.md ← Análisis específico RC (máximo detalle)
│   ├── vida.md
│   └── sura-gap-analysis.md     ← ¿Tiene Sura estos productos?
├── outputs/                     ← Entregables finales
│   ├── estudio-mercado-completo.md
│   ├── resumen-ejecutivo.md
│   └── presentacion/            ← Si se requiere deck
└── referencias/                 ← Marco metodológico y fuentes
    ├── metodologia.md
    ├── fuentes.md
    └── glosario-seguros.md
```

---

## 📋 Alcance del Estudio

### Ramos a cubrir

| Ramo | Profundidad | Notas |
|------|------------|-------|
| GMM (Gastos Médicos Mayores) | Media | Individual + Colectivo |
| Autos | Media | RC obligatoria + cobertura amplia |
| Daños | **Alta** | Ver detalle abajo |
| Vida | Media | Temporal + Dotal + Grupo |

### Daños — Desglose requerido

- **Incendio y líneas aliadas** (Fire & Allied Lines)
- **Terremoto y catástrofes naturales**
- **Transporte** (marítimo, terrestre, aéreo)
- **Crédito y caución**
- **Agrícola y animales**
- **Misceláneos** (robo, vidrios, equipo electrónico, etc.)
- **Responsabilidad Civil** ← **Máximo nivel de detalle**
  - RC General / Operaciones
  - RC Profesional (E&O)
  - RC Directores y Funcionarios (D&O)
  - RC Producto
  - RC Ambiental / Contaminación
  - RC Cyber / Digital (emergente)
  - RC Construcción y Montaje (CAR/EAR)

---

## 🔍 Preguntas Clave a Responder

### Para todos los ramos:
1. ¿Cuáles son los principales competidores y su participación de mercado?
2. ¿Cuál es la propuesta de valor diferenciadora de los líderes?
3. ¿Cuáles son las tendencias de producto (coberturas emergentes, exclusiones relevantes)?
4. ¿Cuál es el perfil del cliente objetivo?
5. ¿Qué canales de distribución dominan?

### Específico para Responsabilidad Civil:
1. ¿Qué segmentos de RC están más desarrollados en México vs. mercados maduros?
2. ¿Existe oferta local para RC Cyber, RC Ambiental, D&O en PyMEs?
3. ¿Cuál es el nivel de penetración real vs. potencial?
4. ¿Qué aseguradoras especializadas participan (Lloyd's, AIG, Chubb, Zurich, etc.)?

### Análisis Sura:
1. ¿Qué productos tiene Sura hoy en cada ramo/subramo?
2. ¿Dónde hay brechas evidentes vs. el mercado?
3. ¿Dónde Sura tiene ventaja competitiva documentada?
4. ¿Qué oportunidades de portafolio existen?

---

## 📊 Fuentes de Información Prioritarias

1. **CNSF** (Comisión Nacional de Seguros y Fianzas) — estadísticas oficiales
   - Anuario estadístico: https://www.cnsf.gob.mx
2. **AMIS** (Asociación Mexicana de Instituciones de Seguros)
   - Estadísticas de sector: https://www.amis.com.mx
3. **Páginas de productos de aseguradoras** — Sura, GNP, Mapfre, AXA, MetLife, Chubb, AIG, Zurich
4. **Swiss Re / Munich Re** — estudios de RC y tendencias globales
5. **Reportes de calificadoras** — AM Best, Fitch sobre aseguradoras MX

---

## ✅ Criterios de Calidad del Entregable

- Cada afirmación de participación de mercado debe tener fuente y fecha
- El análisis de Sura debe distinguir claramente: ✅ Tiene producto / ⚠️ Tiene pero limitado / ❌ No tiene
- El nivel de detalle en RC debe permitir tomar decisiones de portafolio
- El resumen ejecutivo debe ser autocontenido (máx. 2 páginas)

---

## 🧭 Instrucciones para Claude Code

Cuando trabajes en este proyecto:

1. **Lee este CLAUDE.md primero** en cada sesión nueva
2. **Lee el SKILL.md** antes de iniciar cualquier análisis
3. **Documenta tus fuentes** en `referencias/fuentes.md` conforme avances
4. **Guarda análisis intermedios** en `analisis/` antes de consolidar en `outputs/`
5. **Usa web search** para datos de mercado actualizados (2023-2025)
6. **Usa el glosario** en `referencias/glosario-seguros.md` para terminología consistente
7. Cuando hagas el gap analysis de Sura, **busca primero en sura.com.mx** antes de asumir

---

---

## 🎨 Brand — Meridian Consulting

**Firma:** Meridian Consulting — Market Intelligence

### Paleta de colores
| Token | Nombre | Hex |
|-------|--------|-----|
| `--navy` | Midnight Navy | `#0F172A` |
| `--slate` | Deep Slate | `#1E293B` |
| `--ivory` | Soft Ivory | `#F8FAFC` |
| `--graphite` | Graphite Gray | `#475569` |
| `--silver` | Silver Mist | `#CBD5E1` |
| `--teal` | Meridian Teal | `#0F766E` |

### Tipografía
- **Headings:** Manrope (weights: 600, 700, 800)
- **Body:** Inter (weights: 400, 500, 600)

### Personalidad de marca
Minimalista · Ejecutivo · Preciso · Premium · Moderno · Confiable · Analítico

### Reglas visuales para entregables
- Teal **solo como acento** — nunca como color dominante
- Sin gradientes llamativos
- Whitespace generoso — jerarquía editorial fuerte
- Layouts estructurados con lógica de cuadrícula sutil
- Dividers suaves, tipografía limpia, datos presentados sin ruido visual
- El resultado debe sentirse como un entregable de consultoría premium, no como un sitio web

---

*Última actualización: Marzo 2025 | Proyecto Meridian Consulting*
