---
marp: true
theme: default
class: 
transition: slide-up
paginate: true
header: "[Home](#slime-molds-and-cognitive-maps) > [World of the Slime Mold](#world-of-the-slime-mold) > [Computational Models](#computational-models) > [Results and Outcomes](#results-and-outcomes) > [Future directions](#future-directions)"
style: |
    .columns2 { /* style="grid-template-columns: 2fr 1fr" */
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 1rem;
    }
    .columns3 {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
    }
    section {
        align-content: start;
        padding: 60px 40px;
        }
    h1 {
        font-size: 50px;
        color: #35a4ff; /* Replace with your desired color */
        }
    h2 {
        color: #ff8724; /* Replace with your desired color */
        font-size: 35px;
        margin-top: 0px;
        margin-bottom: 5px;
        }
    h3 {
        color: #ffa114; /* Replace with your desired color ff8724 */
        font-size: 30px;
        margin-bottom: 10px;
        margin-top: 0px;
        /* text-decoration: underline; */
        /* font-style: italic */
        }
    h4 {
        color: #ffb744; /* Replace with your desired color */
        font-size: 25px;
        margin-top: 0px;
        /* text-decoration: underline; */
        /* font-style: italic */
        }
    em {
        font-style: italic;
        /* color: #ff8724; Replace with your desired color */
        }
    /* inline code */
    :not(pre) > code {
        padding: 5px 5px;
        border-radius: 5px;
    }
    /* code blocks */
    pre {
        /* background-color: rgba(1, 1, 1, 0.9); */
    }
    pre code {
        color: #fafafa;
        background-color: transparent;
        white-space: pre-wrap !important;
    }
    strong {
        color: #ff7925; /* Replace with your desired color */
        }
    p, li, table {
        font-size: 20px;
        }
    .container {
        display: true;
    }
    .col {
        flex: 1;
    }
    section footer {
        font-size: 10px;
        bottom: 5px;
        left: 15px;
    }
    section header {
        font-size: 15px;
        top: 10px;
        left: 15px;
    }
    img[alt~="center"] {
        display: block;
        margin: 0 auto;
    }
    
---
<!-- markdownlint-disable blank_lines html emphasis blanks-around-tables-->

# Slime Molds and Cognitive Maps

<!-- _header: ""-->

<div class="columns2" style="grid-template-columns: 3fr 2fr" >
<div>

*November 24st, 2026*

*Oğul Can Yurdakul*

*Department of Cognitive Science, UC Irvine*

</div>
<div>

