# Uranus

Uranus is a miner designed to take its users beyond the moon (in this case, to the planet [Uranus](https://en.wikipedia.org/wiki/Uranus)).

## Supported Algorithms
| Algorithm | Fee |
| ----------- | ----------- |
| AstroBWT/v3 | 4.99%

## Usage

### Display available options
`./uranus_<architecture> -h`

### Mine with official Dero protocol
`./uranus_<architecture> -o wss://<pool>:<port> -u <your wallet>`

### Mine with stratum protocol
`./uranus_<architecture> -o straum+tcp://<pool>:<port> -u <your wallet>`

### Mine with secure stratum protocol
`./uranus_<architecture> -o straum+ssl://<pool>:<port> -u <your wallet>`

## Architecture selection
### Intel
| CPU | architecture |
| ----------- | ----------- |
| 4th Gen Intel Core processors | haswell |
| 5th Gen Intel Core processors | broadwell |
| 6th/7th/8th/9th/10th Gen Intel Core processors | skylake |
| 11th Gen Intel Core desktop processors | rocketlake |
| 11th Gen Intel Core mobile processors | tigerlake |
| 12th Gen Intel Core processors | alderlake |

### AMD
For Ryzen processors, check [here](https://en.wikipedia.org/wiki/List_of_AMD_Ryzen_processors) for the specific microarchitecture of your processor.

| CPU | architecture |
| ----------- | ----------- |
| AMD Excavator processors | excavator |
| AMD Zen/Zen+ processors | zen1 |
| AMD Zen 2 processors | zen2 |
| AMD Zen 3 processors | zen3 |

## Notes
1. Older Intel/AMD processors, and ARM processors are not supported for now.
2. The reported hashrate is inclusive of the dev fee. To calculate the effective hashrate, multiply the reported hashrate by `1 - dev fee in decimal`.