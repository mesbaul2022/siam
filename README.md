# Topic 1 — Fresnel Diffraction —  

---

## 1. What are Fresnel half-period zones?

A **Fresnel half-period zone** (usually called a Fresnel zone) is a region on a wavefront such that the path-difference between points in successive zones to a chosen observation point differs by half a wavelength (λ/2). Each zone contributes a spherical-wavelet to the observation point with a phase difference of π relative to the next zone. Constructing the wavefront as concentric rings (zones) centered on the point on the wavefront closest to the observation point divides the total contribution into these alternating phase zones. The idea is used to analyze near-field (Fresnel) diffraction.

---

## 2. Show that the resultant amplitude at a point due to a whole large wavefront is equal to half of the amplitude due to the first half-zone only at that point.

### Qualitative explanation (standard reasoning)

* Let the complex amplitudes contributed at the observation point by successive half-period zones be (a_1, a_2, a_3, \dots). Because each successive zone adds an extra half wavelength of path, the phasors alternate sign: the net phasor sum is
  [
  R = a_1 - a_2 + a_3 - a_4 + \cdots
  ]
* For a large, continuous wavefront the zone areas (and hence the amplitudes (a_n)) vary gradually and decrease slowly as (n) increases. The phasors of successive zones can be drawn head-to-tail and form a spiral (Cornu spiral). As the number of zones → ∞ the spiral approaches a limiting point.
* The limiting resultant (R) is equal to half the first zone's amplitude (a_1/2) (direct geometric result of the phasor construction or Cornu spiral). Intuitively: the alternating series of similar magnitudes converges to about one half of the first term.

### Short mathematical sketch (alternating series idea)

Assume amplitudes change slowly so (a_{n+1}\approx a_n) for early zones. Consider pairing:
[
R = (a_1 - a_2) + (a_3 - a_4) + \cdots
]
Rewriting with a small shift and letting the series extend to many zones, the partial sums converge to a value close to (\tfrac{1}{2}a_1). A clean, rigorous demonstration uses the Fresnel integrals / Cornu spiral: the phasor integral of the continuous wavefront evaluates to a vector of magnitude (\tfrac{1}{2}) the contribution of the first zone.

**Therefore:** For a very large unobstructed wavefront (many zones) the resultant amplitude at the point is approximately ( \boxed{R \approx \dfrac{a_1}{2}} ).

---

## 3. What are half-period zones? Show that amplitude due to a large wave front at a point in front, it is just half that due to the first half period zone acting alone.

 

* Half-period zones are concentric zones on a wavefront such that the path difference from zone to observation point between successive zones is (\lambda/2). Each half-period zone contributes an amount to the resultant amplitude at the observation point with a phase shift of π relative to its neighbor.
* Let the contributions be (a_1, a_2, a_3,\ldots). Because each successive zone introduces a half-wavelength path difference, the phasors alternate in sign and can be represented as:
  [
  R = a_1 - a_2 + a_3 - a_4 + \cdots
  ]
* For a large wavefront, (a_n) vary slowly with (n), so the phasor diagram (Cornu spiral) approaches a limit. That limiting resultant vector equals half the magnitude of the first zone phasor. Formally, using the Fresnel integral evaluation, the amplitude from the entire aperture tends to (\tfrac{1}{2}a_1).

**Hence:** amplitude due to a large wavefront at the point ≈ (\boxed{\dfrac{a_1}{2}}).

---

## 4. Illustrate the amplitude due to a large wavefront at a point in front, where it is just half that due to the first half period zone acting alone.

(See answers 2 and 3 above.) The illustration is the phasor (vector) addition — successive zone phasors make a spiral and the sum ends at a point whose distance from the origin is half the first phasor. This is the classic Fresnel construction (Cornu spiral image).

---

## 5. Explain why departures from rectilinear propagation of light are limited to a small region near the edges of the geometric shadow.

**Explanation:**

* Rectilinear propagation (geometric optics) ignores wave effects. Diffraction (departure from rectilinear paths) is a wave phenomenon and becomes important where the sizes of apertures/obstacles or parts of them are comparable with the wavelength λ or where abrupt phase/ amplitude changes occur — typically at edges.
* Consider an obstacle casting a shadow. Points far inside the geometric shadow are reached only by wavelets that must travel around the obstacle; their amplitudes are strongly reduced and their phases interfere destructively — so the intensity is very small (deep shadow). Points well outside the shadow get contributions from most of the unobstructed wavefront and follow geometric rays.
* The **transition region** (Fresnel region) near the geometric shadow edge is where contributions from parts of the wavefront add with significant phase variations: here diffracted intensity patterns (fringes) appear. The spatial extent of this region scales with (\sqrt{\lambda\cdot\text{distance}}) and is therefore small compared with macroscopic object dimensions if λ is tiny.
* Thus, deviations from straight-line propagation are concentrated near edges (a narrow zone whose width depends on wavelength and geometry).

