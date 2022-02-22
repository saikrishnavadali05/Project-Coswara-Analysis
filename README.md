# Project-Coswara-Analysis
1. Just a walkthrough of the research paper on coswara 2020 by IISC Bengaluru.
2. This paper falls under the category of Audio and Speech Processing using Machine Learning.
3. Arxiv Link : https://arxiv.org/abs/2005.10548


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

#### 3. Coswara Overview
Coswara [22] is an attempt to provide a simple and cost effective tool for diagnosis of COVID-19 using breath, cough and speech sounds. As most of the major symptoms of the disease include respiratory problems, the proposed project aims to detect and quantify the bio-markers of the disease in the acoustics of the these sounds. The project has three stages, depicted in Fig. 3. Below we briefly describe each stage. 

#### 3.1. Data collection 
The goal is to create a dataset of sound samples from healthy and unhealthy individuals, including those identified as COVID-19. For sound data, we focus on nine different categories, namely, breathing (two kinds; shallow and deep), cough (two kinds; shallow and heavy), sustained vowel phonation (three kinds; /ey/ as in made, /i/ as in beet, /u:/ as in cool), and one to twenty digit counting (two kinds; normal and fast paced). We also collect some metadata information, namely, age, gender, location (country, state/province), current health status (healthy / exposed / cured / infected) and the presence of co-morbidity (pre-existing medical conditions). No personally identifiable information is collected. The data is also anonymized during storage.

#### 3.2. Modeling
The collected data will be analysed using signal processing and machine learning techniques. The goal is to build mathematical models aiding identification of bio-markers from sound samples. This stage is a work-in-progress while we create the dataset. We have also initiated regular release of the curated dataset as open access via GitHub platform.

#### 3.3. Diagnosis tool
We aim to release the diagnosis tool as a web/mobile application. The application prompts the user to record voice samples, similar to the dataset collection stage, and provides a score indicating the probability of COVID-19 infection. The final deployment of tool is subject to validation with clinical findings, and authorization /approval from competent healthcare authorities. Given the highly simplistic and cost effective nature of the tool, we hypothesize that, even a partial success for the tool would enable a massive deployment as a first line diagnostic tool to pre-screen the infection.

#### 4. Dataset Description
The project is currently on going. The collection, release, and analysis of the dataset are in progress. Below we provide a description of the most recent release of the dataset.

###### 4.1. Data collection methodology
The data collection strategy focused on reaching out to the human population across the globe. For this, we created a website application providing a simple and interactive user interface. A user could open the application in a web browser (laptop or mobile phone), provide metadata, and proceed to recording the sound samples using the device microphone. The average interaction time with the application is 5 − 7 mins. The user was prompted to use personal device and wipe off the device with a sanitizer before and after recording, and keep the device 10 cm from the mouth during recording.

###### 4.2. Metadata description
The currently released dataset (as of 07 August 2020) has a participant count of 941. Fig. 4 shows the distribution of the participants across gender, age, country (grouped into India and outside), Indian states, and health status (grouped into healthy and unhealthy). Each participant provides 9 audio files, one for each of the sound category.

###### 4.3. Annotation
The audio samples are recorded at a sampling frequency of 48 kHz. All sound files were manually curated. A web interface was designed allowing the annotator (human) to listen to every sound file and answer some questions (a screenshot of the interface is shown in Fig. 5). These questions helped verify the category label, and the quality of the audio file. The annotator was also provide an option to provide any additional comments for each audio file. Fig. 4(f) depicts the quality count of the recordings, pooling all the nine sound categories. Majority of the audio files were rated as clean. While we had 13 annotators, each file was listened by only one annotator. In total, the dataset has 6507 clean, 1117 noisy, and remaining highly degraded audio files corresponding to respiratory sound samples from 941 participants.

