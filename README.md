# BIDS Tracula (under development)

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Reconstructs major white matter pathways with FreeSurfer TRACULA (bids/tracula v6.0.0-4 BIDS App) from a T1-weighted image, DWI and an optional FreeSurfer directory.**

Arranges the T1w and DWI inputs into a one-subject BIDS dataset and runs the bids/tracula BIDS App (FreeSurfer 6 TRACULA, all stages) on it, reusing an existing FreeSurfer subject directory when given. The App is marked as under development. It needs a FreeSurfer license and can take up to a day of compute.

| | |
|---|---|
| 📥 **Inputs** | `neuro/anat/t1w` · `neuro/dwi` · `neuro/freesurfer` (optional) |
| 📤 **Outputs** | `raw` |
| 🐳 **Container** | `bids/tracula:v6.0.0-4` |
| ⚙️ **Resources** | 8 CPUs · 24 h walltime |
| 🔑 **Requires** | `FREESURFER_LICENSE` |
| 🔗 **Run it** | [doi.org/10.25663/bl.app.76](https://doi.org/10.25663/bl.app.76) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `t1` | `neuro/anat/t1w` | yes | T1 image |
| `dwi` | `neuro/dwi` | yes | DWI image |
| `freesurfer` | `neuro/freesurfer` | no | Optional FreeSurfer subject directory for the same subject; passed to TRACULA with --freesurfer_dir so recon-all is not rerun. |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `tracula` | `raw` | TRACULA output directory for the subject as produced by the bids/tracula App. |

<!-- brainlife-app:end -->

