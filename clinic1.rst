==============
 Clinic 1
==============

10th February 2009

Concatenating runs - is it a good idea?
=======================================

   As we're analyzing the data, we've started lumping each condition
   into groups of 2 runs -- i.e. a beginning comprised of runs 1 & 2,
   a middle comprised of runs 3 & 4, and an end comprised of runs 5
   & 6.  In our initial analysis, we'd created separate regressors for
   each of the runs -- i.e. a set of onsets for run 1, a set for run
   2, etc. that led to distinct betas.  It occurred to us that we
   could always create regressors that included onsets for both run 1
   and run 2, since we'd been analyzing them together later on.  We've
   thought about the issues with this approach, but would be grateful
   for your thoughts as well.  The lumped approach, for example, seems
   to allow for more reliable beta estimates, but also (in this
   learning study) for possibly greater sensitivity to linear drifts.

   The second, more specific question related to SPM is the following:
   one clear issue with the above approach is including a constant
   nuisance regressor for each run within the 2-run concatenated
   regressor.  SPM only creates a constant regressor for the lumped
   2-run regressor.  I can create a simple basis for the constant term
   by adding my own nuisance regressor that has, for example, a +1
   corresponding to all onsets for the first run, and a -1 for all
   onsets of the second run.  However, SPM seems to apply a frequency
   filter to these regressors.  In other words, when I look at the
   post-GLM-estimation design matrix, the SPM-produced constant
   regressors remain constant, but the nuisance regressor I've added
   has been temporally filtered.  The second question is whether
   there's a way within SPM to add a nuisance regressor that is not
   pre-processed in the same way as the (for lack of a better term)
   onset regressors.

* What are the benefits of concatenating runs?
* What are the problems?
* What happens to a beta estimate if you concatenate, compared to
  summing over the two sessions?
* Filtering and user-specified regressors


Regressors and amount of activation
===================================

   Can you explain what weighting does in creating contrast vectors?
   For example, if a study has 60 seconds of conditionA, and 20
   seconds of Baseline, the appropriate conditionA>Baseline t-test
   contrast vector would be [1, -3], or [0.3, -1]?  What does this
   ask? Visually, is it amplifying the signal from baseline,
   diminishing the weight of the signal from conditionA? Is this
   sensible to do? Is it better to subsample conditionA so that there
   is equal amount of data with the Baseline?

* Regressors, parameters, and what they mean


Methods of multiple comparison correction
=========================================

   One general category that I think can be somewhat confusing is the
   choice of how to correct a voxel-wise analysis for multiple
   comparisons (the different options available, as well as when one
   would want to use certain approaches over others).  Another topic I
   think would be interesting but may be too specific is analyzing
   data with nonparametric methods (such as with SnPM).

* Multiple comparision correction - see [nichols2003cfe]_



