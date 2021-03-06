load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "eventhandlers.go",
        "scheduler.go",
        "testutil.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/scheduler",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/scheduler/algorithm:go_default_library",
        "//pkg/scheduler/algorithm/predicates:go_default_library",
        "//pkg/scheduler/api:go_default_library",
        "//pkg/scheduler/api/latest:go_default_library",
        "//pkg/scheduler/apis/config:go_default_library",
        "//pkg/scheduler/core:go_default_library",
        "//pkg/scheduler/factory:go_default_library",
        "//pkg/scheduler/internal/cache:go_default_library",
        "//pkg/scheduler/internal/queue:go_default_library",
        "//pkg/scheduler/metrics:go_default_library",
        "//pkg/scheduler/plugins/v1alpha1:go_default_library",
        "//pkg/scheduler/util:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/api/storage/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//staging/src/k8s.io/client-go/informers/apps/v1:go_default_library",
        "//staging/src/k8s.io/client-go/informers/core/v1:go_default_library",
        "//staging/src/k8s.io/client-go/informers/policy/v1beta1:go_default_library",
        "//staging/src/k8s.io/client-go/informers/storage/v1:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes:go_default_library",
        "//staging/src/k8s.io/client-go/listers/core/v1:go_default_library",
        "//staging/src/k8s.io/client-go/tools/cache:go_default_library",
        "//staging/src/k8s.io/client-go/tools/record:go_default_library",
        "//vendor/k8s.io/klog:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "eventhandlers_test.go",
        "scheduler_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "//pkg/api/legacyscheme:go_default_library",
        "//pkg/controller/volume/persistentvolume:go_default_library",
        "//pkg/scheduler/algorithm:go_default_library",
        "//pkg/scheduler/algorithm/predicates:go_default_library",
        "//pkg/scheduler/algorithm/priorities:go_default_library",
        "//pkg/scheduler/api:go_default_library",
        "//pkg/scheduler/apis/config:go_default_library",
        "//pkg/scheduler/core:go_default_library",
        "//pkg/scheduler/factory:go_default_library",
        "//pkg/scheduler/internal/cache:go_default_library",
        "//pkg/scheduler/internal/cache/fake:go_default_library",
        "//pkg/scheduler/internal/queue:go_default_library",
        "//pkg/scheduler/nodeinfo:go_default_library",
        "//pkg/scheduler/volumebinder:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/diff:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//staging/src/k8s.io/client-go/informers:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes/fake:go_default_library",
        "//staging/src/k8s.io/client-go/listers/core/v1:go_default_library",
        "//staging/src/k8s.io/client-go/tools/cache:go_default_library",
        "//staging/src/k8s.io/client-go/tools/record:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//pkg/scheduler/algorithm:all-srcs",
        "//pkg/scheduler/algorithmprovider:all-srcs",
        "//pkg/scheduler/api:all-srcs",
        "//pkg/scheduler/apis/config:all-srcs",
        "//pkg/scheduler/core:all-srcs",
        "//pkg/scheduler/factory:all-srcs",
        "//pkg/scheduler/internal/cache:all-srcs",
        "//pkg/scheduler/internal/queue:all-srcs",
        "//pkg/scheduler/metrics:all-srcs",
        "//pkg/scheduler/nodeinfo:all-srcs",
        "//pkg/scheduler/plugins:all-srcs",
        "//pkg/scheduler/testing:all-srcs",
        "//pkg/scheduler/util:all-srcs",
        "//pkg/scheduler/volumebinder:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
