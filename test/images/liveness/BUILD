package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_binary(
    name = "liveness",
    embed = [":go_default_library"],
    importpath = "k8s.io/kubernetes/test/images/liveness",
)

go_library(
    name = "go_default_library",
    srcs = ["server.go"],
    importpath = "k8s.io/kubernetes/test/images/liveness",
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
