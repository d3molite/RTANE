# Module 01: Wires

This Module consists of four buttons with four symbols.

## Rules
 In the bomb defusal manual will be a sheet with many symbols in multiple columns. Only one column will contain all four shown symbols. The buttons must be pressed in the order, the symbols appeare in.

### Possible patterns

```
+-----+-----+
|  1  |  2  |
+-----+-----+
|  3  |  4  |
+-----+-----+
```
|Pattern No | Pattern | DIP |
|-|-|-|
| 01 |``1	2	3	4``|``0	0	0	0	1``|
| 02 |``4	1	2	3``|``0	0	0	1	0``|
| 03 |``3	4	1	2``|``0	0	0	1	1``|
| 04 |``2	3	4	1``|``0	0	1	0	0``|
| 05 |``4	3	2	1``|``0	0	1	0	1``|
| 06 |``1	4	3	2``|``0	0	1	1	0``|
| 07 |``2	1	4	3``|``0	0	1	1	1``|
| 08 |``3	2	1	4``|``0	1	0	0	0``|	
| 09 |``2	1	3	4``|``0	1	0	0	1``|
| 10 |``4	2	1	3``|``0	1	0	1	0``|
| 11 |``3	4	2	1``|``0	1	0	1	1``|
| 12 |``1	3	4	2``|``0	1	1	0	0``|	
| 13 |``1	2	4	3``|``0	1	1	0	1``|
| 14 |``3	1	2	4``|``0	1	1	1	0``|
| 15 |``4	3	1	2``|``0	1	1	1	1``|
| 16 |``2	4	3	1``|``1	0	0	0	0``|
| 17 |``1	3	2	4``|``1	0	0	0	1``|
| 18 |``4	1	3	2``|``1	0	0	1	0``|
| 19 |``2	4	1	3``|``1	0	0	1	1``|
| 20 |``3	2	4	1``|``1	0	1	0	0``|
| 21 |``1	4	2	3``|``1	0	1	0	1``|
| 22 |``3	1	4	2``|``1	0	1	1	0``|
| 23 |``2	3	1	4``|``1	0	1	1	1``|
| 24 |``4	2	3	1``|``1	1	0	0	0``|


## construction
It would be nice to use buttons with displays (something like the ones used in the stream deck) to be fast in reconfiguring. But there hasn't been any research done yet. 

## Interconnect to bomb core
As this module doesn't need to be aware of anything (if not used as a needy module), it doesn't need to be connected to the data-bus.