---

## 6. What is the radius of the first half period zone in a zone plate behaving like a convex lens of focal length 60 cm for light of wavelength 6000 Å?

### Formula

First zone radius (r_1) is (exact)
[
r_1=\sqrt{ \lambda f + \frac{\lambda^2}{4} } \approx \sqrt{\lambda f} \quad\text{(when } f\gg\lambda).
]

### Values and unit conversions

* Wavelength ( \lambda = 6000\ \text{Å} = 6000\times 10^{-10}\ \text{m} = 6.0\times 10^{-7}\ \text{m}.)
* Focal length ( f = 60\ \text{cm} = 0.60\ \text{m}.)

Compute ( \lambda f = 6.0\times 10^{-7}\times 0.60 = 3.6\times 10^{-7}\ \text{m}^2.)

Digit-by-digit square root:

* (3.6\times 10^{-7} = 36\times 10^{-8}.)
* (\sqrt{36\times 10^{-8}} = \sqrt{36}\times\sqrt{10^{-8}} = 6\times 10^{-4}\ \text{m}.)

So
[
\boxed{r_1 = 6.0\times 10^{-4}\ \text{m} = 0.60\ \text{mm}.}
]

---

## 7. Find the radius of the first zone in a zone plate of focal length 20 cm for light of wavelength 5000 Å.

### Values

* (\lambda = 5000\ \text{Å} = 5.0\times 10^{-7}\ \text{m}.)
* (f = 20\ \text{cm} = 0.20\ \text{m}.)

Compute ( \lambda f = 5.0\times 10^{-7}\times 0.20 = 1.0\times 10^{-7}\ \text{m}^2.)

Digit-by-digit square root:

* (1.0\times 10^{-7} = 10^{-7}.)
* (\sqrt{10^{-7}} = 10^{-3.5} \approx 3.16227766\times 10^{-4}\ \text{m}.)

So
[
\boxed{r_1 \approx 3.1623\times 10^{-4}\ \text{m} = 0.3162\ \text{mm}.}
]

---

## 8. What is radius of the first zone in a zone plate of focal length 30 cm for light of wavelength 6000 Å?

### Values

* (\lambda = 6.0\times10^{-7}\ \text{m})
* (f = 30\ \text{cm} = 0.30\ \text{m})

Compute (\lambda f = 6.0\times10^{-7}\times 0.30 = 1.8\times10^{-7}\ \text{m}^2.)

Digit-by-digit square root:

* (1.8\times10^{-7} = 18\times10^{-8}.)
* (\sqrt{18\times10^{-8}} = \sqrt{18}\times 10^{-4} \approx 4.242640687\times10^{-4}\ \text{m}.)

So
[
\boxed{r_1 \approx 4.2426\times 10^{-4}\ \text{m} = 0.4243\ \text{mm}.}
]

---

## 9. Compare the zone plate with convex lens.

### Similarities

* Both can focus light to a point (produce an image) and obey a lens-like imaging relation in the paraxial approximation.
* For the primary focus they both form an image whose position follows the thin-lens formula ( \dfrac{1}{u} + \dfrac{1}{v} = \dfrac{1}{f} ) where (f) is the effective focal length (for the zone plate’s primary order).
* Both can form magnified or reduced images.

### Differences

* **Principle:** A convex lens focuses by refraction (continuous phase delay across aperture); a zone plate focuses by diffraction/interference (alternating zones provide constructive interference at focus).
* **Material:** Lens is a physical refracting medium; zone plate is usually a thin plate with opaque/transmissive rings (or phase rings for higher efficiency).
* **Multiple foci:** A lens has one principal focal point (plus aberrations); a binary amplitude zone plate has several foci (odd orders) — see Q11. A lens does not produce these multiple, discrete foci.
* **Chromatic behavior:** Lenses have chromatic aberration (f varies with wavelength) but zone plates have even stronger wavelength dependence: (f\propto 1/\lambda) for a given geometry, so focal length changes strongly with λ.
* **Efficiency:** A simple amplitude zone plate transmits only part of incident energy into the desired focus (low efficiency) unless it is a phase zone plate which improves efficiency.
* **Fabrication & weight:** Zone plates can be very thin and fabricated lithographically for X-ray / EUV optics where lenses are impractical.
* **Resolution & diffraction limit:** Both are limited by diffraction; but design tradeoffs differ.

