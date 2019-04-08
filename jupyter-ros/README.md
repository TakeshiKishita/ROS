**OS**: Ubuntu 18.04 bionic  
**Kernel**: x86_64 Linux 4.15.0-46-generic  
**CPU**: Intel Core i7-9700K @ 8x 4.9GHz  
**GPU**: GeForce RTX 2070  
**RAM**: 944MiB / 32034MiB  

**Docker**: 18.09.3, build 774a1f4

```bash
docker build ./ -t jupyter-ros
docker run --name jupyter-ros --runtime=nvidia  -it -p 8888:8888 -v /work:/work jupyter-ros bash
```
