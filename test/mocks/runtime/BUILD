load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_mock",
    "envoy_package",
)

licenses(["notice"])  # Apache 2

envoy_package()

envoy_cc_mock(
    name = "runtime_mocks",
    srcs = ["mocks.cc"],
    hdrs = ["mocks.h"],
    external_deps = ["abseil_optional"],
    deps = [
        "//envoy/runtime:runtime_interface",
        "//envoy/upstream:cluster_manager_interface",
        "//test/mocks:common_lib",
        "//test/mocks/stats:stats_mocks",
        "@envoy_api//envoy/type/v3:pkg_cc_proto",
    ],
)