---

## 10. Define zone plate. Find out the expression of focal length of zone plate.

### Definition

A **zone plate** is an optical device consisting of concentric rings (zones) alternately transparent and opaque (or with alternating phase shifts) designed so that waves from each transparent zone arrive at a chosen focal point in phase (or with controlled phase differences), producing constructive interference at that point.

### Derivation of focal length expression

Let the radius of the (n)-th zone be (r_n). For the focus at distance (f) along the axis, the path from a ring at radius (r_n) to the focus differs from the path from the center by (n) half-wavelengths:
[
\sqrt{r_n^2 + f^2} - f = n\frac{\lambda}{2}.
]
Square both sides:
[
r_n^2 + f^2 = \left(f + n\frac{\lambda}{2}\right)^2
= f^2 + n\lambda f + \frac{n^2\lambda^2}{4}.
]
So
[
\boxed{r_n^2 = n\lambda f + \frac{n^2\lambda^2}{4}.}
]
For (f \gg n\lambda) the (\frac{n^2\lambda^2}{4}) term is negligible and
[
r_n \approx \sqrt{n\lambda f}.
]
Solving for focal length from (r_n^2 \approx n\lambda f) gives
[
\boxed{f \approx \dfrac{r_n^2}{n\lambda}.}
]
For the first zone ((n=1)):
[
\boxed{f \approx \dfrac{r_1^2}{\lambda}.}
]

---

## 11. Show that a zone plate has multiple foci.

### Reasoning

* A zone plate produces constructive interference at positions where path differences are integer multiples of half-wavelengths. If the plate transmits every alternate zone (or otherwise produces the required phase pattern), constructive interference occurs not only for the primary condition ( \Delta = \tfrac{\lambda}{2}) per zone (giving focal length (f)), but also when the effective phase condition corresponds to additional constructive combinations.
* For the m-th order focus, the condition becomes that successive zones differ in phase by (m\pi) (i.e., an odd multiple of π for amplitude zones), leading to focal lengths
  [
  f_m = \frac{f}{m}
  ]
  for odd integers (m = 1,3,5,\dots) (intensities decrease with increasing (m)). Thus a zone plate gives foci at (f, f/3, f/5,\ldots) (and virtual foci on the opposite side for even/other sign conventions). This is the well-known multiple-focus property of (binary) zone plates.

---

## 12. The diameter of the central zone of a zone plate is 3 mm. If a point source of light of wavelength 6000 Å is placed at a distance of 5 m from it. Calculate the position of the first image.

### Given / converted values

* Diameter of central zone (= 3.0\ \text{mm} \Rightarrow) radius (r_1 = 1.5\ \text{mm} = 1.5\times10^{-3}\ \text{m}.)
* Wavelength (\lambda = 6000\ \text{\AA} = 6.0\times10^{-7}\ \text{m}.)
* Object distance (u = 5.0\ \text{m}.)

### Find the focal length (f) (first order)

Use ( f = \dfrac{r_1^2}{\lambda} ).

Digit-by-digit:

* (r_1^2 = (1.5\times10^{-3})^2 = 1.5^2\times10^{-6} = 2.25\times10^{-6}\ \text{m}^2.)
* Divide: (\dfrac{2.25\times10^{-6}}{6.0\times10^{-7}} = \dfrac{2.25}{6.0}\times 10^{-6 -(-7)} = 0.375\times10^{1} = 3.75\ \text{m}.)

So ( \boxed{f = 3.75\ \text{m}.} )

### Image position (thin-lens formula)

Use the lens equation (valid for zone plate primary focus approximation):
[
\frac{1}{u} + \frac{1}{v} = \frac{1}{f}.
]
So
[
\frac{1}{v} = \frac{1}{f} - \frac{1}{u} = \frac{1}{3.75} - \frac{1}{5.0}.
]
Compute:

* (1/3.75 = 0.2666666667\ \text{m}^{-1}) (exactly (4/15)).
* (1/5.0 = 0.2000000000\ \text{m}^{-1}.)
  Difference:
  [
  \frac{1}{v} = 0.2666666667 - 0.2000000000 = 0.0666666667\ \text{m}^{-1}.
  ]
  Thus
  [
  v = \frac{1}{0.0666666667} = 15.0\ \text{m}.
  ]

