<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>LLM Fine-Tuning </title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
            background-color: #0d1117;
            color: #c9d1d9;
            line-height: 1.6;
            padding: 32px;
            max-width: 1000px;
            margin: auto;
        }
        h1, h2, h3 {
            color: #58a6ff;
        }
        code, pre {
            background: #161b22;
            color: #c9d1d9;
            padding: 8px;
            border-radius: 6px;
            overflow-x: auto;
        }
        pre {
            padding: 16px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 16px 0;
        }
        table, th, td {
            border: 1px solid #30363d;
        }
        th, td {
            padding: 10px;
            text-align: left;
        }
        th {
            background-color: #161b22;
        }
        ul {
            margin-left: 20px;
        }
        .badge {
            display: inline-block;
            background: #238636;
            color: white;
            padding: 4px 10px;
            border-radius: 999px;
            font-size: 12px;
            margin-right: 6px;
        }
        footer {
            margin-top: 40px;
            font-size: 14px;
            color: #8b949e;
            border-top: 1px solid #30363d;
            padding-top: 16px;
        }
    </style>
</head>
<body>

<h1>🔧 LLM Fine-Tuning Playground</h1>
<p>
    <span class="badge">LoRA</span>
    <span class="badge">QLoRA</span>
    <span class="badge">Unsloth</span>
</p>

<p>
This repository documents <strong>hands-on fine-tuning experiments on Large Language Models (LLMs)</strong>
using parameter-efficient techniques on limited GPU environments.
The focus is on <strong>real inference behavior</strong>, not just training scripts.
</p>

<hr>

<h2>🚀 What This Repository Covers</h2>
<ul>
    <li>Fine-tuning open-source LLMs on low VRAM GPUs</li>
    <li>LoRA and QLoRA based training workflows</li>
    <li>Hyperparameter impact analysis</li>
    <li>Base vs fine-tuned inference comparison</li>
    <li>Optimized training using Unsloth</li>
</ul>

<h2>🧠 Models Fine-Tuned</h2>
<ul>
    <li>LLaMA-family models</li>
    <li>Mistral</li>
    <li>Qwen</li>
    <li>Nemotron</li>
</ul>

<h2>🛠️ Techniques Used</h2>

<h3>LoRA (Low-Rank Adaptation)</h3>
<ul>
    <li>Trainable low-rank adapters</li>
    <li>Frozen base model weights</li>
    <li>Stable and efficient fine-tuning</li>
</ul>

<h3>QLoRA</h3>
<ul>
    <li>4-bit quantized base model</li>
    <li>Enables training on consumer GPUs</li>
    <li>Slight trade-off in long-context precision</li>
</ul>

<h3>Unsloth</h3>
<ul>
    <li>Faster training and inference</li>
    <li>Lower memory usage</li>
    <li>Optimized attention kernels</li>
</ul>

<h2>📂 Repository Structure</h2

<h2>⚙️ Training Setup</h2>
<ul>
    <li><strong>Platform:</strong> Google Colab / Kaggle</li>
    <li><strong>GPU:</strong> T4 / P100</li>
    <li><strong>Precision:</strong> FP16 / 4-bit</li>
    <li><strong>Batching:</strong> Gradient Accumulation</li>
</ul>

<h2>📊 Hyperparameters Explored</h2>

<table>
    <tr>
        <th>Parameter</th>
        <th>Values Tested</th>
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
    <tr>
        <td>Dataset Size</td>
        <td>Small → Medium</td>
    </tr>
</table>

<h2>🔍 Inference Observations</h2>
<ul>
    <li>Improved instruction adherence</li>
    <li>Reduced hallucinations on domain prompts</li>
    <li>More structured and consistent outputs</li>
    <li>Overfitting observed with small datasets + high epochs</li>
</ul>

<h2>🧪 Evaluation Method</h2>
<ul>
    <li>Prompt-based comparison (before vs after)</li>
    <li>Task completion quality</li>
    <li>Response structure and consistency</li>
</ul>

<h2>🧭 Next Experiments</h2>
<ul>
    <li>RAG + fine-tuned models</li>
    <li>Multi-dataset instruction blending</li>
    <li>Adapter merging and export</li>
    <li>Deployment-focused quantization analysis</li>
</ul>

<footer>
    <p>
        ⚠️ Disclaimer: All experiments are for educational and research purposes using publicly available models and datasets.
    </p>
</footer>

</body>
</html>
