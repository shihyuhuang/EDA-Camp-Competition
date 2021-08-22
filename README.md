# EDA-Camp-Competition
## Problem Formulation

Given a set of n rectangles on 2D-plane and an integer k (1<=k<=n), output exactly k rectilinear polygons such that each rectangle is contained by one polygon. The result is evaluated by the total area of the polygons. The smaller of the total area of output polygons, the better.


## Input file format:
1. First line: k (i.e. the number of output polygons)
2. Second line: n (i.e. the number of input rectangles)
3. From the third line to the end of the input file: Each line corresponds to a rectangle. Each rectangle is
represented by a sequence of eight integers separated by space: x0, y0, x1, y1, x2, y2, x3, y3, where (x0, y0), (x1, y1), (x2, y2), (x3, y3) are the coordinates of the four corners of the rectangles in a clockwise order, and (x0, y0) is the left-bottom corner.
In the testcase(s), the given rectangles will not have “point touch” scenario. That is, the input rectangles will be disjoint (separated) or at least line touch or with overlap area (larger than 0).


## Output file format:
Each line corresponds to a polygon. Each polygon of m corners is represented by a sequence of 2m integers
separated by space: x0, y0, x1, y1, ..., x_m-1, y_m-1, where (x0, y0), (x1, y1), ..., (x_m-1, y_m-1) are the coordinates of the n corners of the polygon in a clockwise order.
For every polygon in the output file, evaluator will identify point touch or line crossing as an illegal polygon. Then, contestant will get no score for this kind of output. Contestant needs to output separate polygons if the answer is with point touch scenario.
Each outputted rectilinear polygon can be either convex or concave, without a hole. If any point touch scenario, it will be treated as disjoint. In the picture below, the red polygon is a legal polygon; while the green shapes should be outputted as 3 polygons (rectangles) or an illegal polygon (crossing point list). A 凹 shape polygon is legal.

<img width="230" alt="截圖 2021-08-21 17 28 04" src="https://user-images.githubusercontent.com/61773397/130317474-4a6427a4-36f9-4b0e-a59a-1f47b2d4e02a.png">

In the optimal solution, one rectangle should belong to only one polygon so that the final total area of output polygons will be minimal. However, the evaluator won’t check whether the output polygons are overlapping or not; it will simply compute the total area of output polygons. The smaller, the better. That is,the resulted polygons are possible /allowable to overlap; but it may not get the highest score.


## (Optional) The extended challenging problems are:
1. to find the largest number (K) of disjoint rectilinear polygons of given n rectangles; and output the ‘K’ non-overlapping rectilinear polygons.
What is the complexity of your algorithm? Please analyze the algorithm.
2. Develop a program which can output any k non-overlapping rectilinear polygons for k = 1, 2, ..., K; where K <= n.
