# TensorFlow Quantitative Finance general math functions.

# Placeholder: load py_library
# Placeholder: load py_test

package(
    default_visibility = ["//tf_quant_finance:__subpackages__"],
    licenses = ["notice"],
)

py_library(
    name = "root_search",
    srcs = ["__init__.py"],
    deps = [
        ":brent",
        ":newton",
        ":utils",
    ],
)

py_library(
    name = "brent",
    srcs = ["brent.py"],
    deps = [
        "//tf_quant_finance/types",
        "//tf_quant_finance/utils",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "brent_test",
    size = "small",
    timeout = "moderate",
    srcs = ["brent_test.py"],
    deps = [
        ":brent",
        ":utils",
        "//tf_quant_finance",
        # test util,
        # tensorflow dep,
    ],
)

py_library(
    name = "newton",
    srcs = ["newton.py"],
    deps = [
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "newton_test",
    size = "small",
    timeout = "moderate",
    srcs = ["newton_test.py"],
    deps = [
        ":newton",
        ":utils",
        "//tf_quant_finance",
        # test util,
        # tensorflow dep,
    ],
)

py_library(
    name = "utils",
    srcs = ["utils.py"],
    deps = [
        # numpy dep,
        # tensorflow dep,
    ],
)

filegroup(
    name = "docs",
    srcs = [
        "README.md",
    ],
)
