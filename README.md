# Social Dynamics in Survival Scenarios

## Overview

This project investigates **how social networks, leadership, and interpersonal relationships influence group survival outcomes in extreme environments**. Using *Season 2 of* **The Island with Bear Grylls** as a real-world case study, we apply concepts from **network science, graph theory, and social network analysis** to model how group cohesion evolves under sustained physical and psychological stress.

---

## Research Questions

* How do **social relationships** evolve under extreme survival pressure?
* Can **network metrics** predict leadership emergence and group cohesion?
* What role do **negative interactions and conflict** play in group fragmentation and failure?
* How do differences in social structure affect survival outcomes between groups?

---

## Case Study: *The Island with Bear Grylls*

* 14 British men and 14 British women
* Separated by gender onto two uninhabited Pacific islands
* Required to survive for **6 weeks** with minimal supplies
* Episodes alternate between the men’s and women’s islands

This setup provides a rare natural experiment for observing **real-time social dynamics** under extreme conditions.

---

## Data Collection

### Dialogue Transcription

* Episodes were converted to audio and transcribed using:

  * **OpenAI Whisper** (speech recognition)
  * **Pyannote-Audio** (speaker diarization)
  * **Pyannote-Whisper** (combined pipeline)
* Each episode produced ~20–30 pages of dialogue
* Transcripts were **manually reviewed and corrected** to:

  * Fix speaker attribution
  * Correct transcription errors
  * Identify meaningful interactions

### Interaction Annotation

Each interaction was manually labeled as:

* **Positive** (e.g., teamwork, shared meals, encouragement)
* **Negative** (e.g., arguments, blame, exclusion)
* **Mixed** (both positive and negative effects across participants)
* **Neutral** (informational or emotionally insignificant; mostly excluded)

Interactions were logged with:

* Timestamp
* Initiator and receiver(s)
* Interaction description
* Numerical valence score

---

## Modeling Approach

### Network Construction

* Individuals are modeled as **nodes**
* Interactions form **weighted edges**, representing relationship strength
* Separate graphs were constructed for:

  * Each episode
  * Each island (men vs. women)
  * Cumulative season-wide networks

### Network Metrics Used

* **Degree Centrality** – identifies socially active and influential individuals
* **Betweenness Centrality** – identifies information brokers and emergent leaders
* **Clustering Coefficient** – measures group cohesion and clique formation
* **Network Density** – evaluates overall connectedness and fragmentation

Graphs were generated and analyzed using **NetworkX**, and visualized with **Matplotlib**.

---

## Key Findings

* Individuals with **high degree and betweenness centrality** frequently emerged as leaders
* **Negative relationships** strongly correlated with:

  * Lower clustering coefficients
  * Group fragmentation
  * Increased likelihood of participant departure
* Groups with **higher clustering coefficients** demonstrated:

  * Better communication
  * Faster conflict resolution
  * Stronger survival performance

### Gender Group Comparison

* The men’s island achieved cohesion earlier, with multiple members sharing leadership roles
* The women’s island initially fragmented into subgroups, delaying cohesion and survival efficiency
* Network metrics closely mirrored observed outcomes in the show

---

## Technologies Used

* **Language:** Python
* **Libraries:** NetworkX, NumPy, Pandas, Matplotlib
* **Speech Processing:** OpenAI Whisper, Pyannote-Audio, Pyannote-Whisper
* **Data Tools:** Excel (manual interaction logging)
* **Artifacts:** Research report, presentation slides, interaction spreadsheets

---

## Why This Project Matters

This project demonstrates the ability to:

* Apply **graph theory and network science** to real-world social systems
* Combine **machine learning tools with human-in-the-loop data labeling**
* Analyze leadership, conflict, and cooperation quantitatively
* Translate qualitative human behavior into **formal network models**

The findings have broader implications for understanding **team dynamics, leadership under stress, and group performance** in extreme or high-stakes environments.

---

## Repository Contents

* `Report.docx` – Full research paper
* `Interactions in Media Template.xlsx` – Interaction dataset
* `results (summary).docx` – Key findings summary
* `Presentation.pptx` – Project presentations

---

## Authors

* **Leo Xu**
* Andrew Hall
* Spencer Low
