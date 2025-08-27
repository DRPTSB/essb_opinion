

## Simulation of Sliced Sphere Lattices

This code simulates slicing through a 3D structure of spheres, like cells in a tissue sample, to see which ones get captured. It helps us understand how the size of an object and the thickness of the slice affect what we can see.

-----

## The Simulations

There are two main simulations in this project.

### 1\. How Slice Thickness Matters

This simulation uses a single sphere size and checks how many are captured as the slice (or "slab") gets thicker.

  * **Metric:** It calculates the ratio of spheres that are **fully inside** the slice versus those that are just **partially clipped** by it.
  * **Method:** To get a smooth average, the whole structure is randomly shifted up and down many times.

### 2\. Comparing Different Sphere Sizes

This simulation uses a single slice thickness to compare how easily different-sized spheres (e.g., small, medium, large) are detected.

  * **Metrics:** It measures the **detection probability** and the **total captured volume** for each sphere size.
  * **Method:** To make the comparison fair, it places an **equal number** of each sphere type in a central "safe zone." This ensures no spheres are lost off the edges during the simulation, making the count for each class constant and reliable.

-----

## How to Run

1.  **Install libraries:** Make sure you have `numpy` and `matplotlib`.
2.  **Run the script:** Open a terminal and run the command:
    ```bash
    python your_script_name.py
    ```
3.  **Customize:** You can easily change parameters like sphere sizes, slice thickness, or the number of runs (`K`) in the `if __name__ == "__main__":` section at the bottom of the script.
