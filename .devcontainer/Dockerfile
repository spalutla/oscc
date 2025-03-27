FROM ubuntu:22.04

# Install necessary packages
RUN apt update && apt install -y \
    verilator \
    python3 python3-pip \
    git make g++ \
    gtkwave \
    && rm -rf /var/lib/apt/lists/*

# Set up Python environment
RUN pip3 install --upgrade pip \
    && pip3 install cocotb cocotb-test pytest

# Set working directory
WORKDIR /workspace

RUN ln -sf /usr/share/zoneinfo/UTC /etc/localtime

CMD ["/bin/bash"]

