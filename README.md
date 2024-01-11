# MDS_non-metric

```R
# Load the "ekman" dataset
data(ekman)

# Convert the dataset into a dissimilarity matrix using Euclidean distances
ekman.diss = sim2diss(ekman, 1)

# Perform non-metric MDS analysis in two dimensions
resnm.ekman = smacofSym(ekman.diss, ndim = 2, metric = FALSE)

# Display the MDS analysis results
resnm.ekman

# Generate a summary of the MDS results
summary(resnm.ekman)

# Create a scatter plot to visualize the 2D representation of data points
plot(resnm.ekman, main = 'smacofSym(ekman.diss, ndim = 2, metric = FALSE)')
