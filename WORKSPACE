workspace(name = "rules_closure_library_repro")

http_archive(
    name = "io_bazel_rules_closure",
    sha256 = "a80acb69c63d5f6437b099c111480a4493bad4592015af2127a2f49fb7512d8d",
    strip_prefix = "rules_closure-0.7.0",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_closure/archive/0.7.0.tar.gz",
        "https://github.com/bazelbuild/rules_closure/archive/0.7.0.tar.gz",
    ],
)

local_repository(
    name = "com_google_javascript_closure_library",
    path = "third_party/com_google_javascript_closure_library",
)

load("@io_bazel_rules_closure//closure:defs.bzl", "closure_repositories")

closure_repositories(
    omit_com_google_javascript_closure_library=True,
)
