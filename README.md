# SWE-Lego Website Mirror

This repository preserves the legacy GitHub Pages URL at <https://swe-lego.github.io/> after the organization moved from **SWE-Lego** to **LegoX**.

The canonical website source is maintained in [LegoX/swe-lego.github.io](https://github.com/LegoX/swe-lego.github.io). A GitHub Actions workflow publishes that source directly to the legacy URL and can be triggered manually if the website ever needs to be republished.

## Published paths

| Path | Source of truth |
|------|-----------------|
| `/` | [LegoX/swe-lego.github.io](https://github.com/LegoX/swe-lego.github.io) (`main`) |
| `/SWE-Review/` | [LegoX/SWE-Review](https://github.com/LegoX/SWE-Review) (`gh-pages`) |

`/SWE-Review/` exists because the SWE-Review paper ([arXiv:2607.06065](https://arxiv.org/abs/2607.06065)) hardcodes `https://swe-lego.github.io/SWE-Review` as its project page. The published PDF cannot be changed, so this repository serves that path. GitHub redirects repository and org URLs after a rename, but GitHub Pages does not — hence the explicit deployment.

Website changes should be made in the canonical LegoX repositories rather than copied into this repository. Re-run the workflow (`workflow_dispatch`) after updating either source to republish.