**Answer:** The first (primary) image is a real image located at ( \boxed{v = 15.0\ \text{m}\ \text{from the zone plate}} ) on the side opposite the point source.

---



# Topic 3 — Fraunhofer Diffraction — 

---

## 1. What is a plane diffraction grating?

A **plane diffraction grating** is an optical element with a large number of equally spaced parallel slits (or grooves) on a plane surface. When monochromatic light is incident on it, each slit acts as a secondary source and the diffracted waves interfere to produce sharp maxima (spectral lines) at directions given by the grating equation. A plane grating disperses different wavelengths into different angles.

---

## 2. Explain the theory of plane diffraction grating

**Basic idea and derivation (normal incidence):**

* Let the grating have slit spacing (grating constant) (d) (distance between adjacent slits) and be illuminated by monochromatic light of wavelength (\lambda) at normal incidence.
* Light from adjacent slits to a point at angle (\theta) has a path difference (d\sin\theta).
* Constructive interference (principal maxima) occurs when the path difference equals an integer multiple of the wavelength:
  [
  \boxed{d\sin\theta = n\lambda,\qquad n = 0, \pm1, \pm2,\dots}
  ]
  where (n) is the diffraction order.
* For a grating with many slits, maxima are very sharp; the angular dispersion (d\theta/d\lambda) is large and improves spectral resolution. Intensity distribution is governed by interference of many equally phased sources multiplied by the single-slit diffraction envelope (if slits have finite width).

---

## 3. Numerical — single-slit Fraunhofer: find wavelength

**Given:** slit width (a = 0.19\ \text{mm} = 1.9\times10^{-4}\ \text{m}).
Screen (focal plane) is (f = 1.8\ \text{m}) from lens. First minima appear at (y = \pm 5\ \text{mm} = 5.0\times10^{-3}\ \text{m}).

**Theory:** First minima (m = ±1) satisfy
[
a\sin\theta = \lambda.
]
For small angles, (\sin\theta \approx \tan\theta \approx y/f). So
[
\lambda = a\frac{y}{f}.
]

**Compute step-by-step (digit-by-digit arithmetic):**

* Multiply (a) and (y):
  [
  a\cdot y = 1.9\times10^{-4}\times 5.0\times10^{-3} = 9.5\times10^{-7}\ \text{m}^2.
  ]
* Divide by (f):
  [
  \lambda = \frac{9.5\times10^{-7}}{1.8} = 5.277777\ldots\times10^{-7}\ \text{m}.
  ]

So
[
\boxed{\lambda \approx 5.28\times10^{-7}\ \text{m} = 528\ \text{nm}.}
]

---

## 4. Show that with red light the width of the central maximum is more than with violet light

**Single-slit central maximum width:** positions of first minima are at (\sin\theta = \pm\lambda/a). For small angles, lateral half-width on screen (y = f\sin\theta \approx f\lambda/a). Full width of central maximum = distance between first minima on both sides:
[
\text{Width}*{\text{central}} = 2\frac{f\lambda}{a}.
]
Since (\lambda*{\text{red}}>\lambda_{\text{violet}}), the central maximum for red light is broader (larger (\lambda) → larger width). Hence red central maximum is wider than violet.

---

## 5. Fraunhofer diffraction pattern from a narrow slit (parallel beam), and conditions for minima & maxima

**Setup:** A single narrow slit of width (a) is illuminated by a parallel monochromatic beam; the Fraunhofer pattern is observed in the far field (or in the focal plane of a lens).

**Amplitude & intensity:** The amplitude distribution as a function of angle (\theta) is proportional to
[
A(\theta) \propto \frac{\sin\beta}{\beta},\quad\text{where }\beta=\frac{\pi a\sin\theta}{\lambda}.
]
Intensity:
[
\boxed{I(\theta)=I_0\left(\frac{\sin\beta}{\beta}\right)^2.}
]

**Conditions:**

* **Minima:** (\sin\beta=0) for nonzero (\beta) ⇒ (\beta = m\pi) with (m=\pm1,\pm2,\dots). Thus
  [
  \boxed{a\sin\theta = m\lambda\quad(\text{minima at }m=1,2,\dots).}
  ]
