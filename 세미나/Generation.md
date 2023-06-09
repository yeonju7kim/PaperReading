## Drag Your GAN: Interactive Point-based Manipulation on the Generative Image Manifold (SIGGRAPH’23)
- ideal controllable image synthesis need 3 properties: flexibility(different spatial attributes-position, pose, shape, expression), precision, generality(category agnostic)
- This paper
  - interactive point-based manipulation
    - Controls diverse spatial attributes
    - Agnostic to object categories
    - Controls more than one point
    - handle points precisely reach the target points
  - 2 sub-problems
    - Supervising the handle points
      - motion supervision is achieved by a shifted feature patch loss 
    - Tracking the handle points
      - point tracking is performed through nearest neighbor search
  - user input: handle points, target points, optional binary mask
  - object: semantic positions of the handle points reach their corresponding target points
    - motion supervision
      - 6번째 feature maps을 사용, shift 하고, mask 밖은 유지하도록 loss 만듦
      - w 학습
    - point tracking 

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
