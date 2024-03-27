In this page, we provide supplementary experiments for our RefinedFields ICML rebuttal.

## Table A
In this table, we increase the number of feature per-plane when training classical single-scale K-Planes.
As illustrated, the rendering quality of K-Planes does not exhibit notable improvements even when drastically increasing the model size.
Hence, K-Planes results are already optimal for the default number of 32 features.
This further highlights the added value of our method, as it exhibits notable improvements to PSNR and SSIM while utilizing the same base representation.

<div align="center">

<table>
    <tr>
        <th>Feature Dimension</th>
        <th>PSNR</th>
        <th>SSIM</th>
    </tr>
    <tr>
        <td>16</td>
        <td>21.25</td>
        <td>0.6627</td>
    </tr>
    <tr>
        <td>32</td>
        <td>21.30</td>
        <td>0.6627</td>
    </tr>
    <tr>
        <td>64</td>
        <td>21.60</td>
        <td>0.6879</td>
    </tr>
    <tr>
        <td>128</td>
        <td>21.69</td>
        <td>0.6896</td>
    </tr>
    <tr>
        <td>256</td>
        <td>21.68</td>
        <td>0.6897</td>
    </tr>
    <tr>
        <td><b>32 (our method)</b></td>
        <td><b>23.42</b></td>
        <td><b>0.7379</b></td>
    </tr>
</table>

</div>


## Table B
In this table, we increase the per-plane resolution when training classical single-scale K-Planes.
As illustrated, the resolution of 512 x 512 is already the optimal resolution for K-Planes. 
Our experiments show that increasing this resolution actually degrades the quality of renderings. 
Hence, K-Planes results are laready optimal ofr the default 512 x 512 resolution.
This also highlights the added value of our method, as it exhibits notable improvements to PSNR and SSIM while utilizing the same base representation.

<div align="center">
    
<table>
    <tr>
        <th>Resolution</th>
        <th>PSNR</th>
        <th>SSIM</th>
    </tr>
    <tr>
        <td>512 x 512</td>
        <td>21.30</td>
        <td>0.6627</td>
    </tr>
    <tr>
        <td>768 x 768</td>
        <td>20.98</td>
        <td>0.6388</td>
    </tr>
    <tr>
        <td>1024 x 1024</td>
        <td>20.44</td>
        <td>0.6128</td>
    </tr>
    <tr>
        <td>1280 x 1280</td>
        <td>19.51</td>
        <td>0.5800</td>
    </tr>
    <tr>
        <td>1536 x 1536</td>
        <td>19.88</td>
        <td>0.5533</td>
    </tr>
    <tr>
        <td><b>512 x 512 (our method)</b></td>
        <td><b>23.42</b></td>
        <td><b>0.7379</b></td>
    </tr>
</table>

</div>

## Figure A
In this figure, we illustrate the rendering PSNR throughout our optimization procedure, and a comparison with K-Planes.
Each section (1 to 9) represents one fitting phase, where K-Planes are replaced with refined K-Planes between two consecutive stages.

As depicted:
  - N1 and N2 are chosen so that the alternating procedure switches stages as soon as the model starts to converge
  - Our method improves upon K-Planes by side-stepping its lower PSNR plateau, through the re-initialization of K-Planes with the improved and _refined_ K-Planes.
  - Hence, this allows our base representation to converge to a significantly higher PSNR than what it would have attained without scene refining.

<p align="center">
  <img src="assets/css/psnr_curve.svg" width="110%"/>
</p>

Note that for illustration purposes, we run K-Planes for a higher number of epochs here, leading to a slower learning rate scheduler for the K-Planes curve.
