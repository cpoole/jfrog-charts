# JFrog Artifactory-ha Chart Changelog
All changes to this chart will be documented in this file.

## [0.16.3] - Sep 11, 2019
* Updated Artifactory version to 6.12.2

## [0.16.2] - Sep 9, 2019
* Updated Artifactory version to 6.12.1

## [0.16.1] - Aug 22, 2019
* Fix the nginx server_name directive used with ingress.hosts

## [0.16.0] - Aug 21, 2019
* Updated Artifactory version to 6.12.0

## [0.15.15] - Aug 18, 2019
* Fix existingSharedClaim permissions issue and example 

## [0.15.14] - Aug 14, 2019
* Updated Artifactory version to 6.11.6

## [0.15.13] - Aug 11, 2019
* Fix Ingress routing and add an example

## [0.15.12] - Aug 6, 2019
* Do not mount `access/etc/bootstrap.creds` unless user specifies a custom password or secret (Access already generates a random password if not provided one)
* If custom `bootstrap.creds` is provided (using keys or custom secret), prepare it with an init container so the temp file does not persist

## [0.15.11] - Aug 5, 2019
* Improve binarystore config
    1. Convert to a secret
    2. Move config to values.yaml
    3. Support an external secret 

## [0.15.10] - Aug 5, 2019
* Don't create the nginx configmaps when nginx.enabled is false

## [0.15.9] - Aug 1, 2019
* Fix masterkey/masterKeySecretName not specified warning render logic in NOTES.txt

## [0.15.8] - Jul 28, 2019
* Simplify nginx setup and shorten initial wait for probes 

## [0.15.7] - Jul 25, 2019
* Updated README about how to apply Artifactory licenses

## [0.15.6] - Jul 22, 2019
* Change Ingress API to be compatible with recent kubernetes versions

## [0.15.5] - Jul 22, 2019
* Updated Artifactory version to 6.11.3

## [0.15.4] - Jul 11, 2019
* Add `artifactory.customVolumeMounts` support to member node statefulset template

## [0.15.3] - Jul 11, 2019
* Add ingress.hosts to the Nginx server_name directive when ingress is enabled to help with Docker repository sub domain configuration 

## [0.15.2] - Jul 3, 2019
* Add the option for changing nginx config using values.yaml and remove outdated reverse proxy documentation

## [0.15.1] - Jul 1, 2019
* Updated Artifactory version to 6.11.1

## [0.15.0] - Jun 27, 2019
* Updated Artifactory version to 6.11.0 and Restart Primary node when bootstrap.creds file has been modified in artifactory-ha

## [0.14.4] - Jun 24, 2019
* Add the option to provide an IP for the access-admin endpoints

## [0.14.3] - Jun 24, 2019
* Update chart maintainers

## [0.14.2] - Jun 24, 2019
* Change Nginx to point to the artifactory externalPort

## [0.14.1] - Jun 23, 2019
* Add values files for small, medium and large installations

## [0.14.0] - Jun 20, 2019
* Use ConfigMaps for nginx configuration and remove nginx postStart command

## [0.13.10] - Jun 19, 2019
* Updated Artifactory version to 6.10.4

## [0.13.9] - Jun 18, 2019
* Add the option to provide additional ingress rules

## [0.13.8] - Jun 14, 2019
* Updated readme with improved external database setup example

## [0.13.7] - Jun 6, 2019
* Updated Artifactory version to 6.10.3
* Updated installer-info template

## [0.13.6] - Jun 6, 2019
* Updated Google Cloud Storage API URL and https settings

## [0.13.5] - Jun 5, 2019
* Delete the db.properties file on Artifactory startup

## [0.13.4] - Jun 3, 2019
* Updated Artifactory version to 6.10.2

## [0.13.3] - May 21, 2019
* Updated Artifactory version to 6.10.1

## [0.13.2] - May 19, 2019
* Fix missing logger image tag

## [0.13.1] - May 15, 2019
* Support `artifactory.persistence.cacheProviderDir` for on-premise cluster 

## [0.13.0] - May 7, 2019
* Updated Artifactory version to 6.10.0

## [0.12.23] - May 5, 2019
* Add support for setting `artifactory.async.corePoolSize`

## [0.12.22] - May 2, 2019
* Remove unused property `artifactory.releasebundle.feature.enabled`

## [0.12.21] - Apr 30, 2019
* Add support for JMX monitoring

## [0.12.20] - Apr29, 2019
* Added support for headless services

## [0.12.19] - Apr 28, 2019
* Added support for `cacheProviderDir`

## [0.12.18] - Apr 18, 2019
* Changing API StatefulSet version to `v1` and permission fix for custom `artifactory.conf` for Nginx

## [0.12.17] - Apr 16, 2019
* Updated documentation for Reverse Proxy Configuration

## [0.12.16] - Apr 12, 2019
* Added support for `customVolumeMounts`

## [0.12.15] - Aprl 12, 2019
* Added support for `bucketExists` flag for googleStorage

## [0.12.14] - Apr 11, 2019
* Replace `curl` examples with `wget` due to the new base image

