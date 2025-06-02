# CLIP-ViT-B-32 Sparse Autoencoder Performance

For CLIP, we recommend using the **Vanilla SAEs (All Patches)**, which we trained on all patches (CLS + spatial). 

We experimented with CLS only, CLS only top k (k=64), and spatial patches only as well. Empirically, we get the best results with All Patches.

For more details, see our whitepaper.

## Vanilla SAEs (All Patches)

| Model | Layer | Sublayer   | l1 coeff. | % Explained var. | Avg L0  | Avg CLS L0 | Cos sim | Recon cos sim | CE    | Recon CE | Zero abl CE | % CE recovered | % Alive features |
|--------|-------|------------|-----------|------------------|---------|-------------|---------|----------------|--------|-----------|--------------|----------------|------------------|
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-0-hook_mlp_out-l1-1e-05) | 0     | mlp_out    | 1e-5      | 98.7             | 604.44  | 36.92       | 0.994   | 0.998          | 6.762  | 6.762     | 6.779        | 99.51          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-0-hook_resid_post-l1-1e-05) | 0     | resid_post | 1e-5      | 98.6             | 1110.9  | 40.46       | 0.993   | 0.988          | 6.762  | 6.763     | 6.908        | 99.23          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-1-hook_mlp_out-l1-1e-05) | 1     | mlp_out    | 1e-5      | 98.4             | 1476.8  | 97.82       | 0.992   | 0.994          | 6.762  | 6.762     | 6.889        | 99.40          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-1-hook_resid_post-l1-1e-05) | 1     | resid_post | 1e-5      | 98.3             | 1508.4  | 27.39       | 0.991   | 0.989          | 6.762  | 6.763     | 6.908        | 99.02          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-2-hook_mlp_out-l1-1e-05) | 2     | mlp_out    | 1e-5      | 98.0             | 1799.7  | 376.0       | 0.992   | 0.998          | 6.762  | 6.762     | 6.803        | 99.44          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-2-hook_resid_post-l1-5e-05) | 2     | resid_post | 5e-5      | 90.6             | 717.84  | 10.11       | 0.944   | 0.960          | 6.762  | 6.767     | 6.908        | 96.34          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-3-hook_mlp_out-l1-1e-05) | 3     | mlp_out    | 1e-5      | 98.1             | 1893.4  | 648.2       | 0.992   | 0.999          | 6.762  | 6.762     | 6.784        | 99.54          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-3-hook_resid_post-l1-1e-05) | 3     | resid_post | 1e-5      | 98.1             | 2053.9  | 77.90       | 0.989   | 0.996          | 6.762  | 6.762     | 6.908        | 99.79          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-4-hook_mlp_out-l1-1e-05) | 4     | mlp_out    | 1e-5      | 98.1             | 1901.2  | 1115.0      | 0.993   | 0.999          | 6.762  | 6.762     | 6.786        | 99.55          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-4-hook_resid_post-l1-1e-05) | 4     | resid_post | 1e-5      | 98.0             | 2068.3  | 156.7       | 0.989   | 0.997          | 6.762  | 6.762     | 6.908        | 99.74          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-5-hook_mlp_out-l1-1e-05) | 5     | mlp_out    | 1e-5      | 98.2             | 1761.5  | 1259.0      | 0.993   | 0.999          | 6.762  | 6.762     | 6.797        | 99.76          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-5-hook_resid_post-l1-1e-05) | 5     | resid_post | 1e-5      | 98.1             | 1953.8  | 228.5       | 0.990   | 0.997          | 6.762  | 6.762     | 6.908        | 99.80          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-6-hook_mlp_out-l1-1e-05) | 6     | mlp_out    | 1e-5      | 98.3             | 1598.0  | 1337.0      | 0.993   | 0.999          | 6.762  | 6.762     | 6.789        | 99.83          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-6-hook_resid_post-l1-1e-05) | 6     | resid_post | 1e-5      | 98.2             | 1717.5  | 321.3       | 0.991   | 0.996          | 6.762  | 6.762     | 6.908        | 99.93          | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-7-hook_mlp_out-l1-1e-05) | 7     | mlp_out    | 1e-5      | 98.2             | 1535.3  | 1300.0      | 0.992   | 0.999          | 6.762  | 6.762     | 6.796        | 100.17         | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-7-hook_resid_post-l1-1e-05) | 7     | resid_post | 1e-5      | 98.2             | 1688.4  | 494.3       | 0.991   | 0.995          | 6.762  | 6.761     | 6.908        | 100.24         | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-8-hook_mlp_out-l1-1e-05) | 8     | mlp_out    | 1e-5      | 97.8             | 1074.5  | 1167.0      | 0.990   | 0.998          | 6.762  | 6.761     | 6.793        | 100.57         | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-8-hook_resid_post-l1-1e-05) | 8     | resid_post | 1e-5      | 98.2             | 1570.8  | 791.3       | 0.991   | 0.992          | 6.762  | 6.761     | 6.908        | 100.41         | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-9-hook_mlp_out-l1-1e-05) | 9     | mlp_out    | 1e-5      | 97.6             | 856.68  | 1076.0      | 0.989   | 0.998          | 6.762  | 6.762     | 6.792        | 100.28         | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-9-hook_resid_post-l1-1e-05) | 9     | resid_post | 1e-5      | 98.2             | 1533.5  | 1053.0      | 0.991   | 0.989          | 6.762  | 6.761     | 6.908        | 100.32         | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-10-hook_mlp_out-l1-1e-05) | 10    | mlp_out    | 1e-5      | 98.1             | 788.49  | 965.5       | 0.991   | 0.998          | 6.762  | 6.762     | 6.772        | 101.50         | 99.80            |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-10-hook_resid_post-l1-1e-05) | 10    | resid_post | 1e-5      | 98.4             | 1292.6  | 1010.0      | 0.992   | 0.987          | 6.762  | 6.760     | 6.908        | 100.83         | 99.99            |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-11-hook_mlp_out-l1-5e-05) | 11    | mlp_out    | 5e-5      | 89.7             | 748.14  | 745.5       | 0.972   | 0.993          | 6.762  | 6.759     | 6.768        | 135.77         | 100              |
| [link](https://huggingface.co/prisma-multimodal/sparse-autoencoder-clip-b-32-sae-vanilla-x64-layer-11-hook_resid_post-l1-1e-05) | 11    | resid_post | 1e-5      | 98.4             | 1405.0  | 1189.0      | 0.993   | 0.987          | 6.762  | 6.765     | 6.908        | 98.03          | 99.99            |

## Vanilla SAEs (CLS only)

| Model | Layer | Sublayer   | l1 coeff. | % Explained var. | Avg CLS L0 | Cos sim | Recon cos sim | CE     | Recon CE | Zero abl CE | % CE recovered | % Alive features |
|-------|-------|------------|-----------|------------------|------------|---------|----------------|--------|-----------|--------------|----------------|------------------|
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_0-hook_resid_post-936.799987792969-82)  | 0     | resid_post | 2e-8      | 82               | 934.83     | 0.98008 | 0.99995        | 6.7622 | 6.7622    | 6.9084       | 99.9984        | 4.33             |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_1-hook_resid_post-314.175018310547-85)  | 1     | resid_post | 8e-6      | 85               | 314.13     | 0.97211 | 0.99994        | 6.7622 | 6.7622    | 6.9083       | 100.00         | 2.82             |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_2-hook_resid_post-711.121887207031-96)  | 2     | resid_post | 9e-8      | 96               | 711.84     | 0.98831 | 0.99997        | 6.7622 | 6.7622    | 6.9083       | 99.9977        | 2.54             |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_3-hook_resid_post-686.334411621094-95)  | 3     | resid_post | 1e-8      | 95               | 687.41     | 0.98397 | 0.99994        | 6.7622 | 6.7622    | 6.9085       | 99.9998        | 4.49             |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_4-hook_resid_post-682.543762207031-95)  | 4     | resid_post | 9e-8      | 95               | 681.08     | 0.98092 | 0.99988        | 6.7622 | 6.7622    | 6.9082       | 100.00         | 15.75            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_5-hook_resid_post-510.356262207031-94)  | 5     | resid_post | 1e-7      | 94               | 506.77     | 0.97404 | 0.99966        | 6.7622 | 6.7622    | 6.9081       | 99.9911        | 16.80            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_6-hook_resid_post-430.556243896484-92)  | 6     | resid_post | 1e-8      | 92               | 423.70     | 0.96474 | 0.99913        | 6.7622 | 6.7622    | 6.9083       | 99.9971        | 29.46            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_7-hook_resid_post-492.959381103516-88)  | 7     | resid_post | 2e-6      | 88               | 492.68     | 0.93899 | 0.99737        | 6.7622 | 6.7622    | 6.9082       | 99.9583        | 51.68            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_8-hook_resid_post-635.018737792969-76)  | 8     | resid_post | 4e-8      | 76               | 623.01     | 0.89168 | 0.99110        | 6.7622 | 6.7625    | 6.9087       | 99.7631        | 82.07            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_9-hook_resid_post-518.621887207031-74)  | 9     | resid_post | 1e-12     | 74               | 521.90     | 0.87076 | 0.98191        | 6.7622 | 6.7628    | 6.9083       | 99.5425        | 93.68            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_10-hook_resid_post-552.512512207031-74) | 10    | resid_post | 3e-7      | 74               | 533.94     | 0.87646 | 0.96514        | 6.7622 | 6.7635    | 6.9082       | 99.1070        | 99.98            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-CLS_11-hook_resid_post-383.75-65)          | 11    | resid_post | 1e-8      | 65               | 386.09     | 0.81890 | 0.89607        | 6.7622 | 6.7853    | 6.9086       | 84.1918        | 99.996           |

