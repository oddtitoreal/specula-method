# Community Co-Creation Protocol
**Version**: 1.0
**Date**: 2026-03-27
**Status**: Normative (Phase 5 operational protocol)
**Repo**: specula-method
**Allineamento**: specula-framework Phase 5 schema (`phase5_cocreation.schema.json`)

---

## 1. Scopo

La Phase 5 (Community Co-Creation) è descritta nel Specula Method come "exposing the preferable future hypothesis to dialogue with communities". Senza un protocollo operativo, rischia di essere una **consultazione teatro**: raccogliere feedback senza che il feedback cambi nulla.

Questo documento specifica *come* funziona la Phase 5 nel dettaglio:
- Quando è obbligatoria vs. facoltativa
- Come il feedback rimodella le decisioni
- Come si gestisce il conflitto quando la community dissocia dai futuri scelti
- Come si traccia la partecipazione e il suo impatto

---

## 2. Quando la Phase 5 è obbligatoria

La Community Co-Creation è **obbligatoria** quando almeno una delle seguenti condizioni è vera:

1. Il brand ha un'identità pubblica consolidata con una community riconoscibile (oltre 5.000 persone)
2. I futuri speculativi generati in Phase 3 hanno impatto diretto su stili di vita, valori, o abitudini delle comunità
3. La AI Constitution dichiara "community" come stakeholder primario
4. Il `moral_entity` definito in Phase 2 è classificato come `caretaker` o `advocate`

La Phase 5 è **facoltativa** (ma raccomandata) per:
- Brand B2B con community interna (team, partner, distributori)
- Progetti in fase di prototyping early-stage senza presenza pubblica

Anche quando facoltativa, se si sceglie di non condurla, **questa scelta deve essere documentata nel Decision Log** con rationale esplicito.

---

## 3. Struttura del processo

### 3.1 Preparazione (pre-Phase 5)

Prima di esporre i futuri speculativi alla community:
- Selezionare i **2-3 scenari** da Phase 1 da sottoporre (non tutti — la scelta è già una posizione)
- Definire il **pubblico** di engagement: chi è la community? (clienti, follower, comunità locali, team interno?)
- Definire il **canale**: workshop fisico, survey digitale, community call, forum aperto, mix
- Definire la **domanda maieutica** che apre il dialogo (non "Vi piace questo futuro?" ma "Cosa vedete che noi non vediamo in questo scenario?")

### 3.2 Esposizione e dialogo

La community viene esposta ai futuri speculativi **come ipotesi aperte, non come annunci**. Il linguaggio conta:
- ✅ "Stiamo esplorando questo futuro — cosa ci sfugge?"
- ❌ "Questo è il nostro futuro — cosa ne pensate?"

