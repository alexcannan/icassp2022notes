# Advanced Graph Signal Processing

## Blurb

There will be 3 parts separated by 2 breaks: Part 1: Dealing with high dimensional structures, Part 2: Generalizing the graph signal domain, Part 3: Working with uncertainty.

Graphs and networks are ubiquitous in science and technology, including imagine processing, research in Internet of Things and analysis of social network data. Since its emergence, graph signal processing (GSP) has become an important tool in such areas. The basic tools of GSP include graph Fourier transform, shift invariant filter bank, as well as graph neural network. Though a successful theory in many respects, GSP faces challenges in many circumstances and requires regular updates with new ideas. In the tutorial, we discuss a few recent developments in advanced graph signal processing, focusing on high dimensional signals and structures.

## Notes

### Dealing with high dimensional structures

- Hilbert spaces for vertices and edges
- $F$-transform and $TV$ (time-vertex) transform for spectral analysis
- Example: Infection/Information propagation over a network
    - SI, SIR, SIRI models (susceptible/infected, susceptible/infected/recovered, etc)
    - Signal at each node $v = f(v)$ step function unbandlimited in time domain
- Filters and shift invariance
    - shift invariance vs weak shift invariance (pretty much bilateral vs unilateral)
        - shift invariance implies weak shift invariance
        - if eigenspace dimensions are all 1, weak shift invariance implies shift invariance
        - if $L$ is self-adjoint, they're linked
    - Convolution filter is shift-invariant
- Asynchronous joint sampling
    - Joint sampling over vertex and Hilbert space domains
    - Synchronous sampling is not always easy: sensor networks, social networks, etc


### Working with uncertainty

- Background: graph binarization and symmetrization
    - binarization parameter $\tau$ needs to be set... they're proposing we don't need to do this
- Disribution of shifts on a graph
    - $V$: finite discrete set, elemnts of a network
    - Suppose $X$ is a set of graph shift operators. $(X,F,\mu_x)$ is a probability space with pdf $\mu_x = p dx$
- Fourier Transform
    - Graph signals: $\R^n = L^2 (V)$
    - The Fourier transform: $\phi_X : L^2 (V) \rarr L^2 (X \times [n])$
    - Left inverse of $\phi_X$:
        - $\psi_X : L^2 (X \times [n]) \rarr L^2(V)$
    - ...
    - Basic Properties
        - $\phi_X$ and $\psi_X$ are well-defined
        - (Left inverse) $\phi_X o \psi_X$
        - ...
    - This guy is fast
- r-level hypersurface helps distinguish between a random signal and a noisy signal
- convolution filter
    - Bi-polynomial filter (Fiberwise convolution)
    - $\Gamma \star, \Gamma \in L^2(X \times [n])$
    - For each $0 \le i \le n-1$ there is apolynomial $a_i(t)$ such that $\Gamma_{x_t}\star = \Sigma_{0 \le i \le n-1}a_i(t)x_t^i$

### Generalizing the graph signal domain

- I got hungry
