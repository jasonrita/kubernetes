load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "internal.go",
        "match.go",
        "tables.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/golang.org/x/text/internal",
    importpath = "golang.org/x/text/internal",
    visibility = ["//visibility:public"],
    deps = ["//vendor/golang.org/x/text/language:go_default_library"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//vendor/golang.org/x/text/internal/tag:all-srcs",
        "//vendor/golang.org/x/text/internal/utf8internal:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
