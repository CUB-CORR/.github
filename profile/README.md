<p align="center">
  <img src="https://github.com/user-attachments/assets/55cf5fe2-4b72-452b-8700-03100b948d07" alt="Charité Outcomes Research Repository (CORR)" width="100%">
</p>
<br>

# Charité Outcomes Research Repository (CORR)

**Routine data from the ICUs and operating rooms of Charité in Berlin, Germany, turned into validated computable clinical concepts that are ready for analysis: for retrospective studies, prospective trials, and bedside use.**

CORR is a joint project of the [Institute of Medical Informatics (IMI)](https://medinfo.charite.de/) and the clinical departments of the interdisciplinary Center for Intensive Care Medicine (ZfI) at Charité – Universitätsmedizin Berlin, Germany.

## CORR in 30 seconds

Every research group derives the same variables from raw EHR exports again and again: the PaO₂/FiO₂ ratio, the SOFA score, ventilator-free days.
Each group does it slightly differently. CORR does this work once: consensus-based and clinician-validated *computable clinical concepts* (CCCs) are thoroughly documented and maintained continuously.

- **Shared concept library.** More than 4,000 *computable clinical concepts* (CCCs). Each one is a versioned, documented, and reviewed pipeline that turns raw EHR documentation into analysis-ready and reliable data.
- **eCRF logic extraction.** The CORR package transforms study ideas into study plans and analysis-ready cohorts following eCRF logic.
- **Large ICU and OR cohort.** Data from three hospital sites, ~30 ICUs, and ~80 operating rooms (ORs) usable through a single framework.
- **One layer, three uses.** The same concepts feed retrospective cohort studies, prospective trials embedded in routine care, and live dashboards back on the ward.

## At a glance

- **>250,000** ICU stays
- **>540,000** surgical procedures
- **>4,000** computable clinical concepts
- **3** hospital sites and **~30** ICUs, with ICU and perioperative records linked across the hospital stay
- **25+** studies running on CORR, several of them prospective
- **Data depth:** hospital information system, patient data management system, and high-frequency physiological data from patient monitors and ventilators, as well as free-text sources

## What CORR is used for

**Retrospective studies.** Choose concepts, a time anchor, an observation window, and cleaning and aggregation rules, following an eCRF logic. CORR returns an analysis-ready cohort together with a flow diagram, a "Table 1", and a data quality report. Typical uses are target trial emulations, outcome and quality monitoring, and physiological questions on ventilation, ECMO, haemodynamics, or AKI.

**Prospective and embedded trials.** Because trial variables already exist as concepts, a pragmatic trial can run on routine data without study-specific documentation. The cluster-randomised *sweet-water* trial (glucose vs. saline as the default IV diluent, six hospitals) assembled its Charité dataset entirely from existing CORR concepts.

**Bedside applications.** The same concepts can power dashboards refreshed from the live data stream, such as an extubation dashboard that tracks successful extubation, reintubation, and discharge with an airway in place for each ICU.

**External validation.** Through [reprodICU](https://github.com/CUB-CORR/reprodICU), findings from Charité can be rerun on 7 harmonised public ICU databases from the US and Europe.

## How it works

- **Pseudonymised and governed.** CORR works on pseudonymised data inside the Charité Health Data Platform. Every project passes a structured approval path: study proposal, CORR feasibility check, approval by the clinical directors, and then the Use and Access Committee at Charité.
- **Standards-aware.** Concepts are progressively mapped to FHIR (MII core data set), OMOP, SNOMED CT, LOINC, and ATC. CORR adds what these standards leave open: *how* a clinically meaningful variable is derived from local documentation.
- **Built to travel.** The framework is designed so that other centres can run the same concepts on their own data.

## Repositories

- **[reprodICU](https://github.com/CUB-CORR/reprodICU)**: open pipeline that harmonises public ICU databases (up to ~470,000 admissions from the US and Europe) into one dataset
- **[reprodICU_examples](https://github.com/CUB-CORR/reprodICU_examples)**: case studies showing reprodICU in practice
- **[pycomorb](https://github.com/CUB-CORR/pycomorb)**: comorbidity and frailty scores in Python (Charlson, Elixhauser, Gagne, HFRS)
- **[cohort-builder](https://github.com/CUB-CORR/cohort-builder)**: cohort definition without code, on top of the CORR concepts
- **[corr-vars-widget](https://github.com/CUB-CORR/corr-vars-widget)**: interactive notebook widgets for the CORR variables package

## Data access and collaboration

Researchers at Charité can register a project through the CORR approval process.
External groups are welcome as collaborators on joint projects, for external validation, or to bring the framework to their own centre.

## Team

CORR is built by an interprofessional team of intensivists, anaesthesiologists, nephrologists, pulmonologists, data scientists, computer scientists, and engineers.

**Project leads**<br>
Dario von Wedel · Felix Balzer

**Authors**<br>
Dario von Wedel · Moritz Thiele · Jan-Hendrik Hardenberg · Julian Felber · Pedram Ramezani · Nils Daum · Aline M. Grimm · Sophie Hollerbach · Emil Nolte · Julius V. Kunz · Susanne Philipp · Henriette Hegermann · Noel Kronenberg · Finn S. Fassbender · Elias Grünewald · Claudia Spies · Sascha Treskatsch · Martin Witzenrath · Kai-Uwe Eckardt · Mirja Mittermaier · Felix Balzer

**CORR Group**<br>
Robert Kelm · Amelya Keles · Julius Christian Tramm · Philipp Enghard · Peter Brunecker · Florian Seidel · Camille Guinemer · Michael Krämer · Marie Mandrela · Fabian Prasser · Charlotte Thibeault · Clara Guthmann · Amin Chaoui · Stefan Haufe · Sophie K. Piper · Denys Shay · Eduardo Salgado · Maximilian Markus · Julius Grunow · Marco Schweitzer · Max Kayser · Belén Millet Pascual-Leone · Antonios Margonis · Falk Meyer-Eschenbach · Lina Mosch · Jon Barrenetxea · Patrick Heeren

**Clinical partners (ZfI)**<br>
Department of Anesthesiology and Intensive Care Medicine (Campus Charité Mitte, Campus Virchow Klinikum, Campus Benjamin Franklin) · Department of Nephrology and Medical Intensive Care · Department of Infectious Diseases, Respiratory Medicine and Critical Care

## Contact

- **General enquiries:** [corr@charite.de](mailto:corr@charite.de)
- **Project leads:** [Dario von Wedel](mailto:dario.von-wedel@charite.de) · [Prof. Felix Balzer](mailto:sekretariat-balzer@charite.de)

<br>

<sub>Charité Outcomes Research Repository (CORR) 2026 · Institute of Medical Informatics, Charité – Universitätsmedizin Berlin, Germany</sub><br>
<sub>ICU and perioperative real-world data, computable clinical concepts, embedded pragmatic trials, critical care data science</sub>