###### 4.4. Acoustic Properties
The 9 sound categories (or classes) are chosen such that physical state of the respiratory system is well captured just by using the sound samples. We tested the complementarity across these sound categories by building a multi-class classifier trained and tested on acoustic features extracted from the different sound
samples. The goal was to build a 9-class (corresponding to the 9 sound categories) classifier and evaluate the confusion matrix.
The clean audio recordings were pooled and grouped by 9 sound categories. A set of different short-time (500 msec, with hop of 100 msec) temporal and spectral acoustic features were extracted from the audio files. These included spectral contrast (7-D), MFCCs (13-D), spectral roll-off (1-D), spectral centroid (1-D), mean square energy (1-D), polynomial fit to the spectrum (2-D), zero-crossing rate (1-D), spectral bandwidth (1-D), and spectral flatness (1−D). After concatenation each 500 msec segment of audio was represented by a 28-D feature. A random forest classifier (see [?], built with default parameters and 30 trees) was trained on a 70 − 30% train-test split for classifying every 500 msec segment into one of the 9 sound categories. The accuracy on test data was 66.74%. Fig. 6 shows resulting confusion matrix for the test data. The test data had an equal share from every class. It is interesting to note that the vowels are less confused, and the digit counting samples are more confused between themselves. This is also the case for
cough samples and breathing samples.

##### 5. Conclusion
We have described our efforts towards a sound based diagnostic tool for COVID-19. The tool, named Coswara, built upon prior studies that have shown good accuracy for detecting other resTRUE CLASS
PREDICTED CLASS
Figure 6: Confusion matrix (on test data) obtained on classifying 9 categories of sounds using a random forest classifier. piratory disorders like asthma, pertussis, tuberculosis and pneumonia. We highlight the rationale for choosing different stimuli in the Coswara database. The progress in data collection in terms of meta data statistics are described. We also highlight the complimentary nature of the stimuli chosen. The next phase in the diagnostic tool development will attempt the use of machine learning algorithms to classify different health conditions and try to identify sound based bio-markers for Covid-19.

##### 6. Acknowledgements
We thank Anand Mohan for his enormous help in web design and data collection efforts, which allowed the recording of data from general public. We also thank Chandrika Thunga, Sonali Singh, Sakya Basak, Venkat Krishnamohan, Jaswanth Reddy, Ananya Muguli, Anirudh Sreeram and Anagha Rajeev for their contribution in annotating the dataset.

