# Greed World

Un RPG sandbox navale data-driven sviluppato in Unity.


## Panoramica

Greed World è un videogioco 2D sandbox che combina esplorazione, commercio, diplomazia, gestione dell'equipaggio e combattimento navale tattico.

Il giocatore naviga in un mondo dinamico influenzato da sistemi economici, relazioni diplomatiche, condizioni meteorologiche, reputazione e comportamenti emergenti dei personaggi. Ogni decisione contribuisce a modellare il modo in cui il mondo reagisce alle azioni del giocatore, generando esperienze uniche guidate dai sistemi di simulazione piuttosto che da eventi completamente scriptati.

Il progetto è stato sviluppato interamente da me nel corso di oltre tre anni e rappresenta sia un videogioco sia un esercizio di software engineering su larga scala, con particolare attenzione ad architettura software, system design e mantenibilità del codice.

> Sviluppato individualmente per oltre 3 anni con un forte focus su UI Engineering, Data-Driven Architecture, System Design e pattern software scalabili.

---

## Architettura Software

Il progetto adotta un'architettura a layer progettata per separare responsabilità, logica di business, accesso ai dati e persistenza.

```text
UI
↓
Managers
↓
Systems
↓
Repositories
↓
Data
```

La codebase è composta da centinaia di script C#, decine di migliaia di righe di codice e decine di sistemi interconnessi.

### Principi Architetturali

- Data-Driven Architecture
- Repository-Based Architecture
- Runtime Entity Database
- JSON-Based Content Database
- Serializable Domain Models
- Event-Driven Communication
- Dependency Injection
- Separation of Concerns

---

## Sistemi Principali

### Data Management System

Sistema di persistenza personalizzato basato su modelli serializzabili.

Funzionalità principali:

- Salvataggio e caricamento dati
- Versionamento dei salvataggi
- Serializzazione JSON
- Cifratura opzionale dei dati
- Gestione modulare dei file
- Persistenza dello stato runtime

### Entity Repository

Database centrale delle entità utilizzato per indicizzare e recuperare dati tramite identificatori univoci.

Caratteristiche:

- Lookup generico delle entità
- Recupero tipizzato dei dati
- Caching runtime
- Comunicazione disaccoppiata tra sistemi
- Implementazione del Repository Pattern

Questo approccio consente ai sistemi di comunicare tramite ID anziché riferimenti diretti, riducendo significativamente l'accoppiamento tra moduli.

### Economy & Trading System

Sistema economico dinamico che regola il valore delle merci in base alle condizioni del mondo di gioco.

Funzionalità:

- Prezzi dinamici
- Rotte commerciali
- Gestione del carico
- Interazioni commerciali
- Fluttuazioni di mercato

### Diplomatic System

Gestisce le relazioni tra:

- Personaggio → Personaggio
- Personaggio → Regno
- Regno → Regno

Le relazioni influenzano missioni, opportunità commerciali, conflitti ed eventi del mondo.

### Personality System

I personaggi sviluppano tratti comportamentali in base alle azioni compiute durante il gioco.

Esempi:

- Avidità
- Onore
- Crudeltà
- Coraggio
- Ambizione

Questi tratti influenzano decisioni dell'IA, diplomazia e reazioni del mondo.

### Knowledge System

Sistema di gestione della conoscenza che distingue tra:

- Esperienza diretta
- Voci e dicerie
- Informazioni condivise

Le informazioni possono deteriorarsi nel tempo, introducendo incertezza e incentivando l'esplorazione.

### Crew Management System

Simula la vita a bordo di una nave.

Funzionalità:

- Consumo di viveri
- Gestione del morale
- Requisiti dell'equipaggio
- Fedeltà dei marinai
- Ammutinamenti

### Weather System

Sistema meteorologico che influenza navigazione, commercio, incontri ed esplorazione.

### Crisis System

Gestisce eventi globali in grado di modificare condizioni economiche, politiche e sociali del mondo di gioco.

### Quest System

Architettura data-driven per la gestione delle missioni.

Supporta:

