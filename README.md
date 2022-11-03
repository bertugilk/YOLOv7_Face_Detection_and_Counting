# YOLOv7_Face_Detection_and_Counting
I trained the dataset containing 2745 human face photos on the GPU named Nvidia RTX3070 using YOLOv7. I got over 90% accuracy as a result of the training. Again, with a special object counting algorithm, I obtained the number of detected faces in the image.

## Dataset link:
https://universe.roboflow.com/mohamed-traore-2ekkp/face-detection-mik1i<br>

## Installation
git clone https://github.com/WongKinYiu/yolov7<br>
cd yolov7<br>
pip install -r requirements.txt<br>

## Training
cd YOLOv7<br>
python train.py --batch 8 --epochs 100 --data "..\data.yaml" --weights  "..\yolov7.pt" --device 0

## Detection
python detect.py --weights "..\weights\best.pt" --conf 0.1 --source images<br>

## Detection and Counting
python detect_and_count.py --weights "..\weights\best.pt" --conf 0.1 --source images<br>

![Stokoe20-58-scaled-1_jpg rf 4a3866396509fd59137030893589a039](https://user-images.githubusercontent.com/48621020/199690616-5f1dc421-7545-418a-87a4-1d7632931f3f.jpg)<br>

## References
https://github.com/WongKinYiu/yolov7
