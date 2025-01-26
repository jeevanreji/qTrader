# **Q-Learning Agent for Automated Trading in Equity Stock Markets**

This project implements an automated trading agent using **Q-learning** and **Double Q-learning** algorithms. The agent dynamically adapts to stock market patterns to maximize trading profits. Two models for state representation are used:
1. **K-means clustering** of historical data to represent states.
2. **Candlestick patterns** to classify stock movements into predefined states.

---

## **Project Highlights**
- Implements reinforcement learning using **Q-learning** and **Double Q-learning** algorithms.
- Optimizes trading strategies by exploring different states, actions, and rewards.
- Supports advanced trading metrics like **Relative Strength Index (RSI)** and **Williams Percent Range**.
- Benchmarked against the **Buy and Hold** policy, showcasing the agent's efficacy in generating profits.

---

## **How the Agent Works**

### **Actions**:
1. **Continue Position**: Maintain the last position unless it leads to a loss exceeding 10%.
2. **Close Short & Continue Long**: Closes a short position if it becomes suboptimal and maintains a long position otherwise.
3. **Close Long & Continue Short**: Closes a long position if it becomes suboptimal and maintains a short position otherwise.

### **State Representation**:
1. **Model 1 - Clusters**:
   - Historical trading sessions are grouped into clusters using **K-means**.
   - States are identified as similar market conditions.

2. **Model 2 - Candlestick Patterns**:
   - Categorizes market movements into six states:
     - UP, HUP, VHUP (upward trends).
     - DOWN, HDOWN, VHDOWN (downward trends).

### **Rewards**:
- Rewards are calculated based on profit/loss during position changes.
- The reward computation incorporates:
  - Profit percentage.
  - Portfolio value at the given timestep.

---

## **Setup Instructions**

### **Prerequisites**:
1. **Programming Languages**:
   - Python 3.x
   - Jupyter Notebook (for running and visualizing models)
2. **Libraries**:
   Install required Python libraries using:
   ```bash
   pip install numpy pandas sklearn matplotlib
