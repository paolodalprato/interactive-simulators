# Opzione A: Animazioni Differenziate per Scenario

## Concept

Invece di un'animazione identica per tutti gli scenari (con solo cambio di colore), ogni scenario avrebbe un comportamento visivo distintivo che racconta visivamente la sua specificità.

## Comportamenti Visivi Proposti

### Stimoli Naturali

#### Dolore (Glutammato)
- **Velocità**: MOLTO veloce (tutto il processo in ~1.5s invece di 3s)
- **Quantità**: Molte vescicole (6-8) che si fondono quasi simultaneamente
- **Effetto**: Flash intenso, quasi "esplosivo" sul dendrite
- **Colore**: Rosso intenso con bagliore
- **Sensazione visiva**: Urgenza, allarme

#### Piacere (Dopamina)
- **Velocità**: Più lenta e "morbida" (~4s)
- **Quantità**: Vescicole che si rilasciano in sequenza, non tutte insieme
- **Effetto**: Onde pulsanti sul dendrite, effetto "glow" che cresce gradualmente
- **Colore**: Verde con sfumature dorate
- **Sensazione visiva**: Gratificazione, calore

#### Paura (Noradrenalina)
- **Velocità**: Rapida con SCARICHE MULTIPLE (3-4 burst consecutivi)
- **Quantità**: Rilascio a raffica, non continuo
- **Effetto**: Dendrite che "lampeggia" ripetutamente
- **Colore**: Arancione con flash bianchi
- **Sensazione visiva**: Allerta, tensione

### Sostanze Quotidiane

#### Caffè (Blocco Adenosina)
- **Meccanismo diverso**: NON mostra rilascio, ma BLOCCO
- **Visualizzazione**: Recettori che si "chiudono" o si coprono
- **Effetto**: Adenosina (pallini grigi) che "rimbalza" sui recettori bloccati
- **Colore**: Marrone caffè per i bloccanti
- **Sensazione visiva**: Barriera, impedimento (positivo)

#### Camomilla (Potenziamento GABA)
- **Velocità**: Molto lenta (~5s)
- **Effetto speciale**: Il segnale si ATTENUA visibilmente
- **Visualizzazione**: Tutto rallenta, colori che sfumano verso toni più soft
- **Colore**: Viola/lavanda con effetto "dissolve"
- **Sensazione visiva**: Calma, rilassamento

#### Vino (GABA + riduzione Glutammato)
- **Velocità**: Rallentata progressivamente
- **Effetto speciale**: Neurotrasmettitori che si muovono in modo meno preciso, "sbandano"
- **Visualizzazione**: Traiettorie non lineari, leggero "wobble"
- **Colore**: Rosso vino con effetto sfocato
- **Sensazione visiva**: Rilassamento ma anche imprecisione

#### Cioccolato (Endorfine)
- **Velocità**: Moderata
- **Effetto speciale**: Piccole "scintille" o particelle extra che accompagnano il rilascio
- **Visualizzazione**: Effetto più festoso, particelle decorative
- **Colore**: Marrone caldo con accenti dorati
- **Sensazione visiva**: Piccolo piacere, comfort

## Implementazione Tecnica

### Struttura Dati Estesa

```javascript
const scenarios = {
  pain: {
    // ... dati esistenti ...
    animation: {
      totalDuration: 1500, // ms
      vesicleCount: 8,
      releasePattern: 'simultaneous', // 'simultaneous' | 'sequential' | 'burst'
      burstCount: 1,
      particleEffect: 'flash',
      dendriteEffect: 'intense-glow',
      movementStyle: 'direct', // 'direct' | 'wave' | 'wobble'
    }
  },
  fear: {
    animation: {
      totalDuration: 2500,
      vesicleCount: 4,
      releasePattern: 'burst',
      burstCount: 4,
      burstInterval: 400, // ms tra i burst
      particleEffect: 'strobe',
      dendriteEffect: 'flashing',
      movementStyle: 'direct',
    }
  },
  coffee: {
    animation: {
      totalDuration: 3000,
      mechanism: 'blocking', // diverso da 'release'
      blockedSubstance: 'adenosine',
      particleEffect: 'bounce',
      receptorEffect: 'closing',
    }
  },
  // ... etc
};
```

### Funzioni di Animazione Specifiche

```javascript
// Invece di un'unica funzione animate(), avere:
const animationStrategies = {
  standard: standardReleaseAnimation,
  burst: burstReleaseAnimation,
  blocking: blockingAnimation,
  attenuating: attenuatingAnimation,
};

function getAnimationStrategy(scenario) {
  if (scenario.animation.mechanism === 'blocking') return animationStrategies.blocking;
  if (scenario.animation.releasePattern === 'burst') return animationStrategies.burst;
  // ... etc
  return animationStrategies.standard;
}
```

## Effort Stimato

- **Refactoring struttura dati**: 1-2 ore
- **Implementazione animazioni differenziate**: 4-6 ore
- **Testing e tuning visivo**: 2-3 ore
- **Totale**: ~8-10 ore di sviluppo

## Note

Questa opzione mantiene il format "simulatore con animazione" ma richiede un investimento significativo per differenziare ogni scenario. Il risultato sarebbe molto più engaging perché ogni click rivelerebbe un comportamento visivo nuovo e specifico.

Da considerare per una versione 2.0 del simulatore.
