# Fuzzy Hashing

Non-random hash outputs

Uses:
- Digital forensices, CSAM, copyright, duplicate file finder, reverse image search

Traditional hashing uses avolanche effect, **fuzzy does not.**

BlockHash = perceptual fuzzy hashing algorithm

Hamming = get distance b/w strings, like levenshtein but better

One method: Distance vector = N dimensional differences matrix

pHash: downsample, grayscale, run DCT, downsample, DCT, downsample, hash

dHash: reduce size, simplify color, compute difference, hash

wHash: basis and scaling function

Perceptual Hash Lookup = allows you to look up based on just the hash

