# 2.0.0

## New options

- Added an option to use a specific hostname for the Tailscale machine instead of "guacamole".
- Added options to allow specification of specific Docker images for "guacamole" and "guacd", e.g. for specific versions or custom rebuilds.

## Changes

- Reconfigured networking so outgoing connections can also go through the Tailscale host used for the web service.
- Silenced repeated postgres warnings from the healthcheck.

# 1.0.0

Initial version.
