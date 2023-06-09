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


