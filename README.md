# M-Small curves in isogeny graphs
Tools for computing supersingular isogeny graphs and identifying M-small points. Used to produce Figure 1 of "Supersingular curves with small non-integer endomorphisms" by Jonathan Love and Dan Boneh https://msp.org/obs/2020/4-1/p02.xhtml

### Step 1
Open Magma in the current director and run 

```
load "M-SmallIsogGraph.magma";
p := 20011;
isogeny_degrees := [2,3];
ExportToMathematica(p, isogeny_degrees);
```

Note: this code may take several minutes to run; while it is running, the terminal will print the total number of vertices found in the graph so far (for p=20011 there will be 871 vertices, but even when all vertices are found, it will take a while to generate all the edges). You can skip Step 1 by using the existing files "SupsingMinnorms.txt" and "SupsingEdges.txt" which were produced by the code above. 

You can also use different values of p and isogeny_degrees to genereate different graphs. To identify the "M-small islands" as in the associated paper, the sequence isogeny_degrees should contain all primes up to 4/pi * sqrt(M).

### Step 2
Ensure that the generated text files "SupsingMinnorms.txt" and "SupsingEdges.txt" are in the same directory as the Mathematica notebook "graph-plotting.nb."

### Step 3
Open "graph-plotting.nb" and evaluate the first cell to generate the graph. You may need to tinker with the settings to make improve the appearance. Change the first line (M=12) to different values of M to highlight more or fewer cells.
