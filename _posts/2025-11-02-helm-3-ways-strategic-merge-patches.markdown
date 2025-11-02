---
layout: post
title: "3-way Strategic Merge Patches in Helm: Release and Manual Changes"
date: 2025-11-02 14:35:00 +0000
categories: helm kubernetes
---

Let's say you have deployed the nginx Helm chart in Kubernetes, with the number of replicas set to 2:

```bash
helm install my-nginx bitnami/nginx --version 22.1.1
```

Now, because of an unexpected increase of incoming traffic, a user manually increases the number of replicas to 3 using kubectl:

```bash
kubectl patch deployment my-nginx -p '{"spec":{"replicas":3}}'
```

Now a new version of nginx is available and we want to upgrade our Helm chart to it, with the initial configuration:

```bash
helm upgrade my-nginx bitnami/nginx --version 22.2.3
```

**What happens to the number of replicas that were manually changed?** Does it get set to the default value which is 1 or does 3 remain?

## How 3-way Strategic Merge Patches Work

In Helm 3, the so-called "3-way Strategic Merge Patches" was introduced. Helm compares the previous revision of the Helm chart with the current revision that is to be applied, and also the live version. If a specific field, let's say `replicas`, was not changed between the previous revision and current revision, it is not changed.

So Helm ensures that manually done changes are not affected and stay applied when doing upgrades or rollbacks.

For more information, see the [Helm documentation on 3-way Strategic Merge Patches](https://helm.sh/docs/faq/changes_since_helm2/#improved-upgrade-strategy-3-way-strategic-merge-patches).

## Resetting Manual Changes

Now, what if you really want to reset manually changed values when doing the upgrade?

Yes, you can use the `--reset-values` flag:

```bash
helm upgrade my-nginx bitnami/nginx --version 22.2.3 --reset-values
```
