```shell
docker run \
--mount type=bind,source="$(pwd)",target=/home/schcrwlr/share \
--rm -it \
schemacrawler/schemacrawler \
/opt/schemacrawler/bin/schemacrawler.sh \
--server=sqlite \
--database=share/chinook-database-2.0.1.sqlite \
--info-level=standard \
--command script \
--title "Chinook Database Schema" \
--script-language python \
--script plantuml.py
```

```shell
docker run \
--mount type=bind,source="$(pwd)",target=/home/schcrwlr \
--rm -it \
schemacrawler/schemacrawler \
/opt/schemacrawler/bin/schemacrawler.sh \
--server mysql \
--host localhost \
--port 3306 \
--user root \
--password=pass \
--database proof_of_solvency_bot \
--info-level standard \
--command schema \
--output-file rfam.pdf
```
```shell
docker run \
--mount type=bind,source="$(pwd)",target=/home/schcrwlr \
--rm -it \
schemacrawler/schemacrawler \
/opt/schemacrawler/bin/schemacrawler.sh \
--server mysql \
--host host.docker.internal \
--port 3306 \
--user root \
--password=pass \
--database proof_of_solvency_bot \
--info-level standard \
--command schema \
--output-file Downloads/rfam.pdf
```

```shell
docker run \
--mount type=bind,source="$(pwd)",target=/home/schcrwlr/share \
--rm -it \
schemacrawler/schemacrawler \
/opt/schemacrawler/bin/schemacrawler.sh \
--server mysql \
--host host.docker.internal \
--port 3306 \
--user root \
--password=pass \
--info-level=standard \
--command script \
--title "test" \
--script-language python \
--script plantuml.py
```

```shell
docker run \
--mount type=bind,source="$(pwd)",target=/home/schcrwlr/share \
--rm -it \
schemacrawler/schemacrawler \
/opt/schemacrawler/bin/schemacrawler.sh \
--server mysql \
--host host.docker.internal \
--port 3306 \
--user root \
--password=pass \
--database proof_of_solvency_bot \
--info-level standard \
--command script \
--script-language python \
--script plantuml.py \
--output-file Documents/sc.puml
```

success:
```shell
docker run \
--mount type=bind,source="$(pwd)",target=/home/schcrwlr/share \
--rm -it \
schemacrawler/schemacrawler \
/opt/schemacrawler/bin/schemacrawler.sh \
--server mysql \
--host host.docker.internal \
--database proof_of_solvency_bot \
--port 3306 \
--user root \
--password=pass \
--info-level=standard \
--command script \
--title "test" \
--script-language python \
--script plantuml.py
```

https://medium.com/geekculture/what-is-schemacrawler-and-why-would-you-need-it-b9c496054533