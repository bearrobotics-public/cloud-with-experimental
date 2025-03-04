# Experimental Cloud API Service
The definition of Experimental Bear Cloud API service.

### Lift
#### CloudAPIService [:material-tag-outline:](../../../changelog.md#february-5-2025 "Available on Beta")
- **Request Type:** [ControlCompartmentRequest](#controlcompartmentrequest)
- **Response Type:** [ControlCompartmentResponse](#controlcompartmentresponse)
- **Description:**
  Control selected compartment with specified action to be performed. 

#### SubscribeCompartmentStatus [:material-tag-outline:](../../../changelog.md#february-5-2025 "Available on Beta")
- **Request Type:** [SubscribeCompartmentStatusRequest](#subscribecompartmentstatusrequest)
- **Response Type:** [SubscribeCompartmentStatusResponse](#subscribecompartmentstatusresponse)
- **Description:**
  Subscribe to robot's mission status.<br>Upon subscription, the server immediately sends the latest known
mission status, followed by updates whenever the mission status changes.

---

##### ControlCompartmentRequest
| Field          | Type   | Description |
|----------------|--------|-------------|
| `robot_id`     | string |             |
| `compartment_control` | [CompartmentStates](../../robot/experimental/Lift.md/#compartmentstates) |             |


##### ControlCompartmentResponse
- *(No fields defined)*


##### SubscribeCompartmentStatusRequest
| Field      | Type   | Description |
|------------|--------|-------------|
| `robot_id` | string |             |

##### SubscribeCompartmentStatusResponse
| Field           | Type                                | Description |
|-----------------|-------------------------------------|-------------|
| `metadata`      | [EventMetadata](../../common/Annotations.md/#eventmetadata) |             |
| `compartment_states` | [CompartmentStates](../../robot/experimental/Lift.md/#compartmentstates) |             |
