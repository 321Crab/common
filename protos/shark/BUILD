
load("@rules_proto//proto:defs.bzl", "proto_library")
load("//bazel:cc_grpc_library.bzl", "cc_grpc_library")
load("//bazel:grpc_build_system.bzl", "grpc_proto_library")
load("//bazel:python_rules.bzl", "py_grpc_library", "py_proto_library")

package(default_visibility = ["//visibility:public"])

proto_library(
    name = "shark_service",
    srcs = ["shark.proto"],
    deps = [
    ],
)

cc_proto_library(
    name = "shark_cc_service",
    deps = [":shark_service"],
)



cc_grpc_library(
    name = "shark_service_cc_grpc",
    srcs = [":shark_service"],
    grpc_only = True,
    deps = [":shark_cc_service"],
)