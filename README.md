# Executive Lab · Landing de Venta v3

Landing page de venta para el programa ejecutivo **Executive Lab · Cohorte J26-06**.

🌐 **Preview en vivo:** https://executive-lab-venta-v3.vercel.app

---

## 📁 Estructura

```
executive-lab-venta/
├── index.html              ← Landing completa (HTML+CSS plano)
└── assets/
    ├── editorial.css       ← Estilos globales del sistema
    ├── programa.css        ← Estilos específicos heredados del clon
    ├── base.js             ← Reveal animations + carrusel testimonios
    ├── hero.webp           ← Imagen rey de ajedrez (hero)
    └── logo.svg            ← Logo Executive Lab
```

---

## 🎯 Cohorte J26-06

- **Precio:** 2.497€ · 2 plazos × 1.300€ · 3 plazos × 900€
- **Audiencia:** C-level, fundadores, comité directivo
- **Tipografía:** DM Serif Display (titulares) + Lato (body)
- **Paleta:** Rojo `#EC4429` · Negro `#0A0A0A` · Crema `#F4EEE6`

---

## 📋 Estructura de bloques (orden)

1. **Nav** (sticky) · Programa · Para quién · Inversión · FAQ
2. **Hero** · negro + VSL Dropbox + CTA "Solicitar acceso"
3. **Trust bar** · marquee infinito con 8 logos (placeholders)
4. **Dolor v2** · dark, 3 cards (Caballo de Troya / Caos / Ruido y coste)
5. **Overview 13 meses** · "30 días para criterio, 12 meses para no perderlo" (Fase 1 + Fase 2)
6. **Intensivo 4 semanas** · roadmap vertical editorial (zigzag)
7. **Departamento I+D** · 4 cards (Filtrado / Casos reales / Herramientas / Comunidad)
8. **CTA intermedio 1** · "Solicitar mi plaza"
9. **Mentores** · 4 cards (Eric, Carlos, Sanchis, Nacho) con 3 credenciales cada uno
10. **Testimonios** · 3 placeholders 9:16 / 16:9
11. **CTA intermedio 2** · "Solicitar mi plaza"
12. **Oferta** · dark, 2 columnas (Qué incluye + Inversión) + microcta dual
13. **Garantía Ejecutiva** · sello circular 100% + condición destacada
14. **CTA intermedio 3** · "Solicitar mi plaza"
15. **¿Para quién?** · encaje SÍ/NO (card unificada con divisor)
16. **FAQ** · 8 preguntas con calendario real J26-06
17. **Cierre dual** · asterisco rotando + 2 CTAs (plaza + WhatsApp)
18. **Footer**

---

## ⚠️ Pendientes operativos (para producción)

### 🔗 URLs reales por sustituir
- [ ] **Link pago directo** Stripe/GHL → buscar `#payment-link-placeholder` (microcta oferta)
- [ ] **Link WhatsApp** → buscar `#whatsapp-placeholder` (cierre dual + microcta oferta)

### 🖼️ Assets reales por subir
- [ ] **8 logos** del trust bar marquee → sustituir `<div class="tm-item">[logo 0X]</div>` por `<img src="...">`
- [ ] **4 fotos mentores** → sustituir placeholders `[ Foto Eric|Carlos|Sanchis|Nacho ]` en `.mv2-photo`
- [ ] **3 vídeos testimonios** (9:16 o 16:9) → sustituir placeholders en `.vid-slide`. Para 9:16 añadir clase `is-vertical` al `<article class="vid-slide">`.
- [ ] **VSL del hero** → migrar de Dropbox temporal a Vimeo / Cloudflare Stream (URL en `<video class="hv2-video">`)

---

## 🎨 Sistema de clases (por bloques)

| Bloque | Clase contenedor | Notas |
|---|---|---|
| Hero | `.hv2-section` | Dark con asterisco/rey de fondo |
| Trust marquee | `.trust-marquee` | `.tm-track` con duplicado para loop infinito |
| Dolor | `.dolor-v2` | Dark, 3 cards numeradas |
| Overview 13m | `.overview-v3` | Crema, 2 cols con divisor vertical |
| 4 semanas | `.weeks-roadmap` | Crema, timeline zigzag con dots rojos |
| Dpto I+D | `.ide-v2` | Crema, 4 cards en grid 2x2 |
| Mentores | `.mentors-v2` | Blanco, 4 cards con 3 credenciales c/u |
| Testimonios | `.section-paper` id="resultados" | Carrusel del clon original |
| Oferta | `.offer-v3` | Dark, 2 cols (features + precio) |
| Garantía | `.guarantee-v2` | Tierra, sello circular animado |
| Encaje | `.encaje-v3` | Crema, card unificada SÍ/NO |
| FAQ | `.faq-v2` | Crema, accordion numerado |
| Cierre dual | `.closing-v2` | Dark, asterisco rotando + 2 CTAs |

---

## 🚀 Deploy

- **Vercel actual:** https://executive-lab-venta-v3.vercel.app
- Para integrar en `executive-lab-site` (Astro): cada bloque está aislado con su `<style>` propio. Carlos puede copiar bloque a bloque y adaptarlos a componentes Astro o mantenerlos como secciones inline.

---

## 📝 Notas de copy

- **Palabra "bootcamp" eliminada** de toda la landing → sustituida por "intensivo" / "intensivo ejecutivo".
- **Precio actualizado** a 2.497€ (antes 2.000€ del PDF antiguo).
- **Financiación actualizada** a 2 plazos × 1.300€ / 3 plazos × 900€.
- **Mentor Euge Oller** retirado del PDF original.
- **8 fechas reales J26-06** integradas en FAQ #01 (Kick-off 28 mayo · Clases 1–25 junio).