Il facilitatore (o l'AI agent in modalità `community_cocreation`) ha il compito di:
1. Raccogliere posizioni divergenti senza neutralizzarle
2. Identificare le tensioni irriducibili (non riconciliarle prematuramente)
3. Documentare le **voci minoritarie** anche se non raggiungono consenso

### 3.3 Sintesi strutturata

L'output obbligatorio della Phase 5 è l'artifact `co_creation` con i seguenti campi **tutti popolati**:

```json
{
  "co_creation": {
    "consensus_areas": ["..."],
    "divergences": [
      {
        "topic": "...",
        "positions": ["position A", "position B"],
        "minority_voices": ["voice statement"]
      }
    ],
    "accepted_changes": ["change accepted from community input"],
    "rejected_changes": ["change explicitly NOT accepted, with rationale"],
    "dissent_log": ["dissent note — required non-empty"]
  }
}
```

**Il campo `dissent_log` deve essere non vuoto.** Se la community non ha espresso dissenso, questo indica un problema metodologico (domanda troppo chiusa, partecipanti non rappresentativi) — non un successo.

**Il campo `rejected_changes` deve essere esplicito.** Ogni feedback ricevuto e non accettato deve comparire qui, con una frase che spiega perché. Il silenzio su questo campo equivale a non aver condotto la co-creazione.

---

## 4. Cosa succede quando la community dissocia

La dissociazione avviene quando la community esprime rifiuto sostanziale dei futuri speculativi proposti. Non è un fallimento — è informazione.

### 4.1 Tipi di dissociazione

| Tipo | Descrizione | Azione obbligatoria |
|---|---|---|
| **Dissociazione parziale** | Consenso su alcuni scenari, rifiuto su altri | Documentare nel `dissent_log`, portare al Circolo di Sintesi |
| **Dissociazione valoriale** | La community rigetta i valori sottostanti agli scenari | Revisione obbligatoria di Phase 2 (Brand Archeology) |
| **Dissociazione totale** | Rifiuto di tutti gli scenari proposti | Re-speculation cycle obbligatorio (ritorno a Phase 1) |
| **Dissociazione silenziosa** | Partecipazione nulla o minima | Considerare come dissociazione parziale, indagare le cause |

### 4.2 Protocollo di escalation

1. **Primo step**: Il facilitatore documenta la dissociazione nel `dissent_log` con dettaglio sufficiente
2. **Secondo step**: Il caso viene portato al Circolo di Sintesi entro 7 giorni dalla chiusura della Phase 5
3. **Terzo step**: Il Circolo delibera (secondo le regole del Governance Charter) se:
   - Procedere a Phase 6 con i futuri confermati dalla maggioranza
   - Modificare i futuri incorporando il feedback della dissociazione
   - Tornare a Phase 1 per un ciclo di re-speculation

**Il Circolo non può ignorare la dissociazione.** Anche scegliere di procedere ignorandola è una delibera che deve essere motivata e documentata nel Decision Log.

### 4.3 Voci minoritarie

Le voci minoritarie non vengono neutralizzate per consenso. Vengono documentate nel campo `minority_voices` delle `divergences` e **rimangono visibili nel Decision Log permanente** del progetto. Non scompaiono solo perché la maggioranza ha deciso diversamente.

---

## 5. Tracciamento della partecipazione

Per prevenire la "co-creazione di facciata" (pochi insider che approvano tutto), la Phase 5 richiede di documentare:

- **Chi ha partecipato**: categorie (non necessariamente identità individuali), numero, canali
- **Chi era assente**: quali segmenti della community non erano rappresentati e perché
- **Come è stato invitato il dissenso**: quale domanda specifica ha aperto lo spazio al dissenso

Questo non è richiesto formalmente dallo schema JSON di Phase 5, ma deve essere incluso nelle **evidence_refs** dell'artifact meta come documento allegato o riferimento.

---

## 6. Integrazione con il Guardian Loop

I segnali raccolti in Phase 5 non spariscono dopo l'avanzamento alla Phase 6. Il Guardian Loop (Phase 6) deve:

- Includere le `divergences` di Phase 5 come segnali da monitorare nel tempo
- Verificare se le `accepted_changes` sono state effettivamente implementate
- Rilevare se nuove voci della community confermano o contraddicono le posizioni raccolte

Il campo `scenario_alignment.emerging` del `guardian_report` è il luogo naturale per segnalare quando la community sta evolvendo rispetto alle posizioni registrate in Phase 5.

---

## 7. Cosa NON è community co-creation

Per chiarezza:

- ❌ Sondaggi di gradimento ("Ti piace il nostro nuovo purpose?")
- ❌ Focus group su messaggi già definiti
- ❌ Consultazione post-decisione ("Vi informiamo che abbiamo deciso X")
- ❌ Engagement unidirezionale (newsletter, post, video senza spazio di risposta)
- ❌ Community di soli fan (nessuno spazio per i critici o gli indifferenti)

La co-creazione Specula richiede che i futuri siano ancora **aperti** quando la community li incontra. Se la decisione è già presa, non è Phase 5 — è comunicazione.

---

## 8. Revisione di questo protocollo

Questo protocollo viene revisionato dopo ogni implementazione completa di Phase 5, con feedback dal facilitatore e dalla community stessa. L'obiettivo è costruire una libreria di casi che migliorino le domande maieutiche e i criteri di rappresentatività.
