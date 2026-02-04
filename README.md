# mokelumne

UC Berkeley Library's Airflow installation, libraries, and Dags.

This is a proof of concept repo for Airflow under Docker Compose/Swarm. As is, it should be deployed with caution.

Consult [Running Airflow in Docker](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html) for more information. The compose file in the initial commit reflects the composed file linked from those docs.

Airflow's configuration is propagated by environment variables defined upstream and that are defined and handled in the base image. You can use a `.env` file or pass them. Arguably, the most important is `AIRFLOW_UID`, which should match the uid you want the container to run as.  The UID set in `example.env` maps to the reserved UID for the `airflow` user in [lap/workflow](https://git.lib.berkeley.edu/lap/workflow/-/wikis/UIDs).
