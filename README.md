# whisper-build-with-openvino-experience-
a doc for self use


## binary build
```
docker run --rm -it -v ./git/:/opt ubuntu:latest
```

in docker bash
```
apt install cmake make build-essential git
```

in docker bash
* follow the instruction of https://docs.openvino.ai/2025/get-started/install-openvino.html?PACKAGE=OPENVINO_BASE&VERSION=v_2025_0_0&OP_SYSTEM=LINUX&DISTRIBUTION=APT
```
wget https://apt.repos.intel.com/intel-gpg-keys/GPG-PUB-KEY-INTEL-SW-PRODUCTS.PUB
apt-key add GPG-PUB-KEY-INTEL-SW-PRODUCTS.PUB
echo "deb https://apt.repos.intel.com/openvino/2025 ubuntu24 main" | tee /etc/apt/sources.list.d/intel-openvino-2025.list
apt update
apt-cache search openvino
apt install openvino-2025.0.0
```
in docker bash
```
git clone https://github.com/ggerganov/whisper.cpp.git
cd whisper.cpp
# using CMake
cmake -B build -DWHISPER_COREML=1
cmake --build build -j --config Release
```

build/bin/*



## converting 
* later sin write la
