# Dreambooth-style fine tuning of Stable Diffusion models

[![Train In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/brian6091/Dreambooth/blob/main/Dreambooth_colab.ipynb)

Yet another notebook for training Stable Diffusion models.

Tested with Tesla T4 and A100 GPUs.

Tested with [Stable Diffusion v1-5](https://huggingface.co/runwayml/stable-diffusion-v1-5) and [Stable Diffusion v2-base](https://huggingface.co/stabilityai/stable-diffusion-2-base).

There are lots of notebooks for Dreambooth-style training. This one borrows elements from [
ShivamShrirao's](https://github.com/ShivamShrirao/diffusers) implementation, but is distinguished by some features:
* based on [Hugging Face](https://huggingface.co/) [Diffusers🧨](https://github.com/huggingface/diffusers) implementation so it's easy to stay up-to-date with rapid access to new features
* exposes lesser-known parameters for experimentation (ADAM optimizer parameters, exposes [cosine_with_restarts](https://huggingface.co/transformers/v2.9.1/main_classes/optimizer_schedules.html#transformers.get_cosine_with_hard_restarts_schedule_with_warmup) learning rate scheduler, etc), all of which are dumped to a json file so you can remember what you did
* training loss and prior class loss are tracked separately (can be visualized using tensorboard)
* option to generate exponentially-weighted moving average (EMA) weights for the unet
* easily switch in different variational autoencoders (VAE) or text encoders
* inference with trained models is done using [Diffusers🧨](https://github.com/huggingface/diffusers) pipelines, does not rely on any web-apps


[<a href="https://www.buymeacoffee.com/jvsurfsqv" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="45px" width="162px" alt="Buy Me A Coffee"></a>](https://www.buymeacoffee.com/jvsurfsqv)
