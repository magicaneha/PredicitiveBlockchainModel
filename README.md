static analysis tool for Hyperledger Fabric smart contracts (chaincode) aimed at increase efficiency of blockchain
My research area expanded my software capabilities in the blockchain field. I created an efficient, private blockchain-based personal data vault to protect users' most sensitive data (e.g., health records and identification documents). I was able to overcome some of the blockchain's well-known inefficiencies by developing a predictive model for pre-fetching expected user data using Python libraries such as pandas, numpy, keras, and tensorflow. caliper benchmarks tools, as well as experimenting with the latest version of IBM's Hyperledger fabric, to test efficiency. I primarily used GO, Hyperledger Fabric, Prometheus, and Docker.


information:
1.	Fabric 2.2
a.	curl -sSL https://bit.ly/2ysbOFE | bash -s -- 2.2.5 1.5.2
b.	open nano ~/.zshrc add path there.
c.	export PATH=<path to download location>/bin:$PATH

./network.sh deployCC -ccn fabcar -ccp ../../caliper-benchmarks/src/fabric/samples/fabcar/go -cci initLedger -ccl go
./network.sh deployCC -ccn smallbank -ccp ../../caliper-benchmarks/src/fabric/scenario/smallbank/go -cci initLedger -ccl go
d.
2.	Caliper 0.4.2
3.	git clone https://github.com/hyperledger/caliper-benchmarks.git
4.	cd caliper-benchmarks
5.	cd caliper-benchmarks


user@ubuntu:~/caliper-benchmarks$ npm install --only=prod @hyperledger/caliper-cli@0.5.0
user@ubuntu:~/caliper-benchmarks$ npx caliper bind --caliper-bind-sut fabric:2.2



npx caliper launch manager \
    --caliper-workspace . \
    --caliper-benchconfig benchmarks/samples/fabric/fabcar/config.yaml \
    --caliper-networkconfig networks/fabric/test-network.yaml --caliper-flow-only-test --caliper-fabric-gateway-enabled

npx caliper launch manager --caliper-fabric-gateway-enabled





docker run \
    -v $PWD:/hyperledger/caliper/workspace \
