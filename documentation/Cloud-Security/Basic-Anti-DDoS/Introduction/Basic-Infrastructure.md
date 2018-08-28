# Infrastructure

    The Basic Anti-DDoS framework consists of three modules: management center equipment, detection equipment and cleaning equipment.
    
## Business Architecture

The basic protection business structure is shown in the following figure:

![Create instance](https://github.com/jdcloudcom/cn/blob/edit/image/Basic%20Anti-DDos/Infrastructure01.png)

Note: 1. The image flow to the detection device 2. The detection device detects an attack, and notifies the management center of the attack information.
      3. After receiving the attack information, the management center shall notify the cleaning equipment to open and clean.
      4. Drain the flow to the cleaning equipment for flow cleaning and re-inject clean flow after cleaning.
      5. Normal flow

| Name | Description |
| - | - |
The management center | is mainly responsible for receiving attack information and sending a cleaning strategy to the cleaning equipment to guide the cleaning equipment to carry out flow cleaning.
| Cleaning equipment | Mainly based on the cleaning strategy issued by the management center, wash the flow of attack, and re-inject the cleaned clean flow.
| Detection Device | Mainly analyzes the traffic components to determine if an attack occurred. If an attack occur, send attack information to that management centre.

## Related Reference

- [What is Basic Anti-DDoS](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Overview.md)
- [Core Concepts](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Core-Concepts.md)
- [Application scenario](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Application-Scenarios.md)
- [Basic Function](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Functions.md)
- [Use limit](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Basic-Anti-DDoS/Introduction/Restrictions.md)
