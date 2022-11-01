# Uranus

Uranus is a miner designed to take its users beyond the moon (in this case, to the planet [Uranus](https://en.wikipedia.org/wiki/Uranus)).

Supports Windows, Linux, and Android.

## Supported Algorithms
| Algorithm | Fee |
| ----------- | ----------- |
| AstroBWT/v3 | ~~4.99%~~ 3.75% |

## Usage

### Display available options
`./uranus -h`

### Mine with official Dero protocol
`./uranus -o wss://<pool>:<port> -u <your wallet>`

### Mine with stratum protocol
`./uranus -o straum+tcp://<pool>:<port> -u <your wallet>`

### Mine with secure stratum protocol
`./uranus -o straum+ssl://<pool>:<port> -u <your wallet>`

### HiveOS
Create a custom miner with the following settings:

| Option | Value |
| ----------- | ----------- |
| Name | uranus |
| Installation URL | https://github.com/Intergalactic-Mining/Uranus/releases/download/0.0.3/uranus-0.0.3_hiveos.tar.gz |
| Hash algorithm | astrobwt |
| Wallet and worker template | %WAL%.%WORKER_NAME% |
| Pool URL | `stratum+tcp://<stratum pool host>:<port>` or `wss://<dero node host>:<port>`  |
| Pass | |
| Extra config arguments | (optional) `-t <number of threads>` |

### Android (ARMv8 only)
1. Install [Termux](https://termux.dev/).
2. Download and extract the miner
`curl -sLO https://github.com/Intergalactic-Mining/Uranus/releases/download/0.0.3/uranus-0.0.3-android-arm64.tar.gz && tar -xf uranus-0.0.3-android-arm64.tar.gz`
3. Run the miner with
`./uranus -o <protocol>://<pool>:<port> -u <your wallet>`

You can use the argument `-t <number of threads>` to change the number of threads used (to avoid thermal throttling).

## Notes
1. Processors older than Intel Haswell and AMD Excavator are not supported for now.
2. The reported hashrate is inclusive of the dev fee. To calculate the effective hashrate, multiply the reported hashrate by `1 - dev fee in decimal`.