# Rocket Simulation MATLAB

Note, all these notes are for the RockSim software used in 2017, and conditions may have changed since.

For our senior design project, we needed to build a rocket that would be able to take a payload up to certain altitude and fall within competition specifications and guidelines. We were scored based on multiple factors, but the results that this simulation sought were:

    1. Actual rocket max. altitude vs. Competition specified altitude
    2. Actual rocket max. altitude vs. Simulation rocket max. altitude
    3. Actual rocket landing radius zone vs. Competition specified landing radius zone

Like other teams, we went to open source software like RockSim to simulate our rocket flight, and aimed to score as many points in the first and third conditions specified above. However, we noticed a error tolerance of around 2-5 percent, with some launches incorrectly predicting to 10 percent.

If the competition required 10,000 ft., our simulation calculated 9550 ft., while our rocket travelled to 9900 ft., that would account for roughly 4 percent margin of error! Not only would we lose points for that, but we would potentially lose points for adjusting flight parameters for the rocket to increase the expected altitude (9550 ft.), only to increase the actual altitude and be farther off of competition specification, losing more points.

Due to this, and the limited amount of resources/funds we had to complete multiple launches, we decided to contact the creators of RockSim and determine the key components that were missing, so that we could create our own code that would account for these missing factors.

The main issues are as follows:

    1. Lack of atmospheric conditions modelling.
    2. Rocket fin geometry, for more accurate coefficient of drag/lift calculation.
    3. Factors accounting for parasitic drag, such as surface finish.
    4. Greater inaccuracy as flight approaches Mach 1.
    
This code solves those problems by taking information input that a user would log into Excel, filling out the required/known fields and providing a more accurate result when actual launches were compared to RockSim vs our coding running simultaneously.

## Usage

Code relies on Microsoft Excel inputs.

Code is implemented in MATLAB, which pulls inputs from Microsoft Excel.
