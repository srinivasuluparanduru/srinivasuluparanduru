
# Containerised a python application
https://docs.docker.com/language/python/containerize/


As your codebase grows larger, traditional methods of file sharing like bind mounts may become inefficient or slow, especially in development environments where frequent access to files is necessary. Synchronized file shares improve bind mount performance by leveraging synchronized filesystem caches. This optimization ensures that file access between the host and virtual machine (VM) is fast and efficient.

https://docs.docker.com/get-started/docker-concepts/running-containers/sharing-local-files/
