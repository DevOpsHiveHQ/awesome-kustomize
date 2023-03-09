# Awesome Kustomize
[![Awesome](https://raw.githubusercontent.com/sindresorhus/awesome/main/media/badge.svg)](https://github.com/sindresorhus/awesome)
 [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/aabouzaid/awesome-kustomize/pulls)

A curated and collaborative list of awesome [Kustomize](https://kustomize.io/) resources.
Feel free to contribute to this repo, [PRs are more than welcome](https://github.com/aabouzaid/awesome-kustomize/pulls)!

<p align="center">
    <img src="img/kustomize.svg" width="80%">
</p>

<!-- omit in toc -->
## Contents

- [Introduction](#introduction)
- [Plugins](#plugins)
  - [Generators](#generators)
  - [Transformers](#transformers)
- [Guides](#guides)
  - [Novice](#novice)
  - [Intermediate](#intermediate)
  - [Advanced](#advanced)
- [Tips \& Tricks](#tips--tricks)
- [Misc](#misc)
- [Related lists](#related-lists)
- [License](#license)


## Introduction

Kustomize introduces a template-free way to customize Kubernetes manifests. It uses a purely declarative approach
to configuration customization, which will help you efficiently manage your Infrastructure as a code (IaC).

Kustomize works as a standalone binary; also, it's built into `kubectl` (since v1.14). It can be used with
off-the-shelf applications like **Helm charts**. Also, it has a deep integration with different **GitOps** tools
like ArgoCD, Flux, and many others.

- **Website:** https://kustomize.io
- **Docs:** https://kubectl.docs.kubernetes.io/references/kustomize
- **Git repo:** https://github.com/kubernetes-sigs/kustomize


## Plugins

Kustomize has 3 types of plugins `generator`, `transformer`, and `validator`.

> **Note**
>
> If you are a plugin developer, it's highly recommended to support the new plugins standard
> [KRM function](https://github.com/kubernetes-sigs/kustomize/blob/master/cmd/config/docs/api-conventions/functions-spec.md).

### Generators

| Name | Description &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Method |
| ---- | -------------------------------------------------------------------------- | ------ |
| [Secretize](https://github.com/bbl/secretize) | Generating Kubernetes Secret from various sources. It's like a swiss army knife, but for Kubernetes secrets | Exec |
| [SopsSecretGenerator](https://github.com/goabout/kustomize-sopssecretgenerator/) | Generating Secrets from sops-encrypted files | Exec, Exec KRM |
| [KSops](https://github.com/viaduct-ai/kustomize-sops) | Generating Secrets from sops-encrypted files | Exec |
| [PolicyGenerator](https://github.com/open-cluster-management-io/policy-generator-plugin) | Generating Open Cluster Management policies | Exec |

### Transformers

| Name | Description &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Method |
| ---- | -------------------------------------------------------------------------- | ------ |
| [HelmValuesTransformer](https://github.com/openinfradev/kustomize-helm-transformer) | Transforming values in HelmRelease CustomResource. It helps to manage a lot of HelmRelease's value in single transformer file | Exec |
| [TemplateTransformer](https://github.com/joshdk/template-transformer) | Transforming templating in resources based on env vars | Exec |


## Guides

📰 Article, 📺 Video, 🧪 Lab

### Novice

- 📰 [Declarative Management of Kubernetes Objects Using Kustomize](https://kubernetes.io/docs/tasks/manage-kubernetes-objects/kustomization/) - Kubernetes Docs
- 📰 [Configure Kubernetes with Kustomize](https://cloud.google.com/anthos-config-management/docs/concepts/kustomize) - Google Cloud
- 📺 [Organizing the YAML mess with Kustomize](https://www.youtube.com/watch?v=1fCAwFGX38U&t=77s) - Florian Assmus
- 📺 [Kustomize: Deploy Your App with Template Free YAML](https://www.youtube.com/watch?v=ahMIBxufNR0) - Ryan Cox, Lyft

### Intermediate

- 🧪 [ArgoCD GitOps Tutorial - Working with Kustomize](https://developers.redhat.com/learning/learn:openshift:develop-gitops/resource/resources:working-kustomize) - Red Hat Developer
- 📰 [3 ways to customize off-the-shelf Helm charts with Kustomize](https://tech.aabouzaid.com/2020/09/3-ways-to-customize-off-the-shelf-helm-charts-with-kustomize-kubernetes.html) - Ahmed AbouZaid

### Advanced

- 📰 [Advanced Kustomize features](https://www.innoq.com/en/blog/advanced-kustomize-features/) - INNOQ
- 📰 [Set OpenAPI patch strategy for Kubernetes Custom Resources](https://tech.aabouzaid.com/2022/11/set-openapi-patch-strategy-for-kubernetes-custom-resources-kustomize.html) - Ahmed AbouZaid
- 📺 [Customizing Kustomize with Client-Side Custom Resources](https://www.youtube.com/watch?v=YlFUv4F5PYc) - Katrina Verey, Apple & Jeff Regan, Google
- 📺 [Own your YAML: extending Kustomize via Plugins](https://www.youtube.com/watch?v=Xoh_OpLoVtI) - Matt McEuen


## Tips & Tricks

- 📰 [Delete a manifest from a Kustomize base](https://tech.aabouzaid.com/2021/05/delete-a-manifest-from-kustomize-base.html)
- 📰 [Apply Kustomize builtin transformers on a single resource](https://tech.aabouzaid.com/2022/04/apply-kustomize-builtin-transformers-on-a-single-resource.html)
- 📰 [Pass extra data to the Containerized KRM function](https://tech.aabouzaid.com/2022/12/pass-extra-data-to-the-containerized-krm-function.html)


## Misc

- [Kustomize plugin for asdf version manager](https://github.com/Banno/asdf-kustomize)


## Related lists

- [Awesome Kubernetes](https://github.com/ramitsurana/awesome-kubernetes)
- [Awesome Kubectl plugins](https://github.com/ishantanu/awesome-kubectl-plugins)
- [Awesome Helm](https://github.com/cdwv/awesome-helm)


## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
    <img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" />
</a>

<br />

This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
Creative Commons Attribution 4.0 International License</a> (CC BY 4.0).
