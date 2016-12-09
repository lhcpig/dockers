[![](https://images.microbadger.com/badges/image/lhcpig/hdfs.svg)](https://microbadger.com/images/lhcpig/hdfs "Get your own image badge on microbadger.com")

This docker is to build HDFS.

---
# 1. build
```bash
sudo docker build . -t lhcpig/hdfs
```

---

# 2. How to use

Just use the command:
```bash
sudo docker run -it -d -h hdfs --name hdfs-test -p9000:9000 -p50070:50070 lhcpig/hdfs
sudo docker exec -it hdfs-test start-dfs.sh
```
