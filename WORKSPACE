load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_github_microsoft_gsl",
    integrity = "sha256-8OMssQZU/qka1WveiRcNeM+/Q2PuCwHY8JfeK6SfbOk=",
    strip_prefix = "GSL-4.0.0",
    urls = [
        "https://github.com/microsoft/GSL/archive/refs/tags/v4.0.0.tar.gz"
    ],
    # To test it from the here, use this
    # bazel test @com_github_microsoft_gsl//...
    build_file_content=
"""
package(default_visibility = ["//visibility:public"])

cc_library(
    name = "gsl",
    strip_include_prefix = "include",
    hdrs = glob(["include/gsl/*"]),
)

cc_test(
    name = "tests",
    # https://learn.microsoft.com/en-us/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996    
    copts = ["-wd4996"],
    srcs = glob(["tests/*.cpp", "tests/*.h"]),
    deps = ["gsl", "@googletest//:gtest_main"],
)
"""
)
