# Swaption instrument

# Placeholder: load py_library
# Placeholder: load py_test

package(
    default_visibility = ["//tf_quant_finance:__subpackages__"],
    licenses = ["notice"],
)

py_library(
    name = "swaption",
    srcs = ["__init__.py"],
    deps = [
        ":swaption_impl",
    ],
)

py_library(
    name = "swaption_impl",
    srcs = ["swaption_impl.py"],
    deps = [
        ":proto_utils",
        "//tf_quant_finance/datetime",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:curve_types",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:instrument",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:processed_market_data",
        "//tf_quant_finance/experimental/pricing_platform/framework/core:types",
        "//tf_quant_finance/experimental/pricing_platform/framework/rate_instruments:cashflow_streams",
        "//tf_quant_finance/experimental/pricing_platform/framework/rate_instruments/interest_rate_swap",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos",
        "//tf_quant_finance/math",
        "//tf_quant_finance/models/hull_white",
        # tensorflow dep,
    ],
)

py_library(
    name = "proto_utils",
    srcs = ["proto_utils.py"],
    deps = [
        "//tf_quant_finance/experimental/pricing_platform/framework/rate_instruments/interest_rate_swap:proto_utils",
        "//tf_quant_finance/experimental/pricing_platform/instrument_protos",
    ],
)

py_test(
    name = "swaption_test",
    size = "medium",
    srcs = ["swaption_test.py"],
    shard_count = 4,
    deps = [
        "//tf_quant_finance",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "proto_utils_test",
    size = "small",
    srcs = ["proto_utils_test.py"],
    shard_count = 2,
    deps = [
        ":proto_utils",
        "//tf_quant_finance",
        # test util,
        # numpy dep,
        # tensorflow dep,
    ],
)
