# Project-Coswara-Analysis
Just a walkthrough of the research paper on coswara 2020 by IISC Bengaluru

# Paper link : https://arxiv.org/pdf/2005.10548.pdf

### Coswara - A Database of Breathing, Cough, and Voice Sounds for COVID-19 Diagnosis

### Abstract

The COVID-19 pandemic presents global challenges transcending boundaries of country, race, religion, and economy. The current gold standard method for COVID-19 detection is the
reverse transcription polymerase chain reaction (RT-PCR) testing. However, this method is expensive, time-consuming, and violates social distancing. Also, as the pandemic is expected to stay for a while, there is a need for an alternate diagnosis tool which overcomes these limitations, and is deployable at a large scale. The prominent symptoms of COVID-19 include cough and breathing difficulties. We foresee that respiratory sounds, when analyzed using machine learning techniques, can provide
useful insights, enabling the design of a diagnostic tool. Towards this, the paper presents an early effort in creating (and analyzing) a database, called Coswara, of respiratory sounds, namely, cough, breath, and voice. The sound samples are collected via worldwide crowdsourcing using a website application. The curated dataset is released as open access. 

As the pandemic is evolving, the data collection and analysis is a work in progress. We believe that insights from analysis of Coswara can be effective in enabling sound based technology solutions for point-of-care diagnosis of respiratory infection, and in the near future this can help to diagnose COVID-19.

## Index Terms: COVID-19, Cough, Breath, Voice, Random Forest

#### 2.1. Cough Sounds
Cough is a powerful reflex mechanism for the clearance of the central airways (trachea and the main stem bronchi) of inhaled and secreted material. Typically, it follows a well defined pattern, with an initial inspiration, glottal closure and development of high thoracic pressure, followed by an explosive expiratory flow as the glottis opens with continued expiratory effort [4].

The reflex is initiated by cough receptors within the central airways that are sensitive to both mechanical and chemical stimuli. Sound is generated during cough by air turbulence, vibration of the tissue, and movement of fluid through the airways [5]. This turbulence generates sound with a broadband “noisy” character, whose frequency content depends on the velocity, density of the gas, and dimensions of the airways from source till the mouth. A cough sound is usually composed of three temporal phases: explosive, intermediate, and voicing phase.
Fig. 2(b) shows a wide-band spectrogram of a sequence of three heavy cough sound signals. Each cough lasts close to 300 ms, and the spectrum exhibits broad spectral spread over 500 Hz, 1.5 kHz, and 3.8 kHz. Interestingly, over one hundred pathological conditions are associated with cough [6]. The acoustic features of a cough sound depend on the air flow velocity as well as the dimensions of vocal tract and airways [4]. This makes it possible to detect cough sounds [7] in audio recordings. As the physical structure of the respiratory system gets altered with respiratory infections, it is even possible to classify pathological condition based on a cough sound. Pertussis is a contagious respiratory disease which mainly affects young children and can be fatal if left untreated. Pramono et al. [8] presented an algorithm for automated diagnosis of pertussis using audio signals by analyzing cough and whoop sounds. Several other recent studies have attempted to identify chronic obstructive pulmonary disease (COPD) (a disease caused primarily due to smoking) [9], and tuberculosis (an infectious disease usually caused by mycobacterium tuberculosis (MTB) bacteria that affects the lungs) [10]. In addition, for respiratory disorders like asthma and pneumonia, algorithms based on cough sounds recorded using a smartphone provides a high level of accuracy [11]. For COVID-19 detection and diagnostics, the research initiatives from University of Cambridge [12], Carnegie Mellon University [13], Wadhwani AI institute [14] and a project from EPFL [15] have already been launched. Also, a recent work by Imran et al. [16] suggests a good accuracy for cough based detection of COVID-19 using a preliminary investigation with a small number of subjects.

#### 2.2. Breath sounds
Breathing difficulty is another common symptom for COVID19. This is often exhibited as a shortness of breath. The early
work by Anderson et al., [17] reported that the spectrogram of breath sounds captured by a smartphone shows distinct patterns for asthmatic conditions compared to healthy individuals. For the diagnostics of COVID-19, the use of breathe sounds is also being attempted by a research group at New York University [18]. Fig. 2(c) shows the wide-band spectrograms of inhaling and exhaling cycles while breathing.

#### 2.3. Voice sounds
The studies show that lung diseases have distinct bio-markers in the speech breathing cycles [19]. The study reported in [20] showed that the phonation threshold pressure, defined as the minimal lung pressure required to initiate and sustain vocal fold oscillation, is correlated with vocal fatigue. The impact of laryngeal dysfunction in breathing patterns of read speech was analyzed in [21]. Fig. 2(a) depicts the spectrogram of a sustained phonation of /ey/ vowel (as in made). In contrast to cough and breath sound sample, there is a clear voicing seen as harmonics and localized concentration of energy at regions defined by formants.
