# Interactive-Segmentation-Papers

## 2016
- [**iFCN**, CVPR2016] Deep Interactive Object Selection. [[Paper](https://openaccess.thecvf.com/content_cvpr_2016/papers/Xu_Deep_Interactive_Object_CVPR_2016_paper.pdf)]   
Key points: first deep-learning-based method, Euclidean distant maps, sampling strategies, refinement by graph cut

## 2017 
- [**RIS-Net**, ICCV2017] Regional Interactive Image Segmentation Networks. [[Paper](https://openaccess.thecvf.com/content_iccv_2017/html/Liew_Regional_Interactive_Image_ICCV_2017_paper.html)]   
Key points: local regional refinement, ROIs sampling, the combination of the global context and local regional segmentation, click discounting factor for training

- [BMVC2017] Deep GrabCut for Object Selection. [[Paper](https://arxiv.org/pdf/1707.00243.pdf)][[Reimplementation in Pytorch](https://github.com/jfzhang95/DeepGrabCut-PyTorch)]   
Key points: transform the loosely-played rectangle as a Euclidean distance map,  convolutional encoder-decoder network

## 2018
- [**DEXTR**, CVPR2018] Deep Extreme Cut: From Extreme Points to Object Segmentation. [[Paper](https://openaccess.thecvf.com/content_cvpr_2018/html/Maninis_Deep_Extreme_Cut_CVPR_2018_paper.html)][[Pytorch](https://github.com/scaelles/DEXTR-PyTorch)]   
Key points: exploit extreme points(left-most, right-most, top, bottom pixels), extensive experiemnts on four tasks

- [CVPR2018] Interactive Image Segmentation with Latent Diversity. [[Paper](https://openaccess.thecvf.com/content_cvpr_2018/papers/Li_Interactive_Image_Segmentation_CVPR_2018_paper.pdf)][[Tensorflow](https://github.com/intel-isl/Intseg)]  
Key points: multi-modality exploration, plausible segmentations, selection network

- [**ITIS**, BMVC2018] Iteratively Trained Interactive Segmentation. [[Paper](https://arxiv.org/pdf/1805.04398v1.pdf)][[Tensoflow](https://github.com/sabarim/itis)]   
Key points: iterative training strategy 

## 2019
- [**BRS**, CVPR2019] Interactive Image Segmentation via Backpropagating Refinement Scheme. [[Paper](https://vcg.seas.harvard.edu/publications/interactive-image-segmentation-via-backpropagating-refinement-scheme/paper)][[Caffe](https://github.com/wdjang/BRS-Interactive_segmentation)]     
Key points: backpropagating refinement scheme in the test phase to enforce user-specified locations to have correct labels, small adjustments in interaction maps 

- [CVPR2019] Content-Aware Multi-Level Guidance for Interactive Instance Segmentation. [[Paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Majumder_Content-Aware_Multi-Level_Guidance_for_Interactive_Instance_Segmentation_CVPR_2019_paper.pdf)]    
Key points: superpixel-based guidance map rather than distant/gaussian map 

## 2020
- [**f-BRS**, CVPR2020] f-BRS: Rethinking Backpropagating Refinement for Interactive Segmentation. [[Paper](https://arxiv.org/abs/2001.10331)][[Pytorch](https://github.com/saic-vul/fbrs_interactive_segmentation/tree/master)]
Key points: based on BRS, auxiliary variables acting on features are involed, only a small part of network are passed to accelerate 

- [**IOG**, CVPR2020] Interactive Object Segmentation with Inside-Outside Guidance. [[Paper](http://openaccess.thecvf.com/content_CVPR_2020/papers/Zhang_Interactive_Object_Segmentation_With_Inside-Outside_Guidance_CVPR_2020_paper.pdf)][[Code](https://github.com/shiyinzhang/Inside-Outside-Guidance)]   
Key points: inside-outside-guidance(click three points), extensive experiments on different datasets and domains 

- [**FCA-Net**, CVPR2020] Interactive Image Segmentation With First Click Attention. [[Paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/Lin_Interactive_Image_Segmentation_With_First_Click_Attention_CVPR_2020_paper.pdf)][[Pytorch](https://github.com/frazerlin/fcanet)]   
Key points: first click attention, click loss(weighted binary cross entropy), structural integrity strategy

- [arXiv2020] Getting to 99% Accuracy in Interactive Segmentation. [[Paper](https://arxiv.org/abs/2003.07932)][[Pytorch](https://github.com/MarcoForte/DeepInteractiveSegmentation)]   
Key points: leverage each user interaction, click by click training regime, very high IoU discussions (up to 99%), image/interaction stream design


## Summary
- User interactive ways:   
bounding box, clicks(object/background points, extreme points, inside/outside points), contours   

- Click embedding ways:  
distant map, gaussian map, guidance map(combined with superpixel segmentation)

- Archietecure:   
Encoder: VGG16, ResNet-34/50/101, U-Net, Denset  
Decoder: Deeplab-v2/v3+/LargeFOV, U-Net

- Post-processing   
graph-cuts, CRF, backpropagating refinement, guided filter layer






