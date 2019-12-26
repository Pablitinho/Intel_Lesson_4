# Intel Lesson 4
Video processing with SSD Mobilenet 

wget http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v2_coco_2018_03_29.tar.gz
tar -xzf ssd_mobilenet_v2_coco_2018_03_29.tar.gz

python mo.py --input_model D:\Courses\Intel_OpenVino\models\ssd_mobilenet_v2_coco_2018_03_29\frozen_inference_gr
aph.pb --tensorflow_object_detection_api_pipeline_config D:\Courses\Intel_OpenVino\models\ssd_mobilenet_v2_coco_2018_03_29\pipeline.config --reverse_input_channels --tensorflow_use_custom_operat
ions_config .\extensions\front\tf\ssd_support.json --model_name D:\Courses\Intel_OpenVino\models\ssd_mobilenet


python app.py -i test_video.mp4 -m ./models/ssd_mobilenet.xml -ct 0.6 -c GREEN


[![Watch the video](https://i.imgur.com/vKb2F1B.png)](./out.mp4)
