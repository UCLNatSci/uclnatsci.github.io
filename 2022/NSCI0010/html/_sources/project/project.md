# IRS 1 Computing Project
For the rest of this course you will put together the concepts and skills you have learnt so far in order to conduct a simple (but genuine) scientific experiment.

**Read this entire document before starting**.

## Measuring Gravity

It is well known that the value of acceleration due to gravity at the Earth's surface ($g$) is approximately $8.91~\mathrm{m}/\mathrm{s}^2$. But how accurately can you measure the value of this physical constant using just a handheld video camera and your nascent programming skills?

The goal of this project is to produce a Python notebook which compares the experimentally recorded motion of a falling object and the expected motion according to physical laws.

### Step 1: Conduct the Experiment

Using a handheld video camera (e.g. the one in your smartphone), record the motion of an object falling vertically from rest. You can use any object you like, but I advise against anything breakable or expensive. You might need to experiment a little to determine a setup which reliably gives a clean and accurate recording, but don't spend a lot of time tinkering; you can refine the experiment later! The output of this step should be a movie file (e.g. `.mov` or `.avi`).

### Step 2: Extract the Data

Extract the data from the recording in the form of a sequence of x and y co-ordinates for each frame.
First you will need to upload the movie file. Then you can use the image manipulation library studied in the last workshop to determine the co-ordinates, but you will need to do this frame-by-frame. The code to extract the frame-by-frame image data from the video file is somewhat painful so I have provided it at the end of this document. The end result should be two arrays `x` and `y` containing the position of the object in each frame.

### Step 3: Analyse the data

The vertical acceleration of an object is defined as

$$a(t) = \frac{d^2y}{dt^2}$$

where $a(t)$ is the (instantaneous) acceleration of the object at time $t$ and $y$ is the object's vertical position. Generate an array `a` containing the vertical acceleration of the object. How close is `a` to the expected value of $g$?

### Step 4: Run the Simulation

An object falling from rest follows the following physical law:

$$ \frac{dx}{dt} = g $$

where $g$ is the acceleration due to gravity.