|Click the links!|Presentation|Handout|
|-|:-:|:-:|
|Dark mode|[link](https://ogulyurdakul.github.io/files/cogs229_slimeMold/)|[link](https://ogulyurdakul.github.io/files/cogs229_slimeMold/dark_hanout.pdf)|
|Light mode|[link](https://ogulyurdakul.github.io/files/cogs229_slimeMold/light.html)|[link](https://ogulyurdakul.github.io/files/cogs229_slimeMold/light_hanout.pdf)|

</div>
</div>

---
<!-- markdownlint-disable blank_lines html emphasis blanks-around-tables-->

# Slime Molds and Cognitive Maps

<!-- _header: ""-->

<div class="columns2" style="grid-template-columns: 3fr 2fr" >
<div>

*November 24st, 2026*

*Oğul Can Yurdakul*

*Department of Cognitive Science, UC Irvine*

</div>
<div>

|Click the links!|Presentation|Handout|
|-|:-:|:-:|
|Dark mode|[link](https://ogulyurdakul.github.io/files/cogs229_slimeMold/)|[link](https://ogulyurdakul.github.io/files/cogs229_slimeMold/dark_hanout.pdf)|
|Light mode|[link](https://ogulyurdakul.github.io/files/cogs229_slimeMold/light.html)|[link](https://ogulyurdakul.github.io/files/cogs229_slimeMold/light_hanout.pdf)|

</div>
</div>

<hr>

- [World of the Slime Mold](#world-of-the-slime-mold)
  - [The slime itself: *Physarum polycephalum*](#the-slime-itself-physarum-polycephalum)
  - [Mapping the world with/of the slime mold](#mapping-the-world-withof-the-slime-mold)
  - [To err is ~~human~~ slime mold](#to-err-is-human-slime-mold)
- [Computational Models](#computational-models)
  - [Analyticaly derived models](#analyticaly-derived-models)
  - [Monte Carlo-based models](#monte-carlo-based-models)
  - [Shortcomings of the current models](#shortcomings-of-the-current-models)
- [Results and Outcomes](#results-and-outcomes)
- [Future directions](#future-directions)

---

<!-- 
footer: "
    Adamatzky (ed.) (2016) “Advances in Physarum Machines,” https://doi.org/10.1007/978-3-319-26662-6

    Mayne (2016). “Biology of the Physarum polycephalum Plasmodium: Preliminaries for Unconventional Computing,” In: Adamatzky, A. (eds) Advances in Physarum Machines. https://doi.org/10.1007/978-3-319-26662-6_1

    Li et al. (2020) “Slime mould algorithm: A new method for stochastic optimization,” https://www.sciencedirect.com/science/article/pii/
"
-->

## World of the Slime Mold

### The slime itself: *Physarum polycephalum*

<div class="columns2" style="grid-template-columns: 3fr 2fr" >
<div>

- eukaryote but not a fungus!
  - amoeboid protist
- "syncytium:" one cell, *millions* of nuclei!

![width:350 center](plasmodium.jpg)
- plasmodium: mobile form
  - few mm$^2$ to over half a m$^2$
  - can move up to 1cm/h
- has inspired many work, including an optimization algorithm

</div>
<div>

![width:400 center](slimeCycle.png)
(a) Fragments of sclerotium. (b) Sporangia. (c) Spores. (d) Swarm cell (arrowed). c, d Scale bar = 10$\upmu$m

</div>
</div>

---

### Mapping the world with/of the slime mold

#### Slime molds as path finders

<!-- 
footer: "
    Nakagaki et al. (2000) “Maze-solving by an amoeboid organism,” https://www.nature.com/articles/35035159

    Tero et al. (2010), “Rules for Biologically Inspired Adaptive Network Design,”  https://www.science.org/doi/10.1126/science.1177894
"
-->

<div class="columns2">
<div>

- Maze solving
  <!-- ![h:200 center](mazeSolving.png)  -->
$\quad\quad$<video src="mazeSolvingReal.mp4" controls height="400" allowfullscreen></video>

[Youtube: Slime mold solving a maze in the lab](https://www.youtube.com/watch?v=F3z_mdaQ5ac)

</div>
<div>



</div>
</div>

---

### Mapping the world with/of the slime mold

#### Slime molds as path finders

<!-- 
footer: "
    Nakagaki et al. (2000) “Maze-solving by an amoeboid organism,” https://www.nature.com/articles/35035159

    Tero et al. (2010), “Rules for Biologically Inspired Adaptive Network Design,”  https://www.science.org/doi/10.1126/science.1177894
"
-->

<div class="columns2">
<div>

- Maze solving
  <!-- ![h:200 center](mazeSolving.png)  -->
$\quad\quad$<video src="mazeSolvingReal.mp4" controls height="400" allowfullscreen></video>

[Youtube: Slime mold solving a maze in the lab](https://www.youtube.com/watch?v=F3z_mdaQ5ac)

</div>
<div>

- Tokyo subway map
    <!-- ![h:200](tokyoBefore.png) ![h:200](tokyoAfter.png)  -->
$\quad\quad\quad\quad$<video src="tokyoMap.mp4" controls height="400" allowfullscreen></video>

[Youtube: Slime mold form a map of the Tokyo-area railway system](https://www.youtube.com/shorts/GwKuFREOgmo)

</div>
</div>

---

### Mapping the world with/of the slime mold - 2

#### Slime molds as "problem solvers"

<!-- 
footer: "
    
    Bajpai et al. (2026) “Tracking and distinguishing slime mold solutions to traveling salesperson problems through synchronized amplification in the non-equilibrium steady state,” http://arxiv.org/abs/2504.03492

    Reid and Beekman (2013) “Solving the Towers of Hanoi – how an amoeboid organism efficiently constructs transport networks,” https://doi.org/10.1242/jeb.081158
"
-->

<div class="columns2">
<div>

- Traveling salesperson problem
  ![width:500 center](travelingSlime.png)

</div>
<div>



</div>
</div>

---

### Mapping the world with/of the slime mold - 2

#### Slime molds as "problem solvers"

<!-- 
footer: "
    
    Bajpai et al. (2026) “Tracking and distinguishing slime mold solutions to traveling salesperson problems through synchronized amplification in the non-equilibrium steady state,” http://arxiv.org/abs/2504.03492

    Reid and Beekman (2013) “Solving the Towers of Hanoi – how an amoeboid organism efficiently constructs transport networks,” https://doi.org/10.1242/jeb.081158
"
-->

<div class="columns2">
<div>

- Traveling salesperson problem
  ![width:500 center](travelingSlime.png)

</div>
<div>

- Towers of Hanoi puzzle
   ![width:350 center](hanoiSetup.png) 
   ![width:350 center](hanoiSolution.jpeg)

</div>
</div>

---

### Mapping the world with/of the slime mold - 3

#### Slime molds as ???

<!-- 
footer: "
    Kay et al., (2022) “Stepwise slime mould growth as a template for urban design,” https://www.nature.com/articles/s41598-022-05439-w

    Evangelidis et al., (2017) “Physarum machines imitating a Roman road network: the 3D approach,” https://www.nature.com/articles/s41598-017-06961-y

    Adamatzky, (2012) “The World’s Colonisation and Trade Routes Formation as Imitated by Slime Mould,” https://arxiv.org/abs/1209.3958v1

"
-->

<div class="columns2">
<div>

- Urban designers?
  ![width:500](urbanDesign.png)

</div>
<div>

</div>
</div>

---

### Mapping the world with/of the slime mold - 3

#### Slime molds as ???

<!-- 
footer: "
    Kay et al., (2022) “Stepwise slime mould growth as a template for urban design,” https://www.nature.com/articles/s41598-022-05439-w

    Evangelidis et al., (2017) “Physarum machines imitating a Roman road network: the 3D approach,” https://www.nature.com/articles/s41598-017-06961-y

    Adamatzky, (2012) “The World’s Colonisation and Trade Routes Formation as Imitated by Slime Mould,” https://arxiv.org/abs/1209.3958v1

"
-->

<div class="columns2">
<div>

- Urban designers?
  ![width:500 center](urbanDesign.png)

</div>
<div>

- Romans??
  ![width:450 center](balkans.png)

</div>
</div>

---

### Mapping the world with/of the slime mold - 3

#### Slime molds as ???

<!-- 
footer: "
    Kay et al., (2022) “Stepwise slime mould growth as a template for urban design,” https://www.nature.com/articles/s41598-022-05439-w

    Evangelidis et al., (2017) “Physarum machines imitating a Roman road network: the 3D approach,” https://www.nature.com/articles/s41598-017-06961-y

    Adamatzky, (2012) “The World’s Colonisation and Trade Routes Formation as Imitated by Slime Mould,” https://arxiv.org/abs/1209.3958v1

"
-->

<div class="columns2">
<div>

- Urban designers?
  ![width:500 center](urbanDesign.png)

</div>
<div>

- Romans??
  ![width:450 center](balkans.png)

- Colonizers???
  ![width:450 center](colonization.png)
  <!-- ![h:140](colonization2.png) -->

</div>
</div>

---

### To err is ~~human~~ slime mold

<!-- 
footer: "
    Latty and Beekman (2011) “Speed-accuracy trade-offs during foraging decisions in the acellular slime mould Physarum polycephalum,” https://dx.doi.org/10.1098/rspb.2010.1624

    ——, (2011) “Irrational decision-making in an amoeboid organism: transitivity and context-dependent preferences,” https://pmc.ncbi.nlm.nih.gov/articles/PMC3013386/
"
-->

<div class="columns2">
<div>

#### Speed-accuracy trade-off

when having to choose between food sources, adding stressors reduce accuracy of choosing the larger one

<div class="columns2">
<div>

![width:290](satSetup.png)



</div>
<div>



</div>
</div>

</div>
<div>



<div class="columns2">
<div>



</div>
<div>



</div>
</div>


</div>
</div>

---

### To err is ~~human~~ slime mold

<!-- 
footer: "
    Latty and Beekman (2011) “Speed-accuracy trade-offs during foraging decisions in the acellular slime mould Physarum polycephalum,” https://dx.doi.org/10.1098/rspb.2010.1624

    ——, (2011) “Irrational decision-making in an amoeboid organism: transitivity and context-dependent preferences,” https://pmc.ncbi.nlm.nih.gov/articles/PMC3013386/
"
-->

<div class="columns2">
<div>

#### Speed-accuracy trade-off

when having to choose between food sources, adding stressors reduce accuracy of choosing the larger one

<div class="columns2">
<div>

![width:290](satSetup.png)

dark: easy
gray: difficult

</div>
<div>

![height:430](satResult.png)

</div>
</div>

</div>
<div>



<div class="columns2">
<div>





</div>
</div>


</div>
</div>

---

### To err is ~~human~~ slime mold

<!-- 
footer: "
    Latty and Beekman (2011) “Speed-accuracy trade-offs during foraging decisions in the acellular slime mould Physarum polycephalum,” https://dx.doi.org/10.1098/rspb.2010.1624

    ——, (2011) “Irrational decision-making in an amoeboid organism: transitivity and context-dependent preferences,” https://pmc.ncbi.nlm.nih.gov/articles/PMC3013386/
"
-->

<div class="columns2">
<div>

#### Speed-accuracy trade-off

when having to choose between food sources, adding stressors reduce accuracy of choosing the larger one

<div class="columns2">
<div>

![width:290](satSetup.png)

dark: easy
gray: difficult

</div>
<div>

![height:430](satResult.png)

</div>
</div>

</div>
<div>

#### Independence of Irrelevant Alternatives

when an overall worse option is introduced into a choice among two, slime molds sometimes choose it

<div class="columns2">
<div>

![width:290](iiaSetup.jpg)



</div>
<div>



</div>
</div>


</div>
</div>

---

### To err is ~~human~~ slime mold

<!-- 
footer: "
    Latty and Beekman (2011) “Speed-accuracy trade-offs during foraging decisions in the acellular slime mould Physarum polycephalum,” https://dx.doi.org/10.1098/rspb.2010.1624

    ——, (2011) “Irrational decision-making in an amoeboid organism: transitivity and context-dependent preferences,” https://pmc.ncbi.nlm.nih.gov/articles/PMC3013386/
"
-->

<div class="columns2">
<div>

#### Speed-accuracy trade-off

when having to choose between food sources, adding stressors reduce accuracy of choosing the larger one

<div class="columns2">
<div>

![width:290](satSetup.png)

dark: easy
gray: difficult

</div>
<div>

![height:430](satResult.png)

</div>
</div>

</div>
<div>

#### Independence of Irrelevant Alternatives

when an overall worse option is introduced into a choice among two, slime molds sometimes choose it

<div class="columns2">
<div>

![width:290](iiaSetup.jpg)

dark: two-choice setup
gray: three-choice setup

</div>
<div>

![height:430](iiaResult.jpeg)

</div>
</div>


</div>
</div>

---

## Computational Models

<!-- 
footer: "
    Kobayashi et al. (2006) “Mathematical Model for Rhythmic Protoplasmic Movement in the True Slime Mold,” https://doi.org/10.1007/s00285-006-0007-0

    Jones (2010) “The emergence and dynamical evolution of complex transport networks from simple low-level behaviours,”  https://www.scopus.com/pages/publications/77949441365

"
-->

<div class="columns2">
<div>

**Analytically derived**

- the slime mold's thickness is assumed to be/approximated by a mathematical rule
  $$\frac{\partial s}{\partial t} = \nabla\cdot(sM\nabla p)$$
  <!-- - $s(\mathbf x, t)$ is the sol thickness
  - $p(\mathbf x, t)$ is sol pressure -->
![width:400 center](solFlow.png)

<div class="columns2" style="gap: 1rem">
<div>



</div>
<div>



</div>
</div>



</div>
<div>



</div>
</div>

---

## Computational Models

<!-- 
footer: "
    Kobayashi et al. (2006) “Mathematical Model for Rhythmic Protoplasmic Movement in the True Slime Mold,” https://doi.org/10.1007/s00285-006-0007-0

    Jones (2010) “The emergence and dynamical evolution of complex transport networks from simple low-level behaviours,”  https://www.scopus.com/pages/publications/77949441365

"
-->

<div class="columns2">
<div>

**Analytically derived**

- the slime mold's thickness is assumed to be/approximated by a mathematical rule
  $$\frac{\partial s}{\partial t} = \nabla\cdot(sM\nabla p)$$
  <!-- - $s(\mathbf x, t)$ is the sol thickness
  - $p(\mathbf x, t)$ is sol pressure -->
![width:400 center](solFlow.png)

<div class="columns2" style="gap: 1rem">
<div>

![width:290](circuitReal.png)
real slime mold patterns

</div>
<div>

![width:290](circuitSim.png)
simulation results

</div>
</div>



</div>
<div>



</div>
</div>

---

## Computational Models

<!-- 
footer: "
    Kobayashi et al. (2006) “Mathematical Model for Rhythmic Protoplasmic Movement in the True Slime Mold,” https://doi.org/10.1007/s00285-006-0007-0

    Jones (2010) “The emergence and dynamical evolution of complex transport networks from simple low-level behaviours,”  https://www.scopus.com/pages/publications/77949441365

"
-->

<div class="columns2">
<div>

**Analytically derived**

- the slime mold's thickness is assumed to be/approximated by a mathematical rule
  $$\frac{\partial s}{\partial t} = \nabla\cdot(sM\nabla p)$$
  <!-- - $s(\mathbf x, t)$ is the sol thickness
  - $p(\mathbf x, t)$ is sol pressure -->
![width:400 center](solFlow.png)

<div class="columns2" style="gap: 1rem">
<div>

![width:290](circuitReal.png)
real slime mold patterns

</div>
<div>

![width:290](circuitSim.png)
simulation results

</div>
</div>



</div>
<div>

**Monte Carlo-based**

- lots of small particles make small decisions to generate overall behavior

![width:250 center](MCunit.png)

</div>
</div>

---

## Computational Models

<!-- 
footer: "
    Kobayashi et al. (2006) “Mathematical Model for Rhythmic Protoplasmic Movement in the True Slime Mold,” https://doi.org/10.1007/s00285-006-0007-0

    Jones (2010) “The emergence and dynamical evolution of complex transport networks from simple low-level behaviours,”  https://www.scopus.com/pages/publications/77949441365

"
-->

<div class="columns2">
<div>

**Analytically derived**

- the slime mold's thickness is assumed to be/approximated by a mathematical rule
  $$\frac{\partial s}{\partial t} = \nabla\cdot(sM\nabla p)$$
  <!-- - $s(\mathbf x, t)$ is the sol thickness
  - $p(\mathbf x, t)$ is sol pressure -->
![width:400 center](solFlow.png)

<div class="columns2" style="gap: 1rem">
<div>

![width:290](circuitReal.png)
real slime mold patterns

</div>
<div>

![width:290](circuitSim.png)
simulation results

</div>
</div>



</div>
<div>

**Monte Carlo-based**

- lots of small particles make small decisions to generate overall behavior

![width:250 center](MCunit.png)

![width:490 center](MCgeneral.png)

</div>
</div>

---

### Analyticaly derived models

<!-- 
footer: "
    Tero et al. (2007) “A mathematical model for adaptive transport network in path finding by true slime mold,” https://www.sciencedirect.com/science/article/pii/S002251930600289X
"
-->

<div class="columns2" style="grid-template-columns: 4fr 3fr">
<div>

Tero et al (2007) adapted Kobayashi et al. (2006)'s model to graphs

- flux $Q_{ij}$ from node $i$ to $j$: 
  $$\qquad Q_{ij} = \dfrac{D_{ij}}{L_{ij}}(p_i - p_j)$$
  where $D_{ij}$ is the conductivity of the edge, $p_i$ are pressures at nodes
- two nodes are special: one is source, one is sink
    <div class="columns3" style="gap: 1rem">
    <div>

    flux _conserved_ at regular node $i$

    $$\sum_j Q_{ij} = 0$$

    </div>
    <div>

    flux _generated_ at source node

    $$\sum_j Q_{\textrm{source},j} = I_0$$

    </div>
    <div>

    flux _consumed_ at sink node

    $$\sum_j Q_{\textrm{sink},j} = -I_0$$

    </div>
    </div>

</div>
<div>

![width:350 center](circuit.png)



</div>
</div>

---

### Analyticaly derived models

<!-- 
footer: "
    Tero et al. (2007) “A mathematical model for adaptive transport network in path finding by true slime mold,” https://www.sciencedirect.com/science/article/pii/S002251930600289X
"
-->

<div class="columns2" style="grid-template-columns: 4fr 3fr">
<div>

Tero et al (2007) adapted Kobayashi et al. (2006)'s model to graphs

- flux $Q_{ij}$ from node $i$ to $j$: 
  $$\qquad Q_{ij} = \dfrac{D_{ij}}{L_{ij}}(p_i - p_j)$$
  where $D_{ij}$ is the conductivity of the edge, $p_i$ are pressures at nodes
- two nodes are special: one is source, one is sink
    <div class="columns3" style="gap: 1rem">
    <div>

    flux _conserved_ at regular node $i$

    $$\sum_j Q_{ij} = 0$$

    </div>
    <div>

    flux _generated_ at source node

    $$\sum_j Q_{\textrm{source},j} = I_0$$

    </div>
    <div>

    flux _consumed_ at sink node

    $$\sum_j Q_{\textrm{sink},j} = -I_0$$

    </div>
    </div>

- adapt the conductivities according to
  $$\dfrac{d}{dt}D_{ij} = f(|Q_{ij}|) - rD_{ij}$$

</div>
<div>

![width:350 center](circuit.png)



</div>
</div>

---

### Analyticaly derived models

<!-- 
footer: "
    Tero et al. (2007) “A mathematical model for adaptive transport network in path finding by true slime mold,” https://www.sciencedirect.com/science/article/pii/S002251930600289X
"
-->

<div class="columns2" style="grid-template-columns: 4fr 3fr">
<div>

Tero et al (2007) adapted Kobayashi et al. (2006)'s model to graphs

- flux $Q_{ij}$ from node $i$ to $j$: 
  $$\qquad Q_{ij} = \dfrac{D_{ij}}{L_{ij}}(p_i - p_j)$$
  where $D_{ij}$ is the conductivity of the edge, $p_i$ are pressures at nodes
- two nodes are special: one is source, one is sink
    <div class="columns3" style="gap: 1rem">
    <div>

    flux _conserved_ at regular node $i$

    $$\sum_j Q_{ij} = 0$$

    </div>
    <div>

    flux _generated_ at source node

    $$\sum_j Q_{\textrm{source},j} = I_0$$

    </div>
    <div>

    flux _consumed_ at sink node

    $$\sum_j Q_{\textrm{sink},j} = -I_0$$

    </div>
    </div>

- adapt the conductivities according to
  $$\dfrac{d}{dt}D_{ij} = f(|Q_{ij}|) - rD_{ij}$$

</div>
<div>

![width:350 center](circuit.png)

- **this is just a lumped circuit model!**
  - $p_i$ is node voltages,
  - $Q_{ij}$ is the current,
  - $G_{ij} = \dfrac{D_{ij}}{L_{ij}}$ is the conductance

<!-- ![width:300 center](wardog.gif) -->
![width:250 center](image.png)

</div>
</div>

---

### Monte Carlo-based models

<!-- 
footer: "
    Jones (2010) “The emergence and dynamical evolution of complex transport networks from simple low-level behaviours,”  https://www.scopus.com/pages/publications/77949441365
"
-->

simple actions of little particles can give rise to complex behavior at the population level...

<div class="columns2" style="grid-template-columns: 2fr 3fr">
<div>

Jones (2010)'s model:

![width:300 center](MCalgo.png)
![width:300 center](MCunit.png)

</div>
<div>

</div>
</div>

---

### Monte Carlo-based models

<!-- 
footer: "
    Jones (2010) “The emergence and dynamical evolution of complex transport networks from simple low-level behaviours,”  https://www.scopus.com/pages/publications/77949441365
"
-->

simple actions of little particles can give rise to complex behavior at the population level...

<div class="columns2" style="grid-template-columns: 2fr 3fr">
<div>

Jones (2010)'s model:

![width:300 center](MCalgo.png)
![width:300 center](MCunit.png)

</div>
<div>

**can we build on this?**

- say each particle "looks" at all the nodes it can travel to and assigns a positive "score" to each of them
  - softmax decision:
    - sample the next node proportional to these scores
  - Metropolis-Hastings decision:
    - sample a candidate next node
      - if better, move there
      - if worse, move or stay probabilistically

</div>
</div>

---

### Shortcomings of the current models

<!-- 
footer: "
    Tero et al. (2007) “A mathematical model for adaptive transport network in path finding by true slime mold,” https://www.sciencedirect.com/science/article/pii/S002251930600289X

    Jones (2010) “The emergence and dynamical evolution of complex transport networks from simple low-level behaviours,”  https://www.scopus.com/pages/publications/77949441365
"
-->

<div class="columns2" style="grid-template-columns: 2fr 3fr">
<div>

Tero et al. (2007):

![height:200 center](circuit.png)

</div>
<div>

- biologically undesirable model
  - the function $f(|Q_{ij}|)$ is not as interpretable
  - food sources are modeled asymmetrically
- no repulsion term: light or slime
- no "exploration"

</div>
</div>

<div class="columns2" style="grid-template-columns: 2fr 3fr">
<div>



</div>
<div>



</div>
</div>

---

### Shortcomings of the current models

<!-- 
footer: "
    Tero et al. (2007) “A mathematical model for adaptive transport network in path finding by true slime mold,” https://www.sciencedirect.com/science/article/pii/S002251930600289X

    Jones (2010) “The emergence and dynamical evolution of complex transport networks from simple low-level behaviours,”  https://www.scopus.com/pages/publications/77949441365
"
-->

<div class="columns2" style="grid-template-columns: 2fr 3fr">
<div>

Tero et al. (2007):

![height:200 center](circuit.png)

</div>
<div>

- biologically undesirable model
  - the function $f(|Q_{ij}|)$ is not as interpretable
  - food sources are modeled asymmetrically
- no repulsion term: light or slime
- no "exploration"

</div>
</div>

<div class="columns2" style="grid-template-columns: 2fr 3fr">
<div>

Jones (2010):

![height:200 center](MCunit.png)

</div>
<div>

- no accounting of the path-finding effects
- no food, no light, just slime

</div>
</div>

---

<!-- 
footer: "
    
"
-->

## Results and Outcomes

- a `ratinabox`-style toolbox emerges!
  - `world = slimeWorld(node_locs, C_, light, slime, opts)`
  - `slime = circuitSlime(world, options)`
  - `slime = softmaxSlime(world, options)`
  - `slime = MHslime(world, options)`
- example:

<div class="columns3" style="grid-template-columns: 1fr 1fr 1fr">
<div>

![height:300 center](results/random_map.png) 

</div>
<div>

![height:300 center](results/random_env.png)

</div>
<div>



</div>
</div>

---

<!-- 
footer: "
    
"
-->

## Results and Outcomes

- a `ratinabox`-style toolbox emerges!
  - `world = slimeWorld(node_locs, C_, light, slime, opts)`
  - `slime = circuitSlime(world, options)`
  - `slime = softmaxSlime(world, options)`
  - `slime = MHslime(world, options)`
- example:

<div class="columns3" style="grid-template-columns: 1fr 1fr 1fr">
<div>

![height:300 center](results/random_map.png) 

</div>
<div>

![height:300 center](results/random_env.png)

</div>
<div>

![height:300 center](results/circuit_random.gif)

</div>
</div>

---

## Results and Outcomes

### Path-finding and detours

<div class="columns3" style="grid-template-columns: 1fr 1fr">
<div>

![height:500 center](results/circuit_gridWorld.gif)

</div>
<div>



</div>
</div>

---

## Results and Outcomes

### Path-finding and detours

<div class="columns3" style="grid-template-columns: 1fr 1fr">
<div>

![height:500 center](results/circuit_gridWorld.gif)

</div>
<div>

![height:500 center](results/circuit_gridWorld2.gif)

</div>
</div>

---

## Results and Outcomes

### Path memory

<div class="columns3" style="grid-template-columns: 1fr 1fr">
<div>

![height:500 center](results/circuit_gridWorld2.gif)

</div>
<div>



</div>
</div>

---

## Results and Outcomes

### Path memory

<div class="columns3" style="grid-template-columns: 1fr 1fr">
<div>

![height:500 center](results/circuit_gridWorld2.gif)

</div>
<div>

![height:500 center](results/circuit_gridWorld3.gif)

</div>
</div>

---

## Results and Outcomes

### Undesirable paths

<div class="columns3" style="grid-template-columns: 1fr 1fr">
<div>

![height:500 center](results/light_gridWorld.png)

</div>
<div>

![height:500 center](results/circuit_gridWorld4.gif)

</div>
</div>

---

<!-- 
footer: "
    
"
-->

## Future directions

<div class="columns3" style="grid-template-columns: 1fr 1fr">
<div>

- Tolman's sun maze: Latent learning in slime molds?

![height:250 center](results/circuit_sunMaze.gif)

</div>
<div>



</div>
</div>

---

<!-- 
footer: "
    
"
-->

## Future directions

<div class="columns3" style="grid-template-columns: 1fr 1fr">
<div>

- Tolman's sun maze: Latent learning in slime molds?

![height:250 center](results/circuit_sunMaze.gif)

![height:250 center](results/softmax_sunMaze.gif)

</div>
<div>



</div>
</div>

---

<!-- 
footer: "
    
"
-->

## Future directions

<div class="columns3" style="grid-template-columns: 1fr 1fr">
<div>

- Tolman's sun maze: Latent learning in slime molds?

![height:250 center](results/circuit_sunMaze.gif)

![height:250 center](results/softmax_sunMaze.gif)

</div>
<div>

- Spatial memory
- Temporal memory: accommodation to repeated stimuli
- Foraging experiments
- Memory sharing in slime molds in contact
- ...

</div>
</div>

---

## Thank you!