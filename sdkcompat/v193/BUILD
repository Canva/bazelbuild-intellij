# Description: Indirections for SDK changes to the underlying platform library.

load("//intellij_platform_sdk:build_defs.bzl", "select_for_ide")

licenses(["notice"])  # Apache 2.0

java_library(
    name = "v193",
    srcs = glob([
        "com/google/idea/sdkcompat/general/**",
        "com/google/idea/sdkcompat/formatter/**",
        "com/google/idea/sdkcompat/platform/**",
        "com/google/idea/sdkcompat/python/**",
        "com/google/idea/sdkcompat/vcs/**",
    ]) + select_for_ide(
        clion = glob([
            "com/google/idea/sdkcompat/clion/**",
            "com/google/idea/sdkcompat/cpp/**",
        ]),
    ),
    visibility = ["//sdkcompat:__pkg__"],
    deps = [
        "//intellij_platform_sdk:plugin_api",
        "//third_party/python",
    ],
)
