# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project's packages adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Add support for `coredns` metric names for version 1.7.0 and above.

## [0.6.0] - 2021-01-25

### Changed

- Ignore secrets of type `helm.sh/release.v1` by default to prevent OOM on starting.

## [0.5.2] - 2021-01-20

### Fixed

- CRDs are now created correctly on the first install of the App.

## [0.5.1] - 2021-01-13

### Fixed

- Update `values.schema.json` to reflect current values file.

## [0.5.0] - 2021-01-05

### Added

- Added values schema for validating default values

### Updated

- sync with upstream chart version kube-prometheus-stack-11.1.7
- prometheus-operator v0.42.1 -> v0.43.2
- prometheus-config-reloader v0.42.1 -> v0.43.2
- prometheus v2.21.0 -> v2.22.1
- updated scripts (changed sync_chart, added generate_patch)

### Fixed

- Fixed helm CRDs issue by adding crd-install job, to ensure CRDs are up to date

## [0.4.0] - 2020-10-15

### Added

- SHA variable for images

### Changed

- Upstream project location an references throughout the chart  
- Change upstream-sync script to new upstream project location and structure
- Replace hyperkube image with kubectl image
- Replace name "prometheus-operator" with "kube-prometheus-stack" in templates

### Updated

- Sync with upstream chart version 10.1.0
- prometheus-operator v0.38.1 -> v0.42.1
- alertmanager v0.20.0 -> v0.21.0
- configmap-reload v0.3.0 -> v0.4.0
- prometheus-config-reloader v0.38.1 -> v0.42.1
- prometheus v2.18.1 -> v2.21.0
- new structure and format to all prometheus rules

## [0.3.4] - 2020-07-22

### Added

- Set default request/limits in deployment (cpu: 100m, memory: 100Mi) per best practice

### Changed

- Sync with upstream
    - Bug fixes
    - Add namespace overwrite

### Updated

- Update architect-orb to `0.10.0`
- kube-state-metrics chart `2.8.8` -> `2.8.11`
- grafana chart `5.1.4` -> `5.3.0`
- grafana chart requirement `5.1.*` -> `5.3.*`
- configmapReloadImage `0.0.1` -> `0.3.0`
- hyperkubeImage `1.12.1` -> `1.16.12`


## [v0.3.3]

### Changed

- Introduce `crd-install` hook for helm 2 compatibility.
- Update Prometheus to 2.18.1
- Update Grafana chart to 5.1.4
- Update prometheus-node-exporter chart to 1.10.0

## [v0.3.2]

### Changed
- Fix CRD installation to support both helm2 and helm3
- Add support for installations in China

## [v0.3.1]

### Changed
- Fix application name in the circleci config

## [v0.3.0]

### Changed
- Fix kubelet service name in the Prometheus Operator deployment 
- Update Prometheus Operator to 0.38.1
- Update Prometheus to 2.17.2
- Update Alert manager to 0.20.0
- Update Grafana chart to 5.0.25
- Update kube-state-metrics chart to 2.8.5
- Update prometheus-node-exporter chart to 1.9.1
- Rename to prometheus-operator-app

## [v0.2.0]

### Changed
- Add Kubernetes 1.16 support
- Update Prometheus Operator to 0.35.0
- Update Prometheus to 2.15.2
- Update Alert manager to 0.19.0
- Update Grafana chart to 4.2.3
- Update kube-state-metrics chart to 2.4.1
- Update prometheus-node-exporter chart to 1.8.1

## [v0.1.1]

### Changed

- Disable App Armor in grafana as it does not work on CoreOS and Flatcar.

## [v0.1.0]

### Added

- First version of the prometheus operator chart.

[Unreleased]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.6.0...HEAD
[0.6.0]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.5.2...v0.6.0
[0.5.2]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.5.1...v0.5.2
[0.5.1]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.5.0...v0.5.1
[0.5.0]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.3.4...v0.4.0
[0.3.4]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.3.3...v0.3.4
[v0.3.3]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.3.2..v0.3.3
[v0.3.2]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.3.1..v0.3.2
[v0.3.1]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.3.0..v0.3.1
[v0.3.0]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.2.0..v0.3.0
[v0.2.0]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.1.1..v0.2.0
[v0.1.1]: https://github.com/giantswarm/prometheus-operator-app/compare/v0.1.0..v0.1.1

[v0.1.0]: https://github.com/giantswarm/prometheus-operator-app/releases/tag/v0.1.0
