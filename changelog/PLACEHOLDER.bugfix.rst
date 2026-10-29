Fix two bugs with NaN lookup indices:

* `~dkist.wcs.models.Unravel` now returns NaN for a NaN index, or one outside the array, and takes input of any shape, so the inverse of a raveled dataset's world coordinates no longer raises for a time outside its frames or for N-dimensional input.
* A NaN or infinite lookup index of a `~dkist.wcs.models.VaryingCelestialTransform` is now outside the table on every platform; on ARM it took the first row's pointing.
