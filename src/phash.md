# Perceptual Hashing Algorithms

Similiar hashes produced for images that are perceptually similiar

Different classes:
- Difference hashing
- Average hashing

## Diff Hashing
1. Convert to grayscale
2. Resize (helps with skewing)
3. Compute diff b/w adjacent pixels
4. Build the hash

Hamming Distance
- Commonly used metric to determine similiarty b/w two hashes

Improved tatoo - 
two roses & two butterflies. different style, color, and detail

Incorporated tatoo - 
Old tatoo is just a butterfly, new one has a bunch of stuff, but the original is still there

Proposed solution:

Difference hashing algo based on one used on image hashing search engines

Terms to know:
- Template Image:
- Query Image:


1. Iteratively uses hash of template and hash of slices of the query
2. Get hamming distance of two hashes
3. Update list of slices iwth Hamming distances less than threshold
4. Sort the resulting list and display top k results

Results:

Imporved tatoos:
- better results when template image size is closer to size of image

Incorporated Tatoo:
- Smaller hammming distance for top matches

Future work:
- Not move pixel by pixel in main image
- Remove duplicates in results
- Feature extraction + hashing

Public database that doesn't use real images of tatoos would be good