* **Maxima:** Nontrivial maxima lie between minima; positions are solutions of
  [
  \frac{d}{d\beta}\left(\frac{\sin\beta}{\beta}\right)=0 \quad\Longrightarrow\quad \tan\beta = \beta,
  ]
  whose first positive solution is (\beta\approx 4.493) (first secondary maximum). The principal (central) maximum is at (\beta=0).

---

## 6. Numerical — slit width (0.2) mm, focal length (20) cm, find distance between first two maxima

**Given:** slit width (a = 0.2\ \text{mm} = 2.0\times10^{-4}\ \text{m}).
Focal length (f = 20\ \text{cm} = 0.20\ \text{m}).
Wavelength (\lambda = 5\times10^{-5}\ \text{cm} = 5\times10^{-7}\ \text{m}).
(“Lens placed very close to slit” ⇒ Fraunhofer pattern in focal plane.)

**Interpretation & approach:** “Distance between the first two maxima” — standard interpretation: distance from central maximum to the first secondary maximum on one side. The central maximum is at (\beta=0); the first secondary maximum occurs at (\beta_1\approx 4.493), where (\beta = \dfrac{\pi a\sin\theta}{\lambda}). For small angles (\sin\theta\approx y/f). So
[
y_1 \approx f\frac{\lambda}{\pi a}\beta_1.
]

**Compute numerically:**

* Compute (\beta_1/\pi = 4.493/3.14159265 \approx 1.4303.)
* Compute (\lambda/a = \dfrac{5.0\times10^{-7}}{2.0\times10^{-4}} = 2.5\times10^{-3}.)
* Multiply: ((\beta_1/\pi)\cdot(\lambda/a) = 1.4303\times 2.5\times10^{-3} = 3.57575\times10^{-3}.)
* Multiply by (f=0.20\ \text{m}):
  [
  y_1 \approx 0.20\times 3.57575\times10^{-3} = 7.1515\times10^{-4}\ \text{m} = 0.715\ \text{mm}.
  ]

**Answer (distance from central maximum to first secondary):**
[
\boxed{y_1 \approx 7.15\times10^{-4}\ \text{m} = 0.715\ \text{mm}.}
]

(If instead the problem meant the spacing between consecutive maxima on the same side, you would compute the second maximum similarly and take the difference — but in common practice the requested distance is central → first secondary.)

---

## 7. Show the intensity of the first secondary maximum ≈ 4.5% of principal maximum

**Intensity formula:** (I(\theta)=I_0(\sin\beta/\beta)^2.) First secondary maximum occurs at (\beta_1) satisfying (\tan\beta_1=\beta_1); numerically (\beta_1\approx 4.493409).

Evaluate
[
\frac{I_{\text{1st sec}}}{I_0}=\left(\frac{\sin\beta_1}{\beta_1}\right)^2.
]

**Compute numerically:**

* (\beta_1\approx 4.493409).
* (\sin\beta_1\approx \sin(4.493409)) and evaluate the ratio:
  [
  \left(\frac{\sin 4.493409}{4.493409}\right)^2 \approx 0.04719\ldots
  ]
  So the first secondary maximum has intensity ≈ (0.0472,I_0), i.e. about (4.72%) of the principal maximum. Rounded commonly in textbooks to about **4.5%**.

Thus
[
\boxed{I_{\text{1st sec}}\approx 0.047,I_0\ (\approx 4.7% \text{ of } I_0).}
]

---

## 8. Deduce missing orders for a double-slit Fraunhofer pattern

**Given:** slit width (a = 0.16\ \text{mm}). Slits are (d = 0.8\ \text{mm}) apart (center-to-center).

**Condition for missing orders:** Interference maxima occur at
[
d\sin\theta = m\lambda \quad(\text{interference}),
]
while single-slit diffraction minima (envelope) occur at
[
a\sin\theta = n\lambda \quad(\text{diffraction minima}).
]
An interference maximum of order (m) will be missing if it coincides with a diffraction minimum: (d\sin\theta = m\lambda) and (a\sin\theta = n\lambda) for some integers (m,n). Eliminating (\sin\theta):
[
\frac{m}{n}=\frac{d}{a}.
]

Compute (d/a = 0.8/0.16 = 5.) So (m = 5n). That means interference orders that are multiples of 5 are missing (they fall at diffraction minima). Thus missing orders are:
[
\boxed{m = 5,,10,,15,\dots}
]
(and negative counterparts on the other side).

---

## 9. Graphical representation of intensity pattern of Fraunhofer single-slit diffraction

**Shape & features:**

* Plot horizontal axis: angle (\theta) or position (y) on the screen; vertical axis: intensity (I(\theta)).
* The central maximum (at (\theta=0)) is the highest and widest; successive maxima (secondary maxima) on both sides are much smaller and decrease rapidly in amplitude.
* Zeros (minima) occur at (\beta=m\pi) ⇒ (a\sin\theta=m\lambda). The envelope of the peaks follows ((\sin\beta/\beta)^2).
* Qualitatively: a tall central hump, then smaller humps symmetrically placed, separated by zeros; the envelope decays ~(1/\beta^2) for large (\beta).

(If drawing: show central peak width (2\lambda f/a), zeros at (m\lambda f/a), and small subsidiary peaks located between zeros, heights ≈ 4.7% (1st), much smaller for further ones.)

---

## 10. Determine the wavelength of a spectral line using a plane transmission grating

**Practical method & formula:**

* Use grating equation: (d\sin\theta = n\lambda), where (d) is grating spacing and (n) is diffraction order.
* If grating has (N) lines per unit length, then (d = 1/N).
* Measure the diffraction angle (\theta_n) for the (n)-th order of the spectral line (using a spectrometer).
* Compute
  [
  \boxed{\lambda = \frac{d\sin\theta_n}{n} = \frac{\sin\theta_n}{nN}.}
  ]
  **Procedure:** Mount the grating, shine the spectral source at normal incidence, measure the angle (\theta) of a chosen order (n), plug in (d) (or (N)) to compute (\lambda). Use several orders and average to reduce experimental error.

---

## 11. Prove that for maximum diffraction angle the number of orders (M) is (M = \dfrac{1}{N\lambda})

**Derivation:**

* Grating constant (d = 1/N) (if (N) is number of lines per unit length).
* Diffraction condition for order (m): (d\sin\theta = m\lambda).
* Maximum possible (\sin\theta) is (1) (grazing); thus highest possible order (M) satisfies
  [
  m_{\max}\lambda \le d \quad\Rightarrow\quad M\le \frac{d}{\lambda}.
  ]
* Substitute (d=1/N):
  [
  M \le \frac{1/N}{\lambda} = \frac{1}{N\lambda}.
  ]
  Hence the maximum possible integer order is
  [
  \boxed{M = \left\lfloor\frac{1}{N\lambda}\right\rfloor,}
  ]
  and for the ideal (non-integer rounding) form one writes (M = \dfrac{1}{N\lambda}) (practically the physically allowed orders are integer values (m = 0,\pm1,\pm2,\dots,\pm\lfloor1/(N\lambda)\rfloor)).

---



# Topic 3 — X-Ray Diffraction (XRD) — 

---

## 1. State Bragg’s law.

**Bragg’s law:**
For X-rays reflected from successive crystal planes separated by distance (d), constructive interference (a diffraction maximum) occurs when the path difference equals an integer multiple of the wavelength:
[
\boxed{n\lambda = 2d\sin\theta}
]
where (n=1,2,3,\ldots) is the order, (\lambda) the X-ray wavelength, and (\theta) the glancing (Bragg) angle measured from the lattice planes.

---

## 2. Discuss diffraction of X-rays & Bragg’s law in crystals.

**Basic idea:**

* A crystal is an ordered 3-D array of atoms; it can be regarded as a set of parallel atomic planes separated by interplanar distance (d).
* When a monochromatic X-ray beam strikes the crystal, X-rays are scattered (weakly) by the atoms in each plane. Waves reflected from different planes may interfere.
* For constructive interference (diffracted beam of appreciable intensity), the extra path travelled by rays reflected from adjacent planes must equal an integer multiple of wavelengths — precisely the Bragg condition (n\lambda=2d\sin\theta).
* Measuring diffraction angles (\theta) for known (\lambda) yields (d) values (and hence crystal structure information); conversely, for known (d) you can determine (\lambda).

**Use in practice:** Bragg’s law is the basis of XRD: indexing peaks (identifying (hkl) planes), measuring lattice parameters, phase identification, strain and crystallite size (via peak broadening), etc.

---

## 3. Numerical — glancing angle (6^\circ), (n=1), (d=2.82\times10^{-8}\ \text{cm}). Find (\lambda).

**Given:** ( \theta = 6.0^\circ,\ n=1,\ d=2.82\times10^{-8}\ \text{cm}.)
Convert (d) to meters:
[
d = 2.82\times10^{-8}\ \text{cm} \times 10^{-2}\ \frac{\text{m}}{\text{cm}} = 2.82\times10^{-10}\ \text{m}.
]

