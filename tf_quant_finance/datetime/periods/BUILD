# TODO(cyrilchimisov): describe this package.

# Placeholder: load py_library

package(
    default_visibility = ["//tf_quant_finance:__subpackages__"],
    licenses = ["notice"],
)

py_library(
    name = "periods",
    srcs = ["__init__.py"],
    deps = [
        ":period_tensors",
        # tensorflow dep,
    ],
)

py_library(
    name = "period_tensors",
    srcs = ["period_tensors.py"],
    deps = [
        "//tf_quant_finance/datetime:constants",
        "//tf_quant_finance/datetime:tensor_wrapper",
        # tensorflow dep,
    ],
)
