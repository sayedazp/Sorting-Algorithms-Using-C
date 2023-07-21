<img src = "../assets/Selection-sort.png" style = "background-color: white;"></img>

in selection sort we are dealing more with indicies not the elements it self at every iteration we need to figure out what element should be in that position, the image above shows the case of selecting the 0-index element of a list then we need to figure out what is the smallest element of it using two pointers one iterates over the list and the other points the smalles element and after iteration finishes a swap operation is done 

- note that we perform one swap per iteration which is more efficient approach that previous methods

- note that every iteration generates the smallest element of the searched range so we can use selection sort approach to figure out the k smallest elements of an array of length n by performing k selection sort internal operations and not the full sorting algorithm!