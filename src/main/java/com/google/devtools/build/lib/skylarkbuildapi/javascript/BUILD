# Description:
#   This package contains interfaces representing the Starlark "build API"
#   (but not the implementation of that API). Ultimately, this package
#   may be broken out of the Bazel package hierarchy to be standalone.
#   Thus, this package should not depend on Bazel-specific packages (only
#   those which contain pure-Starlark concepts, such as the interpreter or
#   annotation interfaces).

load("@rules_java//java:defs.bzl", "java_library")

package(default_visibility = ["//src:__subpackages__"])

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
    visibility = ["//src:__subpackages__"],
)

java_library(
    name = "javascript",
    srcs = glob(["*.java"]),
    deps = [
        "//src/main/java/com/google/devtools/build/lib:syntax",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/skylarkbuildapi",
        "//src/main/java/com/google/devtools/build/lib/skylarkbuildapi/core",
        "//src/main/java/com/google/devtools/build/lib/skylarkinterface",
    ],
)
