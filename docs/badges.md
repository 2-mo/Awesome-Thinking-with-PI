# Badges Style Guide

Consistent badge styles for papers, code, and related links across this repo.

## General rules

- Place badges right below the paper title.
- Order: Paper → Code → Stars (or combined) → Homepage/Project → Dataset → Video → Others.
- Prefer direct PDF for “Paper”; otherwise use arXiv/OpenReview.
- Keep titles as “Title (Venue Year)”; avoid duplicating venue in badges.
- Use short, stable provider names and brand colors where helpful.

## Badge palette (shields.io)

- Paper (PDF):
  - Markdown: `[![Paper](https://img.shields.io/badge/Paper-PDF-b31b1b)](<pdf_url>)`
  - Color: `b31b1b` (paper red); use for CVF/IEEE/ACM when linking direct PDF.
- arXiv (follow think2reason style):
  - Markdown: `[![arXiv](https://img.shields.io/badge/arXiv-YYMM.NNNNN-b31b1b?logo=arxiv)](<arxiv_abs_or_pdf_url>)`
  - Example: `2503.21776` → `https://arxiv.org/pdf/2503.21776` or `https://arxiv.org/abs/2503.21776`
  - Tip: Prefer the PDF link when stable; otherwise use the abs page. If versioning matters, append `vX` in the label: `arXiv-2503.21776v2`.
- OpenReview:
  - Markdown: `[![OpenReview](https://img.shields.io/badge/OpenReview-Link-1abc9c?logo=openreview)](<openreview_url>)`
- IEEE Xplore:
  - Markdown: `[![IEEE](https://img.shields.io/badge/IEEE-Xplore-00629B)](<ieee_xplore_url>)`
- ACM DL:
  - Markdown: `[![ACM](https://img.shields.io/badge/ACM-DL-00599C)](<acm_dl_url>)`
- Code (GitHub):
  - Markdown: `[![Code](https://img.shields.io/badge/Code-GitHub-black?logo=github)](<repo_url>)`
- Stars (GitHub):
  - Social (recommended): `[![Stars](https://img.shields.io/github/stars/<owner>/<repo>?style=social&label=Stars&logo=github)](<repo_url>)`
  - Flat (numeric): `[![Stars](https://img.shields.io/github/stars/<owner>/<repo>?label=Stars&color=black&logo=github)](<repo_url>)`
- Combined Code+Stars (optional, one badge):
  - Social: `[![Code](https://img.shields.io/github/stars/<owner>/<repo>?style=social&label=Code&logo=github)](<repo_url>)`
  - Flat: `[![Code](https://img.shields.io/github/stars/<owner>/<repo>?label=Code&color=black&logo=github)](<repo_url>)`
- Homepage / Project (Website):
  - Markdown: `[![Homepage](https://img.shields.io/badge/Homepage-Website-0a84ff?logo=safari)](<project_or_homepage_url>)`
  - Alternative label: use `Project-Website` for research pages.
- Zhihu (explainer article):
  - Markdown: `[![Zhihu](https://img.shields.io/badge/Zhihu-Explainer-informational?logo=zhihu)](<zhihu_article_url>)`
- WeChat Official Account (explainer):
  - Markdown: `[![WeChat](https://img.shields.io/badge/WeChat-Explainer-07C160?logo=wechat)](<weixin_mp_article_url>)`
  - Color: `07C160` (WeChat green)
- Model weights (Hugging Face):
  - Markdown: `[![Model](https://img.shields.io/badge/Model-HuggingFace-ffcc4d?logo=huggingface)](<hf_model_url>)`
- Demo:
  - Hugging Face Spaces: `[![Demo](https://img.shields.io/badge/Demo-Spaces-ffcc4d?logo=huggingface)](<spaces_url>)`
  - Gradio: `[![Demo](https://img.shields.io/badge/Demo-Gradio-00b4b6?logo=gradio)](<gradio_url>)`
  - Colab: `[![Colab](https://img.shields.io/badge/Colab-Notebook-F9AB00?logo=google-colab)](<colab_url>)`
- Papers with Code / Leaderboard:
  - Markdown: `[![Papers with Code](https://img.shields.io/badge/Papers_with_Code-SOTA-1B1F23?logo=paperswithcode)](<pwc_url>)`
