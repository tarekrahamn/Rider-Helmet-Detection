##Enhancing Road Safety and Accountability Through Automated Rider and Helmet Detection: A Deep Learning Approach

📄 [**[paper]**](https://ieeexplore.ieee.org/document/11022569) 📊 [[**dataset**]](https://universe.roboflow.com/rider-and-helmet-instance-segmentation-and-detection/riders-dataset-segmentation)
## Methodology
<img width="485" height="696" alt="Screenshot 2025-07-19 114159" src="https://github.com/user-attachments/assets/f10988bf-714a-4065-a99f-875aff44ea60" />
We implemented a two-stage deep learning pipeline for automated rider and helmet detection. First, YOLOv8 was used for segmenting two-wheeler riders from images. Then, a VGG16-based classifier detected whether the identified rider was wearing a helmet or not. The dataset was preprocessed with augmentation (resizing, flipping, brightness adjustment), and redundant images were removed to improve accuracy. This hybrid approach ensures precise and reliable helmet compliance detection.

We designed a two-stage deep learning pipeline:

- **Preprocessing**: Removed redundant images and applied augmentation (resizing to 600x600, flipping, brightness +10%).
- **Segmentation**: YOLOv8 detects and segments two-wheeler riders from road images.
- **Classification**: VGG16 classifies whether detected riders are wearing helmets or not.
- This hybrid approach minimizes misclassification and improves compliance detection.


## 📊 Model Performance Comparison (mAP, Precision, Recall)

| **Authors**           | **Model**             | **mAP** | **Precision** | **Recall** |
|------------------------|------------------------|--------:|--------------:|-----------:|
| Nandhini [4]           | SSD Model              | 78.1%   | -             | -          |
| Tomas [5]              | YOLOv5 + YOLOv7        | 95%     | 95.6%         | 91%        |
| Venkateswarl [13]      | YOLOv8                 | -       | 88.63%        | 68.3%      |
| Aboah [14]             | YOLOv8 + TTA           | 95.3%   | 91.8%         | -          |
| Li [20]                | YOLO                   | 95%     | 92%           | 92%        |
| **Our Model (Ours)**   | **YOLOv8 + VGG16**     | **95%** | **99%**       | **96%**    |

✅ **Our model achieved the highest precision and recall**, making it ideal for real-world safety applications.


## Cite
<pre>
@INPROCEEDINGS{11022569,
  author={Hossen, Md Shaharia and Rimi, Maria Akter and Rahman, Tarek and Saad, Sakib Mahmood and Rahman, Raiyan},
  booktitle={2024 27th International Conference on Computer and Information Technology (ICCIT)}, 
  title={Enhancing Road Safety and Accountability Through Automated Rider and Helmet Detection: A Deep Learning Approach}, 
  year={2024},
  volume={},
  number={},
  pages={305-310},
  keywords={Deep learning;Image segmentation;Computer vision;Head;Road accidents;Pipelines;Mortality;Real-time systems;Road safety;Safety;YOLOv8;VGG16;CNN;Helmet detection;Computer Vision;Image Processing;Deep Learning;Reducing Misclassification;Traffic management},
  doi={10.1109/ICCIT64611.2024.11022569}}


</pre>

## Contact
For any queries, please contact us at trahman221182@bscse.uiu.ac.bd

