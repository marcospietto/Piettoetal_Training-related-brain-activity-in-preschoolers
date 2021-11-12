# Piettoetal_Training-related-brain-activity-in-preschoolers
These are the EEG data from Pietto et al (JCE, 2021). This project is part of a larger collaboration between the Unidad de Neurobiología Aplicada (CEMIC - CONICET, Argentina; http://pobrezaydesarrollocognitivo.blogspot.com/) and the Laboratorio de Inteligencia Artificial Aplicada (Instituto de Cs. de la Computación, Fac. de Cs. Exactas y Naturales, UBA - CONICET, Argentina; https://liaa.dc.uba.ar/). Our general goal is to study the influence of adverse environmental conditions on brain function and the effectiveness of cognitive interventions for changing neural activity underliying executive functions's demanding tasks.

In the present study, we examined the impact of two individualized cognitive training interventions on cognitive performance and neural activity in preschoolers from poor homes. Participants were classified based on their basal performance (i.e. high- and low-performers) in an inhibitory control task, and then separated into intervention and control groups within each performance level. The control groups completed three games without cognitive control demands. The intervention groups performed three activities with increased cognitive demands adjusted according to their cognitive baseline performance. Children were trained weekly for 12 weeks and tested before and after the intervention, at kindergarten, using EEG recordings during a Go/NoGo task performance. Training-related changes were observed only for children who participated in the intervention activities. Low-performers exhibited changes in behavior (i.e. post-error slowing) and mid-frontal neural activity (i.e. N2) associated with conflict processing. However, the high-performers group had larger training effects on conflict-related activity (i.e. N2, ERN, theta power).

# How to cite us
#### Please, if you like it / use it cite us:
Pietto, M. L., Giovannetti, F., Segretin, M. S., Rueda, R., Kamienkowski, J. E., & Lipina, S. J. (2021). Conflict-Related Brain Activity after Individualized Cognitive Training in Preschoolers from Poor Homes. Journal of Cognitive Enhancement, 1-34.

# Data
Data is organized in two structures, one (DATA) containing the stimulus and response-locked activity with Event-Related Potentials (ERP) and Event-Related Spectral Perturbation (ERSP) each, and one (INFO) containing the ID of subjects, the ID of the group of each subject, and the segments times of stimulus and response-locked activity.

Name 	Size 	Bytes 	Class 	Description
DATA  1X1   1713152 struct  Stimulus-locked: activity anchored to Go and NoGo stimuli. Response-locked: activity anchored to Correct and Error responses.
DATA.stimulus-locked 1x1 861920  struct  ERP: Event-Related Potential. ERSP: Event-Related Spectral Perturbation (Theta frequency band).
DATA.response-locked 1x1 850880  struct  ERP: Event-Related Potential. ERSP: Event-Related Spectral Perturbation (Theta frequency band).
DATA.stimulus-locked.ERP and .ERSP  1x2 430784  cell  cell n1: pre-intervention session. cell n2: post-intervention session.
DATA.response-locked.ERP and .ERSP  1x2 425264  cell  cell n1: pre-intervention session. cell n2: post-intervention session.
DATA.stimulus_locked.ERP{1}, .ERP{2}, ERSP{1} and ERSP{2} 115x78x3  215280 double  Samples, Subjects, correct trials: 1- Go; 2- NoGo; 3- NoGo minus Go.
DATA.response_locked.ERP{1}, .ERP{2}, ERSP{1} and ERSP{2} 115x77x3  212520 double  Samples, Subjects, responses: 1- Correct Go; 2- Error NoGo; 3- Error minus Correct.

Stimulus-locked data were segmented into epochs of 200 ms before to 800 ms after target onset (in trials associated with correct responses); response-locked data were segmented into epochs of 400 ms before to 600 ms after the press of the button (in trials associated with correct and error responses). Baseline activity was subtracted from each epoch using the average activity in the intervals [−200, 0] ms and [−400, -50] ms for stimulus-locked and response-locked waveforms, respectively.  Stimulus-locked waveforms were re-referenced offline to the algebraic average of P7/P8 channels (the closest electrodes to the right/left mastoids) and response-locked signals were re-referenced to a pseudo-average reference including channels O1, O2, T7, T8, AF3, AF4. Finally, the average activity was calculated over a frontal ROI (F3/F4 electrodes). For further details on data collection and preprocessing please refer to Pietto et al (JCE, 2021).