## [0.12.13] - Aprl 07, 2019
* Add support for providing the Artifactory license as a parameter

## [0.12.12] - Apr 10, 2019
* Updated Artifactory version to 6.9.1

## [0.12.11] - Aprl 04, 2019
* Add support for templated extraEnvironmentVariables

## [0.12.10] - Aprl 07, 2019
* Change network policy API group

## [0.12.9] - Aprl 04, 2019
* Apply the existing PVC for members (in addition to primary)

## [0.12.8] - Aprl 03, 2019
* Bugfix for userPluginSecrets

## [0.12.7] - Apr 4, 2019
* Add information about upgrading Artifactory with auto-generated postgres password

## [0.12.6] - Aprl 03, 2019
* Added installer info

## [0.12.5] - Aprl 03, 2019
* Allow secret names for user plugins to contain template language

## [0.12.4] - Apr 02, 2019
* Fix issue #253 (use existing PVC for data and backup storage)

## [0.12.3] - Apr 02, 2019
* Allow NetworkPolicy configurations (defaults to allow all)

## [0.12.2] - Aprl 01, 2019
* Add support for user plugin secret

## [0.12.1] - Mar 26, 2019
* Add the option to copy a list of files to ARTIFACTORY_HOME on startup

## [0.12.0] - Mar 26, 2019
* Updated Artifactory version to 6.9.0

## [0.11.18] - Mar 25, 2019
* Add CI tests for persistence, ingress support and nginx

## [0.11.17] - Mar 22, 2019
* Add the option to change the default access-admin password

## [0.11.16] - Mar 22, 2019
* Added support for `<artifactory|nginx>.<readiness|liveness>Probe.path` to customise the paths used for health probes

## [0.11.15] - Mar 21, 2019
* Added support for `artifactory.customSidecarContainers` to create custom sidecar containers
* Added support for `artifactory.customVolumes` to create custom volumes

## [0.11.14] - Mar 21, 2019
* Make ingress path configurable

## [0.11.13] - Mar 19, 2019
* Move the copy of bootstrap config from postStart to preStart for Primary

## [0.11.12] - Mar 19, 2019
* Fix existingClaim example

## [0.11.11] - Mar 18, 2019
* Disable the option to use nginx PVC with more than one replica

## [0.11.10] - Mar 15, 2019
* Wait for nginx configuration file before using it

## [0.11.9] - Mar 15, 2019
* Revert securityContext changes since they were causing issues

## [0.11.8] - Mar 15, 2019
* Fix issue #247 (init container failing to run)

## [0.11.7] - Mar 14, 2019
* Updated Artifactory version to 6.8.7

## [0.11.6] - Mar 13, 2019
* Move securityContext to container level

## [0.11.5] - Mar 11, 2019
* Add the option to use existing volume claims for Artifactory storage

## [0.11.4] - Mar 11, 2019
* Updated Artifactory version to 6.8.6

## [0.11.3] - Mar 5, 2019
* Updated Artifactory version to 6.8.4

## [0.11.2] - Mar 4, 2019
* Add support for catalina logs sidecars

## [0.11.1] - Feb 27, 2019
* Updated Artifactory version to 6.8.3

## [0.11.0] - Feb 25, 2019
* Add nginx support for tail sidecars

## [0.10.3] - Feb 21, 2019
* Add s3AwsVersion option to awsS3 configuration for use with IAM roles

## [0.10.2] - Feb 19, 2019
* Updated Artifactory version to 6.8.2

## [0.10.1] - Feb 17, 2019
* Updated Artifactory version to 6.8.1
* Add example of `SERVER_XML_EXTRA_CONNECTOR` usage

## [0.10.0] - Feb 15, 2019
* Updated Artifactory version to 6.8.0

## [0.9.7] - Feb 13, 2019
* Updated Artifactory version to 6.7.3

## [0.9.6] - Feb 7, 2019
* Add support for tail sidecars to view logs from k8s api

## [0.9.5] - Feb 6, 2019
* Fix support for customizing statefulset `terminationGracePeriodSeconds`

## [0.9.4] - Feb 5, 2019
* Add support for customizing statefulset `terminationGracePeriodSeconds`

## [0.9.3] - Feb 5, 2019
* Remove the inactive server remove plugin

## [0.9.2] - Feb 3, 2019
* Updated Artifactory version to 6.7.2

## [0.9.1] - Jan 27, 2019
* Fix support for Azure Blob Storage Binary provider

## [0.9.0] - Jan 23, 2019
* Updated Artifactory version to 6.7.0

## [0.8.10] - Jan 22, 2019
* Added support for `artifactory.customInitContainers` to create custom init containers

## [0.8.9] - Jan 18, 2019
* Added support of values ingress.labels

## [0.8.8] - Jan 16, 2019
* Mount replicator.yaml (config) directly to /replicator_extra_conf

## [0.8.7] - Jan 15, 2018
* Add support for Azure Blob Storage Binary provider

## [0.8.6] - Jan 13, 2019
* Fix documentation about nginx group id

