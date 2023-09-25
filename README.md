# z boson minimisation
This program checks and filters the data from the file names FILE1 and FILE2 and performs a least
squares fitting on the data to minimise values of z0 mass and z0 width. This occurs twice, once
with the partial width kept constant at the quoted value, and once where it is treated as a
variable and minimised alongside the mass and width. A plot is made of the data and is compared
to the predicted shape. The functions below with "_fpw" in the title have a fixed partial width,
whereas the ones without that in the title have variable partial width.

https://www.desmos.com/calculator/ths4xe1my0 This graph was helpful to me for plotting a).

Following that, the program creates a contour plot of the reduced chi-squared at variable z0 mass
and width. This process is quite computationally intense O(n^3), with a triple nested for loop
running for INTERVALS * INTERVALS * len(data) iterations. This is equally true for INTERVALS_2.

The code then produces a contour plot of the chi-squared zoomed in so that the contour lines
indicate standard deviations away from the minimised value. From this uncertanties on the
values of Z0 mass and Z0 width can be found, which hopefully agree with the ones found through
curve_fit.

The figure is saved to the default directory.

The code is versatile for other data sets, and other decay products, although the
contour plot assumes the width energy is smaller than the mass energy.

Last update 07/12/21
