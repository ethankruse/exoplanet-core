FROM nvidia/cuda:10.2-devel-ubuntu18.04

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y \
      git \
      python3-pip \
      && \
    apt-get autoremove --purge -y && \
    apt-get autoclean -y && \
    rm -rf /var/cache/apt/* /var/lib/apt/lists/*

RUN python3 -m pip install -U pip && \
    python3 -m pip install pytest && \
    python3 -m pip install -U jax==0.2.13 jaxlib==0.1.65+cuda102 -f https://storage.googleapis.com/jax-releases/jax_releases.html
