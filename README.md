<p align="center">
  <img src="assets/solarsats-logo.svg" alt="SolarSats logo: the sat symbol inside a rising sun, with a rising chart line" width="160">
</p>

# SolarSats

**How many sats can your surplus solar stack?**

SolarSats is an open-source calculator for anyone considering mining as an alternative to buying bitcoin. Pick a miner, describe your solar site, and it estimates the sats you'd stack over the rig's life, block by block, across the halving schedule. Every figure is in sats: no fiat and no BTC price.

**[Open the calculator →](https://blankworker1.github.io/solar-sats/)**

## What it does

- **Built on the block schedule.** The subsidy follows the protocol exactly: 50 BTC halved every 210,000 blocks, down to the last new sat at block 6,929,999, around 2140.
- **Sats per block for each halving period**, averaged over every network block, plus what the rig earns at full power.
- **Solar model** with monthly yields and day length by latitude. The miner either runs at full power or underclocks to follow the sun, and a sunny/cloudy day mix is optional.
- **Miner profiles** from a Bitaxe up to an Antminer S21 Pro, each filling in hashrate and power when picked.
- **Mine versus buy:** sats stacked, set beside the hardware price in sats.
- **Braiins Pool payouts over Lightning** (FPPS, KYC-free), with your auto-payout threshold: when the first payout lands and how often after that.

It assumes your solar is surplus, meaning power that would otherwise go unused or exported.

## Use it

It's a single self-contained HTML file with no build step and no server. Open `index.html` in a browser, or use the GitHub Pages link above. Inputs are saved in your browser only.

## Repo layout

```
index.html                  v1 calculator (locked)
docs/v2-design.md           v2 design: local dashboard and curtailment
assets/solarsats-logo.svg   logo (PNG alongside)
```

## Roadmap: v2

v2 adds a local dashboard and controller that run on a Raspberry Pi Zero 2 W beside a Victron GX system:

- live PV, battery and miner data on a wall tablet
- miner power that follows your solar surplus, with the house and battery served first
- actual results against the calculator's projection, used to calibrate it

See [docs/v2-design.md](docs/v2-design.md). The default reference hardware is a Victron EasySolar-II GX and a Braiins OS miner. Adapters for other inverters and miners are welcome.

## Caveats

The results are estimates. Network hashrate, fees and weather will differ from any single assumption, so check the network inputs against current figures before relying on the numbers. Miner specs are the makers' rated figures, and individual units vary.

## Contributing

Issues and pull requests are welcome, especially:

- solar yield presets for more locations
- miner profiles
- v2 adapters

## Licence

TBD.
