package(default_visibility = ["//visibility:public"])

cc_library(
    name = "ifc",
    srcs = [
        "assert.cxx",
        "file.cxx",
        "ifc-dom/charts.cxx",
        "ifc-dom/decls.cxx",
        "ifc-dom/exprs.cxx",
        "ifc-dom/literals.cxx",
        "ifc-dom/names.cxx",
        "ifc-dom/sentences.cxx",
        "ifc-dom/stmts.cxx",
        "ifc-dom/syntax.cxx",
        "ifc-dom/types.cxx",
        "ifc-printer/printer.cxx",
        "ifc-reader/operators.cxx",
        "ifc-reader/reader.cxx",
        "ifc-reader/util.cxx",
        "sgraph.cxx",
    ] + select({
        "@platforms//os:windows": ["hash_win.cxx"],
        "//conditions:default": ["sha256.cxx"],
    }),
    linkopts = select({
        "@platforms//os:windows": ["bcrypt.lib"],
        "//conditions:default": [],
    }),
    hdrs = [
        "ifc-dom/common.hxx",
        "ifc-printer/printer.hxx",
    ],
    deps = [
        "//include:ifc",
    ],
)

cc_binary(
    name = "ifc-printer",
    srcs = ["ifc-printer/main.cxx"],
    deps = ["ifc"],
)
