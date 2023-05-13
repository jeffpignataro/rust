load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@rules_rust//rust:repositories.bzl", "rules_rust_dependencies", "rust_register_toolchains")
load("//cargo:crates.bzl", "raze_fetch_remote_crates")

# To find additional information on this release or newer ones visit:
# https://github.com/bazelbuild/rules_rust/releases
http_archive(
    name = "rules_rust",
    sha256 = "37f40490169dc94013c7566c75c861977a2c02ce5505b7e975da0f7d5f2231c8",
    urls = ["https://github.com/bazelbuild/rules_rust/releases/download/0.16.1/rules_rust-v0.16.1.tar.gz"],
)

rules_rust_dependencies()

rust_register_toolchains()

# Note that this method's name depends on your gen_workspace_prefix setting.
# `raze` is the default prefix.
raze_fetch_remote_crates()
