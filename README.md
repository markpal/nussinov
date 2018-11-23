Compilation:

GCC

gcc main.cpp -o nuss -lgomp -fopenmp -O3 -lm

ICC

icc main.cpp -o nuss -qopenmp -O3

Usage:

./nuss filename [method] [number of threads]

filename - RNA sequence length in FASTA (first line is skipped - header)

method - oryg,pluto,tstile,tilecorr.  Default oryg (original).

number of threads - integer, default maximal number of threads in openmp.

For example:

./nuss sequence/test.txt
./nuss sequence/test.txt tstile 48
