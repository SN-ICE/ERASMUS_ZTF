# Characterization of type Ia SNe 91bg-like in ZTF

## The goals of this project are presented below:

1) Calculation of the peak magnitude of 3800 supernovae using SNCosmo
2) Observation of the flux in relation to time
3) Comparison between the different models of SNCosmo
4) Construction of the Hubble diagrams
5) Discard some SNe using the 3-sigma clipping method
6) Binning of the clipped residuals, the color and the color excess
7) Analysis of the color and the color excess in every group
8) Analysis of the RMS and the parameters from the Hubble diagrams in every group

## Below I display the process to achieve these:

•	First, to be able to use SNCosmo, you need to convert all the SNooPy files to a format that is compatible with SNCosmo. This can be done using the “To_SNCosmo.ipynb” code.

•	Now you can use SNCosmo to its full extent and derive the parameters you need to make the lightcurve plots, as well as calculate the peak magnitude for every supernova using the code “SN_data.ipynb”. All the parameters are eventually saved in a file in the folder named “lists” depending on the model you used. I also run the code with the same 4 models but fit the redshift (z) instead of using the one I had from the initial data.

•	This way you are able to compare the different models with fitted or fixed redshift, which can easily be done using the code “comparison.ipynb” and the file “models.csv”. After the comparison, I concluded that the best way to continue the project is with the salt3-nir model and using the fixed redshift I had from the initial data, but one can try another model without making big changes to the code. Some diagrams from the comparison are displayed in the folder “comparison_plots” as examples.

•	After that, you are ready to construct the hubble diagrams using the “hubble_diagrams.ipynb” code. The code also makes a plot of the residuals and finds the RMS. After that, with the 3sigma-clipping process, I was able to get rid of the residuals that were far from the mean value and to make the “parameters.txt” file which contains the parameters needed for the construction of the hubble diagram, as well as the RMS. 

•	What was left was to bin the clipped residuals and separate them in groups. Doing this with the ”groups.ipynb” code, I was able to find the parameters and the RMS, and bin the color and the color excess for every group. The results can be seen in the “groups_residuals” folder.

•	Using the clipped residuals, I found the clipped supernovae (see “tab.txt” file) and used it to bin the clipped color and color excess through the “bins_c,x1.ipynb” code, divide them to groups and again find the parameters and the RMS, as well as bin the color and the color excess for every group too. The results can be seen in the “groups_c” folder and the “groups_x1” folder respectively.
