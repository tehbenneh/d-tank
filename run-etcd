#env ETCD_INITIAL_CLUSTER="etcd-01=http://192.168.101.101:2380,etcd-02=http://192.168.101.102:2380,etcd-03=http://192.168.101.103:2380"
env ETCD_INITIAL_CLUSTER_STATE="new"
env ETCD_INITIAL_CLUSTER_TOKEN="etcd-cluster-01"
env ETCD_INITIAL_ADVERTISE_PEER_URLS=http://${IP}:2380
env ETCD_DATA_DIR="/var/dtank/etcd"
env ETCD_LISTEN_PEER_URLS=http://${IP}:2380
env ETCD_LISTEN_CLIENT_URLS=http://${IP}:2379
env ETCD_ADVERTISE_CLIENT_URLS=http://${IP}:2379
env ETCD_NAME=$HOSTNAME

env DISCOVERY="$(curl -w "\n" 'https://discovery.etcd.io/new?size=3')"

/usr/local/bin/etcd

#>>/var/log/etcd.log 2>&1
