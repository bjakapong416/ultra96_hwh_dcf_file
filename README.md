# ultra96_hwh_dcf_file

# Example for Tensorflow

vai_c_tensorflow --frozen_pb=../quantize/deploy_model.pb --arch=./custom.json --output_dir=launchmodel --net_name=SignLanguageMNISTnet --options "{'mode':'normal'}"


# Example for Caffe

model_name=$1

modelzoo_name=$2

vai_c_caffe \
--prototxt ../../AI-Model-Zoo/models/all_models_1.2/caffe/${modelzoo_name}/quantized/Edge/deploy.prototxt \
--caffemodel ../../AI-Model-Zoo/models/all_models_1.2/caffe/${modelzoo_name}/quantized/Edge/deploy.caffemodel \
--arch ./custom.json \
--output_dir ./compiled_output/${modelzoo_name} \
--net_name ${model_name} \
--options "{'mode': 'normal'}"
