In this page, we provide supplementary experiments for our RefinedFields ICML rebuttal.

# Tables

## Table 1
In this table, we increase the number of feature per-plane when training classical single-scale K-Planes.
As illustrated, the rendering quality of K-Planes does not exhibit notable improvements even when drastically increasing the model size.
Hence, K-Planes results are already optimal for the default number of 32 features.
This further highlights the added value of our method, as it exhibits notable improvements to PSNR and SSIM while utilizing the same base representation.

<center>
| Feature Dimension |   PSNR   |   SSIM    |
| :---------------: | :------: | :-------: |
| 16                |   21.25  |   0.6627  |
| 32                |   21.30  |   0.6627  |
| 64                |   21.60  |   0.6879  |
| 128               |   21.69  |   0.6896  |
| 256               |   21.68  |   0.6897  |
|-------------------|----------|-----------|
|**32 (our method)**| **23.42**| **0.7379**|
</center>

## Table 2
In this table, we increase the per-plane resolution when training classical single-scale K-Planes.
As illustrated, the resolution of 512 x 512 is already the optimal resolution for K-Planes. 
Our experiments show that increasing this resolution actually degrades the quality of renderings. 
Hence, K-Planes results are laready optimal ofr the default 512 x 512 resolution.
This also highlights the added value of our method, as it exhibits notable improvements to PSNR and SSIM while utilizing the same base representation.

<center>
| Resolution               |   PSNR   |    SSIM   |
| :----------------------: | :------: | :-------: |
| 512 x 512                |   21.30  |   0.6627  |
| 768 x 768                |   20.98  |   0.6388  |
| 1024 x 1024              |   20.44  |   0.6128  |
| 1280 x 1280              |   19.51  |   0.5800  |
| 1536 x 1536              |   19.88  |   0.5533  |
|--------------------------|----------|-----------|
|**512 x 512 (our method)**| **23.42**| **0.7379**|
</center>



![Figure](assets/css/schema.svg)
