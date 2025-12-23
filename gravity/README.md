# Simulatore gravità 2D | 2D Gravity Simulator

Un simulatore interattivo per esplorare l'attrazione gravitazionale tra particelle e osservare la formazione di strutture complesse da regole semplici.

An interactive simulator to explore gravitational attraction between particles and observe the formation of complex structures from simple rules.

## 🎯 Cosa imparerai | What You'll Learn

Questo simulatore ti aiuta a comprendere | This simulator helps you understand:
- La legge di gravitazione universale di Newton (F = G·m₁·m₂/r²)
- Come comportamenti complessi emergono da regole semplici
- La conservazione della quantità di moto nelle collisioni
- L'effetto della costante gravitazionale sulla dinamica del sistema

## 🚀 Provalo | Try It

**Online**: [Visualizza simulatore](https://paolodalprato.github.io/interactive-simulators/gravity/gravity-simulator.html)

**Incorporalo nel tuo sito | Embed in your website**:
```html
<iframe 
  src="https://paolodalprato.github.io/interactive-simulators/gravity/gravity-simulator.html" 
  width="100%" 
  height="1400" 
  frameborder="0"
  style="border: none; border-radius: 12px;">
</iframe>
```

## 🎮 Come usarlo | How to Use

1. **Regola i parametri iniziali**: numero di particelle, velocità iniziale, costante gravitazionale G
2. **Premi "Avvia"**: osserva le particelle che si attraggono e si fondono
3. **Sperimenta**: cambia G durante la simulazione per vedere effetti immediati
4. **Premi "Reset"**: ricomincia con nuove condizioni

### Prova questi scenari | Try These Scenarios

**Formazione rapida di ammassi | Rapid cluster formation**:
- G = 300-400
- Particelle = 100-150
- Velocità iniziale = 0,5

**Aggregazione lenta | Slow aggregation**:
- G = 20-30
- Particelle = 50
- Velocità iniziale = 1,0

**Poche particelle tracciabili | Few trackable particles**:
- G = 100
- Particelle = 20-30
- Velocità iniziale = 0,3

## 🔬 Caratteristiche principali | Key Features

- **Fisica realistica**: implementazione accurata della legge di gravitazione universale
- **Visualizzazione masse**: colori che variano dal rosso (massa piccola) al violetto (massa grande)
- **Conservazione quantità di moto**: le collisioni rispettano le leggi fisiche
- **Comportamento emergente**: strutture complesse emergono spontaneamente
- **Parametri regolabili**: controllo completo su numero particelle, velocità e gravità
- **Bilingue**: disponibile in italiano e inglese

## 📚 Contesto didattico | Educational Context

**Pubblico target | Target audience**: Studenti di scuola superiore e università, appassionati di fisica, insegnanti

**Prerequisiti | Prerequisites**: Conoscenza base di fisica (forze, massa, velocità)

**Casi d'uso | Use cases**:
- Dimostrazioni in classe di fisica
- Auto-apprendimento sulla gravitazione
- Esplorazione del comportamento emergente nei sistemi fisici
- Visualizzazione di concetti astratti di fisica

**Concetti dimostrati | Concepts demonstrated**:
- Legge di gravitazione universale (F ∝ m₁·m₂/r²)
- Dipendenza della forza dalla distanza (legge dell'inverso del quadrato)
- Conservazione della massa e della quantità di moto
- Comportamento emergente in sistemi complessi
- Formazione di strutture per auto-aggregazione gravitazionale

**Misconcezioni comuni affrontate | Common misconceptions addressed**:
- "La gravità agisce istantaneamente" → no, ma a questa scala la differenza è impercettibile
- "Servono enormi masse per effetti gravitazionali visibili" → dipende dalla scala e dalla costante G
- "Le collisioni cosmiche sono esplosive" → spesso sono fusioni che conservano momento

## 🛠️ Dettagli tecnici | Technical Details

- **Tecnologie | Technologies**: HTML5, React 18, Tailwind CSS, Canvas 2D
- **Formato | Format**: File HTML singolo autosufficiente | Single self-contained HTML file
- **Requisiti | Requirements**: Browser moderno (Chrome, Firefox, Safari, Edge)
- **Mobile-friendly**: Ottimizzato per desktop, visualizzabile su mobile

**Fisica implementata | Physics implemented**:
- Forza gravitazionale: F = G · m₁ · m₂ / r²
- Integrazione numerica: metodo di Eulero con dt = 0,016s (60 FPS)
- Collisioni: fusione perfettamente anelastica con conservazione quantità di moto
- Bordi: rimbalzo con coefficiente di restituzione 0,8

## 📖 Fonti e riferimenti | Sources and References

- Newton, I. (1687). *Philosophiæ Naturalis Principia Mathematica*
- Goldstein, H., Poole, C., & Safko, J. (2002). *Classical Mechanics* (3rd ed.)
- Concetti di sistemi complessi e comportamento emergente dalla teoria dei sistemi dinamici

## 📄 Licenza | License

Licenza MIT - Libero di usare, modificare e distribuire con attribuzione.

MIT License - Free to use, modify, and distribute with attribution.

## 👤 Autore | Author

**Paolo Dalprato**
- Sito web | Website: [ai-know.pro](https://ai-know.pro)
- Substack: [paolodalprato.substack.com](https://paolodalprato.substack.com)
- GitHub: [@paolodalprato](https://github.com/paolodalprato)
