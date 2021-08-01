# SlidingBlockPuzzle
This is a program to solve sliding block puzzles. These puzzles consist of a number of rectangular blocks in a tray. The goal is to slide the pieces without lifting any out of the tray until a certain configuration is achieved.

To try out one of these puzzles for yourself, you can try out these online web apps: [Pennant](https://www.bsswebsite.me.uk/Puzzlewebsite/Pennantpuzzle/Pennantpuzzle.htm), [Red Donkey](https://www.bsswebsite.me.uk/Puzzlewebsite/Reddonkeypuzzle/Reddonkeypuzzle.htm)

## Formatting
Blocks are represented by their top-left coordinate and their bottom-right coordinate. For example, the block at the top-left corner of the tray configuration above has its top-left coordinate at 0 0, and has its bottom-right coordinate at 1 0. Thus, this block is represented by the line: \
0 0 1 0 

The 2 × 2 block in the tray configuration above is represented by the line:\
1 1 2 2 

Tray configuration files represent trays and all of the blocks contained in a tray. The first line of every tray configuration file will have two positive integers: the height and the width of the tray (separated by a single space character). All subsequent lines of each tray configuration will have four space-separated non-negative integers that represent a block. Blocks can appear in the tray configuration file in any order. You may assume that the length and width of a tray are no greater than 256 each.

The tray configuration on the previous page can be represented by a file containing the following: \
5 4 \
0 0 1 0 \
0 3 1 3 \
2 0 3 0 \
2 3 3 3 \
1 1 2 2 \
3 1 3 2 \
4 0 4 0 \
4 1 4 1 \
4 2 4 2 \
4 3 4 3 

Goal configuration files are similar to tray configuration files, except they don’t specify the dimensions of the tray. Instead, each line of a goal configuration file specifies the position of a block. In the example above, if our goal was to move the 2 × 2 block two spaces down in the tray configuration above (and we didn’t care where any of the other blocks were), our goal configuration file would contain the single line: \
3 1 4 2

If we also wanted to have other blocks at other positions, we would have more lines in our goal configuration file. Note that if there were multiple 2 × 2 blocks in the initial configuration, any of the 2 × 2 blocks can be at the specified position to satisfy the goal file example above.

Each move is represented by four non-negative space-separated integers. The first two integers make up the current top-left coordinate of the block we want to move. The last two integers make up the top-left coordinate of where we want the block to be after we execute the move. In the example above, if you wanted to move the 2 × 2 block up one space, you would output the move: \
1 1 0 1
