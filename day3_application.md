# Whiteboard Design Session 3: Application

## Device Lifecycle Management
Discuss and document how Contoso DrillDown should handle the following flows related to the metering appliance lifecycle at a customer site:
- Create a device identity
- Install device
- Activate device
- Update software running on a device
- Manage device metadata

## Device to Cloud Communication
Considering the amount of data the appliances are generating, what ingestion channel would you recommend? At what initial scale?

## Cloud to Device Communication
What types of cloud to device communications do you see as part of your solution? 
Are there any platform limitations you need to be aware of?

## Message processing
Which requirements are relevant for the selection of processing platform? What would be your preferred candidate(s)?
How do you address the scalability and reliability requirements? How would you handle the availability vs consistency dilemma ([CAP Theorem](https://en.wikipedia.org/wiki/CAP_theorem))?
At which point in the data lifecycle management would you address the time-series logic? 
What is your approach to composing period aggregates and updating period-over-period comparisons?

## "Cold" Path Processing
Do you expect the "cold" data to require any additional processing? What is your platform of choice to implement it?

## On-site Appliances
How do you plan to utilize the on-site appliance capacities? 
How would you address the remote application maintenance and configuration management issue?
Which additional opportunities do you see in running parts of the data processing pipeline directly on the appliance?

## Summary and Presentation
Refer to the questions from the quality dimensions you selected on day 1: do you see them adequately addressed in your vision?
Consolidate your ideas and conclusions, diagram your solution, and prepare a 10' presentation in a chalk-talk format.


