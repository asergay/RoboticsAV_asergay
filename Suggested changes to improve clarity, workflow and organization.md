**Suggested changes to improve clarity, workflow and organization.** 

<u>The Git stuff</u>

1. Workspace organization and git introduction has to be brought in as early as possible. To maintain a consistent workspace configuration and to avoid confusion, all instructions in the handouts and practical ppts should reflect the "recommended catkin workspace configuration". 

```
\sae_ws
    \git_ws
        \bootcamp-assignments        # fetched from their local fork (origin)
        \f110-simulator-public       # cloned from the SAE-bootcamp link
    \ros_ws
        \build
        \devel
        \src
        	\*f110-simulator-public   # Symbolic link to ~/git_ws/f110-simulator-public
            \*bootcamp-assignments    # Symbolic link to ~/git_ws/bootcamp-assignments
            \ros-package1
            \ros-package2
            ...
```

2. Therefore along with Handout1 - Ubuntu and ROS installation, there should be another handout (Handout1.2 - Git Workflow/workspace configuration). This will contain:

   Handout 1.2:

   1. Installing Git
   2. Resources to learn Git properly
   3. Forking the "SAE-bootcamp" repository and setting remotes
   4. Cloning the fork
   5. Pushing updates
   6. Fetching updates from the upstream
   7. Creating branches
   8. README best practices
   9. Recommended workspace configuration
   10. Symlinks

3. The Git Assignment (Practical 1) will now only contain information on what is desired from their first submission:

   1. The forked repository should look as expected
   2. Create an empty ROS package that only has a README 

   

<u>Topics and Assignments:</u>

While a lot of the content is largely there, it might be useful to review the deployment order. Here are a few suggestions to consider:

The lead-time for Assignments 2 & 3 (Practicals 4 and 6, AEB, Wall following) are very long (two weeks), but the lead-time for assignments 5 & 6 (Practicals 9 & 10, Pure-pursuit & Autonomous Lane Detection) is very short (one week).  This can be resolved by:

1. Shifting Assignment 3 to Week 5 (Practical 5)
2. Week 10 (Machine Learning and AI) will now come after Week 7 (Perception). This fits because Week 10 was essentially "Advanced perception". Autonomous Lane Keeping Assignment will be assigned here. 
3. The Assignment "Navigate to a goal with SLAM based obstacle avoidance" will now be assigned along with the handout on SLAM. 
4. The handout on "Pure-pursuit" will be provided on the final Theory week, but not as an assignment. This work will now feature in the final project. 



To avoid confusion, the proposed "updated order" will look like this:

​	**Theory 1:** Course Introduction

​	**Practical 1**: ROS Basics. **Assignment 1:** "ROS Comparison","Working with Git"

​	**Theory 2:** Mechatronics

​	**Practical 2:** ROS Networking, rostopics, launch files, Gazebo

​	**Theory 3:** Sense-Think-Act Reintroduction

​	**Practical 3:** F110 Simulation in Gazebo

​	**Theory 4:** WMR Architecture and Kinematics

​	**Practical 4:** Explore F110 simulator, Laplace, PID. **Assignment 2:** Longitudinal Control (AEB) 

​	**Theory 5:** Perception Sensors and Lidar

​	**Practical 5:** Demo the AEB. **Assignment 3:** Lateral control: Wall following

​	**Theory 6:** Perception

​	**Practical 6:** Demo Wall following (In fact, Assignment 4 can be assigned here, so students can brainstorm solutions as they sit through the theory classes in the next week)

​	**Theory 7:** AI and Machine Learning

​	**Practical 7:** Implement object detection, Practical lane keeping **Assignment 4:** Advanced Lane Detection

​	**Theory 8:** Localization

​	**Practical 8:** Possibly a continuation of Practical 7. I doubt it will fit in one session.

​	**Theory 9:** SLAM

​	**Practical 9:** Demo the Lane Detection. **Assignment 5:** Navigate to a goal with SLAM based obstacle avoidance

​	**Theory 10:** Navigation and Control

​	**Practical 10:** Pure Pursuit. **Final Project is Assigned**

​	**Week 11-12-13:** Final Project implementation. This will be a staged implementation, and students can be expected to demonstrate "non-graded" intermediate results. 

**The stages of the final project**

Step 1: Generate way-points by driving the car around the track using keyboard teleop

Step 2: Create a pure-pursuit algo to follow the waypoints

Step 3: The car should actively avoid unknown obstacles while following the waypoints through follow-the-gap

Step 4: Use TinyYolo to identify the stop sign and stop for 3 seconds