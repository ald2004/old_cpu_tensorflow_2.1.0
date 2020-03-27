# old_cpu_tensorflow_2.1.0
">>> import tensorflow as tf"


">>> tf.__version__"
'2.1.0'
## without avx,nogcp,nohdfs,nonccl with sse3 sse4.1 sse4.2
bazel build //tensorflow/tools/pip_package:build_pip_package --config=v2 --config=noaws --config=nogcp --config=nohdfs --config=nonccl -c opt --copt=-msse3 --copt=-msse4.1 --copt=-msse4.2
