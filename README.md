
# GCP Example Network

### Resources Created

  * A `network`.
  * A `public_subnet`.
  * A `private_subnet`.


## Compatibility

Tested with:
  * Cloudify 4.2


## Pre-installation steps

Upload the required plugins:

  * [GCP Plugin](https://github.com/cloudify-cosmo/cloudify-gcp-plugin/releases).

_Check the blueprint for the exact version of the plugin._


If you do not provide your own `deployment inputs` below, you must add these secrets to your Cloudify Manager `tenant`:

  * `gcp_client_x509_cert_url`
  * `gcp_gcp_client_email`
  * `client_id`
  * `gcp_project_id`
  * `gcp_private_key_id`
  * `gcp_private_key`
  * `gcp_zone`, such as `us-east1-b`.
  * `gcp_region`, such as `us-east1`.


## Installation

On your Cloudify Manager, navigate to `Local Blueprints` select `Upload`.

[Right-click and copy URL](https://github.com/cloudify-examples/gcp-example-network/archive/master.zip). Paste where it says `Enter blueprint url`. Provide a blueprint name, such as `examples-network` in the field labeled `blueprint name`. Select `simple-blueprint.yaml` from `Blueprint filename` menu.

After the new blueprint has been created, click the `Deploy` button.

Navigate to `Deployments`, find your new deployment, select `Install` from the `workflow`'s menu. At this stage, you may provide your own values for any of the default `deployment inputs`.


## Update Deployment

In order to provide outbound internet access to the private subnet, you can update the deployment.

Navigate to `Deployments`, find your deployment, click on it. Once the deployment's page has loaded, click the `Update Deployment` button. [Right-click and copy URL](https://github.com/cloudify-examples/vpc-scenario2-blueprint/archive/master.zip). Paste where it says `Enter new blueprint url`. This time, select `update-blueprint.yaml` from `Blueprint filename` menu.


## Uninstallation

Navigate to the deployment and select `Uninstall`. When the uninstall workflow is finished, select `Delete deployment`.
