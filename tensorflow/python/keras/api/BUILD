# Description:
# Package for TensorFlow.

load("//tensorflow/python/tools/api/generator:api_gen.bzl", "gen_api_init_files")
load("//tensorflow/python/tools/api/generator:api_init_files.bzl", "KERAS_API_INIT_FILES")
load("//tensorflow/python/tools/api/generator:api_init_files_v1.bzl", "KERAS_API_INIT_FILES_V1")

package(
    default_visibility = ["//visibility:public"],
    licenses = ["notice"],  # Apache 2.0 License
)

keras_packages = [
    "tensorflow.python",
    "tensorflow.python.keras",
    "tensorflow.python.keras.activations",
    "tensorflow.python.keras.applications.densenet",
    "tensorflow.python.keras.applications.imagenet_utils",
    "tensorflow.python.keras.applications.inception_resnet_v2",
    "tensorflow.python.keras.applications.inception_v3",
    "tensorflow.python.keras.applications.mobilenet",
    "tensorflow.python.keras.applications.mobilenet_v2",
    "tensorflow.python.keras.applications.nasnet",
    "tensorflow.python.keras.applications.resnet",
    "tensorflow.python.keras.applications.resnet_v2",
    "tensorflow.python.keras.applications.vgg16",
    "tensorflow.python.keras.applications.vgg19",
    "tensorflow.python.keras.applications.xception",
    "tensorflow.python.keras.backend",
    "tensorflow.python.keras.callbacks",
    "tensorflow.python.keras.callbacks_v1",
    "tensorflow.python.keras.constraints",
    "tensorflow.python.keras.initializers",
    "tensorflow.python.keras.losses",
    "tensorflow.python.keras.metrics",
    "tensorflow.python.keras.models",
    "tensorflow.python.keras.ops",
    "tensorflow.python.keras.optimizers",
    "tensorflow.python.keras.regularizers",
    "tensorflow.python.keras.saving.model_config",
    "tensorflow.python.keras.saving.save",
    "tensorflow.python.keras.saving.saved_model_experimental",
    "tensorflow.python.keras.utils.data_utils",
    "tensorflow.python.keras.utils.generic_utils",
    "tensorflow.python.keras.utils.io_utils",
    "tensorflow.python.keras.utils.layer_utils",
    "tensorflow.python.keras.utils.multi_gpu_utils",
    "tensorflow.python.keras.utils.np_utils",
    "tensorflow.python.keras.utils.vis_utils",
    "tensorflow.python.keras.wrappers.scikit_learn",
]

gen_api_init_files(
    name = "keras_python_api_gen",
    api_name = "keras",
    api_version = 1,
    output_files = KERAS_API_INIT_FILES_V1,
    output_package = "tensorflow.python.keras.api",
    package_deps = [
        "//tensorflow/python/keras",
        "//tensorflow/python:no_contrib",
    ],
    packages = keras_packages,
)

gen_api_init_files(
    name = "keras_python_api_gen_compat_v1",
    api_name = "keras",
    api_version = 1,
    output_dir = "_v1/",
    output_files = KERAS_API_INIT_FILES_V1,
    output_package = "tensorflow.python.keras.api._v1",
    package_deps = [
        "//tensorflow/python/keras",
        "//tensorflow/python:no_contrib",
    ],
    packages = keras_packages,
)

gen_api_init_files(
    name = "keras_python_api_gen_compat_v2",
    api_name = "keras",
    api_version = 2,
    output_dir = "_v2/",
    output_files = KERAS_API_INIT_FILES,
    output_package = "tensorflow.python.keras.api._v2",
    package_deps = [
        "//tensorflow/python/keras",
        "//tensorflow/python:no_contrib",
    ],
    packages = keras_packages,
)
