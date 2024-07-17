---
title: LocalStorageCapacityIsolationFSQuotaMonitoring
content_type: feature_gate
_build:
  list: never
  render: false

stages:
  - stage: beta
    defaultValue: false
    fromVersion: "1.31"
---
When `LocalStorageCapacityIsolation`
is enabled for
[local ephemeral storage](/docs/concepts/configuration/manage-resources-containers/), the backing filesystem for [emptyDir volumes](/docs/concepts/storage/volumes/#emptydir)
supports project quotas and they are enabled and when `UserNamespacesSupport` is enabled, use project quotas to monitor
[emptyDir volume](/docs/concepts/storage/volumes/#emptydir) storage consumption rather than
filesystem walk for better performance and accuracy.
