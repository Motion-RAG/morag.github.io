---
title: "MoRAG"
layout: gridlay
excerpt: "MoRAG"
sitemap: false
permalink: /
---

[comment]: Title
<h2 align="center">MoRAG:<br>Multi-Fusion Retrieval Augmented Generation Framework for Human Motion</h2>

[comment]: Authors
<p style="text-align: center;">
<a href="https://www.linkedin.com/in/sai-shashank-54288219b" style="color: #CC0000"> Sai Shashank Kalakonda</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://shubhmaheshwari.github.io" style="color: #CC0000"> Shubh Maheshwari</a>
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
  <video width="100%" preload="auto" controls autoplay muted loop playsinline>
    <source src="{{ site.url }}{{ site.baseurl }}/images/morag/Teaser.mp4" type="video/mp4">
    </video>
  <p>&nbsp;</p>
  <figcaption>
    MoRAG incorporats part-specific motion retrieval models to enhances the quality of generation and retrieval tasks for diverse text descriptions.
    </figcaption>
</div>
</figure>
</center>

<hr style="border: 1px solid #555555;">

<center>

<h3 align="center"> Abstract </h3>
</center>
We introduce MoRAG, 
- a novel multi-part fusion based retrieval- augmented generation strategy for text-based human motion generation. 
- The method enhances motion diffusion models by leveraging additional knowledge obtained through an improved motion retrieval process. 
- By effectively prompting large language models (LLMs), we address spelling errors and rephrasing issues in motion retrieval. 
- Our approach utilizes a multi-part retrieval strategy to improve the generalizability of motion retrieval across the language space. We create diverse samples through spatial composition of the retrieved motions. 
- Furthermore, by utilizing low-level, part-specific motion information, we are able
to construct motion samples for unseen text descriptions.
- Our experiments demonstrate that our framework can serve as a plug-and-play module, improving the performance of motion diffusion models.
- Code, pretrained models and sample videos will be made available. 

<hr style="border: 1px solid #555555;">
<!-- 
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

<hr style="border: 1px solid #555555;"> -->

<center>
<h3 align="center"> Overview </h3> 

<figure>
        <div style = "position:relative">
            <video width="100%" preload="auto" controls autoplay muted loop playsinline>
                <source src="{{ site.url }}{{ site.baseurl }}/images/morag/MoRAG_Framework.mp4" type="video/mp4">
    </video>
        </div>
    <p>&nbsp;</p>
    <figcaption>
        Given a text description <i>text</i>, we generate part-specific descriptions corresponding to "Torso," "Hands," and "Legs" by prompting an LLM. These generated descriptions are used as queries to retrieve corresponding part-specific motions: R<sup>i</sup><sub>torso</sub>, R<sup>i</sup><sub>hands</sub>, and R<sup>i</sup><sub>legs</sub> from the part-specific motion databases D<sup>i</sup><sub>torso</sub>, D<sup>i</sup><sub>hands</sub>, and D<sup>i</sup><sub>legs</sub>, respectively. The retrieved motions are then fused to construct a full-body motion sequence C<sup>i</sup> that aligns with the input text. The constructed motion samples are used as additional information in the motion generation pipeline during both training and inference, alongside the input text, to further improve model performance.
    </figcaption>
</figure>
</center>


<hr style="border: 1px solid #555555;">


<!-- <h3 align="center"> Comparisons </h3> 
---
gallery_a: [ abc.png, def.png, xyz.png ]

---
{% include carousel.html height="50"
   unit="%" duration="7" images=gallery_a %} -->

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
</center> 
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
</center> -->

<p>&nbsp;</p>

<h3 align="center"> Citation </h3>

```
@InProceedings{MoRAG,
title={MoRAG: Multi-Fusion Retrieval Augmented Generation Framework for Human Motion},
author={Kalakonda, Sai Shashank and Maheshwari, Shubh and Sarvadevabhatla, Ravi Kiran},
booktitle={arXiv preprint},
year={2024}
}
```

<p>&nbsp;</p>
<p>&nbsp;</p>
