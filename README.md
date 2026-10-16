# Container With Most Water - Phase: Two Pointer Optimization

This repository contains solutions and explanations for the "Container With Most Water" problem (LeetCode 11).

What I added
- `solutions/container_with_most_water.py` — Python implementations:
  - `max_area_bruteforce` (O(n^2))
  - `max_area_two_pointer` (O(n)) with step recording for visualization
  - `visualize_steps` — prints step-by-step pointer movement and decisions
  - a small CLI demo in `__main__` that runs both algorithms and shows the visualization

Why this matters
- Brute-force checks all pairs; two-pointer uses observations about limiting side to get O(n) time and O(1) extra space.
- This is a classic optimization pattern useful in geometry, resource allocation, and systems design.

Complexity summary
- Brute-force: Time O(n^2), Space O(1)
- Two-pointer: Time O(n), Space O(1)

Key intuition: move the smaller wall
- The area is width * min(height[left], height[right]). If you move the taller wall inward, the width decreases and the limiting height (the smaller of the two) does not increase, so area cannot increase. Moving the smaller wall gives a chance to find a taller limiting wall and thus possibly a larger area.

Run the demo
- From the repository root run: `python3 solutions/container_with_most_water.py`

Submission: This adds the solution implementations and an explanation (README).
