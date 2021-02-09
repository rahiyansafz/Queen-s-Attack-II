
Queen's Attack II
You will be given a square chess board with one queen and a number of obstacles placed on it. Determine how many squares the queen can attack.

A queen is standing on an n x n chessboard. The chess board’s rows are numbered from 1 to n, going from bottom to top. Its columns are numbered from 1 to n, going from left to right. Each square is referenced by a tuple, (r, c), describing the row, r, and column, c, where the square is located.

The queen is standing at position (rq, cq). In a single move, she can attack any square in any of the eight directions (left, right, up, down, and the four diagonals). In the diagram below, the green circles denote all the cells the queen can attack from (4, 4):


![qa1](https://user-images.githubusercontent.com/70625091/107354836-db620580-6af8-11eb-9a91-c626a5f695a5.png) 


There are obstacles on the chessboard, each preventing the queen from attacking any square beyond it on that path. For example, an obstacle at location (3, 5) in the diagram above prevents the queen from attacking cells (3, 5), (2, 6), and (1, 7):


![qa2](https://user-images.githubusercontent.com/70625091/107354887-eddc3f00-6af8-11eb-9245-e77468e6040b.png)


Given the queen’s position and the locations of all the obstacles, find and print the number of squares the queen can attack from her position at . In the board above, there are such squares.

Function Description
Complete the queensAttack function in the editor below. It should return an integer that describes the number of squares the queen can attack.

queensAttack has the following parameters:

n: an integer, the number of rows and columns in the board
k: an integer, the number of obstacles on the board
r_q: integer, the row number of the queen’s position
c_q: integer, the column number of the queen’s position
obstacles: a two dimensional array of integers where each element is an array of 2 integers, the row and column of an obstacle
Input Format
The first line contains two space-separated integers n and k, the length of the board’s sides and the number of obstacles.

The next line contains two space-separated integers rq and cq, the queen’s row and column position.

Each of the next k lines contains two space-separated integers r[i] and c[i], the row and column position of obstacle[i].

Constraints
1 <= n <= 105
1 <= k <= 105
A single cell may contain more than one obstacle.
There will never be an obstacle at the position where the queen is located.
Subtasks
For 30% of the maximum score:

0 < n <= 100
0 <= k <= 100
For 55% of the maximum score:

0 < n <= 1000
0 <= k <= 105
Output Format
Print the number of squares that the queen can attack from position (rq, cq)

Sample Input 0
1
2
4 0
4 4
Sample Output 0
1
9
Explanation 0
The queen is standing at position (4, 4) on a 4 x 4 chessboard with no obstacles:


![qa3](https://user-images.githubusercontent.com/70625091/107354976-0ea49480-6af9-11eb-9320-79c32d88bc00.png)


Sample Input 1
1
2
3
4
5
5 3
4 3
5 5
4 2
2 3
Sample Output 1
1
10
Explanation 1
The queen is standing at position (4, 3) on a 5 x 5 chessboard with k = 3 obstacles:


![qa4](https://user-images.githubusercontent.com/70625091/107355020-1ebc7400-6af9-11eb-993d-afeed3843320.png)


The number of squares she can attack from that position is 10.

Sample Input 2
1
2
1 0
1 1
Sample Output 2
1
0
Explanation 2
Since there is only one square, and the queen is on it, the queen can move 0 squares.
