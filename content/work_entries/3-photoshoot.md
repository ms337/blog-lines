---
layout: page
title: Photoshoot
category: devproject
---

(On hold: could not solve the technical problem to get a releasable MVP)

Pursued a start-up that enables users to pay and get new, AI-generated, realistic photos for their social media, Tinder, etc. Did 90% the technical work including model implementation, data engineering, model training and backend engineering, with 10% done by friends working part-time.  

[Rick](https://ricksugden.com/) is my co-founder.

- Iterated over 12 GAN-based models built from SOTA research. 
- Implemented advanced techniques such as distributed training (DDP), mixed-precision training and code profiling.
- Built web scrapers to get 800K+ training images from ecommerce sites and built a custom data processing pipeline to assembled a cleaned, curated training and evaluation datasets.

Launched but model is very poor at generalizing at real world inputs even though it works well with training data. Currently trying solutions with more data, and new architectures including diffusion models.

You can see more technical detail in our training dashboards covering all model details, data details, example generations and training logs:

[WandB Dashboard](https://wandb.ai/msinghal/spgan_spliced_runs?workspace=user-msinghal)

