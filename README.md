# guacamole-tailscale-compose

An easy [Compose](https://docs.docker.com/compose/) setup to run [Apache Guacamole](https://guacamole.apache.org) and register it with [Tailscale](https://tailscale.com).

## Usage

1.  Copy [.env.example](./.env.example) to ".env".

2.  Edit settings:

    -   Set "POSTGRES_PASSWORD" to a random password.

    -   Get a key from [Keys](https://login.tailscale.com/admin/settings/keys) and put it in "TS_AUTHKEY".

    -   **Optional:** Change "GUACAMOLE_IMAGE" and "GUACD_IMAGE" if you want to use different images.

3.  Start the compose:

    ```shell
    docker compose up
    ```

4.  Go to http://guacamole:8080/guacamole/.

5.  Sign in as `guacadmin` with password `guacadmin`, add your own user, and remove access to that default user.

All state will be stored in a "volumes" directory, which Compose will create. The entire system can be reset by shutting down the containers, removing that directory and starting again.

## Thanks

Thanks to:

-   [guacamole-docker-compose](https://github.com/boschkundendienst/guacamole-docker-compose/), which I based my first draft on before creating this setup.
-   And, of course, the [Apache Guacamole](https://guacamole.apache.org/) team.
