# Automatically generated by "pub global run bazel:bazelify".
# DO NOT MODIFY BY HAND

# Bazelify: 1 libraries.
load("@io_bazel_rules_dart//dart/build_rules:core.bzl", "dart_library")

# Bazelify: 1 web apps.
load("@io_bazel_rules_dart//dart/build_rules:ddc.bzl", "dart_ddc_bundle")
load("@io_bazel_rules_dart//dart/build_rules:dev_server.bzl", "dev_server")
load("@io_bazel_rules_dart//dart/build_rules:web.bzl", "dart_web_application")

package(default_visibility = ["//visibility:public"])

_PUB_DEPS = [
    "@stack_trace//:stack_trace",
    "@stagexl//:stagexl",
]

# Generated automatically for package:pop_pop_win
dart_library(
    name = "pop_pop_win",
    srcs = glob(["lib/**", "web/**"]),
    deps = _PUB_DEPS,
    pub_pkg_name = "pop_pop_win",
)
# Generated automatically for package:pop_pop_win|web/main.dart
dart_web_application(
    name = "main",
    srcs = glob(["web/**"]),
    script_file = "web/main.dart",
    deps = _PUB_DEPS + [
        ":pop_pop_win",
    ],
)
dev_server(
    name = "main_dartium_serve",
    deps = _PUB_DEPS + [
        ":pop_pop_win",
    ],
    data = glob(["web/**"]),
)
dart_ddc_bundle(
    name = "main_ddc_bundle",
    entry_library = "web/main.dart",
    entry_module = ":pop_pop_win",
    input_html = "web/index.html",
    output_dir = "web",
)
dev_server(
    name = "main_ddc_serve",
    data = [":main_ddc_bundle"],
    script_args = [
        "--package-spec=main_ddc_bundle.packages",
        "--uri-substitution=web/index.html:web/main_ddc_bundle.html",
    ],
)