# Changelog

We document all notable changes to this project in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.1] - 2021-05-25

### Fixed

* Updated inlets image to reflect external changes.


## [0.4.0] - 2021-03-19

### Added

* Add helpers to implement lifecycle methods for Kubernetes API objects.

### Changed

* `helper.Own` and `helper.OwnUncontrolled` now return an error when the owner has not been persisted.

## [0.3.2] - 2021-03-15

### Fixed

* An individual document in a parsed manifest can now be larger than 32kB.

## [0.3.1] - 2021-03-09

### Fixed

* The `AllowAll()` method of a `NetworkPolicy` object now correctly allows both ingress and egress traffic.

## [0.3.0] - 2021-03-09

### Added

* Add a configurable error handling reconciler.
* Port reconciler chaining and a single namespace filtering reconciler from Relay Core.
* Add support for conditionally loading Kubernetes objects based on boolean predicates or the existence of another object.

### Fixed

* Prevent the tunnel application from attempting to connect before the tunnel service endpoint is bound.

## [0.2.1] - 2021-02-24

### Fixed

* The tunnel application now waits for the proxy connection to be established before invoking its callback.

### Build

* Update timeutil package to v0.3.0.

## [0.2.0] - 2021-02-02

### Added

* Add [controller-runtime](https://github.com/kubernetes-sigs/controller-runtime/)-compatible reconcilers for generating self-signed TLS secrets and automatically setting the CA bundle for webhook configurations.
* Add support for passing event recorders through a context.
* Add object support for webhook configurations.
* Add support for impersonation to end-to-end testing framework.

### Fixed

* `RetryLoader`s now correctly report whether the retry operation succeeded as their boolean outcome.

### Changed

* Upgrade klog to v2.
* Improve and refactor object ownership helpers.

## [0.1.0] - 2021-01-06

### Added

* Initial release.

[Unreleased]: https://github.com/puppetlabs/leg/compare/k8sutil/v0.4.1...HEAD
[0.4.1]: https://github.com/puppetlabs/leg/compare/k8sutil/v0.4.0...k8sutil/v0.4.1
[0.4.0]: https://github.com/puppetlabs/leg/compare/k8sutil/v0.3.2...k8sutil/v0.4.0
[0.3.2]: https://github.com/puppetlabs/leg/compare/k8sutil/v0.3.1...k8sutil/v0.3.2
[0.3.1]: https://github.com/puppetlabs/leg/compare/k8sutil/v0.3.0...k8sutil/v0.3.1
[0.3.0]: https://github.com/puppetlabs/leg/compare/k8sutil/v0.2.1...k8sutil/v0.3.0
[0.2.1]: https://github.com/puppetlabs/leg/compare/k8sutil/v0.2.0...k8sutil/v0.2.1
[0.2.0]: https://github.com/puppetlabs/leg/compare/k8sutil/v0.1.0...k8sutil/v0.2.0
[0.1.0]: https://github.com/puppetlabs/leg/compare/c09b3cdca7104d5ea79152368de260f5d40316b6...k8sutil/v0.1.0
