# Nombre de la asignación

Participantes
- Galileo Teco
- Hector Castro
- Martin Castañeda
- Carlos Rodriguez
- Jose Villafuerte
- Fidel Salas
- Cristina Ramirez
- Damian Cabrera
- Jaquelina Hipolito

Actividades
- BackUp
- Upgrades Master

Comandos
backup
- docker run --rm --net host -v $PWD:/vol \
    -v /etc/kubernetes/pki/etcd:/etc/kubernetes/pki/etcd:ro \
    -e ETCDCTL_API=3 k8s.gcr.io/etcd:3.3.10 \
    etcdctl --endpoints=https://[127.0.0.1]:2379 \
            --cacert=/etc/kubernetes/pki/etcd/ca.crt \
            --cert=/etc/kubernetes/pki/etcd/healthcheck-client.crt \
            --key=/etc/kubernetes/pki/etcd/healthcheck-client.key \
            snapshot save /vol/snapshot
    Snapshot saved at /vol/snapshot

  sudo apt install kubeadm=1.27.0-00

  sudo kubeadm upgrade plan

  sudo kubeadm upgrade apply v1.27.0

  sudo apt install kubelet=1.27.0-00

  scp  /etc/kubernetes/admin.conf k8s:nodo 2 y 3


Recursos externos
- Recurso externo

Artifactos
- Anexar artifactos al directorio de respuesta
