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

## Foes

| State | Description |
|-|-|
| -1 | No foe |
| 0 | Idle, off screen |
| 1 | Idle, on screen |
| 2 | Encountered |
| 32 | Attacking |
| 33 | Attack complete |


### Bosses

#### Bronze Guardian

| State | Time | Description |
|-|-|-|
| 1 | 333 | Walking |
| 2 | 299 | Idle |
| 32 | 35 | Attacking |
| 33 | 78 | Hammer down |

#### Dysangelos

##### Phase 1

| State | Time | Description |
|-|-|-|
| 100 | 171 | Dialogue |
| 101 | 44 | Dialogue |
| 102 | 19 | Dialogue |
| 126 | 43 | Dialogue |
| 127 | 279 | Dialogue |
| 116 | 14 | Dialogue |
| 117 | 59 | Dialogue |
| 118 | 29 | Dialogue |
| 2 | 29 | Idle (1st time) |
| 2 | 59 | Idle |
| 32 | 29 | Normal attack |
| 33 | 24 | Normal attack complete |
| 32 | 30 | Laser eye |
| 33 | 65 | Laser eye complete |

##### Phase 2

| State | Time | Description |
|-|-|-|
| 124 | 69 | Transformation |
| 125 | 15 | Transformation |
| 2 | 15 | Idle (1st time) |
| 2 | 9 | Element change |
| 32 | 59 | Attack |
| 33 | 24 | Attack done |

##### Phase 3

| State | Time | Description |
|-|-|-|
| 107 | 149 | Transformation |
| 108 | 15 | Transformation |
| 2 | 15 | Idle |
| 32 | 49 | Attack |
| 33 | 23 | Attack done |
| 2 | 59 | Idle |
| 106 | 8 | Shield against element |
| 107 | 299 | Transform to hover |
| 108 | 13 | Transform back |
| 0 | 326 | Post transform idle |
| 2 | 326 | Post transform idle |
| 109 | 59 | Laser eye 1 |
| 110 | 14 | Laser eye 2 |
| 111 | 89 | Laser eye 3 |
| 112 | 123 | Laser eye 4 |
| 113 | 44 | Laser eye 5 |
| 114 | 14 | Laser eye 6 (damage)|
| 115 | 89 | Laser eye 7 |
| 0 | 447 | Post laser eye idle |
| 2 | 447 | Post laser eye idle |

