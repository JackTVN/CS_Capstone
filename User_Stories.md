## Member
#### CS Senior: Chi Thanh Tran
#### EECE Senior: Luke Grochocki, Hebron Mekuria, Kian Palmer


# User Stories
### US-01 - Farm Manager
#### Stakeholder Category: Primary

As a farm manager, I want the sensor system to identify information and data related to potential disease, so that I can know which areas of my farm to check and how to deal with it.

### US-02 - Farm Worker
#### Stakeholder Category: Primary

As a farm worker, I want sensor nodes to transmit their data to a central system, so that I can access brief farm data without having to go to every nodes location.

### US-03 - Researcher
#### Stakeholder Category: Secondary

As a researcher, I want the system to record measurements with timestamps, so that the change in environmental conditions before, during, and after the disease period can be used for further research.

### US-04 - Environmentalist
#### Stakeholder Category: Hidden

As an environmentalist, I want the sensor system to not affect the nature and farm negatively through its compartment, so that there will be no pollution or eletrical incident that create harmful aftermath to the environment.

# Use Cases
## UC-01 - Monitor Disease Risk (Expands US-01)
### Use case name: Monitor Crop Disease

### Primary actor: Farm Manager
### Secondary actors: Sensor System, Sensor Nodes

### Preconditions:
Sensor nodes is operational and configured

### Main Success Flow:
1. System constantly retrieves sensor data.
2. System evaluates data toward disease condition criteria.
4. System saves disease status and measurement.
3. Farm Manager looks up latest disease information whenever needed.
5. Farm Manager uses result to determine where to inspect and how to resolve.

### Alternate Flow — Early Notification:

1. System retrieves sensor data.
2. System evaluates data toward disease condition criteria.
3. System notices high chance of disease criteria fulfilled.
4. System notifies Farm Manager by desired method.
5. Farm Manager know where to resolve problem.

### Exception Flow — Invalid Measurement:

1. System detects unreadable data/measurement.
2. System marks said measurement as unavailable.
3. System cleans the unavilable data to fit the disease detection algorithm.
4. System notifies Farm Manager about unreadable data/malfunction.

### Postcondition:
Farm sensor data is always available to be look up and inspect, with disease status alongside to be wary of. Also notify early disease to Farm Manager when in need.

# Acceptance Criteria
### AC-01 — Normal Operation
Given valid sensor data are available,

When the Farm Manager requests disease status,

Then the system shall display a disease status, the correlated measurements, and the timestamp of said measurements.

### AC-02 — Exception

Given a sensor measurement is missing,

When the system detect the missing measurement,

Then the system shall clean the detected data, and notify the Farm Manager of missing/unreadable data.