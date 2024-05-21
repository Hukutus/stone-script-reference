# Stone Story RPG Stonescript Reference

[Official Stonescript manual](https://stonestoryrpg.com/stonescript/manual.html)

## TODO
- [ ] Add proper desciption about the game and about Stonescript
- [ ] Use proper terminology for descriptions
- [ ] Add all bosses
- [ ] Add all foes
- [ ] Add all weapons
- [ ] Add example code

## Example: Logging state in game
```
>`0,0,Foe state: @foe.state@, time: @foe.time@
```

## Weapons

| State | Description |
|-|-|
| 0 | UI only |
| 1 | Idle, waiting to be in range |
| 2 | Attack, pre-damage |
| 3 | Attack, post damage |
| 4 | Cooldown |

## Foes

| State | Description |
|-|-|
| -1 | No foe |
| 0 | Sleeping |
| 1 | Waking up |
| 2 | Engaged |
| 32 | Attacking, pre-damage |
| 33 | Attacking, post-damage |
| 4 | Dead |
| 100+ | Unique states |

### Bosses

#### Bronze Guardian

| State | Time | Description |
|-|-|-|
| 1 | 333 | Walking |
| 2 | 299 | Standing still (1st time) |
| 2 | 352 | Standing still |
| 32 | 35 | Attacking |
| 33 | 239 | Hammer down |


#### Dysangelos

##### Phase 1

| State | Time | Description |
|-|-|-|
| 100 | 171 | Transformation |
| 101 | 44 | Transformation |
| 102 | 19 | Transformation |
| 126 | 43 | Transformation |
| 127 | 279 | Transformation |
| 116 | 14 | Transformation |
| 117 | 59 | Transformation |
| 118 | 29 | Transformation (battle starts) |
| 2 | 29 | Idle (1st time) |
| 2 | 59 | Idle |
| 32 | 29 | Attack, pre-damage|
| 33 | 24 | Attack, post-damage |
| 32 | 30 | Laser eye, pre-damage |
| 33 | 65 | Laser eye, post-damage |

##### Phase 2

| State | Time | Description |
|-|-|-|
| 124 | 69 | Transformation |
| 125 | 15 | Transformation (battle starts) |
| 2 | 15 | Idle (1st time) |
| 2 | 9 | Element change |
| 32 | 59 | Attack, pre-damage |
| 33 | 24 | Attack, post-damage |

##### Phase 3

| State | Time | Description |
|-|-|-|
| 107 | 149 | Transformation |
| 108 | 15 | Transformation (battle starts) |
| 2 | 15 | Idle (1st time) |
| 2 | 59 | Idle |
| 32 | 49 | Attack 1, pre-damage |
| 33 | 23 | Attack 1, post-damage |
| 32 | 29 | Attack 2 (stun & shield), pre-damage |
| 33 | 65 | Attack 2, post-damage |
| 106 | 8 | Cast adaptive defense buff |
| 107 | 299 | Transformation |
| 108 | 13 | Transformation |
| 0 | 326 | Post-transformation idle |
| 2 | 326 | Post-transformation idle |
| 109 | 59 | Orb 1 |
| 110 | 14 | Orb 2 |
| 111 | 89 | Orb 3 |
| 112 | 123 | Orb 4 |
| 113 | 44 | Orb 5 |
| 114 | 14 | Orb 6, pre-damage |
| 115 | 89 | Orb 7, post-damage |
| 0 | 447 | Post-orb idle |
| 2 | 447 | Post-orb idle |

