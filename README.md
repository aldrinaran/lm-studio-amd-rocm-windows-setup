# 🚀 LM Studio + AMD ROCm GPU Acceleration on Windows (Tested on RX 7800 XT)

This is a step-by-step guide to enable **GPU offload in LM Studio** using an **AMD GPU with ROCm backend on Windows**.  
Tested on **RX 7800 XT** using **HIP SDK 6.2.4**, this setup boosted performance from **~8 tokens/sec (CPU)** to **~68 tokens/sec (GPU)** using Qwen 7B Q4_K_M.

> if you want to use LM Studio with an AMD GPU on Windows, this might save you a lot of headache!

---

## 🧰 Requirements

- AMD GPU (tested: **RX 7800 XT**)
- [HIP SDK 6.2.4](https://www.amd.com/en/developer/resources/rocm-hub/hip-sdk.html) installed
- Latest version of [LM Studio](https://lmstudio.ai) (Windows)

---

## ⚙️ Setup Steps

1. **Install HIP SDK 6.2.4**  
   👉 https://www.amd.com/en/developer/resources/rocm-hub/hip-sdk.html

2. **Launch LM Studio**, then go to:
   - `App Settings → Runtime`

3. Under **Runtime Extension Packs**, click:
   - ✅ `Download ROCm llama.cpp (Windows)`

4. Then go to **My Engines** :
   - Set **Default Selections** to:
     - ✅ `ROCm llama.cpp (Windows)`

5. Load a **GGUF model** (e.g. Qwen 7B Q4_K_M or Mistral 7B Q4_K_M)

6. Run a prompt and check performance:
