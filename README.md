# Intel Lesson 4

Video processing with SSD Mobilenet 

## Download model and uncompress

wget http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v2_coco_2018_03_29.tar.gz

tar -xzf ssd_mobilenet_v2_coco_2018_03_29.tar.gz

## Convert Tensorflow Model to IR (Intermediate Representation)

python mo.py --input_model D:\Courses\Intel_OpenVino\models\ssd_mobilenet_v2_coco_2018_03_29\frozen_inference_gr
aph.pb --tensorflow_object_detection_api_pipeline_config D:\Courses\Intel_OpenVino\models\ssd_mobilenet_v2_coco_2018_03_29\pipeline.config --reverse_input_channels --tensorflow_use_custom_operat
ions_config .\extensions\front\tf\ssd_support.json --model_name D:\Courses\Intel_OpenVino\models\ssd_mobilenet

## Execute

python app.py -i test_video.mp4 -m ./models/ssd_mobilenet.xml -ct 0.6 -c GREEN

## Example output 
<video width="320" height="240" controls>
  <source src="https://github.com/Pablitinho/Intel_Lesson_4/out.mp4" type="video/mp4">
</video>




![](out.mp4)