## [0.8.5] - Jan 13, 2019
* Updated Artifactory version to 6.6.5

## [0.8.4] - Jan 8, 2019
* Make artifactory.replicator.publicUrl required when the replicator is enabled

## [0.8.3] - Jan 1, 2019
* Updated Artifactory version to 6.6.3
* Add support for `artifactory.extraEnvironmentVariables` to pass more environment variables to Artifactory

## [0.8.2] - Dec 28, 2018
* Fix location `replicator.yaml` is copied to

## [0.8.1] - Dec 27, 2018
* Updated Artifactory version to 6.6.1

## [0.8.0] - Dec 20, 2018
* Updated Artifactory version to 6.6.0

## [0.7.17] - Dec 17, 2018
* Updated Artifactory version to 6.5.13

## [0.7.16] - Dec 12, 2018
* Fix documentation about Artifactory license setup using secret

## [0.7.15] - Dec 9, 2018
* AWS S3 add `roleName` for using IAM role

## [0.7.14] - Dec 6, 2018
* AWS S3 `identity` and `credential` are now added only if have a value to allow using IAM role

## [0.7.13] - Dec 5, 2018
* Remove Distribution certificates creation.

## [0.7.12] - Dec 2, 2018
* Remove Java option "-Dartifactory.locking.provider.type=db". This is already the default setting.

## [0.7.11] - Nov 30, 2018
* Updated Artifactory version to 6.5.9

## [0.7.10] - Nov 29, 2018
* Fixed the volumeMount for the replicator.yaml

## [0.7.9] - Nov 29, 2018
* Optionally include primary node into poddisruptionbudget

## [0.7.8] - Nov 29, 2018
* Updated postgresql version to 9.6.11

## [0.7.7] - Nov 27, 2018
* Updated Artifactory version to 6.5.8

## [0.7.6] - Nov 18, 2018
* Added support for configMap to use custom Reverse Proxy Configuration with Nginx

## [0.7.5] - Nov 14, 2018
* Updated Artifactory version to 6.5.3

## [0.7.4] - Nov 13, 2018
* Allow pod anti-affinity settings to include primary node

## [0.7.3] - Nov 12, 2018
* Support artifactory.preStartCommand for running command before entrypoint starts

## [0.7.2] - Nov 7, 2018
* Support database.url parameter (DB_URL)

## [0.7.1] - Oct 29, 2018
* Change probes port to 8040 (so they will not be blocked when all tomcat threads on 8081 are exhausted)

## [0.7.0] - Oct 28, 2018
* Update postgresql chart to version 0.9.5 to be able and use `postgresConfig` options

## [0.6.9] - Oct 23, 2018
* Fix providing external secret for database credentials

## [0.6.8] - Oct 22, 2018
* Allow user to configure externalTrafficPolicy for Loadbalancer

## [0.6.7] - Oct 22, 2018
* Updated ingress annotation support (with examples) to support docker registry v2

## [0.6.6] - Oct 21, 2018
* Updated Artifactory version to 6.5.2

## [0.6.5] - Oct 19, 2018
* Allow providing pre-existing secret containing master key
* Allow arbitrary annotations on primary and member node pods
* Enforce size limits when using local storage with `emptyDir`
* Allow `soft` or `hard` specification of member node anti-affinity
* Allow providing pre-existing secrets containing external database credentials
* Fix `s3` binary store provider to properly use the `cache-fs` provider
* Allow arbitrary properties when using the `s3` binary store provider

## [0.6.4] - Oct 18, 2018
* Updated Artifactory version to 6.5.1

## [0.6.3] - Oct 17, 2018
* Add Apache 2.0 license

## [0.6.2] - Oct 14, 2018
* Make S3 endpoint configurable (was hardcoded with `s3.amazonaws.com`)

## [0.6.1] - Oct 11, 2018
* Allows ingress default `backend` to be enabled or disabled (defaults to enabled)

## [0.6.0] - Oct 11, 2018
* Updated Artifactory version to 6.5.0

## [0.5.3] - Oct 9, 2018
* Quote ingress hosts to support wildcard names

## [0.5.2] - Oct 2, 2018
* Add `helm repo add jfrog https://charts.jfrog.io` to README

## [0.5.1] - Oct 2, 2018
* Set Artifactory to 6.4.1

## [0.5.0] - Sep 27, 2018
* Set Artifactory to 6.4.0

## [0.4.7] - Sep 26, 2018
* Add ci/test-values.yaml

## [0.4.6] - Sep 25, 2018
* Add PodDisruptionBudget for member nodes, defaulting to minAvailable of 1

## [0.4.4] - Sep 2, 2018
* Updated Artifactory version to 6.3.2

## [0.4.0] - Aug 22, 2018
* Added support to run as non root
* Updated Artifactory version to 6.2.0

## [0.3.0] - Aug 22, 2018
* Enabled RBAC Support
* Added support for PostStartCommand (To download Database JDBC connector)
* Increased postgresql max_connections
* Added support for `nginx.conf` ConfigMap
* Updated Artifactory version to 6.1.0
