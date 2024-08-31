---
title: "MoRAG"
layout: gridlay
excerpt: "MoRAG"
sitemap: false
permalink: /
---

[comment]: Title
<h2 align="center">Action-GPT:<br>Leveraging Large-scale Language Models for Improved and
Generalized Action Generation</h2>

[comment]: Authors
<p style="text-align: center;">
<a href="https://www.linkedin.com/in/sai-shashank-54288219b" style="color: #CC0000"> Sai Shashank Kalakonda</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://shubhmaheshwari.github.io/website" style="color: #CC0000"> Shubh Maheshwari</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://ravika.github.io" style="color: #CC0000"> Ravi Kiran Sarvadevabhatla</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</p>

<p style="text-align: center;">

[Paper](https://arxiv.org/abs/2211.15603){: .btn}
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

[Code](https://github.com/actiongpt/actiongpt){: .btn}
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

</p>


<center>
<figure>
    <div class="embed-container">
        <img src="{{ site.url }}{{ site.baseurl }}/images/actiongpt/teaser.gif" width="75%" />
    </div>
    <p>&nbsp;</p>
    <figcaption>
        Sample text conditioned action generations from our large language model based approach (Action-GPT-TEACH). By incorporating large language models, our approach results in noticeably improved generation quality for seen and useen categories.
    </figcaption>
</figure>
</center>

<hr style="border: 1px solid #555555;">

<center>

<h3 align="center"> Abstract </h3>
</center>
We introduce Action-GPT,
- A plug and play framework for incorporating Large Language Models (LLMs) into text-based action generation models
- By carefully crafting prompts for LLMs, we generate richer and fine-grained descriptions of the action.
- We show that utilizing these detailed descriptions instead of the original action phrases leads to better alignment of text and motion spaces.
- Our experiments show qualitative and quantitative improvement in the quality of synthesized motions produced by recent text-to-motion models.
- Code, pretrained models and sample videos will be made available. 

<hr style="border: 1px solid #555555;">

<h3 align="center"> Motivation </h3> 
<center>
<figure>
    <div class="embed-container">
        <img src="{{ site.url }}{{ site.baseurl }}/images/actiongpt/motivation.gif" width="100%" />
    </div>
    <p>&nbsp;</p>
    <figcaption>
        Action-GPT Motivation: We generate richer and fine-grained body movement descriptions of the actions, by carefully prompting large-language models. These detailed descriptions instead of the original action phrases leads to better alignment of text and motion spaces resulting in an enhanced quality of motion sequence generations.
    </figcaption>
</figure>
</center>

<hr style="border: 1px solid #555555;">

<center>
<h3 align="center"> Overview </h3> 

<figure>
        <div style = "position:relative; left:-120px;">
    <img  src="{{ site.url }}{{ site.baseurl }}/images/actiongpt/overview.gif" width="130%" height="100%" style="box-shadow: 0px 0px 0px"/>
        </div>
    <p>&nbsp;</p>
    <figcaption>
        Action-GPT Overview: Given an action phrase, we first create a suitable prompt using an engineered prompt function. The result is passed to a large-scale language model (GPT-3) to obtain multiple action descriptions containing fine-grained body movement details. 
        The corresponding deep text representations are obtained using Description Embedder. The aggregated version of these embeddings is processed by the Text Encoder. During training, the action pose sequence is processed by a Motion Encoder. 
         The encoders are associated with a deterministic sampler (autoencoder) or a VAE style generative model.
        During training(shown with black), the latent text embedding and the latent motion embedding are aligned. During inference(shown in green), the sampled text embedding is provided to the Motion Decoder which outputs the generated action sequence.
    </figcaption>
</figure>
</center>


<hr style="border: 1px solid #555555;">


<h3 align="center"> Comparisons </h3> 

<!-- <center>
<figure>
        <div id="comparisions">
    <img src="{{ site.url }}{{ site.baseurl }}/images/actiongpt/ActionGPT-Main-diagram.png" width="100%" />
        </div>
    <p>&nbsp;</p>
    <figcaption>
        Visual comparison of generated motion sequences across models trained on Action-GPT framework on BABEL dataset. Note that the generations using Action-GPT are well-aligned with the semantic information of action phrases. The example in right bottom-row shows latent space editing similar to  MotionCLIP. Action-GPT is better able to transfer the drink from mug style from standing to sitting pose.
    </figcaption>
</figure>
</center> -->
<center>
<div class="embed-container">
  <video width="100%" preload="auto" controls>
    <source src="{{ site.url }}{{ site.baseurl }}/images/actiongpt/qualitative_analysis.mp4" type="video/mp4">
    </video>
  <p>&nbsp;</p>
  <figcaption>
        Visual comparison of generated motion sequences across models trained on Action-GPT framework on BABEL dataset. Note that the generations using Action-GPT are well-aligned with the semantic information of action phrases. The example in the end shows latent space editing similar to  MotionCLIP. Action-GPT is better able to transfer the drink from mug style from standing to sitting pose.
    </figcaption>
</div>
</center>

<p>&nbsp;</p>

<h3 align="center"> Citation </h3>

```
@InProceedings{Action-GPT,
title={Action-GPT: Leveraging Large-scale Language Models for Improved and Generalized Action Generation},
author={Kalakonda, Sai Shashank and Maheshwari, Shubh and Sarvadevabhatla, Ravi Kiran},
booktitle={arXiv preprint https://arxiv.org/abs/2211.15603},
year={2022}
}
```

<p>&nbsp;</p>
<p>&nbsp;</p>
