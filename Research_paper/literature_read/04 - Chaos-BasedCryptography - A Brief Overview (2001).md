By Ljupčo Kocarev



although this
paper raises more questions than pro-
vides answers, it nevertheless contains
seeds for future work.



chaotic systems. They
are characterized by sensitive depen-
dence on initial conditions, similarity
to random behavior, and continuous broad-band power spectrum.

The possibility
for self-synchronization of chaotic os-
cillations [1] has sparked an avalanche
of works on application of chaos in
cryptography




Block ciphers transform a rela-
tively short string (typically 64 or 128
bits) to a string of the same length un-
der control of a secret key. A block-
encryption algorithm is usually written
in the form of a mapping x n + 1 =
E(xn, z), n = 0, …, k – 1, where the
plaintext x0, the cryptogram xk and the
secret key z are sequences of letters in
finite alphabets. The advantage of
block ciphers is that they form a
flexible tool that can be used in cryp-
tography: they can be used to construct
other primitives.



A pseudo-random number genera-
tor is a deterministic method, usually
described with a mapping, to produce
from a small set of “random” numbers,
called the seed, a larger set of random-
looking numbers called pseudo-ran-
dom numbers.


block-encryption algorithms can be re-
written as discrete-time dynamical sys-
tems, x n + 1 = F(x n) where the initial
condition x0 is plain-text to be en-
crypted, and the final state x k is a
ciphertext, then it is the property of the
map being chaotic that implies
“spreading out of the influence of a
single plaintext digit over many
ciphertext digits”. To ensure a compli-
cated structure of trajectories of the
dynamical system proposed for an en-
cryption algorithm, we postulate that,
except being chaotic, the system
should be mixing (more precisely K-
mixing). Moreover, to ensure that the
parameters of the system can be used as
encryption keys, we postulate that the
system has robust chaos, that is, the sys-
tem is chaotic for a large set of param-
eters.


The mixing prop-
erty of chaotic maps is closely related
to the property of diffusion in encryp-
tion transformations (algorithms)




Actually, a chaotic system
does not generate information, that is,
its evolution is completely determined
by its initial state. A chaotic system
merely converts the information about
its initial state into a form which is vis-
ible to the measuring system. Every
letter in the coarse-grained trajectory,
which is a sequence of letters, brings
an additional amount of information
about the initial state.



The word random in deterministic
dynamical systems is linked to incom-
pressibility of information: a trajectory
of the system is termed random when
the shortest program that generates it
has (essentially) the same size as the
trajectory itself. The trajectory of a
point x is called random if its algorith-
mic complexity is positive. The fol-
lowing theorem is of essential signifi-
cance in this case [15]: For chaotic
systems the trajectories of almost all
state points x ∈ X are random and their
algorithmic complexity is equal to the
Kolmogorov-Sinai entropy hKS. As a
disturbing consequence, no finite com-
puter program can produce or predict
a chaotic trajectory, or in the language
of Joseph Ford [16], for any additional
bit of the initial state, a computer pro-
gram can output only one additional bit
about the chaotic trajectory.



What is the source
of the unpredictability and information
generation of a chaotic behavior? The
finite precision of any real measuring
system and the sensitive dependence
of a chaotic evolution to a change in
initial states combine to an inability for
long-term prediction of chaotic behav-
ior.


Chaoticity of the behavior im-
plies random trajectories that are not
computable by any finite computer
program.


The central question in cryptogra-
phy is security. The basic properties
characterizing a secure object are “ran-
domness-increasing” and “computa-tionally unpredictable”.



A pseudo-random bit (or
number) generator is a deterministic
method (usually defined as a mapping
G : M1 → M2, where Mi are finite sets)
to produce from a small set of random
bits (called the seed) a larger set of ran-
dom-looking bits (called pseudo-ran-
dom bits). The notion of randomness-
increasing is impossible in classical
information theory because any deter-
ministic mapping G applied to a dis-
crete probability distribution P never
increases entropy, i.e., H(G(P)) ≤ H(P).

a pseudo-random number genera-
tor is polynomial-time unpredictable if
and only if for every finite initial seg-
ment of a sequence that has been pro-
duced by such a generator, but with
any element deleted from that seg-
ment,



If a deterministic function is
unpredictable, then it is difficult to
prove anything about it, in particular,
it is difficult to prove that is unpredict-
able. Most of the results about
unpredictability and cryptographic se-
curity follow from certain assumptions
concerning the intractability of certain
number-theoretical problems by proba-
bilistic polynomial-time procedures. For
example, the statement that the x2 mod N
generator is unpredictable is proven un-
der the so called quadratic residuacity
assumption