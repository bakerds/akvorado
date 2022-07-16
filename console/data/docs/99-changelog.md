# Changelog

For each version, changes are listed in order of importance. Minor
changes are not listed here. Each change is mapped to a category
identified with a specific icon:
- 💥: breaking change
- ✨: new feature
- 🗑️: removed feature
- 🔒: security fix
- 🩹: bug fix
- 🌱: miscellaneous change

## Unreleased

- ✨ *inlet*: add an option to ignore ASN received from flows [PR #7][]
- 🩹 *console*: fix maximum value computation for the grid view
- 🌱 *orchestrator*: adapt partition key for each consolidated flow
  tables in ClickHouse to limit the number of partitions (this change
  won't be applied on an existing installation)
- 🌱 *inlet*: add `default-sampling-rate` as an option
- 🌱 *inlet*: only require either input or output interface for a valid flow
- 🌱 *build*: switch from Yarn to npm as a Javascript package manager [PR #4][]
- 🌱 *docker-compose*: pull image from GitHub instead of building it
- 🌱 *doc*: add more tips to the troubleshooting section

[PR #4]: https://github.com/vincentbernat/akvorado/pull/4
[PR #7]: https://github.com/vincentbernat/akvorado/pull/7

## 1.4.1 - 2022-07-12

- 🔒 *docker-compose*: expose two HTTP endpoints, one public (8081) and one private (8080)
- 🌱 *docker-compose*: restart ClickHouse container on failure

## 1.4.0 - 2022-07-09

<!-- This does not make sense to put these changes as it is the first
public release. Once there are enough releases, strip this one. -->

- 🚀 first public release under the AGPL 3.0 license
- ✨ *fake-exporter*: add a new service to simulate an exporter for demo purpose (SNMP and Netflow)
- ✨ *console*: allow a user to save filters
- ✨ *orchestrator*: allow a user to map network to names
- ✨ *console*: add an option to include or exclude L2 encapsulation from reported sizes
- 🩹 *console*: fill missing values with 0 for time series charts
- 🩹 *console*: use the resolution to select the best consolidated table when no table contains old enough data
- 🌱 *console*: enable completion on various widgets
- 🌱 *cmd*: ignore keys starting with dot in YAML configuration (see the provided configuration file as an example)
- 🌱 *orchestrator*: store several configurations for each component (see the provided configuration file as an example)
- 🌱 *orchestrator*: add ability to override AS mappings