- License (repo):
  - Markdown: `[![License](https://img.shields.io/github/license/<owner>/<repo>?color=blue)](<repo_url>/blob/main/LICENSE)`
- DOI / Zenodo:
  - DOI: `[![DOI](https://img.shields.io/badge/DOI-10.xxxx%2Fxxxx-4B8BBE)](<doi_url>)`
  - Zenodo: `[![Zenodo](https://img.shields.io/badge/DOI-Zenodo-1682e6?logo=zenodo)](<zenodo_url>)`
- Google Scholar:
  - Markdown: `[![Scholar](https://img.shields.io/badge/Google_Scholar-Citations-4285F4?logo=googlescholar)](<scholar_profile_or_paper_url>)`
- Video:
  - YouTube: `[![Video](https://img.shields.io/badge/Video-YouTube-FF0000?logo=youtube)](<youtube_url>)`
  - Bilibili: `[![Bilibili](https://img.shields.io/badge/Bilibili-Video-00A1D6?logo=bilibili)](<bilibili_url>)`
- Dataset:
  - Generic: `[![Dataset](https://img.shields.io/badge/Dataset-Link-2CA5E0?logo=google-drive)](<dataset_url>)`
  - Kaggle: `[![Dataset](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?logo=kaggle)](<kaggle_url>)`
  - BaiduPan: `[![Dataset](https://img.shields.io/badge/Dataset-BaiduPan-2932e1?logo=baidu)](<baidupan_url>)`

Notes:

- Use either the combined badge or the separate `Code` + `Stars` pair; avoid showing both.
- Use English labels for consistency across files; localized variants are optional if a section is fully Chinese.
- Prefer not to use inline HTML in README; keep badges as Markdown for simplicity.
- Provide concise alt text (the bracket text before the URL) describing the target.

## Template (copy/paste)

```markdown
### Title: Paper Name (Venue Year)

[![Paper](https://img.shields.io/badge/Paper-PDF-b31b1b)](<pdf_url>)
[![arXiv](https://img.shields.io/badge/arXiv-YYMM.NNNNN-b31b1b?logo=arxiv)](<arxiv_url>)
[![Code](https://img.shields.io/github/stars/<owner>/<repo>?style=social&label=Code&logo=github)](<repo_url>)
[![Homepage](https://img.shields.io/badge/Homepage-Website-0a84ff?logo=safari)](<project_or_homepage_url>)
[![Zhihu](https://img.shields.io/badge/Zhihu-Explainer-informational?logo=zhihu)](<zhihu_article_url>)
[![WeChat](https://img.shields.io/badge/WeChat-Explainer-07C160?logo=wechat)](<weixin_mp_article_url>)
[![Model](https://img.shields.io/badge/Model-HuggingFace-ffcc4d?logo=huggingface)](<hf_model_url>)
[![Demo](https://img.shields.io/badge/Demo-Spaces-ffcc4d?logo=huggingface)](<spaces_url>)
[![Colab](https://img.shields.io/badge/Colab-Notebook-F9AB00?logo=google-colab)](<colab_url>)
[![Dataset](https://img.shields.io/badge/Dataset-Link-2CA5E0?logo=google-drive)](<dataset_url>)
[![Video](https://img.shields.io/badge/Video-YouTube-FF0000?logo=youtube)](<video_url>)
[![License](https://img.shields.io/github/license/<owner>/<repo>?color=blue)](<repo_url>/blob/main/LICENSE)
[![DOI](https://img.shields.io/badge/DOI-10.xxxx%2Fxxxx-4B8BBE)](<doi_url>)

Highlight: One-sentence takeaway of the main contribution.
```

Alternative (minimal):

```markdown
### Title: Paper Name (Venue Year)

[![Paper](https://img.shields.io/badge/Paper-PDF-b31b1b)](<pdf_url>)
[![Code](https://img.shields.io/github/stars/<owner>/<repo>?style=social&label=Code&logo=github)](<repo_url>)
```

## Notes

- Use either Paper-PDF or arXiv (or both). If both available, list PDF first.
- For CVPR OpenAccess (thecvf.com) PDF, still use `Paper-PDF` badge.
- For non-PDF paper pages (e.g., Springer/Elsevier landing pages), use:
  - `[![Paper](https://img.shields.io/badge/Paper-Page-6c757d)](<landing_page_url>)`
- Keep badge text short; avoid long identifiers in labels.
