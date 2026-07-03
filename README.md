# 🛡️ Black-Box Behavioral Testing of Socio-Cultural Biases in LLMs

Questo repository ospita l'infrastruttura metodologica, i dataset e gli script di valutazione per l'analisi dei bias socio-culturali nei Large Language Models (LLM) open-weights. 

🎓 **Contesto Accademico**  
Questo progetto è stato sviluppato come attività di ricerca e tirocinio per il Corso di Laurea in Informatica presso l'Università degli Studi di Salerno (UNISA).
* **Studente:** Francesco Di Giovanni (Studente al 3° anno di Informatica)
* **Supervisore:** Prof. Fabio Palomba

---

## 🎯 Obiettivi della Ricerca
Le fasi iniziali del progetto definiscono un percorso strutturato per l'identificazione dei bias nell'intelligenza artificiale generativa, l'analisi della loro evoluzione temporale e la comprensione del plateau prestazionale[cite: 2]. Dopo un'indagine preliminare sulle macro-categorie di bias (storico-culturale, di compiacenza, di sensibilità, allucinatorio e di consistenza del contesto), la ricerca si concentra verticalmente sul **Bias socio-culturale**[cite: 2, 3].

L'obiettivo primario è quantificare e studiare il **Performance-Fairness Gap** nel tempo: il delicato compromesso tra la capacità computazionale del modello di risolvere un problema (*Performance*) e la sua imparzialità socio-culturale (*Fairness*)[cite: 3].

## 🔬 Setup Sperimentale
L'infrastruttura richiede una selezione rigorosa dei modelli basata su criteri di: disponibilità *Open-Weights*, presenza di più generazioni temporali, dimensioni equiparabili e diversità geografica/di *alignment*[cite: 4].

* **Taglia scelta:** Modelli tra i **7B e i 12B di parametri**[cite: 5]. Questa fascia dimensionale garantisce una sensibilità linguistica sufficiente per elaborare dilemmi etici e sociali, mantenendo i modelli abbastanza leggeri per l'esecuzione in locale e permettendo di isolare i bias derivanti dai dati di pre-training rispetto alla "forza bruta" dei parametri[cite: 5].
* **Famiglie selezionate:**[cite: 5]
  * 🦙 **LLaMA:** Baseline per misurare il *Western-centric bias*.
  * 💎 **Gemma:** Analizzato per il suo *over-refusal* come meccanismo di marginalizzazione.
  * 🐉 **Qwen:** Inclusione per mappare l'interiorizzazione dei valori del collettivismo asiatico.
  * 🌪️ **Mistral:** Selezionato per il suo *base alignment* più leggero e delegato al *system prompt*.

## 🏗️ Pipeline Metodologica
Il protocollo sperimentale si fonda sulle linee guida dell'Ingegneria del Software Empirica e dell'AI Auditing per garantire riproducibilità e oggettività[cite: 6]:

1. **Definizione dei Failure Modes:** I bias sono operazionalizzati come "firme comportamentali" (*behavioral signatures*) osservabili a priori (es. rifiuto ingiustificato, stereotipizzazione)[cite: 6].
2. **Metriche Quantitative:** Utilizzo di metriche matematiche scalari e distribuzionali per quantificare in modo coerente il *Performance-Fairness Gap* tra architetture differenti[cite: 6].
3. **Costruzione della Codebook:** Stesura di *Annotation Guidelines* formali per superare i limiti dei classificatori automatici e garantire un elevato accordo tra gli annotatori umani[cite: 6].
4. **Costruzione del Dataset:** Ingegnerizzazione di benchmark mirati utilizzando relazioni metamorfiche (alterazione di un singolo costrutto socio-demografico) per favorire l'emersione di bias latenti[cite: 6].
5. **Tassonomia dei prompt:** Classificazione semantica degli input (es. Logica, Etica) per stratificare i risultati ed evitare fattori di confondimento[cite: 6].
6. **Prompt Templating:** Utilizzo di template standardizzati e invariabili per neutralizzare l'instabilità di formato e garantire l'assenza di artefatti valutativi[cite: 6].

## 🚀 Sviluppi e Roadmap
Attualmente, il repository è in fase di implementazione tecnica. I prossimi step operativi includono[cite: 7]:
- [ ] 📝 Costruzione formale dei *persona prompt*
- [ ] 🛠️ Validazione del protocollo sperimentale
- [ ] ⚙️ Sviluppo degli script Python per l'automazione delle inferenze locali
- [ ] 📊 Analisi statistica dei dati generati

## 📚 Bibliografia di Riferimento
La metodologia adottata si fonda sulle più recenti pubblicazioni in conferenze e riviste top-tier (FSE, ACL, EMNLP, ICLR), tra cui lavori su *Metamorphic Testing* per LLM, *Bias Similarity Measurement* e *Prompt Sensitivity*.
