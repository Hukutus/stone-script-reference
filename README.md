# Stone Story RPG Stonescript Reference
TODO: Add description of the game and the language

[Official Stonescript manual](https://stonestoryrpg.com/stonescript/manual.html)

## Logging values yourself
```
>`x,y,msg
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
| 32 | Preparing attack |
| 33 | Attack complete |


### Bosses

#### Bronze Guardian

| State | Time | Description |
|-|-|-|
| 1 | 333 | Walking |
| 2 | 299 | Idle |
| 32 | 35 | Preparing attack |
| 33 | 78 | Hammer down |

