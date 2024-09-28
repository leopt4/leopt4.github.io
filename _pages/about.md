---
permalink: /
title: "Curriculum Vitae"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

## 📝 About me
Erasmus Scholar pursuing a Master of Medical Imaging and Applications with a strong background in AI engineering and computer vision. Experienced in developing and deploying AI models for various applications, including smart traffic systems, distracted driver detection, and medical imaging. Passionate about integrating AI solutions into real-world problems and continuously improving model performance.

## 💼 EXPERIENCE

### Technical Lead | Robotics - Autopilot
**Viettel High Technology Industries Corporation**  
**Duration:** January 2021 – July 2023
- Led an autopilot team of 5 members.
- Responsible for technical decisions, team communication.
- Designed software system of the autopilot.
  
### Robotics Engineer
**Viettel Aerospace Institute**  
**Duration:** March 2020 – January 2021  
- Designed and developed a navigation system for UAV.
- Calibrated and tested autonomous sensors.
  
### Junior Researcher
**Hanoi University of Science and Technology**  
**Duration:** June 2016 – Aug 2020
- Researched new algorithms and control theory in autonomous vehicles.
- Published 5 papers on journals and conferences.


## 🚀 ACHIEVEMENT
### CONTROL
- [**Adaptive/Approximate Dynamic Programming**](https://www.sciencedirect.com/science/article/abs/pii/S0019057822001495)  
  Developed an optimal path following controller based on Reinforcement Learning without requiring prior knowledge of the dynamic systems.

- [**Controller and Seeker for Suicide Drone**](https://github.com/huytrnq/Semi-Automated-Data-Labeling-Tool)  
  Designed controllers in attack phase based on image processing data. They allow drones to attack the target with an error of less than 3 meters.

- [**Pick and Place Task on Turtlebot Kobuki 4-DoF Mobile Manipulator**](https://github.com/leopt4/turtlebot_taskpriority_manipulation)
  Applied Task-Priority Kinematic Controller for mobile base and manipulator, Image Processing to detect objects, Behavior-tree for task planning.

### NAVIGATION
- [**Robust Graph SLAM for Autonomous Navigation**](https://github.com/leopt4/slam_turtlebot)  
  Implemented an online SLAM and full SLAM using GTSAM library and ROS on the turtlebot platform with onboard sensors - 2D LIDAR, Wheel Encoders, and Magnetometer compass.
  The system's positioning error is less than 3cm in lab environment and is capable of close-loop detection.
- [**GNSS-Denied Navigation System for Unmanned Aerial Vehicles**](https://github.com/leopt4/slam_turtlebot)  
  Applied Extended Kalman Filter and SLAM to navigation system which allow UAV to operate in GNSS-denied environment.
  Optimized modelling and calibration methods for low-cost sensors: IMU, Barometer, GNSS receiver helping to reduce the cost of products

### PERCEPTION AND PLANNING
- [**Autonomous Exploration and Path Planning in 3D Environments**](https://github.com/leopt4/turtlebot_exploration_planning)  
  Used TARE planner for global planner and Falco for local planner to solve the exploration task. The system was deployed in turtlebot with depth camera.

- [**Visual Inertial Odometry**](https://github.com/leopt4/turtlebot_vio)  
  Integrated Camera and IMU data through Smart Projection Pose Factors for efficient state estimation.
  Implemented on Stonefish simulation using ROS and GTSAM.


## 🎓 EDUCATION
**Erasmus Mundus Joint Master in Intelligent Field Robotic Systems (IFRoS)**  
_University of Girona, University of Zagreb, Eötvös Loránd University_  
**Duration:** September 2023 – Present
**GPA:** 9.05/10.0

**Bachelor of Control Engineering and Automation**  
**Talented Engineer’s Programme**
_Ha Noi University of Science and Technology, Vietnam_  
**GPA:** 3.37/4.0 - Top 5%


## 🔧 SKILLS
- **Programming Languages:** C/C++/C#, Python, Matlab/Simulink
- **Robotic Framework:** ROS, Ardupilot/PX4, GTSAM
- - **AI & Machine Learning:** Pytorch, OpenCV, Matplotlib
- **Tools:** Git, Docker, Jupyter Notebook, Linux
- **Languages:** English (IELTS: 7.0 overall)
  

## 🎖️ HONORS & AWARDS
- **Erasmus Mundus Joint Masters Scholarship in Intelligent Field Robotic Systems (IFRoS) IN 2023**
- **Excellent Engineer Awards in Viettel Corporation in 2021 and 2022**
- **Bronze Medals in the National Physics Olympiad in 2015**
<!-- This is the front page of a website that is powered by the [Academic Pages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages. [GitHub pages](https://pages.github.com) is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the respository. This template was forked from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) created by Michael Rose, and then extended to support the kinds of content that academics have: publications, talks, teaching, a portfolio, blog posts, and a dynamically-generated CV. You can fork [this repository](https://github.com/academicpages/academicpages.github.io) right now, modify the configuration and markdown files, add your own PDFs and other content, and have your own site for free, with no ads! An older version of this template powers my own personal website at [stuartgeiger.com](http://stuartgeiger.com), which uses [this Github repository](https://github.com/staeiou/staeiou.github.io).

A data-driven personal website
======
Like many other Jekyll-based GitHub Pages templates, Academic Pages makes you separate the website's content from its form. The content & metadata of your website are in structured markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the [GitHub pages](https://pages.github.com/) service creates static HTML pages based on these files, which are hosted on GitHub's servers free of charge.

Many of the features of dynamic content management systems (like Wordpress) can be achieved in this fashion, using a fraction of the computational resources and with far less vulnerability to hacking and DDoSing. You can also modify the theme to your heart's content without touching the content of your site. If you get to a point where you've broken something in Jekyll/HTML/CSS beyond repair, your markdown files describing your talks, publications, etc. are safe. You can rollback the changes or even delete the repository and start over -- just be sure to save the markdown files! Finally, you can also write scripts that process the structured data on the site, such as [this one](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb) that analyzes metadata in pages about talks to display [a map of every location you've given a talk](https://academicpages.github.io/talkmap.html).

Getting started
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
2. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
3. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
4. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
5. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
6. Check status by going to the repository settings, in the "GitHub pages" section

Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the Academic Pages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring Academic Pages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful. -->
