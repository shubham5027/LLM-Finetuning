<h1 align="center">🔧 LLM Fine-Tuning </h1>

<p align="center">
  <b>LoRA · QLoRA · Unsloth · Low-VRAM Training</b>
</p>

<p align="center">
  Hands-on fine-tuning experiments on Large Language Models (LLMs)  
  with a focus on real inference behavior.
</p>

<hr/>

<h2>🚀 What This Repository Covers</h2>

<ul>
  <li>Fine-tuning open-source LLMs on low VRAM GPUs</li>
  <li>LoRA and QLoRA based training workflows</li>
  <li>Unsloth optimized training & inference</li>
  <li>Hyperparameter impact analysis</li>
  <li>Base vs Fine-Tuned inference comparison</li>
</ul>

<h2>🧠 Models Fine-Tuned</h2>

<ul>
  <li>LLaMA-family models</li>
  <li>Mistral</li>
  <li>Qwen</li>
  <li>Nemotron</li>
</ul>

<h2>🛠️ Techniques Used</h2>

<h3>🔹 LoRA (Low-Rank Adaptation)</h3>
<ul>
  <li>Trainable low-rank adapters</li>
  <li>Frozen base model weights</li>
  <li>Efficient and stable fine-tuning</li>
</ul>

<h3>🔹 QLoRA</h3>
<ul>
  <li>4-bit quantized base model</li>
  <li>Enables fine-tuning on consumer GPUs</li>
  <li>Minor trade-off in long-context precision</li>
</ul>

<h3>🔹 Unsloth</h3>
<ul>
  <li>Faster training and inference</li>
  <li>Reduced VRAM usage</li>
  <li>Optimized attention & adapter kernels</li>
</ul>

<h2>📂 Repository Structure</h2>


<h2>⚙️ Training Setup</h2>

<table>
  <tr>
    <th align="left">Platform</th>
    <td>Google Colab / Kaggle</td>
  </tr>
  <tr>
    <th align="left">GPU</th>
    <td>T4 / P100</td>
  </tr>
  <tr>
    <th align="left">Precision</th>
    <td>FP16 / 4-bit</td>
  </tr>
  <tr>
    <th align="left">Batching</th>
    <td>Gradient Accumulation</td>
  </tr>
</table>

<h2>📊 Hyperparameters Explored</h2>

<table>
  <tr>
    <th align="left">Parameter</th>
    <th align="left">Values Tested</th>
  </tr>
  <tr>
    <td>LoRA Rank (r)</td>
    <td>8, 16, 32</td>
  </tr>
  <tr>
    <td>Alpha</td>
    <td>16, 32, 64</td>
  </tr>
  <tr>
    <td>Learning Rate</td>
    <td>1e-4 → 2e-5</td>
  </tr>
  <tr>
    <td>Epochs</td>
    <td>1 – 5</td>
  </tr>
</table>

<h2>🔍 Inference Observations</h2>

<ul>
  <li>Improved instruction adherence</li>
  <li>Reduced hallucination for domain prompts</li>
  <li>More structured outputs</li>
  <li>Overfitting with small datasets + high epochs</li>
</ul>

<h2>🧪 Evaluation Strategy</h2>

<ul>
  <li>Prompt-based comparison (before vs after)</li>
  <li>Task completion accuracy</li>
  <li>Response consistency and structure</li>
</ul>

<h2>🧠 Key Learnings</h2>

<ul>
  <li>Dataset quality &gt; model size</li>
  <li>LoRA rank tuning matters more than epochs</li>
  <li>Unsloth speeds up experimentation significantly</li>
  <li>Inference behavior is the real success metric</li>
</ul>

<h2>🧭 Next Experiments</h2>

<ul>
  <li>RAG + fine-tuned models</li>
  <li>Multi-dataset instruction blending</li>
  <li>Adapter merging & export</li>
  <li>Deployment-focused quantization</li>
</ul>

<hr/>

<p align="center">
  ⚠️ <b>Disclaimer:</b> All experiments are for educational and research purposes using publicly available models and datasets.
</p>
