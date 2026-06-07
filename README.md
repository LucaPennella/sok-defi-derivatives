# Unified Framework and Comparative Study of Decentralized Finance Derivatives Protocols

This repository accompanies the paper:

**"A Unified Framework and Comparative Study of Decentralized Finance Derivatives Protocols"**

## Overview

The repository contains simulations of derivative contract dynamics in DeFi, as described in the paper. It currently focuses on:

- Perpetual futures

The simulations are based on Monte Carlo price paths and track:

- Position equity
- Realized PnL (profit and loss)
- Liquidation events
- Funding costs
- Trading fees

## Mapping to the analytical framework

The simulation code follows the analytical abstraction introduced in the paper. In particular, the perpetual futures simulation is organized around three levels:

- `instrument_parameters`: position direction, collateral, leverage, maintenance margin, and position size;
- `market_parameters`: price process, volatility, drift, time step, and simulation horizon;
- `protocol_parameters`: trading fees, borrowing costs, funding-rate rule, liquidation rule, and slippage assumptions.

This structure clarifies which components belong to the derivative instrument, which components describe the simulated market environment, and which components encode protocol-level mechanisms. It also defines the boundary between the abstract analytical framework introduced in the paper and the specific perpetual-futures instantiation implemented in the simulation code.

## Structure

- `Perpetuals-Simulation-notebook.ipynb`: Jupyter notebook implementing Monte Carlo simulations for perpetual futures contracts.
