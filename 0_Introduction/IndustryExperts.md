

# Challenges for the Industry
- how do we deliver for millions of customers
- how do we deal with larger maps
- how do we deal with different geometry
- how do we say strong things about such complex systems?
  - formally verify the code?
    - difficult to scale, and calculating all potential inputs is hard. still useful for most important components.
  - Simulate it?
    - simulators are not that good and cant simulate very detailed sensors as well. still useful.
  - Drive Drive Drive?
    - record millions of miles and playback interesting failures in simulated testing.
  - All are useful methods and should be used in tandem


# Zoox Approach
Build cars from the ground up instead of putting sensors on cars. Leverage being an agile startup to design cars that can work better around existing infrastructure.

Design Choices
- Bidirectional Cars
- All Wheel Steering