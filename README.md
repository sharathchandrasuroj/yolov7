# yolov7
**Official YOLOv7 Object Detection with Pretrained weights**

1.Clone the official YOLOv7 repository

2.Create yolov7 folder

Download and unzip Yolov7 repository

3.Open Anaconda Prompt, move to directory

  1.create virtual environment
    conda create -n yolov7 python==3.9 -y
    conda cativate yolov7

4.Install required libraries

    pip install -r requirements.txt

5.Installing pytorch library
  For CPU-----
    the requirements.txt will install CPU based pytorch

  For GPU -----
    1.Goto official pytorch webpage---->> Select Required CUDA based Pytorch version and install it.
      
      To check pytorch version ,open prompt
        python
        import pytorch
        torch.cuda.is_available()
        torch.cuda.version()
        exit()

6.Download petrained yolov7 weights form official website------->>>> yolov7.pt  or  yolov7_tiny.pt

7.To run the object detection model
    
    python detect.py --weights yolov7.pt --conf 0.4 --img-size 640 --source image.jpg

    o/p:run/detect/expN/image.jpg

8.Object detection for video files
    
    python detect.py --weights yolov7.pt --conf 0.4 --img-size 640 --source video.mp4

    o/p: yolov7/run/detect/expN/video.mp4

9.For yolov7-tiny versio object detction 
    
    python detect.py --weights yolov7-tiny.pt --conf 0.4 --img-size 640 --source video.mp4
    

    1.Object detection using video camera, keep "source 0"
       
        python detect.py --weights yolov7-tiny.pt --conf 0.4 --img-size 640 --source 0


10.To change the thickness and colors of bounding boxes,open detect.py and update line_thickness=1/3/5 in line number 117

      python detect.py --weights yolov7-tiny.py --conf 0.4 --img-size 640 --source image.jpg
    
    
        
