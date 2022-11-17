$ docker history --format "{{.Size}} - {{.ID}} - {{.CreatedBy}}" --no-trunc neo4j:5.1.0-enterprise
0B - sha256:762f1e7c7218526a1ce4213b45ebe29ac7b1846575ec3d983984f3cf8aa5f2d5 - /bin/sh -c #(nop)  CMD ["neo4j"]
0B - <missing> - /bin/sh -c #(nop)  ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
0B - <missing> - /bin/sh -c #(nop)  EXPOSE 7473 7474 7687
0B - <missing> - /bin/sh -c #(nop)  VOLUME [/data /logs]
0B - <missing> - /bin/sh -c #(nop) WORKDIR /var/lib/neo4j
0B - <missing> - /bin/sh -c #(nop)  ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
230MB - <missing> - |1 NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz /bin/sh -c apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
25kB - <missing> - /bin/sh -c #(nop) COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
2.43MB - <missing> - |1 NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz /bin/sh -c addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
0B - <missing> - /bin/sh -c #(nop)  ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
0B - <missing> - /bin/sh -c #(nop)  ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
329MB - <missing> - /bin/sh -c #(nop) COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
0B - <missing> - /bin/sh -c #(nop)  ENV JAVA_HOME=/opt/java/openjdk
0B - <missing> - /bin/sh -c #(nop)  CMD ["bash"]
80.5MB - <missing> - /bin/sh -c #(nop) ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 