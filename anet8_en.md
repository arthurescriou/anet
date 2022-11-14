# Anet TME 8

The goal of this lesson is to implement swarm algorithms in the SVB simulation (http://app.svb-41.com).

## Swarm rush

Implement the first swarm algorithms of the lecture.

With all the same ships :

- thrust to a speed of 10%

- when a enemy ship is detected in radar range turn to aim it and communicate its position in the radio

- when another ship send an enemy position turn to aim it

### Some documentation about communication

A ship that send every enemy in its radar to other ships of its team.

```ts
export const ai: svb.AI<Data> = ({ stats, radar, ship, comm }) => {
  // Read the enemies.
  const enemies = svb.radar.closeEnemies(radar, stats.team, stats.position)

  // For each enemy, signal its position, and move back from the enemy to keep
  //   them to the maximum range possible.
  if (enemies.length > 0)
    enemies.forEach(e => comm.sendMessage(e.enemy.position.pos))
}
```

A ship that wait to receive message through radio.
Target look like a radar signal.

```ts
export const ai: svb.AI<Data> = ({ ship, comm }) => {
  // Read the last messages.
  const messages = comm.messagesSince(0)
  if (messages) {
    const target = messages[0].content.message
  }
}
```

Your ship must do both.
