# Description:
#   Contains the Keras Application package (internal TensorFlow version).

load("@org_keras//keras:keras.bzl", "tf_py_test")

package(
    default_visibility = [
        # Remove this deps to integration test.
        "//keras:friends",
    ],
    licenses = ["notice"],
)

py_library(
    name = "applications",
    srcs = [
        "__init__.py",
        "densenet.py",
        "efficientnet.py",
        "efficientnet_v2.py",
        "imagenet_utils.py",
        "inception_resnet_v2.py",
        "inception_v3.py",
        "mobilenet.py",
        "mobilenet_v2.py",
        "mobilenet_v3.py",
        "nasnet.py",
        "regnet.py",
        "resnet.py",
        "resnet_v2.py",
        "vgg16.py",
        "vgg19.py",
        "xception.py",
    ],
    srcs_version = "PY3",
    visibility = ["//visibility:public"],
    deps = [
        "//:expect_numpy_installed",
        "//:expect_tensorflow_installed",
        "//keras:activations",
        "//keras:backend",
        "//keras:models",
        "//keras/engine",
        "//keras/layers",
        "//keras/utils:data_utils",
        "//keras/utils:layer_utils",
    ],
)

tf_py_test(
    name = "applications_test",
    size = "medium",
    srcs = ["applications_test.py"],
    shard_count = 40,
    tags = [
        "no_rocm",
        "notsan",  # b/168814536
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/testing_infra:test_combinations",
    ],
)

# Add target for each application module file, to make sure it only
# runs the test for the application models contained in that
# application module when it has been modified.
# TODO(b/146940090): Remove the "no_oss" tag in the following tests.
tf_py_test(
    name = "applications_load_weight_test_resnet",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=resnet"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
        "notsan",  # b/168814536
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_resnet_v2",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=resnet_v2"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
        "notsan",  # TODO(b/170901700)
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_vgg16",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=vgg16"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_vgg19",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=vgg19"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_xception",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=xception"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_inception_v3",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=inception_v3"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_inception_resnet_v2",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=inception_resnet_v2"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_mobilenet",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=mobilenet"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_mobilenet_v2",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=mobilenet_v2"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_mobilenet_v3_small",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=mobilenet_v3_small"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_mobilenet_v3_large",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=mobilenet_v3_large"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_densenet",
    size = "large",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=densenet"],
    main = "applications_load_weight_test.py",
    shard_count = 3,
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_efficientnet",
    size = "large",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=efficientnet"],
    main = "applications_load_weight_test.py",
    shard_count = 8,
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_efficientnet_v2",
    size = "large",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=efficientnet_v2"],
    main = "applications_load_weight_test.py",
    shard_count = 8,
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_regnet",
    size = "large",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=regnet"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_nasnet_mobile",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=nasnet_mobile"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "applications_load_weight_test_nasnet_large",
    srcs = ["applications_load_weight_test.py"],
    args = ["--module=nasnet_large"],
    main = "applications_load_weight_test.py",
    tags = [
        "no_oss",
        "no_pip",
    ],
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras/preprocessing",
    ],
)

tf_py_test(
    name = "imagenet_utils_test",
    size = "medium",
    srcs = ["imagenet_utils_test.py"],
    shard_count = 2,
    deps = [
        ":applications",
        "//:expect_absl_installed",
        "//:expect_tensorflow_installed",
        "//keras",
        "//keras/testing_infra:test_combinations",
    ],
)