By Bragg (first order),
[
\lambda = \frac{2d\sin\theta}{n} = 2d\sin(6^\circ).
]

Compute:

* (\sin6^\circ \approx 0.104528).
* (\lambda = 2\times 2.82\times10^{-10}\times 0.104528 \approx 5.8954\times10^{-11}\ \text{m}.)

Expressed in common units:
[
\boxed{\lambda \approx 5.90\times10^{-11}\ \text{m} = 0.0590\ \text{nm} = 0.590\ \text{\AA}.}
]

---

## 4 & 5. Explain the reason(s) for using X-rays in XRD analysis (specific reasons).

**Reasons (specific):**

1. **Wavelength comparable to interatomic spacings.** Typical interplanar distances (d) in crystals are on the order of (1)–(4\ \text{\AA}). X-ray wavelengths (≈0.5–2 Å for lab sources) are therefore comparable to (d), satisfying the Bragg condition and producing diffraction.
2. **Penetration & scattering:** X-rays penetrate solids sufficiently and scatter from electron clouds of atoms (elastic scattering), producing measurable diffraction intensities related to atomic positions.
3. **Non-destructive & versatile:** XRD is non-destructive and works for powders, thin films, and single crystals; it yields phase identification, lattice constants, strain, crystal size, and preferred orientation.
4. **High angular resolution:** Small changes in interplanar spacing produce measurable angular shifts, enabling precise lattice parameter measurement.

(These are the specific practical/physical reasons that make X-rays ideal for crystallography.)

---

## 6. Using Scherrer Equation — given (\lambda=1.54\ \text{\AA}), (2\theta_{\max}=46.2^\circ), (2\theta_{\min}=30.0^\circ). Find crystallite size.

**Interpretation & formula:** Scherrer equation:
[
D = \frac{K\lambda}{\beta\cos\theta}
]
where

* (D) is crystallite (coherent diffraction domain) size,
* (K) is shape factor (use (K\approx0.9) unless specified),
* (\lambda) is X-ray wavelength,
* (\beta) is peak broadening (FWHM) in **radians** (commonly taken as the full width in (2\theta) units),
* (\theta) is Bragg angle of the peak (center), i.e. (\theta = \dfrac{2\theta_{\text{center}}}{2} = \theta_{\text{center}}).

**We take** (\beta = 2\theta_{\max}-2\theta_{\min} = 46.2^\circ - 30.0^\circ = 16.2^\circ) (converted to radians), and the peak center (2\theta_c = (46.2+30.0)/2 = 38.1^\circ), so (\theta = 19.05^\circ).

**Conversions:**

* (\lambda = 1.54\ \text{\AA} = 1.54\times10^{-10}\ \text{m}.)
* (\beta = 16.2^\circ = 0.2827433\ \text{rad}.)
* (\cos\theta = \cos(19.05^\circ) \approx 0.9455.)

**Compute:**
[
D = \frac{0.9\times 1.54\times10^{-10}}{0.2827433\times 0.9455}
\approx 5.186\times10^{-10}\ \text{m}.
]

Expressed in nm:
[
\boxed{D \approx 5.19\times10^{-10}\ \text{m} \approx 0.519\ \text{nm} \quad(\approx 5.19\ \text{\AA}).}
]

**Remark:** The Scherrer result depends strongly on how (\beta) is measured (instrumental broadening correction, unit radians, peak shape). A very large (\beta) (16.2°) yields an extremely small apparent crystallite size; in practice one would ensure (\beta) is the intrinsic FWHM (after subtracting instrumental broadening) and typically (\beta) values are small (fractions of a degree).

---

## 7. Crystallite size of ZnO nanoparticles (given (2\Theta=34^\circ), (\lambda=0.154\ \text{nm}), (\text{FWHM}=\beta=0.0051\ \text{rad}))

**Given:** (2\Theta=34^\circ \Rightarrow \theta=17^\circ).
(\lambda = 0.154\ \text{nm} = 1.54\times10^{-10}\ \text{m}.)
(\beta = 0.0051\ \text{rad}). Use (K=0.9).

**Scherrer formula:**
[
D = \frac{K\lambda}{\beta\cos\theta}.
]

Compute:

