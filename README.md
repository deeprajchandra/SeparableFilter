# SeparableFilter: code will be made available soon. I'm still working on it.
This code extends the kernel size for cuda::separableFilter beyond 16.

In cuda::SeparableFilter the maximum size of the kernel is 16. But there are times when we require to use kernel size beyond 16. 
I've pulled this code from cuda libraries and modified it so that the kernel size can go beyond 16. The max kernel size that can be reached is 32.

Currently, the size of the kernel (#line $$) is 45. But it can be changed to anything less 64.

How it's done?

SeparableFiter (cuda) works in two phases: first with RowFilter then with ColumnFilter. I pulled the code from library files and modified them.

Usage:
In order to achieve Non-Separable Filter:
1. First, use the RowFilter. Then,
2. use the ColumnFilter.

RowFilter()


ColumnFilter()
