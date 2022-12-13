# drone-charts

[![Build Status](https://drone.cryptic.systems/api/badges/volker.raschek/drone-runner-charts/status.svg)](https://drone.cryptic.systems/volker.raschek/drone-runner-charts)
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/drone-ce)](https://artifacthub.io/packages/search?repo=drone-ce)

This is an inofficial helm chart for
[drone-runner](https://github.com/drone/drone-runner-kube) and should replace
the official unmaintained helm chart
[repository](https://github.com/drone/drone-runner-kube).

This helm chart can be found on [artifacthub.io](https://artifacthub.io/) and
can be installed via helm.

> The repository has been changed and causes error messages when interacting
> with the old repository definition. Please remove the chart repo
> `volker.raschek` and replace it with `drone`.

```bash
helm repo add drone https://charts.cryptic.systems/drone
helm install drone drone/drone-runner
```

## Customization

All [configuration
options](https://docs.drone.io/runner/kubernetes/configuration/reference/) can
be defined in the `values.yml` file below the `config` section. Alternatively
can be the options passed via the `--set` flag of the `helm install` command.

| value                                                   | reference                                                                                                           |
| ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `config.DRONE_ANNOTATIONS_DEFAULT`                      | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone-annotations-default/)         |
| `config.DRONE_DEBUG`                                    | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_debug/)                       |
| `config.DRONE_DOCKER_CONFIG`                            | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_docker_config/)               |
| `config.DRONE_HTTP_BIND`                                | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_http_bind/)                   |
| `config.DRONE_HTTP_HOST`                                | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_http_host/)                   |
| `config.DRONE_HTTP_PROTO`                               | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_http_proto/)                  |
| `config.DRONE_IMAGE_CLONE`                              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_image_clone/)                 |
| `config.DRONE_IMAGE_PLACEHOLDER`                        | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_image_placeholder/)           |
| `config.DRONE_LABELS_DEFAULT`                           | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_labels_default/)              |
| `config.DRONE_LIMIT_EVENTS`                             | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_limit_events/)                |
| `config.DRONE_LIMIT_REPOS`                              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_limit_repos/)                 |
| `config.DRONE_LIMIT_TRUST`                              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_limit_trust/)                 |
| `config.DRONE_NAMESPACE_DEFAULT`                        | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_namespace_default/)           |
| `config.DRONE_NAMESPACE_RULES`                          | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_namespace_rules/)             |
| `config.DRONE_NAMESPACE_RULES_FILE`                     | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_namespace_rules_file/)        |
| `config.DRONE_NODE_SELECTOR_DEFAULT`                    | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_node_selector_default/)       |
| `config.DRONE_POLICY_FILE`                              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_policy_file/)                 |
| `config.DRONE_REGISTRY_PLUGIN_ENDPOINT`                 | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_registry_plugin_endpoint/)    |
| `config.DRONE_REGISTRY_PLUGIN_SKIP_VERIFY`              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_registry_plugin_skip_verify/) |
| `config.DRONE_REGISTRY_PLUGIN_TOKEN`                    | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_registry_plugin_token/)       |
| `config.DRONE_RESOURCE_LIMIT_CPU`                       | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_resource_limit_cpu/)          |
| `config.DRONE_RESOURCE_LIMIT_MEMORY`                    | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_resource_limit_memory/)       |
| `config.DRONE_RESOURCE_REQUEST_CPU`                     | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_resource_request_cpu/)        |
| `config.DRONE_RESOURCE_REQUEST_MEMORY`                  | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_resource_request_memory/)     |
| `config.DRONE_RPC_DUMP_HTTP`                            | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_rpc_dump_http/)               |
| `config.DRONE_RPC_DUMP_HTTP_BODY`                       | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_rpc_dump_http_body/)          |
| `config.DRONE_RPC_HOST`                                 | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_rpc_host/)                    |
| `config.DRONE_RPC_PROTO`                                | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_rpc_proto/)                   |
| `config.DRONE_RPC_SECRET`                               | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_rpc_secret/)                  |
| `config.DRONE_RPC_SKIP_VERIFY`                          | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_rpc_skip_verify/)             |
| `config.DRONE_RUNNER_CAPACITY`                          | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_runner_capacity/)             |
| `config.DRONE_RUNNER_DEVICES`                           | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_runner_devices/)              |
| `config.DRONE_RUNNER_ENV_FILE`                          | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_runner_env_file/)             |
| `config.DRONE_RUNNER_ENVIRON`                           | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_runner_environ/)              |
| `config.DRONE_RUNNER_MAX_PROCS`                         | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_runner_max_procs/)            |
| `config.DRONE_RUNNER_NAME`                              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_runner_name/)                 |
| `config.DRONE_RUNNER_PRIVILEGED_IMAGES`                 | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_runner_privileged_images/)    |
| `config.DRONE_SECRET_PLUGIN_ENDPOINT`                   | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_secret_plugin_endpoint/)      |
| `config.DRONE_SECRET_PLUGIN_SKIP_VERIFY`                | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_secret_plugin_skip_verify/)   |
| `config.DRONE_SECRET_PLUGIN_TOKEN`                      | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_secret_plugin_token/)         |
| `config.DRONE_SERVICE_ACCOUNT_DEFAULT`                  | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_service_account_default/)     |
| `config.DRONE_TRACE`                                    | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_trace/)                       |
| `config.DRONE_UI_DISABLED`                              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_ui_disabled/)                 |
| `config.DRONE_UI_PASSWORD`                              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_ui_password/)                 |
| `config.DRONE_UI_REALM`                                 | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_ui_realm/)                    |
| `config.DRONE_UI_USERNAME`                              | [Documentation](https://docs.drone.io/runner/kubernetes/configuration/reference/drone_ui_username/)                 |