- Obiettivi
- Prerequisiti
- Ricompense
- Progressione guidata da eventi

### Dialogue System

Sistema di dialogo integrato con reputazione, diplomazia e stato del mondo.

### AI System

Sistema di simulazione comportamentale delle fazioni.

Gestisce:

- Commercio
- Pattugliamento
- Ricerca di bersagli
- Evitamento delle minacce
- Navigazione strategica
- Attività autonome del mondo

### Battle System

Sistema di combattimento navale a turni basato su griglia esagonale.

Funzionalità:

- Posizionamento tattico
- Gestione della gittata dei cannoni
- Pianificazione del movimento
- Orientamento della nave
- Combattimenti nave contro nave

Il posizionamento e l'angolo di attacco rappresentano elementi fondamentali della strategia.

---

## Front-End & UI Engineering

L'intera interfaccia utente è stata progettata e sviluppata da me.

Funzionalità implementate:

- Data Binding
- Tooltip dinamici
- Finestre modali
- Drag & Drop
- Liste dinamiche
- Ordinamenti
- Filtri
- Menu contestuali
- Flussi UI complessi

L'architettura della UI segue principi MVC e MVVM per mantenere una chiara separazione tra presentazione e logica applicativa.

---

## Gestione dei Dati

Greed World utilizza un'architettura di persistenza a doppio livello.

### Static JSON Repository

I contenuti statici del gioco sono archiviati in file JSON e caricati in modelli serializzabili fortemente tipizzati.

Esempi:

- Oggetti
- Navi
- Città
- Regni
- Classi
- Missioni
- Effetti

### Runtime Entity Database

Lo stato dinamico della partita viene gestito tramite repository runtime dedicati.

Vantaggi:

- Scalabilità
- Manutenibilità
- Recupero efficiente dei dati
- Separazione tra contenuti e stato della partita

---

## Design Patterns

Durante lo sviluppo sono stati utilizzati numerosi pattern software:

- Singleton
- Observer / Event Bus
- Factory
- Fluent Builder
- Strategy
- State Machine
- Repository
- Dependency Injection
- Command
- MVC
- MVVM
- ECS
- Data-Driven Design

---

## Strumenti di Sviluppo

Per velocizzare lo sviluppo e migliorare il debugging sono stati realizzati strumenti interni dedicati.

Tra questi:

- Editor Windows personalizzate
- Tool di debug e visualizzazione runtime
- Generatori automatici di dati
- Utility di ispezione e testing

---

## Tecnologie

- Unity
- C#
- JSON Serialization
- Newtonsoft Json
- Odin Serializer

Architettura e Design:

- MVC
- MVVM
- ECS
- Repository Pattern
- Dependency Injection
- Event-Driven Architecture
- Data-Driven Design

---

## Screenshot

<p align="center">
  <img width="450" alt="Screenshot #1" src="https://github.com/user-attachments/assets/e98a0dad-4fc9-4773-8747-82ceaae00930" />
  <img width="450" alt="Screenshot #2" src="https://github.com/user-attachments/assets/1f3fac4c-dc72-4591-8e02-9aa68db04560" />
  <img width="450" alt="Screenshot #3" src="https://github.com/user-attachments/assets/5c4dbfdb-8b63-4c93-a3e1-7423541172c6" />
  <img width="450" alt="Screenshot #4" src="https://github.com/user-attachments/assets/7146bae4-6ca9-4aac-bb92-a6ad85e68684" />
  <img width="450" alt="Screenshot #5" src="https://github.com/user-attachments/assets/83b37799-0ccc-45ca-99bb-889b120a39a3" />
</p>

---

## Stato del Progetto

Il progetto è attualmente in sviluppo attivo.

La versione corrente include un prototipo giocabile e continua a essere utilizzata come piattaforma di sperimentazione per architetture software, UI engineering e system design.

---

## Codice Sorgente

Il codice sorgente è mantenuto in una repository privata.

Questa repository pubblica esiste come vetrina del progetto e documentazione delle soluzioni architetturali, dei sistemi sviluppati e dei concetti di software engineering esplorati durante lo sviluppo.
