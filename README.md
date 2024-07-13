# SE-model-XENONnT-code
This repository the code I came up with for my Bachelor thesis involving the modelling of the delayed single and few electron emissions in XENONnT. Note: it includes only the finalized versions necessary to completely recreate the results from my report. 

peak_selection.ipynb includes some based plots created by STRAX, the processing framework for XENONnT. These plots were used to select the peaks for study (see All plots/peak_selection.png)

The folder Fit Results includes the results from iminuits extended maximum likelihood estimator, saved as NumPy arrays so they can easily be read in. There are two files per fit: the parameter values themselves and the resulting covariance matrix (suffix "_cov.npy"). The prefix of each file name gives:
1. expon_fit = The exponential function fit to study the varying livetime windows of each S2 peak
2. const_fit = A uniform continuous density function fit to all of the selected SE signals
3. power_law = A power law probability density function fit to the time differences between each SE and the preceeding S2
4. broken_power_law = A continuous broken power law density function fit to the time differences between each SE and the preceeding S2
5. cumulative_power_law = The cumulative power law function as described by Eq. 4 and 5. in the report. Fit to 2000 S2 peaks and the SEs associated with it

"notebook_containing_fits_3hr_run.ipynb" is the main notebook used for the results. It shows these fits and explores some various properties of the SE signals used to develop these models
