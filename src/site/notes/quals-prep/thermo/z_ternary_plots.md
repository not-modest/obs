---
{"dg-publish":true,"permalink":"/quals-prep/thermo/z-ternary-plots/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

A ternary plot is a triangular diagram used to represent mixtures of three components whose fractions sum to a constant (usually 1 or 100%). It is the natural 2D representation of 3‑component composition space.
![Pasted image 20260103162255.png|700](/img/user/quals-prep/src/Pasted%20image%2020260103162255.png)

---

## 1. Composition constraint and coordinates

Let the three components be A, B, and C, with composition variables:

- Mole fractions: $x_A, x_B, x_C$, or  
- Mass fractions: $w_A, w_B, w_C$, or  
- Volume fractions: $\phi_A, \phi_B, \phi_C$

All of these obey the same constraint:
$$
x_A + x_B + x_C = 1
$$

Because of this single constraint, there are only two independent degrees of freedom. The set of all possible compositions forms an equilateral triangle (a 2‑simplex) in 2D.

A ternary plot is that triangle, where:

- Vertex A: $x_A = 1, x_B = 0, x_C = 0$  
- Vertex B: $x_A = 0, x_B = 1, x_C = 0$  
- Vertex C: $x_A = 0, x_B = 0, x_C = 1$

Any interior point represents a mixture with $0 < x_i < 1$ and $x_A + x_B + x_C = 1$.

---

## 2. Geometry: barycentric (trilinear) coordinates

Mathematically, a point $P$ in the ternary diagram is described by barycentric coordinates:
$$
P = x_A A + x_B B + x_C C
$$
with:
$$
x_A + x_B + x_C = 1, \quad x_i \ge 0
$$

Key geometric facts:

- The perpendicular distance from a point to side BC is proportional to $x_A$.  
- The distance to side CA is proportional to $x_B$.  
- The distance to side AB is proportional to $x_C$.

Thus, each component fraction is encoded as distance to the opposite side. “Reading” a ternary plot is essentially reading these distances with the help of grid lines.

If the triangle is equilateral with height $H$, then, in normalized form:
$$
x_A = \frac{d_A}{H}, \quad
x_B = \frac{d_B}{H}, \quad
x_C = \frac{d_C}{H}
$$
where $d_A, d_B, d_C$ are the perpendicular distances from the point to the sides opposite A, B, and C, respectively, and $d_A + d_B + d_C = H$.

---

## 3. Converting between Cartesian and ternary coordinates

Take an equilateral triangle with vertices at:
$$
A = (0, 0), \quad
B = (1, 0), \quad
C = \left(\frac{1}{2}, \frac{\sqrt{3}}{2}\right)
$$

Given barycentric coordinates $(x_A, x_B, x_C)$ with $x_A + x_B + x_C = 1$, the Cartesian coordinates $(X, Y)$ of the corresponding point are:
$$
X = x_A X_A + x_B X_B + x_C X_C
= x_B + \frac{1}{2} x_C
$$
$$
Y = x_A Y_A + x_B Y_B + x_C Y_C
= \frac{\sqrt{3}}{2} x_C
$$

Given $(X, Y)$ inside the triangle, the inverse:

1. First get $x_C$ from the vertical coordinate:
   $$
   x_C = \frac{2Y}{\sqrt{3}}
   $$
2. Then use the horizontal coordinate:
   $$
   X = x_B + \frac{1}{2} x_C
   \Rightarrow
   x_B = X - \frac{1}{2} x_C
   $$
3. Finally:
   $$
   x_A = 1 - x_B - x_C
   $$

This gives a concrete mapping between composition triples and points in the 2D diagram.

---

## 4. Phase behavior on ternary diagrams

For a ternary system at fixed temperature and pressure, a ternary phase diagram overlays phase regions on the composition triangle.

Common structures:

- Single‑phase region: compositions where the mixture is homogeneous (e.g., one liquid phase).
- Two‑phase region: area where the mixture splits into two coexisting phases with compositions given by endpoints of tie lines.
- Three‑phase region: sometimes present, represented by a small triangle connecting three coexisting compositions.

If a mixture splits into two phases $\alpha$ and $\beta$ with compositions:
$$
\mathbf{x}^{(\alpha)} = (x_A^{(\alpha)}, x_B^{(\alpha)}, x_C^{(\alpha)}),
\quad
\mathbf{x}^{(\beta)} = (x_A^{(\beta)}, x_B^{(\beta)}, x_C^{(\beta)})
$$
and phase fraction of $\alpha$ is $f_\alpha$, then the overall composition $\mathbf{z}$ obeys a lever rule:
$$
\mathbf{z} = f_\alpha \mathbf{x}^{(\alpha)} + (1 - f_\alpha)\,\mathbf{x}^{(\beta)}
$$
This appears geometrically as the overall point lying on the straight line segment between the two phase points in the triangle.

---

## 5. Uses in chemical engineering

Typical ChemE uses:

- Liquid–liquid extraction: solute–solvent–carrier diagrams to design extraction stages, operating lines, and to apply the lever rule geometrically.
- Crystallization / solubility: representing solute–coformer–solvent systems; identifying regions where solid phases appear.
- Surfactant/oil/water systems: mapping microemulsion and phase behavior (Winsor regions).
- Compositional data more generally: any 3‑component normalized data set can be visualized as points in a ternary triangle.

Conceptually, a ternary plot is just the 2D geometric representation of all triples $(x_A, x_B, x_C)$ that satisfy the mass‑fraction constraint:
$$
x_A + x_B + x_C = 1, \quad 0 \le x_i \le 1
$$
with triangle geometry providing a convenient way to visualize composition and phase behavior.
