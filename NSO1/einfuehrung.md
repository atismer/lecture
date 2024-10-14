<style>

#left {
  left:-8.33%;
  text-align: left;
  float: left;
  width:50%;
  z-index:-10;
}

#right {
  left:31.25%;
  top: 75px;
  float: right;
  text-align: right;
  z-index:-10;
  width:50%;
}
#fs-size {
  font-size:2px;
}

</style>
## Einführung


### Organisation

<div id="left">

- Vorlesung
  - [Alexander Tismer](https://www.ihs.uni-stuttgart.de/institut/team/Tismer/)
  <!-- .element: target="_blank" -->
- Übung
  - [Marco Zorn](https://www.ihs.uni-stuttgart.de/institut/team/Zorn/)
  <!-- .element: target="_blank" -->
- Sprechstunde 
  - Termine nach Vereinbarung
- Prüfung mündlich 40 Minuten
  - Termine nach Vereinbarung

</div>
<div id="right">
  <img
    src="assets/la-grid-flow.png"
    width="50%"
  />
</div>


### Zeitplan

<div id="left">
  
| Thema                   |       |
|------------------------:|:-----:|
| Einführung              | 1     |
| Grundgleichungen        | 2     |
| Ortsdiskretisierung FDM | 3/4   |
| Turbulenz               | 5/6   |
| Zeitdiskretisierung FDM | 7     |
| FVM                     | 8/9   |
| Turbomaschinen          | 10    |
| Geometrie               | 11    |
| Vernetzung              | 12    |
| Optimierung             | 13/14 |

</div>
<div id="right">

| Thema                      |       |
|---------------------------:|:-----:|
| Ortsdiskretisierung (H)    | 1     |
| Zeitdiskretisierung (H)    | 2     |
| Einführung (CFX)           | 3     |
| Backward-Facing-Step (CFX) | 4     |
| Rechnerübungen             | 5/6   |
| Simulation Turbine (CFX)   | 7     |
| Rechnerübungen             | 8/9   |
| Vernetzung (H)             | 10    |
| Optimierung                | 11/12 |

</div>
<p class="r-fit-text">
10 Vorlesungen in 14 x 90 Minuten und 9 Übungen in 12 x 90 Minuten<br>
1 x Institutsbesichtigung und 2 x Offene Sprechstunde
</p>


### Literatur

+ **Ferziger, J. H.; Peric, M.**; "Numerische Strömungsmechanik"; 
  Springer-Verlag, 2008
+ **Laurien, E.; Örtel, H.**; "Numerische Strömungsmechanik"; 
  Vieweg-Verlag, 2010
+ **Pope, S. B.**; "Turbulent Flows"; Cambridge Univ. Pr., 2006
+ **Moukalled, F.; Mangani, L.; Darwish, M.**;
  "The Finite Volume Method in Computational Fluid Dynamics"; Springer, 2016
+ **Weicker, K.**; "Evolutionäre Algorithmen"; Springer Vieweg, 2015


### Hydraulische Maschine - Auslegung

<div class="tworl">
<div>

- Bestehende Anlage
- Saugrohr fix (Änderung sehr teuer)
- Kontour von Nabe und Kranz fix

</div>
<div>

**Ziel:** 
Möglichst hoher Wirkungsgrad unter Einhaltung der Auslegungsdaten 

</div>
</div>
<video
  data-autoplay
  data-src="assets/IHSnew_HLRS_reduced.mp4"
  loop="loop"
  width="600"
></video>

<div class="ref" style="font-size: 60%;">

[1] Junginger, B.; Investigation of the Influences of Gaps at the Runner 
Blade for an Axial Turbine Using Hybrid Turbulence Models; Bundesprojekt
[axialgap](https://www.gauss-centre.eu/results/computational-and-scientific-engineering/investigation-of-the-influences-of-gaps-at-the-runner-blade-for-an-axial-turbine-using-hybrid-turbulence-models); 
2016

</div>


### Hydraulische Maschine - Simulation und Eigenschaften

<div class="r-stack">
  <img src="assets/le-la-sa_0.png"/>
  <img
    class="fragment fade-in"
    data-fragment-index="1"
    src="assets/le-la-sa_1.png"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="2"
    src="assets/le-la-sa_2.png"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="3"
    src="assets/le-la-sa_3.png"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="4"
    src="assets/le-la-sa_4.png"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="5"
    src="assets/le-la-sa_5.png"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="6"
    src="assets/le-la-sa_6.png"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="7"
    src="assets/le-la-sa_77.png"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="8"
    src="assets/le-la-sa_7.png"
  />
 
</div>

- Inkompressible Wasserströmung mit kinematischer Viskosität $\nu = 10^{-6}$
- Rohrturbine mit z.B. $D = 4m$ Durchmesser und einer Zuströmgeschwindigkeit von 
  $v=1\frac{m}{s}$ und damit hohen $Re$-Zahlen bzw. turbulenter Strömung
<!-- .element: class="fragment" data-fragment-index="4" -->
- Steigender Druckgradient
<!-- .element: class="fragment" data-fragment-index="5" -->
- Vernetzung des Strömungsgebiets
<!-- .element: class="fragment" data-fragment-index="6" -->
- Stehende und rotierende Gebiete müssen berechnet und gekoppelt werden
<!-- .element: class="fragment" data-fragment-index="7" -->


### Hydraulische Maschine - Geometrische Beschreibung

<div class="r-stack">
  <img 
    src="assets/para_anim0000.png"
    width="60%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="1"
    src="assets/para_anim0001.png"
    width="60%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="2"
    src="assets/para_anim0002.png"
    width="60%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="3"
    src="assets/para_anim0003.png"
    width="60%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="4"
    src="assets/para_anim0004.png"
    width="60%"
  />
</div>

- Auslegung der Maschine auf Blattschnitten 
- Definition von Freiheitsgraden zur Veränderung der Geometrie
- Erzeugung der dreidimensionalen Geometrie durch Verbinden von Kurven 
- Verwendung von nicht-uniformen, rationalen B-Splines (NURBS)


### Grundgleichungen

Beschreibung von Strömungen durch Navier-Stokes-Gleichungen:
<div class="r-stack">

`$$
\begin{aligned}
  \frac{\partial{}}{\partial{t}} \underline{u} + 
  \underline{u} \cdot \left( \nabla \cdot \underline{u} \right)
  & =
  \nu \nabla \cdot \left( \nabla \cdot \underline{u} \right) -
  \frac{1}{\rho} \nabla p
  \\
  \nabla \cdot \underline{u} 
  & = 
  0
\end{aligned}
$$`
<!-- .element: class="fragment fade-in-then-out" data-fragment-index="2" -->
`$$
\begin{aligned}
  \textcolor{blue}{\frac{\partial{}}{\partial{t}} \underline{u}} + 
  \textcolor{orange}{\underline{u} \cdot \left( \nabla \cdot \underline{u} \right)}
  & =
  \textcolor{magenta}{\nu \nabla \cdot \left( \nabla \cdot \underline{u} \right)} -
  \textcolor{green}{\frac{1}{\rho} \nabla p}
  \\
  \nabla \cdot \underline{u} 
  & = 
  0
\end{aligned}
$$`
<!-- .element: class="fragment fade-in" data-fragment-index="3" -->

</div>

- Unbekannte $\phi$ bzw. $\underline{u}$ und $\underline{p}$ sind 
  kontinuierliche Felder (Kontinuumsmechanik)
<!-- .element: class="fragment fade-in" data-fragment-index="4" -->
- Numerik löst partielle Differentialgleichungen an diskreten Stellen (Gitter)
<!-- .element: class="fragment fade-in" data-fragment-index="5" -->

<div class="r-stack">
  <img 
    src="assets/fvm0000.png"
    width="70%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="1"
    src="assets/fvm0001.png"
    width="70%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="2"
    src="assets/fvm0002.png"
    width="70%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="3"
    src="assets/fvm0003.png"
    width="70%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="4"
    src="assets/fvm0004.png"
    width="70%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="5"
    src="assets/fvm0005.png"
    width="70%"
  />
</div>


### Finite-Differenzen-Methode

Eindimensionales Konvektions-Diffusions-Problem
`$
u\pp{\phi}{x} = \Gamma \pp{}{x}\pp{\phi}{x}
$` 
mit $u,\Gamma=\mathrm{const}$

<div class="r-stack">

`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
  \hide{
    \rightarrow u \dd{\phi}{x}
    \rightarrow \at{u \dd{\phi}{x}}{k}
    \rightarrow u \fd{\phi}{k+1}{k-1}{2 \delta x}
  }
\\
\Gamma \pp{}{x}\pp{\phi}{x}
  &
  \hide{
    \rightarrow  \Gamma \dd{(\dd{\phi}{x})}{x}
    \rightarrow  \at{\Gamma \dd{(\dd{\phi}{x})}{x}}{k}
    \rightarrow  \Gamma \fd{ \at{\dd{\phi}{x}}{} }{ k+1 }{ k }{ \delta x }
    \rightarrow
      \Gamma 
      \frac
        {\fd{\phi}{k+1}{k}{\delta x} - \fd{\phi}{k}{k-1}{\delta x}}
        {\delta x}
  }
  \\
  &
  \hide{
    \rightarrow \Gamma \ffd{\phi}{k+1}{k}{k-1}{\delta x^2}
  }
\end{aligned}}$`
<!-- .element: class="fragment fade-in-then-out" data-fragment-index="0" -->
`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
    \rightarrow u \dd{\phi}{x}
  \hide{
    \rightarrow \at{u \dd{\phi}{x}}{k}
    \rightarrow u \fd{\phi}{k+1}{k-1}{2 \delta x}
  }
\\
\Gamma \pp{}{x}\pp{\phi}{x}
  &
    \rightarrow  \Gamma \dd{(\dd{\phi}{x})}{x}
  \hide{
    \rightarrow  \at{\Gamma \dd{(\dd{\phi}{x})}{x}}{k}
    \rightarrow  \Gamma \fd{ \at{\dd{\phi}{x}}{} }{ k+1 }{ k }{ \delta x }
    \rightarrow
      \Gamma 
      \frac
        {\fd{\phi}{k+1}{k}{\delta x} - \fd{\phi}{k}{k-1}{\delta x}}
        {\delta x}
  }
  \\
  &
  \hide{
    \rightarrow \Gamma \ffd{\phi}{k+1}{k}{k-1}{\delta x^2}
  }
\end{aligned}}$`
<!-- .element: class="fragment fade-in-then-out" data-fragment-index="1" -->
`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
    \rightarrow u \dd{\phi}{x}
    \rightarrow \at{u \dd{\phi}{x}}{k}
  \hide{
    \rightarrow u \fd{\phi}{k+1}{k-1}{2 \delta x}
  }
\\
\Gamma \pp{}{x}\pp{\phi}{x}
  &
    \rightarrow  \Gamma \dd{(\dd{\phi}{x})}{x}
    \rightarrow  \at{\Gamma \dd{(\dd{\phi}{x})}{x}}{k}
  \hide{
    \rightarrow  \Gamma \fd{ \at{\dd{\phi}{x}}{} }{ k+1 }{ k }{ \delta x }
    \rightarrow
      \Gamma 
      \frac
        {\fd{\phi}{k+1}{k}{\delta x} - \fd{\phi}{k}{k-1}{\delta x}}
        {\delta x}
  }
  \\
  &
  \hide{
    \rightarrow \Gamma \ffd{\phi}{k+1}{k}{k-1}{\delta x^2}
  }
\end{aligned}}$`
<!-- .element: class="fragment fade-in-then-out" data-fragment-index="2" -->
`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
    \rightarrow u \dd{\phi}{x}
    \rightarrow \at{u \dd{\phi}{x}}{k}
    \rightarrow u \fd{\phi}{k+1}{k-1}{2 \delta x}
\\
\Gamma \pp{}{x}\pp{\phi}{x}
  &
    \rightarrow  \Gamma \dd{(\dd{\phi}{x})}{x}
    \rightarrow  \at{\Gamma \dd{(\dd{\phi}{x})}{x}}{k}
  \hide{
    \rightarrow  \Gamma \fd{ \at{\dd{\phi}{x}}{} }{ k+1 }{ k }{ \delta x }
    \rightarrow
      \Gamma 
      \frac
        {\fd{\phi}{k+1}{k}{\delta x} - \fd{\phi}{k}{k-1}{\delta x}}
        {\delta x}
  }
  \\
  &
  \hide{
    \rightarrow \Gamma \ffd{\phi}{k+1}{k}{k-1}{\delta x^2}
  }
\end{aligned}}$`
<!-- .element: class="fragment fade-in-then-out" data-fragment-index="3" -->
`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
    \rightarrow u \dd{\phi}{x}
    \rightarrow \at{u \dd{\phi}{x}}{k}
    \rightarrow u \fd{\phi}{k+1}{k-1}{2 \delta x}
\\
\Gamma \pp{}{x}\pp{\phi}{x}
  &
    \rightarrow  \Gamma \dd{(\dd{\phi}{x})}{x}
    \rightarrow  \at{\Gamma \dd{(\dd{\phi}{x})}{x}}{k}
    \rightarrow  \Gamma \fd{ \at{\dd{\phi}{x}}{} }{ k+1 }{ k }{ \delta x }
    \rightarrow
      \Gamma 
      \frac
        {\fd{\phi}{k+1}{k}{\delta x} - \fd{\phi}{k}{k-1}{\delta x}}
        {\delta x}
  \\
  &
    \rightarrow \Gamma \ffd{\phi}{k+1}{k}{k-1}{\delta x^2}
\end{aligned}}$`
<!-- .element: class="fragment fade-in" data-fragment-index="4" -->

</div>

<div class="r-stack">
  <p>
  Differential
  </p>
  <!-- .element: class="fragment fade-in-then-out" data-fragment-index="0" -->
  <p>
  Differential $\rightarrow$ Differenzen
  </p>
  <!-- .element: class="fragment fade-in-then-out" data-fragment-index="1" -->
  <p>
  Differential $\rightarrow$ Differenzen
  </p>
  <!-- .element: class="fragment fade-in-then-out" data-fragment-index="2" -->
  <p>
  Differential $\rightarrow$ Differenzen $\rightarrow$ lineare Approximation
  </p>
  <!-- .element: class="fragment fade-in-then-out" data-fragment-index="3" -->
  <p>
  Differential $\rightarrow$ Differenzen $\rightarrow$ lineare Approximation
  </p>
  <!-- .element: class="fragment fade-in" data-fragment-index="4" -->
</div>

<div class="r-stack">
  <img 
    src="assets/fdm-fvm0000.png"
    width="40%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="2"
    src="assets/fdm-fvm0002.png"
    width="40%"
  />
</div>

Koeffizienten
`$
\left(
-\frac{u}{2 \delta x}-\frac{\Gamma}{\delta x^2}
\right) \phi_{k-1}
+\left(
\frac{2\Gamma}{\delta x^2}
\right) \phi_{k}
+\left(
\frac{u}{2 \delta x}-\frac{\Gamma}{\delta x^2}
\right) \phi_{k+1} = 0
$`
<!-- .element: class="fragment fade-in" data-fragment-index="5" -->


### Finite-Volumen-Methode

Eindimensionales Konvektions-Diffusions-Problem
`$
u\pp{\phi}{x} = \Gamma \pp{}{x}\pp{\phi}{x}
$` 
mit $u,\Gamma=\mathrm{const}$

<div class="r-stack">

`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
  \hide{
    \rightarrow 
      \intV{u\pp{\phi}{x}}
    \rightarrow 
      \intS{u \phi}
    \rightarrow
      - \at{u \phi}{k}
      + \at{u \phi}{k+1} 
    \rightarrow
      - u \frac{\phi_{m-1} + \phi_{m}}{2}
      + u \frac{\phi_m + \phi_{m+1}}{2}
  }
  \\
  &
  \hide{
    \rightarrow
    u\fd{\phi}{m+1}{m-1}{2}
  }
  \\
\Gamma \pp{}{x} \pp{\phi}{x}
  &
  \hide{
    \rightarrow 
      \intV{\Gamma \pp{}{x}\pp{\phi}{x}}
    \rightarrow 
      \intS{\Gamma \pp{\phi}{x}}
    \rightarrow
      - \at{\Gamma\pp{ \phi}{x}}{k}
      + \at{\Gamma \pp{\phi}{x}}{k+1} 
  }
  \\
  &
  \hide{
    \rightarrow
      - \Gamma \fd{\phi}{m}{m-1}{\delta x}
      + \Gamma \fd{\phi}{m+1}{m}{\delta x}
    \rightarrow
    \Gamma \ffd{\phi}{m+1}{m}{m-1}{\delta x}
  }
\end{aligned}}$`
<!-- .element: class="fragment fade-in-then-out" data-fragment-index="0" -->
`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
    \rightarrow 
      \intV{u\pp{\phi}{x}}
    \rightarrow 
      \intS{u \phi}
  \hide{
    \rightarrow
      - \at{u \phi}{k}
      + \at{u \phi}{k+1} 
    \rightarrow
      - u \frac{\phi_{m-1} + \phi_{m}}{2}
      + u \frac{\phi_m + \phi_{m+1}}{2}
  }
  \\
  &
  \hide{
    \rightarrow
    u\fd{\phi}{m+1}{m-1}{2}
  }
  \\
\Gamma \pp{}{x} \pp{\phi}{x}
  &
    \rightarrow 
      \intV{\Gamma \pp{}{x}\pp{\phi}{x}}
    \rightarrow 
      \intS{\Gamma \pp{\phi}{x}}
  \hide{
    \rightarrow
      - \at{\Gamma\pp{ \phi}{x}}{k}
      + \at{\Gamma \pp{\phi}{x}}{k+1} 
  }
  \\
  &
  \hide{
    \rightarrow
      - \Gamma \fd{\phi}{m}{m-1}{\delta x}
      + \Gamma \fd{\phi}{m+1}{m}{\delta x}
    \rightarrow
    \Gamma \ffd{\phi}{m+1}{m}{m-1}{\delta x}
  }
\end{aligned}}$`
<!-- .element: class="fragment fade-in-then-out" data-fragment-index="1" -->
`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
    \rightarrow 
      \intV{u\pp{\phi}{x}}
    \rightarrow 
      \intS{u \phi}
    \rightarrow
      - \at{u \phi}{k}
      + \at{u \phi}{k+1} 
  \hide{
    \rightarrow
      - u \frac{\phi_{m-1} + \phi_{m}}{2}
      + u \frac{\phi_m + \phi_{m+1}}{2}
  }
  \\
  &
  \hide{
    \rightarrow
    u\fd{\phi}{m+1}{m-1}{2}
  }
  \\
\Gamma \pp{}{x} \pp{\phi}{x}
  &
    \rightarrow 
      \intV{\Gamma \pp{}{x}\pp{\phi}{x}}
    \rightarrow 
      \intS{\Gamma \pp{\phi}{x}}
    \rightarrow
      - \at{\Gamma\pp{ \phi}{x}}{k}
      + \at{\Gamma \pp{\phi}{x}}{k+1} 
  \\
  &
  \hide{
    \rightarrow
      - \Gamma \fd{\phi}{m}{m-1}{\delta x}
      + \Gamma \fd{\phi}{m+1}{m}{\delta x}
    \rightarrow
    \Gamma \ffd{\phi}{m+1}{m}{m-1}{\delta x}
  }
\end{aligned}}$`
<!-- .element: class="fragment fade-in-then-out" data-fragment-index="2" -->
`${\scriptsize\begin{aligned}
u \pp{\phi}{x}
  &
    \rightarrow 
      \intV{u\pp{\phi}{x}}
    \rightarrow 
      \intS{u \phi}
    \rightarrow
      - \at{u \phi}{k}
      + \at{u \phi}{k+1} 
    \rightarrow
      - u \frac{\phi_{m-1} + \phi_{m}}{2}
      + u \frac{\phi_m + \phi_{m+1}}{2}
  \\
  &
    \rightarrow
    u\fd{\phi}{m+1}{m-1}{2}
  \\
\Gamma \pp{}{x} \pp{\phi}{x}
  &
    \rightarrow 
      \intV{\Gamma \pp{}{x}\pp{\phi}{x}}
    \rightarrow 
      \intS{\Gamma \pp{\phi}{x}}
    \rightarrow
      - \at{\Gamma\pp{ \phi}{x}}{k}
      + \at{\Gamma \pp{\phi}{x}}{k+1} 
  \\
  &
    \rightarrow
      - \Gamma \fd{\phi}{m}{m-1}{\delta x}
      + \Gamma \fd{\phi}{m+1}{m}{\delta x}
    \rightarrow
    \Gamma \ffd{\phi}{m+1}{m}{m-1}{\delta x}
\end{aligned}}$`
<!-- .element: class="fragment fade-in" data-fragment-index="3" -->

</div>

<div class="r-stack">
  <p>
  Differential
  </p>
  <!-- .element: class="fragment fade-in-then-out" data-fragment-index="0" -->
  <p>
  Differential $\rightarrow$ Integral mit Divergenztheorem
  </p>
  <!-- .element: class="fragment fade-in-then-out" data-fragment-index="1" -->
  <p>
  Differential $\rightarrow$ Integral mit Divergenztheorem
  </p>
  <!-- .element: class="fragment fade-in-then-out" data-fragment-index="2" -->
  <p>
  Differential $\rightarrow$ Integral mit Divergenztheorem
  $\rightarrow$ lineare Approximation
  </p>
  <!-- .element: class="fragment fade-in" data-fragment-index="3" -->
</div>

<div class="r-stack">
  <img 
    src="assets/fdm-fvm0002.png"
    width="40%"
  />
  <img
    class="fragment fade-in"
    data-fragment-index="1"
    src="assets/fdm-fvm0003.png"
    width="40%"
  />
</div>

Koeffizienten
`$
\left(
-\frac{u}{2}-\frac{\Gamma}{\delta x}
\right) \phi_{m-1}
+\left(
\frac{2\Gamma}{\delta x}
\right) \phi_{m}
+\left(
\frac{u}{2}-\frac{\Gamma}{\delta x}
\right) \phi_{m+1} = 0
$`
<!-- .element: class="fragment fade-in" data-fragment-index="4" -->


### Lineares Gleichungssystem

FVM liefert
`$
\left(
-\frac{u}{2}-\frac{\Gamma}{\delta x}
\right) \phi_{m-1}
+\left(
\frac{2\Gamma}{\delta x}
\right) \phi_{m}
+\left(
\frac{u}{2}-\frac{\Gamma}{\delta x}
\right) \phi_{m+1} = 0
$`

- Koeffizienten für die `$m$`-te Zeile
- Analoges Aufstellen für alle anderen Auswertestellen liefern das lineare 
  Gleichungssystem

`$${\scriptsize
\begin{bmatrix}
\blacksquare & \blacksquare & 0  & \dots & \dots & \dots & 0\\
\blacksquare & \ddots & \ddots & 0 & & & \vdots\\
0 & \ddots & \ddots  & \ddots & 0 &  & \vdots\\
\vdots & 0 & \blacksquare  & \blacksquare & \blacksquare& 0 & \vdots\\
\vdots & & 0 & \ddots & \ddots& \ddots & 0\\
\vdots & & & 0 & \ddots& \ddots & \blacksquare\\
0 & \dots & \dots  & \dots & 0 & \blacksquare & \blacksquare\\
\end{bmatrix}
\begin{bmatrix}
\phi_1 \\
\vdots \\
\phi_m \\
\vdots \\
\phi_N \\
\end{bmatrix}
= \begin{bmatrix}
0 \\
\vdots \\
0 \\
\vdots \\
0 \\
\end{bmatrix}
\mathrm{mit} \; \blacksquare \; \mathrm{für\ Einträge} \neq 0
}$$`

- Matrix hat für den gezeigten Fall eine Bandstruktur
- Matrix ist fast immer schwachbesetzt und die Besetzungsstruktur ist abhängig 
  vom verwendeten Berechnungsgitter


### Turbulenzmodellierung

<div class="twocolumn">
<div>

<video
    data-autoplay
    data-src="assets/elbow_turbulenz.mp4"
    loop="loop"
    width="500">
</video>

</div>
<div>

- Lösung der Navier-Stokes-Gleichungen (DNS)
  - Auflösung aller Wirbelskalen
- Rechenaufwand bei großer $Re$-Zahl mehr als 100 Jahre
- Komplette oder teilweise Modellierung der Wirbelskala
  - RANS (zeitliche Mittelung) oder LES (räumliche Filterung)

</div>
</div>

Bei RANS entsteht der Reynoldsspannungstensor aus den nicht-linearen
Konvektionstermen in

`${\scriptsize
  \pp{}{t} \uv + 
  \underbrace{
    \uv \cdot \left( \nabla \cdot \uv \right)
  }_{
  \mathrm{nicht-linear}
  } =
  \nu \nabla \cdot \left( \nabla \cdot \underline{u} \right) -
  \frac{1}{\rho} \nabla p
}$`

Dieser Tensor wird durch Turbulenzmodellierung approximiert.

<div class="ref" style="font-size: 60%;">

[1] Krappel, T.; Large Eddy Simulation of a Complete Francis Turbine; 
Bundesprojekt
[LESFT](https://www.gauss-centre.eu/results/computational-and-scientific-engineering/large-eddy-simulation-of-a-complete-francis-turbine?no_cache=1&sword_list%5B0%5D=krappel&cHash=fd004c0078d48dc042bd56d5bf051285); 
2020

</div>


### Evolutionäre Optimierung

<div class="twocolumn">
<div>

__Ausgangspopulation__<br>
Kleine Schlangen mit großen Mäulern

</div>
<div>

Frisst zu große, giftige Kröten
- Kleiner Organismus kann Menge an Gift nicht verdauen

</div>
</div>

<div class="twocolumn">
<div>

__Selektionsfaktor__<br>
Giftige Aga-Kröte

</div>
<div>

Einige Schlangen verändern sich

- Mutation
- Paarung (Rekombination)

</div>
</div>

<div class="twocolumn">
<div>

__Neue Population__<br>
Große Schlange mit kleinen Mäulern

</div>
<div>

Bessere Anpassung an Selektionsfaktor

- Können nur kleinere Kröten mit weniger Gift fressen
- Größerer Organismus ermöglicht Verdauung

</div>
</div>


### Evolutionäre Optimierung - Teilturbine

<div class="untwo">
<div>
<img
  src="assets/bs_sketch.png"
  width="400"
/>
</div>
<div>

- Strömung durch Eintritt $(E)$, Umströmung des Profils $(S)$ und Austritt 
durch $(A)$
- Periodische Flächen $(P_A)$ und $(P_B)$
- Strukturierte Bereiche des Netzes sind grau dargestellt
- Gütefunktion ist ein gewichtetes Mittel aus Kavitation, Wirkungsgrad und 
  Fallhöhe
</div>
</div>
Ergebnisse und Initialisierung der Optimierungen 
<img
  src="assets/bs_opts.png"
  width="600"
/>

<div class="ref" style="font-size: 60%;">

[1] Tismer, A.; Entwicklung einer Softwareumgebung zur automatischen Auslegung 
    von hydraulischen Maschinen mit dem Inselmodell; 2020;
    [ISBN 978-3-948328-01-6](https://elib.uni-stuttgart.de/handle/11682/11108)<br>

</div>


### Evolutionäre Optimierung - Teilturbine

<video
    data-autoplay
    data-src="assets/bs_small_80x10_pareto_fit.mp4"
    loop="loop"
    width="700">
</video>

<div class="ref" style="font-size: 60%;">

[1] Tismer, A.; Entwicklung einer Softwareumgebung zur automatischen Auslegung 
    von hydraulischen Maschinen mit dem Inselmodell; 2020;
    [ISBN 978-3-948328-01-6](https://elib.uni-stuttgart.de/handle/11682/11108)<br>

</div>


### Anwendung: Wasserkraftwerk in Nepal

<img
  src="assets/nepal_over.png"
  width="600"
/>

Leistungsschwankungen der Turbine verursacht durch Trifurkation

<div class="ref" style="font-size: 60%;">

[1] Hoffmann, H., Roswora, R.R., Egger, A.: Rectification of Marsyangdi 
    Trifurcation; Hydro Vision 2000 Conference Technical Papers, HCI 
    Publications Inc.

</div>


### Anwendung: Wasserkraftwerk in Nepal

<img
  src="assets/nepal_cfd.png"
  width="700"
/>

<div class="ref" style="font-size: 60%;">

[1] Hoffmann, H., Roswora, R.R., Egger, A.: Rectification of Marsyangdi 
    Trifurcation; Hydro Vision 2000 Conference Technical Papers, HCI 
    Publications Inc.

</div>


### Anwendung: Wasserkraftwerk in Nepal

<img
  src="assets/nepal_erg.png"
  width="800"
/>

**Lösung:** Einbau von Blechen

<div class="ref" style="font-size: 60%;">

[1] Hoffmann, H., Roswora, R.R., Egger, A.: Rectification of Marsyangdi 
    Trifurcation; Hydro Vision 2000 Conference Technical Papers, HCI 
    Publications Inc.

</div>


### Anwendung: Wasserkraftwerk in Nepal - 15 Jahre später

<img
  src="assets/nepal_15y.png"
  width="800"
/>

<div class="ref" style="font-size: 60%;">

[1] Kirschner, O. et al.; Experimentelle und numerische Strömungsanalyse einer 
    Trifurkation eines 150-MW-Kraftwerkes; Wasserwirtschaft. 109; 2019;
    DOI: 10.1007/s35147-019-0223-3

</div>


### Anwendung: Wasserkraftwerk in Nepal - 15 Jahre später

<div class="tworl">
<div>

Original

<video
    data-autoplay
    data-src="assets/nepal_org.mp4"
    loop="loop"
    width="475">
</video>

</div>
<div>

Modifikation

<video
    data-autoplay
    data-src="assets/nepal_opt.mp4"
    loop="loop"
    width="475">
</video>

</div>
</div>

<div class="ref" style="font-size: 60%;">

[1] Kirschner, O. et al.; Experimentelle und numerische Strömungsanalyse einer 
    Trifurkation eines 150-MW-Kraftwerkes; Wasserwirtschaft. 109; 2019;
    DOI: 10.1007/s35147-019-0223-3

</div>


### Anwendung: Gezeitenströmung

<img
  src="assets/tidal_sketch.png"
  width="300"
/>
<img
  src="assets/tidal_mesh.png"
  width="600"
/>
<div class="untwo">
<div>
<img
  src="assets/tidal_tiefe.png"
  width="400"
/>
</div>
<div>

- Geometriedaten aus geometrischem Informationssystem (GIS)
- Kopplung von TPXO für Randbedingungen

</div>
</div>

<div class="ref" style="font-size: 60%;">

[1] Ruopp, A.; Optimierung von symmetrischen Gezeitenströmungstubinen und deren 
    Analyse in großräumigen Gezeitenströmungsgebieten; 2016; 
    ISBN 978-3-9812054-2-8<br>

</div>


### Anwendung: Gezeitenströmung

<div class="untwo">
<div>
<img
  src="assets/tidal_block-theo.png"
  width="190"
/>
</div>
<div>
Theoretisches Potenzial über Kanalverblockung
</div>
<div>
<img
  src="assets/tidal_block-prac.png"
  width="190"
/>
</div>
<div>
Technisches Potenzial über Verblockung der nutzbaren Fläche
</div>
<div>
<img
  src="assets/tidal_block-prac-withturb.png"
  width="190"
/>
</div>
<div>

Reales Potenzial über Platzierung einzelner Turbinen 
  - Berücksichtigung der Hauptströmungsrichtungen
  - Fernfeldeinfluss mit Nachlaufschatten 

<div class="ref" style="font-size: 60%;">

[1] Ruopp, A.; Optimierung von symmetrischen Gezeitenströmungstubinen und deren 
    Analyse in großräumigen Gezeitenströmungsgebieten; 2016; 
    ISBN 978-3-9812054-2-8<br>

</div>

</div>
</div>


### Anwendung: Gezeitenströmung

Zeitlicher Verlauf der Strömungsrichtung<br>
<video
    data-autoplay
    data-src="assets/tidal_sim-measure.mp4"
    loop="loop"
    width="375">
</video><br>
Strömungsfeld in zwei Zeitschritten
<div class="tworl">
<div>
<img
  src="assets/tidal_flow.png"
  width="200"
/>
</div>
<div>
<img
  src="assets/tidal_flow2.png"
  width="200"
/>
</div>
</div>

<div class="ref" style="font-size: 60%;">

[1] Ruopp, A.; Optimierung von symmetrischen Gezeitenströmungstubinen und deren 
    Analyse in großräumigen Gezeitenströmungsgebieten; 2016; 
    ISBN 978-3-9812054-2-8<br>

</div>


### Anwendung: Gezeitenströmung

Beispiel des Verlaufs der Anströmbedingungen

<div class="tworl">
<div>
<video
    data-autoplay
    data-src="assets/tidal_cfd.mp4"
    loop="loop"
    width="400">
</video>
</div>
<div>
<img
  src="assets/tidal_block-prac-withturb.png"
  width="400"
/>
</div>
</div>

- Starke Variation der lokalen Anströmrichtungen
- Turbinenverbund verblockt maßgeblich Kernströmung im Kanal

<div class="ref" style="font-size: 60%;">

[1] Ruopp, A.; Optimierung von symmetrischen Gezeitenströmungstubinen und deren 
    Analyse in großräumigen Gezeitenströmungsgebieten; 2016; 
    ISBN 978-3-9812054-2-8<br>

</div>
