load("@k8s_adhoc//:defaults.bzl", "k8s_adhoc")
load("@io_bazel_rules_k8s//k8s:objects.bzl", "k8s_objects")

k8s_adhoc(
    name = "cronjob",
    kind = "CronJob",
    template = ":cronjob.yaml",
)

k8s_adhoc(
    name = "configmap",
    kind = "ConfigMap",
    template = ":configmap.yaml",
)

# from the config map objects
# can do k8s_objects or create each one individually

k8s_objects(
    name = "metrics",
    objects = [
        # cronjob and config map
        ":cronjob",
        ":configmap",
    ],
)

