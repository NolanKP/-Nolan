# -Nolan
# Wearable AR Golf Coach

This project aims to revolutionize golf putting by leveraging augmented reality (AR), real-time trajectory calculations, and depth-sensing technology. Our wearable AR device provides golfers with a visual guide to optimize their putting stroke, maximizing accuracy and consistency on real greens.
Our ultimate goal is to enable golfers to achieve a 95% success rate on putts within 15 yards, even on challenging greens with complex slopes and terrain. By combining advanced physics-based trajectory modeling, real-time depth sensing, and intuitive AR visualization, the system empowers players to make precise, confident strokes under varying conditions.

Using a combination of depth cameras, AR glasses, and advanced algorithms, the system dynamically visualizes a **small dot** above the putter head. This dot acts as a guide to:
- Indicate the optimal stroke amplitude for a successful putt.

## Key Features
- **Trajectory Visualization**: Predict the ball's trajectory based on green topography.
- **Dynamic Guidance**: Display a small AR dot above the putter head to guide the player's stroke.
- **Real-Time Feedback**: Adjust the dot's movement and position dynamically to reflect terrain and speed requirements.
- **Precision Optimization**: Ensure the ball follows the calculated trajectory with minimal deviation.

## How It Works
1. **Depth Sensing**: The ZED2i stereo camera captures the green's topography and sends real-time data to the Jetson Orin Nano for processing.
2. **Trajectory Calculation**: The system computes the optimal putting line, taking into account factors like slope, terrain friction, and distance to the hole.
3. **AR Visualization**: Using Xreal AR glasses, the system displays:
   - A visual trajectory line for the ball.
   - A dynamic dot above the putter head, guiding the stroke's amplitude and direction.
   - The player follows the dot's movement to execute the ideal stroke.
   
## Current Progress
### Hardware
- Jetson Orin Nano: Handles trajectory calculations and real-time processing.
- ZED2i Stereo Camera: Captures 3D depth data of the green.
- Xreal AR Glasses: Projects AR visuals for trajectory and guidance.

### Software
- Depth sensing: Successfully capturing topography data.
- Trajectory algorithm: In progress, focusing on physics-based modeling.
- AR rendering: Initial visualizations functional, working on real-time stability.

## Goals
- Finalize trajectory prediction algorithms to handle varied terrains.
- Enhance AR rendering for a smoother and more intuitive user experience.
- Validate the system's accuracy through on-green testing.

## Roadmap
### Phase 1: MVP (Minimum Viable Product)
- Display the calculated trajectory line connecting the ball and the hole on a monitor (not yet integrated into an AR device).
- The trajectory line will typically appear as a curve overlaid on the green due to its uneven (hilly) terrain. The calculation of the trajectory is based on:
  1. The friction coefficient of the green.
  2. 3D point-cloud data retrieved by the depth camera.
  3. The ultimate velocity of the ball (0.05m/s), which is the velocity required as the ball approaches the hole to ensure a successful putt without overrolling or stopping prematurely.


### Phase 2:Visualization
- Integrate AR visualization of the trajectory line and guidance dot into Xreal AR glasses.
- Ensure the dot dynamically guides the putter stroke along the calculated trajectory.

### Phase 3: Field Testing
- Test the system on actual golf greens.
- Collect user feedback and refine the device.

## How to Contribute
We are looking for collaborators with expertise in:
- **Algorithm Development**: Real-time trajectory prediction based on 3D depth data.
- **AR Development**: Optimizing rendering pipelines for Xreal AR glasses.

If you're interested in contributing, please reach out!

## Contact
Feel free to contact us for collaboration or questions:
- **Email**: [peixuan0@outlook.com]
- **GitHub Issues**: Open an issue in this repository for discussions or suggestions.

## License
This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.
