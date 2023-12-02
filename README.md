# Cricket Tournament Smart Contract

## Overview

This smart contract, named `CricketTournament`, is developed for managing a cricket tournament. It specifically focuses on keeping track of the top scorer and their total runs throughout the tournament. The contract allows the declaration of a new top scorer, triggering an event to signify when a cricketer surpasses the current leading run total.

## Features

- **Top Scorer Tracking:** The contract maintains information about the current top scorer and their total runs.
  
- **Declaration of Top Scorer:** The `declareTopScorer` function enables the declaration of a new top scorer by providing the cricketer's address and their total runs.

- **Event Emission:** Whenever a new top scorer is declared, the contract emits the `NewTopScorer` event, capturing the cricketer's address and their total runs.

## Usage

1. **Declaration of Top Scorer:**
   - Use the `declareTopScorer` function by providing the cricketer's address and their total runs.
   - Ensure that the total runs provided are greater than 0.

```solidity
function declareTopScorer(address cricketer, uint totalRuns) public {
    
}
```

2. **Event Handling:**
   - Listen for the `NewTopScorer` event to stay informed about changes in the top scorer.

```solidity
event NewTopScorer(address indexed cricketer, uint totalRuns);
```

## Error Handling

- The contract utilizes `assert` to ensure that the total runs provided are greater than 0.
- The `require` statement prevents redundant declarations by checking if the specified cricketer is not already the current top scorer.
- If the provided total runs do not surpass the current top scorer's runs, the contract `reverts` with the message "New cricketer did not beat the current top scorer."

## Author 
Shashank 

shashanksr762@gmail.com

