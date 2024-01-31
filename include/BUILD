package(default_visibility = ["//visibility:public"])

cc_library(
    name = "ifc",
    #strip_include_prefix = "ifc",
    includes = ["."],
    hdrs = [
        "ifc/abstract-sgraph.hxx",
        "ifc/assertions.hxx",
        "ifc/basic-types.hxx",
        "ifc/dom/node.hxx",
        "ifc/file.hxx",
        "ifc/index-utils.hxx",
        "ifc/operators.hxx",
        "ifc/pathname.hxx",
        "ifc/pp-forms.hxx",
        "ifc/reader.hxx",
        "ifc/source-word.hxx",
        "ifc/underlying.hxx",
        "ifc/util.hxx",
        "ifc/version.hxx",
    ],
    deps = [
        "@com_github_microsoft_gsl//:gsl",
    ]
)
