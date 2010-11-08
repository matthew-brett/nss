==========
 Clinic 3
==========

Guest-starring none other than Jean-Baptiste Poline.

Statistical power - more subjects or more scanning runs?
========================================================

My question involves maximizing statistical power, specifically power to
make group inferences in a design treating subject as a random
variable. Is it best to scan N subjects for T length fMRI scans, or 2*N
subjects for T/2 length scans?

(e.g. better to scan 15 subjects for 90 minutes each or 30 subjects for
45 minutes each)

Are there other factors (effect size, analysis strategy, etc) that might
affect this decision?

Answer from JB among others - all other things being equal, you would
want to collect enough data per subject so that the variance within
subject is roughly equal to the variance between subjects.

Jittering of event onset with respect to TR
===========================================

I've heard some groups say that ER-design necessitates stimuli
time-locked to trs, whereas other groups specifically advise that
stimuli be out of synch with trs to increase sampling variability. Is
there one strategy that's more effective?

Answer: jittering onsets with respect to the TR is common, probably
beneficial, but it probably does not make much difference.

