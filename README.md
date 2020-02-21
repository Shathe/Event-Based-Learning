# Event-Based-Learning

Hacer un código chulo desde el principio. Ultimo proyecto mio y puede shacerlo bien y con calma



## Primeros pasos

Usar pytorch

Entrenamiento de clasificacion de algun tutorial primero

Dataset:

El dataset tiene qu eser asi 

https://github.com/Shathe/lidar-bonnetal/blob/948cfb3a67b3e97e717e261afc204cf8deb1c5f1/train/tasks/semantic/dataset/kitti/parser.py#L22

DataserLoader:

https://github.com/Shathe/lidar-bonnetal/blob/948cfb3a67b3e97e717e261afc204cf8deb1c5f1/train/tasks/semantic/dataset/kitti/parser.py#L338

## N-Cars

descargar dataset

https://github.com/Shathe/Ev-Matching/blob/master/data_extraction/Event.py

https://github.com/Shathe/Ev-Matching/blob/master/data_extraction/EventRepresentation.py







## Ablation Study

La arquitectura es, dada una represnetacion (aprendida o no), despues, encadenarle una red de clasificacion normal en plan efficientnet o algo



- [ ] [IETS](https://link.springer.com/epdf/10.1007/978-3-030-27272-2_35?shared_access_token=MbeJ8WMHDmiRsMopFePo7Pe4RwlQNchNByi7wbcMAY6m3l_EBYi5m5NnMpPG0EINrl6dJsRFKl-k-7rZg8hHip6hmitq-DSVqvGF9uALq-GT6er_lgOPwg1Csi7liZbp8ZY0n9_bchR4e4EV429bsQ%3D%3D) que da 0.976 accuracy
- [ ] HOTS/HATS(0.929)/Mean-surface??
- [ ] Grid (implementatcion que ya tenias)
- [ ] Grid + mascara
- [ ] PointNet (lo mio de lidar)
- [ ] PointNet (lo mio de lidar) + mascara
- [ ] ConvLSTM
- [ ] ConvLSTM + mascara
- [ ] Combinaciones varias entre ellas con: self-attention tanto en las features como en mascara  2D (SPADE)



La idea de la máscara es, aprender como tenias pensado (convlstm o conv) una máscara (sigmoid) de tamaño nº pixels por pixel, o en el caso del grid, nº de slices, para mutiplicar esta mascara por la representacion input de entrada y con eso, vovler a hacer la ConvLSTM o convs  o pointNets para aprender de nuevo. La idea es primero aprender a filtrar los eventos y luego aprender de los evnetos filtrados



Añadir self-pretraining adivinando eventos o grayscale?

Pensar cosas guays deeventos Como auperpoint



