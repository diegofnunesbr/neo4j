# Neo4j

### Instalar o Neo4j no Kubernetes:

- `git clone git@github.com:diegofnunesbr/neo4j.git`
- `cd neo4j`
- `helm install --create-namespace neo4j -n neo4j .`

### Configurar o Neo4j no arquivo hosts do Windows:

- `sudo tee -a /mnt/c/Windows/System32/drivers/etc/hosts <<< "$(ifconfig eth0 | grep 'inet ' | awk '{print $2}') neo4j.local"`

### Remover o Neo4j no Kubernetes:

- `helm uninstall neo4j -n neo4j`