## Top K SAEs (CLS only, k = 64)

| Model | Layer | Sublayer   | % Explained var. | Avg CLS L0 | Cos sim | Recon cos sim | CE     | Recon CE | Zero abl CE | % CE recovered | % Alive features |
|-------|-------|------------|------------------|------------|---------|----------------|--------|-----------|--------------|----------------|------------------|
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_0-hook_resid_post)  | 0     | resid_post | 90               | 64         | 0.98764 | 0.99998        | 6.7622 | 6.7622    | 6.9084       | 99.995         | 46.80            |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_1-hook_resid_post)  | 1     | resid_post | 96               | 64         | 0.99429 | 0.99999        | 6.7622 | 6.7622    | 6.9083       | 100.00         | 4.86             |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_2-hook_resid_post)  | 2     | resid_post | 96               | 64         | 0.99000 | 0.99998        | 6.7622 | 6.7622    | 6.9083       | 100.00         | 5.50             |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_3-hook_resid_post)  | 3     | resid_post | 95               | 64         | 0.98403 | 0.99995        | 6.7622 | 6.7622    | 6.9085       | 100.00         | 5.21             |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_4-hook_resid_post)  | 4     | resid_post | 94               | 64         | 0.97485 | 0.99986        | 6.7621 | 6.7622    | 6.9082       | 99.998         | 6.81             |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_5-hook_resid_post)  | 5     | resid_post | 93               | 64         | 0.96985 | 0.99962        | 6.7622 | 6.7622    | 6.9081       | 99.997         | 21.89            |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_6-hook_resid_post)  | 6     | resid_post | 92               | 64         | 0.96401 | 0.99912        | 6.7622 | 6.7622    | 6.9083       | 100.00         | 28.81            |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_7-hook_resid_post)  | 7     | resid_post | 90               | 64         | 0.95057 | 0.99797        | 6.7622 | 6.7621    | 6.9082       | 100.03         | 65.84            |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_8-hook_resid_post)  | 8     | resid_post | 87               | 64         | 0.93029 | 0.99475        | 6.7622 | 6.7620    | 6.9087       | 100.11         | 93.75            |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_9-hook_resid_post)  | 9     | resid_post | 85               | 64         | 0.91814 | 0.98865        | 6.7622 | 6.7616    | 6.9083       | 100.43         | 98.90            |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_10-hook_resid_post) | 10    | resid_post | 86               | 64         | 0.93072 | 0.97929        | 6.7622 | 6.7604    | 6.9082       | 101.19         | 94.55            |
| [link](https://huggingface.co/Prisma-Multimodal/sae-top_k-64-cls_only-layer_11-hook_resid_post) | 11    | resid_post | 84               | 64         | 0.91880 | 0.94856        | 6.7622 | 6.7578    | 6.9086       | 102.97         | 97.99            |

## Vanilla Spatial Patches

| Model | Layer | Sublayer   | l1 coeff. | % Explained var. | Avg L0   | Cos sim | Recon cos sim | CE     | Recon CE | Zero abl CE | % CE recovered | % Alive features |
|-------|-------|------------|-----------|------------------|----------|---------|----------------|--------|-----------|--------------|----------------|------------------|
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_0-hook_resid_post-989.203430175781-99)  | 0     | resid_post | 1e-12     | 99               | 989.19   | 0.99    | 0.99           | 6.7621 | 6.7621    | 6.9084       | 99.9981        | 100.00           |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_1-hook_resid_post-757.82958984375-99)   | 1     | resid_post | 3e-11     | 99               | 757.83   | 0.99    | 0.99           | 6.7622 | 6.7622    | 6.9083       | 99.9969        | 45.39            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_2-hook_resid_post-1007.89801025391-99)  | 2     | resid_post | 4e-12     | 99               | 1007.89  | 0.99    | 0.99           | 6.7622 | 6.7622    | 6.9083       | 100.00         | 97.93            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_3-hook_resid_post-935.601989746094-99)  | 3     | resid_post | 2e-8      | 99               | 935.06   | 0.99    | 0.99           | 6.7622 | 6.7622    | 6.9085       | 99.9882        | 100.00           |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_4-hook_resid_post-965.410095214844-99)  | 4     | resid_post | 3e-8      | 99               | 965.15   | 0.99    | 0.99           | 6.7622 | 6.7622    | 6.9082       | 99.9842        | 100.00           |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_5-hook_resid_post-964.674072265625-99)  | 5     | resid_post | 1e-8      | 99               | 966.38   | 0.99    | 0.99           | 6.7622 | 6.7622    | 6.9081       | 99.9961        | 100.00           |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_6-hook_resid_post-1006.57165527344-99)  | 6     | resid_post | 1e-8      | 99               | 1006.62  | 0.99    | 0.99           | 6.7622 | 6.7622    | 6.9083       | 100.00         | 99.97            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_7-hook_resid_post-984.1376953125-99)    | 7     | resid_post | 1e-8      | 99               | 984.19   | 0.99    | 0.99           | 6.7622 | 6.7622    | 6.9082       | 100.00         | 100.00           |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_8-hook_resid_post-965.125-99)           | 8     | resid_post | 3e-8      | 99               | 965.12   | 0.99    | 1.00           | 6.7622 | 6.7622    | 6.9087       | 100.00         | 92.37            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_9-hook_resid_post-854.891540527344-99)  | 9     | resid_post | 9e-8      | 99               | 854.92   | 0.99    | 1.00           | 6.7622 | 6.7622    | 6.9083       | 99.9991        | 85.43            |
| [link](https://huggingface.co/Prisma-Multimodal/imagenet-sweep-vanilla-x64-Spatial_max_11-hook_resid_post-829.0498046875-99)   | 11    | resid_post | 3e-7      | 99               | 829.09   | 0.99    | 1.00           | 6.7622 | 6.7622    | 6.9086       | 100.00         | 55.71            |

## Top K Transcoders (All Patches)

*CLIP Top-K transcoder performance metrics for all patches.*

| Model                                                                 | Layer | Block | % Explained var. | k    | Avg CLS L0 | Cos sim | CE     | Recon CE | Zero abl CE | % CE recovered |
|-----------------------------------------------------------------------|-------|-------|------------------|------|------------|---------|--------|----------|-------------|----------------|
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-768-x64-all_patches_0-mlp-96)  | 0     | MLP   | 96               | 768  | 767        | 0.9655  | 6.7621 | 6.7684   | 6.8804      | 94.68          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-256-x64-all_patches_1-mlp-94)  | 1     | MLP   | 94               | 256  | 255        | 0.9406  | 6.7621 | 6.7767   | 6.8816      | 87.78          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-1024-x64-all_patches_2-mlp-93) | 2     | MLP   | 93               | 1024 | 475        | 0.9758  | 6.7621 | 6.7681   | 6.7993      | 83.92          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-1024-x64-all_patches_3-mlp-90) | 3     | MLP   | 90               | 1024 | 825        | 0.9805  | 6.7621 | 6.7642   | 6.7999      | 94.42          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-512-x64-all_patches_4-mlp-76)  | 4     | MLP   | 76               | 512  | 29         | 0.9830  | 6.7621 | 6.7636   | 6.8080      | 96.76          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-1024-x64-all_patches_5-mlp-91) | 5     | MLP   | 91               | 1024 | 1017       | 0.9784  | 6.7621 | 6.7643   | 6.8296      | 96.82          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-1024-x64-all_patches_6-mlp-94) | 6     | MLP   | 94               | 1024 | 924        | 0.9756  | 6.7621 | 6.7630   | 6.8201      | 98.40          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-1024-x64-all_patches_7-mlp-97) | 7     | MLP   | 97               | 1024 | 1010       | 0.9629  | 6.7621 | 6.7631   | 6.8056      | 97.68          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-1024-x64-all_patches_8-mlp-98) | 8     | MLP   | 98               | 1024 | 1023       | 0.9460  | 6.7621 | 6.7630   | 6.8017      | 97.70          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-1024-x64-all_patches_9-mlp-98) | 9     | MLP   | 98               | 1024 | 1023       | 0.9221  | 6.7621 | 6.7630   | 6.7875      | 96.50          |
| [link](https://huggingface.co/Prisma-Multimodal/CLIP-transcoder-topk-1024-x64-all_patches_10-mlp-97)| 10    | MLP   | 97               | 1024 | 1019       | 0.9334  | 6.7621 | 6.7636   | 6.7860      | 93.95          |

# DINO-B-32 Sparse Autoencoder Performance

## Vanilla SAEs (All Patches)

| Model | Layer | Sublayer | Avg L0 | % Explained var. | Avg CLS L0 | Cos sim | CE | Recon CE | Zero abl CE | % CE Recovered |
|-------|-------|----------|--------|------------------|-------------|----------|------|-----------|---------------|----------------|
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_0-resid_post-507-98)  | 0  | resid_post | 507  | 98 | 347  | 0.95009 | 1.885033 | 1.936518 | 7.2714 | 99.04 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_1-resid_post-549-95)  | 1  | resid_post | 549  | 95 | 959  | 0.93071 | 1.885100 | 1.998274 | 7.2154 | 97.88 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_2-resid_post-661-95)  | 2  | resid_post | 812  | 95 | 696  | 0.95600 | 1.885134 | 2.006115 | 7.2015 | 97.72 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_3-resid_post-989-95)  | 3  | resid_post | 989  | 95 | 616  | 0.96315 | 1.885131 | 1.961913 | 7.2068 | 98.56 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_4-resid_post-876-99)  | 4  | resid_post | 876  | 99 | 845  | 0.99856 | 1.885224 | 1.883169 | 7.1636 | 100.04 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_5-resid_post-1001-98) | 5  | resid_post | 1001 | 98 | 889  | 0.99129 | 1.885353 | 1.875520 | 7.1412 | 100.19 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_6-resid_post-962-99)  | 6  | resid_post | 962  | 99 | 950  | 0.99945 | 1.885239 | 1.872594 | 7.1480 | 100.24 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_7-resid_post-1086-98) | 7  | resid_post | 1086 | 98 | 1041 | 0.99341 | 1.885371 | 1.869443 | 7.1694 | 100.30 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_8-resid_post-530-90)  | 8  | resid_post | 530  | 90 | 529  | 0.94750 | 1.885511 | 1.978638 | 7.1315 | 98.22 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_9-resid_post-1105-99) | 9  | resid_post | 1105 | 99 | 1090 | 0.99541 | 1.885341 | 1.894026 | 7.0781 | 99.83 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_10-resid_post-835-99) | 10 | resid_post | 835  | 99 | 839  | 0.99987 | 1.885371 | 1.884487 | 7.3606 | 100.02 |
| [link](https://huggingface.co/Prisma-Multimodal/DINO-vanilla-x64-all_patches_11-resid_post-1085-99) | 11 | resid_post | 1085 | 99 | 1084 | 0.99673 | 1.885370 | 1.911608 | 6.9078 | 99.48 |