###### 7. References
[1] “Naming the coronavirus disease (COVID-19) and the virus
that causes it,” World Health Organization. https://www.who.
int/emergencies/diseases/novel-coronavirus-2019/technicalguidance/naming-the-coronavirus-disease-(covid-2019)-and-thevirus-that-causes-it, 2020.
[2] C. Menni, A. M. Valdes, M. B. Freidin, C. H. Sudre, L. H.
Nguyen, D. A. Drew, S. Ganesh, T. Varsavsky, M. J. Cardoso,
J. S. El-Sayed Moustafa, A. Visconti, P. Hysi, R. C. E.
Bowyer, M. Mangino, M. Falchi, J. Wolf, S. Ourselin,
A. T. Chan, C. J. Steves, and T. D. Spector, “Realtime tracking of self-reported symptoms to predict potential
COVID-19,” Nature Medicine, 2020. [Online]. Available:
https://doi.org/10.1038/s41591-020-0916-2
[3] J. E. Huber and E. T. Stathopoulos, Speech Breathing Across the
Life Span and in Disease. John Wiley & Sons, Ltd, 2015, ch. 2,
pp. 11–33.
[4] W. Thorpe, M. Kurver, G. King, and C. Salome, “Acoustic analysis of cough,” in The Seventh Australian and New Zealand Intelligent Information Systems Conference. IEEE, 2001, pp. 391–394.
[5] M. Polverino, F. Polverino, M. Fasolino, F. Ando, A. Alfieri, and `
F. De Blasio, “Anatomy and neuro-pathophysiology of the cough
reflex arc,” Multidisciplinary respiratory medicine, vol. 7, no. 1,
p. 5, 2012.
[6] G. A. Fontana and J. Widdicombe, “What is cough and what
should be measured?” Pulmonary pharmacology & therapeutics,
vol. 20, no. 4, pp. 307–312, 2007.
[7] C. Pham, “Mobicough: Real-time cough detection and monitoring using low-cost mobile devices,” in Intelligent Information and
Database Systems, N. T. Nguyen, B. Trawinski, H. Fujita, and T.- ´
P. Hong, Eds. Berlin, Heidelberg: Springer Berlin Heidelberg,
2016, pp. 300–309.
[8] R. X. A. Pramono, S. A. Imtiaz, and E. Rodriguez-Villegas, “A
cough-based algorithm for automatic diagnosis of pertussis,” PloS
one, vol. 11, no. 9, 2016.
[9] A. Windmon, M. Minakshi, P. Bharti, S. Chellappan, M. Johansson, B. A. Jenkins, and P. R. Athilingam, “Tussiswatch: A smartphone system to identify cough episodes as early symptoms of
chronic obstructive pulmonary disease and congestive heart failure,” IEEE journal of biomedical and health informatics, vol. 23,
no. 4, pp. 1566–1573, 2018.
[10] G. Botha, G. Theron, R. Warren, M. Klopper, K. Dheda,
P. Van Helden, and T. Niesler, “Detection of tuberculosis by automatic cough sound analysis,” Physiological measurement, vol. 39,
no. 4, p. 045005, 2018.
[11] P. Porter, U. Abeyratne, V. Swarnkar, J. Tan, T.-w. Ng, J. M. Brisbane, D. Speldewinde, J. Choveaux, R. Sharan, K. Kosasih et al.,
“A prospective multicentre study testing the diagnostic accuracy
of an automated cough sound centred analytic system for the identification of common respiratory disorders in children,” Respiratory research, vol. 20, no. 1, p. 81, 2019.
[12] “Cambridge university, UK - COVID-19 sounds app,” Weblink
https://covid-19-sounds.org/en/, last accessed May 8, 2020.
[13] “CMU sounds for covid project,” Weblink
https://node.dev.cvd.lti.cmu.edu/, last accessed May 8, 2020.
[14] “Cough against covid - wadhwani AI institute,” Weblink
https://coughagainstcovid.org/, 2020.
[15] “Cough for COVID-19 detection,” Weblink
https://coughvid.epfl.ch/, last accessed May 8, 2020.
[16] A. Imran, I. Posokhova, H. N. Qureshi, U. Masood, S. Riaz,
K. Ali, C. N. John, and M. Nabeel, “AI4COVID-19: AI enabled
preliminary diagnosis for COVID-19 from cough samples via an
app,” arXiv preprint arXiv:2004.01275, 2020.
[17] K. Anderson, Y. Qiu, A. R. Whittaker, and M. Lucas, “Breath
sounds, asthma, and the mobile phone,” The Lancet, vol. 358, no.
9290, pp. 1343–1344, 2001.
[18] “Breathing sounds for COVID-19,” Weblink
https://breatheforscience.com/, last accessed May 8, 2020.
[19] L. Lee, R. G. Loudon, B. H. Jacobson, and R. Stuebing, “Speech
breathing in patients with lung disease,” American Review of Respiratory Disease, vol. 147, pp. 1199–1199, 1993.
[20] A. Chang and M. P. Karnell, “Perceived phonatory effort and
phonation threshold pressure across a prolonged voice loading
task: a study of vocal fatigue,” Journal of Voice, vol. 18, no. 4,
pp. 454–466, 2004.
[21] C. M. Sapienza, E. T. Stathopoulos, and W. Brown Jr, “Speech
breathing during reading in women with vocal nodules,” Journal
of Voice, vol. 11, no. 2, pp. 195–201, 1997.
[22] “Indian institute of science - Coswara: A sound based diagnostic tool for covid19,” Weblink https://coswara.iisc.ac.in/, last accessed May 8, 20
