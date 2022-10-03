---
AUTOGENERATED: DO NOT EDIT FILE DIRECTLY
title: Empty
---


# Empty

### Description

This environment is an empty room, and the goal of the agent is to reach the
green goal square, which provides a sparse reward. A small penalty is
subtracted for the number of steps to reach the goal. This environment is
useful, with small rooms, to validate that your RL algorithm works
correctly, and with large rooms to experiment with sparse rewards and
exploration. The random variants of the environment have the agent starting
at a random position for each episode, while the regular variants have the
agent always starting in the corner opposite to the goal.

### Mission Space

"get to the green goal square"

### Action Space

| Num | Name         | Action       |
|-----|--------------|--------------|
| 0   | left         | Turn left    |
| 1   | right        | Turn right   |
| 2   | forward      | Move forward |
| 3   | pickup       | Unused       |
| 4   | drop         | Unused       |
| 5   | toggle       | Unused       |
| 6   | done         | Unused       |

### Observation Encoding

- Each tile is encoded as a 3 dimensional tuple:
    `(OBJECT_IDX, COLOR_IDX, STATE)`
- `OBJECT_TO_IDX` and `COLOR_TO_IDX` mapping can be found in
    [minigrid/minigrid.py](minigrid/minigrid.py)
- `STATE` refers to the door state with 0=open, 1=closed and 2=locked

### Rewards

A reward of '1' is given for success, and '0' for failure.

### Termination

The episode ends if any one of the following conditions is met:

1. The agent reaches the goal.
2. Timeout (see `max_steps`).

### Registered Configurations

- `MiniGrid-Empty-5x5-v0`
- `MiniGrid-Empty-Random-5x5-v0`
- `MiniGrid-Empty-6x6-v0`
- `MiniGrid-Empty-Random-6x6-v0`
- `MiniGrid-Empty-8x8-v0`
- `MiniGrid-Empty-16x16-v0`