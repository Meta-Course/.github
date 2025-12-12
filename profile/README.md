# MetaClass

[![Live Demo (JS)](https://img.shields.io/badge/Live_Demo-Visit-brightgreen)](https://Meta-Course.github.io)
[![Report Bug](https://img.shields.io/badge/Report-Bug-red)](https://github.com/Meta-Course/Meta-Course.github.io/issues)

<div align="center">
  <img 
    style="width: 900px;"
    src="https://github.com/Meta-Course/.github/blob/main/Landing.jpg">
</div>

**MetaClass** is an automated academic management platform designed to align unstructured lecture data with structured course syllabi.

The system utilizes multimodal AI (Google Gemini) to ingest lecture content, audio, transcripts, and whiteboard imagery, and dynamically map it to specific examination scopes defined in a syllabus. Unlike static note-taking tools, MetaClass maintains a reactive state: updates to the syllabus or re-processing of lecture data trigger a global re-classification of all stored content.

### Core Functionality

**Syllabus-Driven Content Classification**
The system parses natural language or PDF syllabi to generate a structured course schema. All subsequent data entries (lectures) are analyzed against this schema to determine their relevance to specific assessment milestones (e.g., Midterm vs. Final).

**Multimodal Data Ingestion**
MetaClass aggregates data from multiple sources into a unified "Session Object":
* **Audio:** Speech-to-text transcription and summarization.
* **Visual:** OCR and context analysis of whiteboard photos.
* **Text:** Direct extraction of deadlines, formulas, and key terms.

**Dynamic Scope Analysis**
The platform employs a reactive architecture. If the syllabus definition changes (e.g., a topic moves from Midterm to Final), the system re-evaluates previously stored sessions and re-assigns them to the correct logical bucket without manual intervention.

### Feature Set

* **Timeline Visualization:** A chronological view of course progression mapped to exam milestones.
* **Topic Heatmaps:** Frequency analysis of lecture topics against syllabus requirements to estimate exam probability.
* **Contextual Asset Management:** Automatic grouping of flashcards, quizzes, and notes into relevant exam folders.
* **Task Prioritization:** Heuristic extraction of deliverables, categorized by urgency (Exercises, Assignments, Exam Warnings).
* **Accessibility:** Automated translation pipelines and high-contrast rendering for generated content.

### Technical Stack

* **AI Model:** Google Gemini (Multimodal capabilities for Text, Audio, and Vision).
* **Data Processing:** Custom state machine for syllabus-lecture alignment.
