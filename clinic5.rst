Clinic 5
========

Questions in no order:

    I'm running a training study in which I'm interested in seeing how a change
    in a behavioral measure is correlated with changes in task-related BOLD (and
    DTI, cortical thickness, resting BOLD, etc.). I'm not sure how to best
    approach this analysis. The only GLM I've tried so far is a paired t-test,
    and it's not clear to me how to add a regressor to this GLM that represents
    a change between sessions. I've also thought about computing change maps at
    the single subject level, and correlating these changes with the behavioral
    change.

and

    how to effectively look for spikes using tsdiffana.  In particular, I'd like to know:

    a. Should we be using realigned images or raw data, and does it matter
    whether we've done slice timing correction already

    b. The biggest variations I get are from the eyes, and this skews the y-axis
    tremendously.  Is there a way to easily mask out the eyes?
    
    c. If you get a sudden head jerk and the subject moves back into their
    original position, as indicated by a large vertical pattern of X's and
    verified by looking at the raw images and/or realignment parameters, what do
    you do with your data? In AFNI, you can censor specific volumes, and all
    packages allow you to add motion parameters into your GLM. However, couldn't
    their movement screw up the rigid-body realignment, and if so, what do you
    do to preserve the integrity of your remaining time series.
    
    d. The requisite annoying question: how much is too much variance?
