# Local volatility model.

# Placeholder: load py_library
# Placeholder: load py_test

package(
    default_visibility = ["//tf_quant_finance:__subpackages__"],
    licenses = ["notice"],
)

py_library(
    name = "local_volatility",
    srcs = ["__init__.py"],
    deps = [
        ":local_volatility_model",
    ],
)

py_library(
    name = "local_volatility_model",
    srcs = ["local_volatility_model.py"],
    deps = [
        "//tf_quant_finance/black_scholes",
        "//tf_quant_finance/datetime",
        "//tf_quant_finance/experimental/pricing_platform/framework/market_data:volatility_surface",
        "//tf_quant_finance/math",
        "//tf_quant_finance/math:piecewise",
        "//tf_quant_finance/math/interpolation",
        "//tf_quant_finance/models:euler_sampling",
        "//tf_quant_finance/models:generic_ito_process",
        "//tf_quant_finance/models:utils",
        # tensorflow dep,
    ],
)

py_test(
    name = "local_volatility_model_test",
    size = "large",
    timeout = "long",
    srcs = ["local_volatility_model_test.py"],
    shard_count = 30,
    tags = [
        "nomsan",  # TODO(b/231568581)
        "notsan",
    ],
    deps = [
        "//tf_quant_finance",
        # test util,
    ],
)
