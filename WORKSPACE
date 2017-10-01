workspace(name = "org_tensorflow_tensorboard")

http_archive(
    name = "io_bazel_rules_closure",
    sha256 = "25f5399f18d8bf9ce435f85c6bbf671ec4820bc4396b3022cc5dc4bc66303609",
    strip_prefix = "rules_closure-0.4.2",
    urls = [
        "http://mirror.bazel.build/github.com/bazelbuild/rules_closure/archive/0.4.2.tar.gz",  # 2017-08-29
        "https://github.com/bazelbuild/rules_closure/archive/0.4.2.tar.gz",
    ],
)

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "8c333df68fb0096221e2127eda2807384e00cc211ee7e7ea4ed08d212e6a69c1",
    strip_prefix = "rules_go-0.5.4",
    urls = [
        "http://mirror.bazel.build/github.com/bazelbuild/rules_go/archive/0.5.4.tar.gz",
        "https://github.com/bazelbuild/rules_go/archive/0.5.4.tar.gz",
    ],
)

http_archive(
    name = "io_bazel_rules_webtesting",
    sha256 = "4a34918cdb57b7c0976c1d6a9a7af1d657266b239c9c1066c87d6f9a4058bc7d",
    strip_prefix = "rules_webtesting-a9f624ac542d2be75f6f0bdd255f108f2795924a",
    urls = [
        "http://mirror.bazel.build/github.com/bazelbuild/rules_webtesting/archive/a9f624ac542d2be75f6f0bdd255f108f2795924a.tar.gz",  # 2017-09-11
        "https://github.com/bazelbuild/rules_webtesting/archive/a9f624ac542d2be75f6f0bdd255f108f2795924a.tar.gz",
    ],
)

load("@io_bazel_rules_closure//closure:defs.bzl", "closure_repositories")

closure_repositories()

load("@io_bazel_rules_go//go:def.bzl", "go_repositories")

go_repositories()

load("@io_bazel_rules_webtesting//web:repositories.bzl", "browser_repositories", "web_test_repositories")

web_test_repositories(
    omit_com_google_code_findbugs_jsr305 = True,
    omit_com_google_code_gson = True,
    omit_com_google_errorprone_error_prone_annotations = True,
    omit_com_google_guava = True,
    omit_junit = True,
    omit_org_hamcrest_core = True,
)

load("//third_party:workspace.bzl", "tensorboard_workspace")

# Please add all new dependencies in workspace.bzl.
tensorboard_workspace()
