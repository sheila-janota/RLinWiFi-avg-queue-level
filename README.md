# RLinWiFi-avg-queue-level
This repository presents a contention window optimization solution for Wi-Fi where the network information is based on the averaged normalized transmission queues’ level.

## Prerequisites
1) Installation of python 3.6 and tensorflow dependencies are needed to run the simulation. 

Installation of the following libraries are also needed.
tqdm==4.35.0
torch==0.4.1
torchvision==0.2.1
tensorflow==1.14.0
numpy==1.16.3
comet-ml==2.0.12

2) Installation of the ns3-gym environment (https://github.com/tkn-tub/ns3-gym).

3) CometML account is also needed (https://www.comet.ml/signup) to observe the resultsing the graphs. After creating it update the `comet_token.json` file with your credentials.

Run BEB tests

positional arguments:
  N                     number of stations for the scenario (min: 5)

optional arguments:
  -h, --help            show this help message and exit
  --scenario SCENARIOS [SCENARIOS ...]
                        scenarios to run (available: [basic, convergence])
  --beb                 run 802.11 default instead of look-up table
```

Example:
```bash
python agent_training.py                                          # DDPG agent
python tf_agent_training.py                                       # DQN agent
python beb_tests.py --beb 5 10 15 --scenario basic convergence    # Original 802.11 backoff
```
