common
======
Common Microservices

Current chart version is `2.1.1`





## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| client.ingress.disabled | bool | `false` |  |
| client.ingress.type | string | `"http"` |  |
| client.noVolumes | bool | `false` | Setar como true se não houverem configmaps no frontend |
| client.ports.port | int | `80` |  |
| configMapJob.image.pullPolicy | string | `"IfNotPresent"` |  |
| configMapJob.image.repository | string | `"repositoryit/configmaps"` |  |
| configMapJob.image.tag | string | `"latest"` |  |
| configMapJob.kubectlImage.pullPolicy | string | `"IfNotPresent"` |  |
| configMapJob.kubectlImage.repository | string | `"gcr.io/google_containers/hyperkube"` |  |
| configMapJob.kubectlImage.tag | string | `"v1.14.1"` |  |
| configMapJob.serviceAccountName | string | `"configmap-admin"` |  |
| deployment.image.imagePullPolicy | string | `"Always"` |  |
| deployment.image.tag | string | `"latest"` |  |
| deployment.labelAtualizacaoConfigMap | string | `"true"` |  |
| deployment.memory.max | int | `512` |  |
| deployment.memory.min | int | `256` |  |
| deployment.ports.name | string | `"http"` |  |
| deployment.ports.port | int | `8080` |  |
| deployment.replicaCount | int | `1` |  |
| deployment.resources.limits.cpu | string | `"1000m"` |  |
| deployment.resources.limits.memory | string | `"768Mi"` |  |
| deployment.resources.requests.cpu | string | `"100m"` |  |
| deployment.resources.requests.memory | string | `"256Mi"` |  |
| deployment.version | int | `1` |  |
| glowroot.image.repository | string | `"repositoryit/glowroot-sidekick"` |  |
| glowroot.image.tag | string | `"0.13.1"` |  |
| istio.autoInjection | string | `"enabled"` |  |
| istio.enabled | bool | `false` |  |
| istio.gateway.altServer.hosts[0] | string |  |  |
| istio.gateway.altServer.port.name | string |  |  |
| istio.gateway.altServer.port.number | int |  |  |
| istio.gateway.altServer.port.protocol | string |  |  |
| istio.gateway.defaultServer.hosts[0] | string | `"*"` |  |
| istio.gateway.defaultServer.port.name | string | `"http"` |  |
| istio.gateway.defaultServer.port.number | int | `80` |  |
| istio.gateway.defaultServer.port.protocol | string | `"HTTP"` |  |
| istio.gateway.existingGateway | string |  | Endereço de um gateway padrão que já exista no cluster; faz com que não se crie um gateway no istio |
| istio.gateway.name | string | `"gateway"` |  |
| istio.gateway.selector.istio | string | `"ingressgateway"` |  |
| microservice.glowroot.enabled | bool | `false` |  |
| microservice.glowroot.url | string | `"http://glowroot-central.central-collector:8181"` |  |
| microservice.health.disabled | bool | `false` |  |
| microservice.health.livenessProbe.failureThreshold | int | `30` |  |
| microservice.health.livenessProbe.initialDelaySeconds | int | `120` |  |
| microservice.health.livenessProbe.periodSeconds | int | `20` |  |
| microservice.health.path | string | `"/management/health"` |  |
| microservice.health.readinessProbe.failureThreshold | int | `1` |  |
| microservice.health.readinessProbe.initialDelaySeconds | int | `120` |  |
| microservice.health.readinessProbe.periodSeconds | int | `10` |  |
| microservice.health.scheme | string | `"HTTP"` |  |
| microservice.hpa.enabled | bool | `false` |  |
| microservice.hpa.maxReplicas | int | `10` |  |
| microservice.hpa.metrics[0].resource.name | string | `"cpu"` |  |
| microservice.hpa.metrics[0].resource.target.averageUtilization | int | `80` |  |
| microservice.hpa.metrics[0].resource.target.type | string | `"Utilization"` |  |
| microservice.hpa.metrics[0].type | string | `"Resource"` |  |
| microservice.hpa.minReplicas | int | `1` |  |
| microservice.istioLoadBalancer.simple | string | `"ROUND_ROBIN"` |  |
| microservice.jdk | int | `8` |  |
| microservice.language | string | `java` | Alternativas: "java", "php", "dotnet" (em incremento) |
| microservice.framework | string | `spring` | Alternativas: "spring", "hibernate" (em incremento) |
| microservice.springProfiles | string | `"prod,swagger"` |  |
| registry.config.key | string | `"registry-config-uri"` |  |
| registry.config.name | string | `"registry"` |  |
| registry.config.value | string | `"changeit"` |  |
| registry.secret.key | string | `"registry-admin-password"` |  |
| registry.secret.name | string | `"registry"` |  |
| registry.secret.value | string | `"changeit"` |  |
