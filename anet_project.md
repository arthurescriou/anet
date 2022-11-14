# Anet Project

The goal of the project is to describe and implement a swarm algorithm using grafcet and state machine.

The algorithm must be built to the SVB simulation.

We want here to build a swarm with different kind of ships which have different role in the swarm.

It can be done with iterations, the code can work with only some of the implementations.

For every of the following agents you have to submit a grafcet describing the code and the code of the ships. You have also to join a documentation on how to use it in the submitted report.

## Agents

Every agents described here must be autonomous but must also work together.

### Attacker

- thrust to a speed of 10%

- when a enemy ship is detected in radar range turn to aim it and communicate its position in the radio

- when another ship send an enemy position turn to aim it

### Scout

- thrust to a speed of 10%

- when a enemy ship is detected in radar range thrust back to stop and communicate its position in the radio

### Reserve

- do not move at start

- when a enemy ship is detected in radar range turn to aim it

- when another ship send an enemy position go to that position

### Defender

- go to a determined position

- when a enemy ship is detected in radar range turn to aim it and communicate its position in the radio

If you have an idea about a different agent you can also add it to the list and to the report.

## Work expected

You must submit a 6-10 pages report and the code you describe in it. Your grafcet can be included in the report but you must explain your choices of implementations and the conditions and actions you use in the grafcet.
