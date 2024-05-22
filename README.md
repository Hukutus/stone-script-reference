# Stone Story RPG Stonescript Reference

- **Note:** Durations may differ depending on distance from foe.
- Some durations might be incorrect (Bolesh, Mushrooms) due to usage of Ice weapons during data collection.

[Official Stonescript manual](https://stonestoryrpg.com/stonescript/manual.html)

## TODO
- [ ] Add proper desciption about the game and about Stonescript
- [ ] Use proper terminology for descriptions
- [ ] Add all bosses
- [ ] Add all foes with special states
- [ ] Add example code
- [ ] Make sure all data is collected without inflicting debuffs on foes (Bolesh, Mushrooms)

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
| 32 | Attack, pre-damage |
| 33 | Attack, post-damage |
| 4 | Dead |
| 100+ | Unique states |

### Bosses

#### Deadwood Canyon
- Element: None, weakness: None

##### Xyloalgia

| State | Duration | Description | Next |
|-|-|-|-|
| 0 | 204 | Waking up | 1 |
| 1 | 199 | Engaged | 2 |
| 2 | 199 | Idle (1st time) | 32 |
| 2 | 74 | Idle | 32 |
| 32 | 33 | Attack, pre-damage | 33 |
| 33 | 66 | Attack, post-damage | 2 |
| 4 | 53 | Poena transformation | -1 |

##### Poena

| State | Duration | Description | Next |
|-|-|-|-|
| 1 | 119 | Waking up | 2 |
| 2 | 119 | Engaged | 32 |
| 32 | 33 | Attack, pre-damage | 33 |
| 33 | 66 | Attack, post-damage | 2 |

#### Caves of Fear
- Element: Poison, weakness: Ice

##### Bolesh

| State | Duration | Description | Next |
|-|-|-|-|
| 1 | 269 | Emerging from nest | 2 |
| 2 | 2 | Engaged | 100 |
| 2 | 14 | Engaged | 133, 142|
| 2 | 1 | Engaged (melee) | 133 |
| 100 | 14 | Some animation? | 2 |
| 101 | 14 | Buff (ranged) | 2 |
| 104 | 29 | Debuff (melee) | 2 |
| 133 | 69* | Ranged attack, pre-damage | 2 |
| 2 | 0 | Ranged attack, post-damage | 133 |
| 142 | 37* | Melee attack, post-damage | 143 |
| 143 | 24* | Melee attack, post-damage | 2 |

*\* Data possibly affected by Chill debuff*


#### Mushroom Forest
- Element: Vigor, weakness: Poison
##### Angry Shroom
| State | Duration | Description | Next |
|-|-|-|-|
| 1 | 99 | Waking up | 2 |
| 2 | 0 | Engaged | 32 |
| 32 | 69* | Attack, pre-damage | 33 |
| 33 | 36* | Attack, post-damage | 2 |
| 4 | 8 | Transformation | 2 |

*\* Data possibly affected by Chill debuff*

##### Morel & Enoki
| State | Duration | Description | Next |
|-|-|-|-|
| 2 | 179 | Engaged (1st time) | 32 |
| 32 | 29* | Attack, Morel, pre-damage | 33 |
| 33 | 29* | Attack, Morel, post-damage | 32 |
| 32 | 22* | Attack, Enoki, pre-damage | 33 |
| 33 | 24* | Attack, Enoki, post-damage | 32 |
| 4 | 42 | Death, Morel |  |

*\* Data possibly affected by Chill debuff*

#### Haunted Halls
- Element: Æther, weakness: Vigor
##### Pallas Phase 1
##### Pallas Phase 2

#### Boiling Mine
- Element: Fire, weakness: Æther
##### Bronze Guardian

| State | Time | Description |
|-|-|-|
| 1 | 333 | Waking up (walking) |
| 2 | 299 | Idle (1st time) |
| 2 | 352 | Idle |
| 32 | 35 | Attack, pre-damage|
| 33 | 239 | Attack, post-damage (hammer down) |

#### Icy Ridge
Element: Ice, weakness: Fire
##### Hrimnir

#### Temple
Element: Poison, weakness: Ice
##### Nagaraja

#### Rocky Plateau
Element: Varies
##### Dysangelos Phase 1

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

##### Dysangelos Phase 2

| State | Time | Description |
|-|-|-|
| 124 | 69 | Transformation |
| 125 | 15 | Transformation (battle starts) |
| 2 | 15 | Idle (1st time) |
| 2 | 9 | Element change |
| 32 | 59 | Attack, pre-damage |
| 33 | 24 | Attack, post-damage |

##### Dysangelos Phase 3

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
| 109 | 59 | Super Energy Ball 1 |
| 110 | 14 | Super Energy Ball 2 |
| 111 | 89 | Super Energy Ball 3 |
| 112 | 123 | Super Energy Ball 4 |
| 113 | 44 | Super Energy Ball 5 |
| 114 | 14 | Super Energy Ball 6, pre-damage |
| 115 | 89 | Super Energy Ball 7, post-damage |
| 0 | 447 | Sleeping, post Super Energy Ball |
| 2 | 447 | Idle, post Super Energy Ball |