* (\cos17^\circ \approx 0.9563.)
* Numerator (K\lambda = 0.9\times 1.54\times10^{-10} = 1.386\times10^{-10}\ \text{m}.)
* Denominator (\beta\cos\theta = 0.0051\times 0.9563 \approx 0.004877.)
* So (D \approx 1.386\times10^{-10}/0.004877 \approx 2.842\times10^{-8}\ \text{m}.)

In nanometers:
[
\boxed{D \approx 2.84\times10^{-8}\ \text{m} = 28.4\ \text{nm}.}
]

(So the estimated crystallite size ≈ **28.4 nm**.)

---

## 8. Determine interplanar distance of lattice crystal according to Bragg’s law.

**From Bragg’s law:** For order (n),
[
n\lambda = 2d\sin\theta \quad\Longrightarrow\quad \boxed{d = \frac{n\lambda}{2\sin\theta}.}
]
For the first order ((n=1)):
[
\boxed{d = \frac{\lambda}{2\sin\theta}.}
]

**Note:** For cubic crystals you can also relate (d) to lattice parameter (a) and Miller indices ((hkl)):
[
\boxed{d_{hkl} = \frac{a}{\sqrt{h^2+k^2+l^2}} \quad(\text{simple cubic}).}
]
Combine with Bragg’s law to index peaks and find (a).

---

## 9. Interpret Debye–Scherrer formula in particle-size measurement system.

**Debye–Scherrer (Scherrer) formula:**
[
D = \frac{K\lambda}{\beta\cos\theta}
]
interprets the broadening of XRD peaks as arising from finite crystallite (coherent diffraction domain) size (D). Small crystallites cause peak broadening because a finite number of scattering planes produces a spread of scattering angles.

**Key points & interpretation:**

* **Proportionality:** Peak width (\beta) (FWHM in radians) is inversely proportional to domain size (D). Larger particles → narrower peaks; smaller particles → broader peaks.
* **Constants:** (K) is a shape factor (0.89–1.0 commonly; (K\approx0.9) used for roughly spherical crystallites).
* **Limitations & corrections:**

  * (\beta) must be corrected for instrumental broadening (subtract instrument contribution in quadrature): (\beta_{\text{sample}}^2=\beta_{\text{obs}}^2-\beta_{\text{inst}}^2).
  * Microstrain (lattice distortions) also broadens peaks; Williamson–Hall analysis separates size and strain effects.
  * Scherrer gives average domain size (coherent scattering length), not necessarily particle physical size in presence of agglomeration or polycrystallinity.
  * Valid for small sizes (typically <100 nm) and modest broadening; assumes uniform strain and isotropic domains.

**Conclusion:** Scherrer is a practical, approximate method to estimate nanoscale crystallite size from XRD peak broadening when used carefully with instrument correction and consideration of strain.

---

## 10. Diagram and description of unit-cell planes (001), (100), (101)

**Miller indices recap:** A plane with Miller indices ((hkl)) cuts the crystal axes at (a/h,, b/k,, c/l) (with intercepts ∞ if the index is 0) in the direct lattice. For a cubic cell (edges (a) and orthogonal axes), the interpretation and simple diagrams are:

* **(001) plane:**

  * Miller indices ((0,0,1)). Intercepts: (\infty,\ \infty,\ c/1).
  * It is a plane parallel to the (x)–(y) face, cutting the (z)-axis at (z=c). In a cubic cell this is the top (or bottom) face — i.e. a face perpendicular to the z-axis.
  * ASCII/description: imagine the cube; the (001) plane is the top square face.

* **(100) plane:**

  * Miller indices ((1,0,0)). Intercepts: (a/1,\ \infty,\ \infty).
  * Plane perpendicular to the x-axis, a face of the cube (the face at x = a). In a cube this is a side face.

* **(101) plane:**

  * Miller indices ((1,0,1)). Intercepts: (a/1,\ \infty,\ c/1).
  * This plane cuts the (x)-axis at (x=a), is parallel to the (y)-axis (does not cut it), and cuts the (z)-axis at (z=c). Geometrically it is an oblique plane that passes through the two faces at x=a and z=c and is parallel to y. In a cube of edge (a), the (101) plane passes through the mid-edge corners (it’s a diagonal plane that contains the line connecting (a,0,0) to (0,0,a) and is parallel along y).
  * ASCII sketch (very simple):

```
Cube oriented with axes x (right), y (out), z (up).

(001) : horizontal top face (z = a)
(100) : vertical face at x = a (right face)
(101) : diagonal plane cutting x and z; contains points (a,0,0) and (0,0,a) and is parallel to y
```

# siam
