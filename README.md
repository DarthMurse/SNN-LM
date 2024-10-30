# SNN-LM
A repository to record the progressing in spiking language models. 

## Spiking LMs
+ [SpikeGPT: Generative Pre-trained Language Model with Spiking Neural Networks](https://arxiv.org/abs/2302.13939)
+ [SPIKEBERT: A LANGUAGE SPIKFORMER LEARNED FROM BERT WITH KNOWLEDGE DISTILLATION](https://arxiv.org/abs/2308.15122) 
+ [SpikingBERT: Distilling BERT to Train Spiking Language Models Using Implicit Differentiation](https://arxiv.org/abs/2308.10873)
+ [SpikeZIP-TF: Conversion is All You Need for Transformer-based SNN](https://arxiv.org/abs/2406.03470)
+ [SpikeLM: Towards General Spike-Driven Language Modeling via Elastic Bi-Spiking Mechanisms](https://arxiv.org/abs/2406.03287)
+ [SpikeLLM: Scaling up Spiking Neural Network to Large Language Models via Saliency-based Spiking](https://arxiv.org/abs/2407.04752)

## Spiking ViTs
+ [SPATIO-TEMPORAL APPROXIMATION: A TRAINING- FREE SNN CONVERSION FOR TRANSFORMERS](https://openreview.net/forum?id=XrunSYwoLr)
+ [Towards High-performance Spiking Transformers from ANN to SNN Conversion](https://openreview.net/forum?id=BZi746oBG8&referrer=%5Bthe%20profile%20of%20Zecheng%20Hao%5D(%2Fprofile%3Fid%3D~Zecheng_Hao1))

## Main Information
| Model | Method | Timestep | Parameters | Efficiency | Hardware Compatibility |
| --- | --- | --- | --- | --- | --- |
| SpikeGPT | Direct Training | 1 | 216M | 4.53% | No, $Y[t+1] = \sigma(RX[t]) \cdot \frac{\exp(KX[t])VX[t] + \exp(W)A[t]}{\exp(KX[t]) + \exp(W)B[t]}$ |
| SpikeBERT | Direct Training | 16 | 109M | 27% - 30% | No, LayerNorm |
| SpikingBERT | Direct Training | 16 | 50M | 50% | No, Softmax and LayerNorm |
| SpikeZIP-TF | Conversion | 64 | 355M | 17% (doubful, diffenrent method) | No, Softmax and LayerNorm |
| SpikeLM | Direct Training | 4 | 109M | 26.7% | No, Softmax and LayerNorm |
| SpikeLLM | Conversion | W4A4(t=4) | 7B | 6.87% | No, Softmax and LayerNorm | 