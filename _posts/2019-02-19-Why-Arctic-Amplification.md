---
layout: post
title: "[Research] What causes the arctic amplification of surface warming?"
date: 2019-02-25
use_math: true
---

<p>The Earth's surface is warming 2-3x faster in the Arctic than the global average. There are many different reasons for this Arctic amplification of warming but there is still debate on which is the dominant mechanism.</p>

<div style="text-align:center;valign:center"><img src="https://micamus.github.io/images/cmip5_PA.png" alt="CMIP5 PA" style="width: 500px; height: auto;" class="center"></div>

<p>The figure above is from <a href='http://www.cgd.ucar.edu/staff/cdeser/docs/submitted.smith.pamip.mar18.pdf'>Smith et al. $($2018$)$</a> and shows the <i>pattern</i> of surface warming in projections of future climate change. The land warms faster than the ocean and the Arctic region warms from 2 to 4 times faster than the global mean $($see zonal average plot on the right$)$. </p>

<p>What are the possible reasons for this amplified warming?</p>

<div style="text-align:center"><img src="https://micamus.github.io/images/pm14.png" alt="Polar Amplif decomp" style="width:250px;height:250px;" class="center"></div>

<p>Using <a href='https://climatedataguide.ucar.edu/climate-data/radiative-kernels-climate-models'>radiative kernels</a>, <a href='https://www.nature.com/articles/ngeo2071'>Pithan and Mauritsen $($2014$)$</a> decomposed the pattern of warming into contributions from the different forcings and feedbacks. The figure above shows how much each forcing and feedback contribute to tropical warming $($x-axis$)$ and Arctic warming $($y-axis$)$. The albedo, for example, is a feedback that only affects the high latitudes, hence does not contribute to tropical warming $($0 on x-axis$)$ but does contribute to Arctic warming $($around 3.3K$)$. The distance from the one-to-one line $($gray dashed$)$ indicates whether the forcing/feedback contributes to Arctic or tropical amplification.</p>

<h3>Sea ice albedo feedback</h3>

<div style="text-align:center"><img src="https://micamus.github.io/images/SAF.jpg" alt="NASA SAF" style="width:500px;height:auto;" class="center"></div>

<p>This figure from <a href='https://svs.gsfc.nasa.gov/12277'>NASA</a> shows the 2016 Arctic sea ice minimum $($911,000 square miles$)$ and the 1981-2010 average $($gold line$)$. This decrease in sea ice extent leads to a decrease in surface albedo and induces additional local warming.</p>

<p>As can be seen from the Pithan and Mauritsen $($2014$)$ figure, this is one of the dominant mechanisms for polar amplification. Idealized climate models that keep the sea ice albedo fixed as the climate warms still have Arctic amplification though, even if the amount of polar amplification in these simulations depends the type of insolation used $($see <a href='https://journals.ametsoc.org/doi/full/10.1175/JCLI-D-17-0627.1'>Kim et al. $($2018$)$</a>$)$. This suggests there are more fundamental mechanisms at play.</p>

<h3>Planck feedback</h3>

<p>The instantaneous impact of increasing greenhouse gas concentrations is to reduce the outgoing longwave radiation $($OLR$)$ at the top-of-atmosphere $($TOA$)$. Since the global-mean TOA outgoing longwave radiation must be equal to the absorbed solar radiation, which we assume does not change, the surface and tropospheric temperature must increase to increase the OLR. We artificially separate the vertical structure of warming into a vertically homogeneous part and its deviation. The Planck feedback corresponds to the total increase in OLR per degree of vertically homogeneous warming.</p>

<div style="text-align:center"><img src="https://micamus.github.io/images/planck_fb.png" alt="Planck fb" style="width:400px;height:250px;" class="center"></div>

<p>The figure above is a schematic representation of the temperature dependence of infrared radiation. The Stefan-Boltzmann law lets us link the energy radiated by Earth $($mostly in the infrared spectrum$)$ and its temperature : $E=\sigma T^4$ where $\sigma$ is a constant. As illustrated in the figure, a cold body needs a higher increase in temperature to reach the same increase in radiation than a warm body. This is caused by the concavity of the curve, or its nonlinearity. Since the high latitudes are colder than the rest of the planet, this is thought to be a cause for polar amplification.</p>

<p>My <a href='https://journals.ametsoc.org/doi/10.1175/JCLI-D-17-0603.1'>first PhD project</a> consisted in testing how important this mechanism is. We used an idealized atmospheric gray radiation model with aquaplanet surface boundary condition $($just ocean, no continents$)$, no clouds and no sea ice. We simply replaced $E=\sigma T^4$ by $E=A + BT$ in the radiation code so that the increase in temperature necessary to increase the OLR is the same for all initial temperatures. This had no effect on the pattern of surface air warming as other factors such as atmospheric energy transport and lapse rate feedback changed to compensate. However, we did find that the $E=\sigma T^4$ nonlinearity affects the vertical structure of warming.</p>

<h3>Atmospheric energy transport</h3>

<p>While the role of the atmospheric energy transport does not seem dominant in Pithan and Mauritsen's figure, its role becomes important if the surface albedo feedback is artificially cancelled in idealized climate model simulations.</p>

<p>The simplest model to understand the role of atmospheric energy transport in polar amplification is the moist energy balance model $($see <a href='https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2010GL045440'>Hwang and Frierson $($2010$)$ for example$)$</a>. In this one-dimensional model, where each point represents a latitude band, the difference between absorbed shortwave radiation and emitted longwave radiation is balanced by diffusion of moist static energy $($MSE$)$. MSE is conserved in the event of latent heat release $($heat released when water vapor condenses to liquid$)$. Since saturation vapor pressure is exponentially related to temperature, the initial increase in temperature increases the water vapor content more in the tropics than in the poles hence increases the gradient of the moist component of the moist static energy, which leads to more convergence of moist static energy flux. Assuming this was the only mechanism responsible for polar amplification, Tim and I wrote a <a href='https://journals.ametsoc.org/doi/full/10.1175/JCLI-D-17-0578.1'>paper</a> estimating the amount of polar amplification using this model and which do not require the use of numerical model simulations.</p>

<h3>Lapse rate feedback</h3>

The lapse rate feedback refers to the vertical structure of temperature change. 