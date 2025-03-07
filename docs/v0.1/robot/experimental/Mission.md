### Message Types

#### MissionParams
`MissionParams` allows any kind of `params` (Currently, there is only `oneoff_params`).

| Field          | Type                      | Description |
|----------------|---------------------------|-------------|
| `oneoff_params` | [OneoffParams](#oneoffparams) | Parameters for a oneoff mission. |

#### OneoffParams
`OneoffParams` defines extra parameters for a oneoff mission, particularly related to elevator usage.

| Field          | Type                          | Description |
|----------------|-------------------------------|-------------|
| `elevator_mode`| [ElevatorMode](#elevatormodeenum) | Specifies the elevator-related mission parameter. |

#### ElevatorModeEnum
| Value                          | Number | Description |
|--------------------------------|--------|-------------|
| ELEVATOR_MODE_UNKNOWN        | 0      | Default unknown state. |
| ELEVATOR_MODE_BOARDING       | 1      | The robot ignores the gap between the elevator and the floor when boarding. |
