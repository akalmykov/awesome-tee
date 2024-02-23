# awesome-tee
A curated list of resources about Trusted Execution Environments (Intel SGX, AMD SEV, etc)

## Intel SGX
### Tutorials & Samples
- [Linux Installation Instructions & Guides](https://download.01.org/intel-sgx/latest/linux-latest/docs)
   - [Solving Ubuntu apt-get NO_PUBKEY problem](https://github.com/akalmykov/awesome-tee/blob/main/intel-sgx-apt-repo-ubuntu.md)
- [SGX101](https://sgx101.gitbook.io/sgx101/)
- [SampleEnclave](https://github.com/intel/linux-sgx/tree/master/SampleCode/SampleEnclave) - the project demonstrates several fundamental usages of Intel(R) Software Guard (+simulation mode on Linux)
- [How to Run Intel® Software Guard Extensions' Simulation Mode](https://www.intel.com/content/www/us/en/developer/articles/training/usage-of-simulation-mode-in-sgx-enhanced-application.html)
- [Code Sample: Intel® Software Guard Extensions Remote Attestation End-to-End Example](https://www.intel.com/content/www/us/en/developer/articles/code-sample/software-guard-extensions-remote-attestation-end-to-end-example.html)
### Utils
- [SGX-hadware test](https://github.com/ayeks/SGX-hardware)

### SGX Libraries
- [Intel® Software Guard Extensions SSL](https://github.com/intel/intel-sgx-ssl)

### SDKs and LibOS based on SGX
- [Fortanix](https://www.fortanix.com/intel-sgx)
   - [Rust EDP](https://edp.fortanix.com/docs/)
- [Teaclave](https://teaclave.apache.org/)
- [Gramine](https://gramineproject.io/)
- [Scone](https://scontain.com/index.html?lang=en)
- [MesaTEE](https://anquan.baidu.com/product/mesatee)
- [MesaPy](https://github.com/mesalock-linux/mesapy)
- [Edgeless Systems EGo](https://www.edgeless.systems/products/ego/)
- [Edgeless RT](https://github.com/edgelesssys/edgelessrt)
- [Enarx](https://enarx.dev/)
- [Occlum](https://github.com/occlum/occlum)
- [Mystikos](https://github.com/deislabs/mystikos)
- [SGX-LKL-OE (Open Enclave Edition)](https://github.com/lsds/sgx-lkl)

### SGX and Rust
- [Secure computation in Rust: Using Intel's SGX instructions with Teaclave and Fortanix](https://blog.lambdaclass.com/secure-computation-in-rust-using-intels-sgx-instructions-with-teaclave-and-fortanix)

### SGX Cloud providers
- [Alpha3Cloud](https://alpha3cloud.com/public-cloud/compute/intel-sgx/)
   - [SGX hardware test results](https://github.com/akalmykov/awesome-tee/blob/main/sgx-hardware-Alpha3Cloud.md)
- [OVHCloud](https://www.ovhcloud.com/en/bare-metal/uc-confidential-computing/)
- [Alibaba Cloud](https://www.alibabacloud.com/help/en/ecs/user-guide/build-an-sgx-encrypted-computing-environment)
- [IBM](https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-bm-server-provision-sgx)
- [Vultr](https://zenlot.medium.com/intel-sgx-development-on-vultr-30cdfd5c9754)
  
### SGX and Web
- [SGX-ready NGINX open source server](https://github.com/enclaive/enclaive-docker-nginx-sgx)
 
### SGX and Blockchains
- [Demystifying remote attestation by taking it on-chain](https://collective.flashbots.net/t/demystifying-remote-attestation-by-taking-it-on-chain/2629)
- [DCAP v3 on-chain remote attestation](https://github.com/automata-network/automata-dcap-v3-attestation)
- [EPID on-chain remote attestation](https://github.com/PufferFinance/rave/) (EPID is depricated)



