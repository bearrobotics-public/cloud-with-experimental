### Lift Messages

#### CompartmentStates
`CompartmentStates` has the states of all compartments.

| Field                | Type        | Description |
|----------------------|------------|-------------|
| `compartment_states`  | [CompartmentState](#compartmentstate)<br>*repeated* | List of compartment states.        |


---

#### CompartmentControl
`CompartmentControl` is used to control the state of compartments, including LED and door states.

| Field          | Type        | Description |
|---------------|------------|-------------|
| `compartments`  |  `int32`<br>*repeated* | List of compartment states.        |
| `led`         | [Led](#compartmentcontrolledenum)  | LED control command. |
| `door`        | [Door](#compartmentcontroldoorenum) | Door control command. |

##### CompartmentControlLedEnum
| Name          | Number | Description |
|--------------|--------|-------------|
| LED_UNKNOWN | 0      | Change nothing. |
| LED_OFF    | 1      | Turn off the LED. |
| LED_ON     | 2      | Turn on the LED. |

##### CompartmentControlDoorEnum
| Name          | Number | Description |
|--------------|--------|-------------|
| DOOR_UNKNOWN | 0      | Change nothing. |
| DOOR_CLOSE   | 1      | Close the door. |
| DOOR_OPEN    | 2      | Open the door. |

---

#### CompartmentState
`CompartmentState` represents the state of a single compartment, including its LED and door status.

| Field            | Type      | Description |
|-----------------|-----------|-------------|
| `compartment_id` | `int32`   | ID of the compartment. |
| `led`           | [Led](#compartmentstateledenum)  | Current LED state. |
| `door`          | [Door](#compartmentstatedoorenum) | Current door state. |

##### CompartmentStateLedEnum
| Name          | Number | Description |
|--------------|--------|-------------|
| LED_UNKNOWN | 0      | Unknown LED state. |
| LED_OFF    | 1      | LED is off. |
| LED_ON     | 2      | LED is on. |

##### CompartmentStateDoorEnum
| Name            | Number | Description |
|----------------|--------|-------------|
| DOOR_UNKNOWN | 0      | Unknown door state. |
| DOOR_CLOSING | 1      | Door is currently moving to close. |
| DOOR_CLOSED  | 2      | Door is fully closed. |
| DOOR_OPENING | 3      | Door is currently moving to open. |
| DOOR_OPENED  | 4      | Door is fully opened. |
| DOOR_ERROR   | 5      | Door encountered an error (e.g., obstacle stuck or hardware issue). |

