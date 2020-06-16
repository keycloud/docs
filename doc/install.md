# Install KeyCloud
A `nginx` reverse proxy is included which is configured to listen to port `80` and `443`, additionally port `8080` ist used for the KeyCloud backend and another more flexible one for the PostgreSQL database (default is `5432`). We recommend to stay with our configuration and disable services blocking those ports in your setup.

1. Install `docker` and `docker-compose`
2. Clone your repository `git clone git@github.com:keycloud/keycloud.git`
3. Navigate into `./keycloud/server`
4. Delete the `docker-compose.yml` file and rename the `docker-compose-alt.yml` file to `docker-compose.yml`
5. Adjust the `.env` file, the `PG_ADMIN` values are not necessary. In case you stay with our configuration `POSTGRES_DB=keycloud` and `POSTGRES_HOST=keycloud-db`
6. Edit the `nginx.conf` and replace `keycloud-dev.zeekay.dev` with your hostname (line 12)
7. Install `letsencrypt (certbot)` and create TLS certificates for your hostname or domain.
8. Open the `nginx-conf` again and adjust line 27 and 28 to fit your certificate location
9. Fire everything up using `docker-compose up -d`

The API is reachable at `https://hostname`, the dashboard at `https://hostname/dashboard/`
