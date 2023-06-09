## BLIP-2: Bootstrapping Language-Image Pre-training with Frozen Image Encoders and Large Language Models
- cross-modal alignment 중요
  - Flamingo는 contrastive loss 사용
  - BLIP-2는 Querying Transformer(Q-former) with two stage pre-training strategy 제안
- 3 pretraining objectives
  - Image-Text Contrastive Learning loss: query representation과 CLS 토큰 
  - Image-Grounded Text Loss
  - Image-Text Matching loss

## (보다가 찾아봄) BEIT vs DEIT vs MAE
- DEIT: data-efficient(완전 다름, distillation)
- BEIT: MIM, 달리의 image tokenizer, BERT
- MAE

## Grounding Language Models to Images for Multimodal Inputs and Outputs
- frozen Text-only language model에 visual grounding 
- language model의 incontext learning과 free-form text generation 가능
- language model은 frozen하고, input output linear layer를 finetune
- linear layer로 image space에서 text space로 projection
![image](https://github.com/yeonju7kim/PaperReading/assets/95571735/7cb3f3c3-7386-483e-8e60-4b252d77faa6)
- InfoNCE, where NCE stands for Noise-Contrastive Estimation, is a type of contrastive loss function used for self-supervised learning.

## IFSeg: Image-free Semantic Segmentation via Vision-Language Model
- 
