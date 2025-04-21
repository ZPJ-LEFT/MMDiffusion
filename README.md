# MMDiffusion

面向 AIGC 的图像生成需求，结合 Diffusion 技术部署图像生成算法，实现基于文本、图像、音频等多模态条件控制的多风格图像生成，并对推理效率进行优化。

## DDPM算法

基于 DDPM 实现无条件的随机图像生成，然后利用 Classifier-free Guidance，利用文本、图像等多模态信息实现受控图像生成。

## Stable Diffusion算法

调研 Stable Diffusion 核心技术 (如 CLIP、VAE、DiT 等)，复现 SD1.5 实现文本生成图像，利用 ControlNet、LORA 和 Dreambooth 技术，实现风格迁移、个性注入等。

## 推理效率优化

试验 DDIM、Euler、Heun、LMS、DPM 等加速采样器，利用 DeepCache 实现对 UNet 中间特征的缓存复用，无需重训练即可将推理速度提升至原来的 1.5-2 倍。

# 参考资料

- [Diffuser GitHub](https://github.com/huggingface/diffusers/tree/main)
- [Diffuser Docs](https://huggingface.co/docs/diffusers/quicktour)
