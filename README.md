# Reinforcement_Learning_based_financial_Trading_Bot

## Project Domain

Financial trading involves the buying and selling of financial instruments with a profit making objective. These can be cash instruments, like shares, forex or bonds. Through the recent technological advancements, it has become possible to leverage technology to solve real life domain specific business/ customer centric problems. Automation is a trending area in the engineering domain which can help simplify and maximize the outcome of interest. Apart from this, deep learning approaches like reinforcement learning have a great potential to solve attain automation in certain business domains, thereby maximizing the work outcome. Introducing technology in the financial sector has become a field by itself known as financial technology. Financial technology (FinTech) is the technology and innovation that aims to compete with traditional financial methods in the delivery of financial services.

## Probelem Statement

Introducing Automation in Financial Trading of assets using Reinforcement Learning where the agent will be able to perform actions in the custom trading environment using an actor critic approach.

## Project Objectives

The main aim of the project is to design deep learning approaches to implement the following pertaining to financial/crypto markets.

1. Build a trading bot based on Reinforcement Learning where the agent can make decisions to buy, sell or hold financial assets based on experience in the environment.
2. Leverage the Actor-Critic methodology to build the best possible reinforcement model which maximizes the award (Monetary profit in this case).
3. Use various Actor-Critic approaches like A2C, DDPG, PPO and TD3.
4. Evaluate the model and derive a visualization indicating the performance in trade and hence the profits earned.

## Methodology

1. ACQUIRING THE DATASET

   - The dataset of past 10-15 years were downloaded using the Yahoo Finance API.
   - Indian scenario was considered in choosing the companies for stock related data. Reliance, HDFC bank and Wipro were considered in the implementation.

   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/dataset.png)

2. Pre-Processing of the dataset

   - An additional feature was created in the dataset thereby leveraging the technical indicator.
   - Moving Average Convergence Divergence (MACD) is a trend-following momentum indicator that shows the relationship between two moving averages of a security’s price.
   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/processedDataset.png)

3. Creation of Custom Trading Environment:
   - There should be a trading environment in which the Agent performs actions as per the action space and learns based on the reinforcement received.
4. Usage of Actor-Critic Strategies to make the agent learn in the environment

   - Actor-critic learning is a reinforcement-learning technique in which you simultaneously learn a policy function and a value function.
   - The policy function tells you how to make decisions, and the value function helps improve the training process for the value function.

   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/RL.png)

   - `Proximal Policy Optimization (PPO)`

     - PPO is introduced to control the policy gradient update and ensure that the new policy will not be too different from the older one.
     - PPO tries to simplify the objective of Trust Region Policy Optimization (TRPO) by introducing a clipping term to the objective function.

   - `A2C (Advantage Actor Critic)`

     - A2C uses 2 copies of the same agent working in parallel to update gradients with different data samples.
     - Each agent works independently to interact with the same environment.

   - `DDPG (Deep Deterministic Policy Gradient)`

     - DDPG combines the frameworks of both Q-learning and policy gradient, and uses neural networks as function approximators.

   - `TD3 (Twin Delayed DDPG)`
     Features of TD3:
     1. Using a pair of critic networks (The twin part of the title)
     2. Delayed updates of the actor (The delayed part)
     3. Action noise regularisation

5. Evaluating the Reinforcement Learning Agent:

   - The model is evaluated in the test environment based on the following metrics:
     - `Sharpe Ratio:` The Sharpe ratio adjusts a portfolio’s past performance—or expected future performance—for the excess risk that was taken by the investor. A high Sharpe ratio is good when compared to similar portfolios or funds with lower returns.
     - `Total Profits generated:` Maximization of monetary profits is of paramount importance. So through test set, net profits are also considered over a period of time.

6. Backtesting of strategy
   - Backtesting is accomplished by reconstructing, with historical data, trades that would have occurred in the past using rules defined by a given strategy. The result offers statistics to gauge the effectiveness of the strategy.

## Results and Discussions

    Performance of the trading agent on 3 different test environments are as follows:

1. RELIANCE<br/>

   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/reliance.png)

2. WIPRO<br/>

   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/Wipro.png)

3. HDFC<br/>

   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/HDFC.png)

   ### BACKTESTING RESULTS

4. RELIANCE<br/>

   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/relianceB.png)

5. WIPRO<br/>

   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/wiproB.png)

6. HDFC<br/>
   - ![alt text](https://github.com/yatinsatija/Reinforcement_Learning_based_financial_Trading_Bot/blob/main/ResultsImages/HDFCb.png)
