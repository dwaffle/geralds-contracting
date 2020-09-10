# Gerald's Contracting Application
![Gerald](https://media.gettyimages.com/photos/architect-looking-over-blueprints-picture-id868951616?s=612x612)
### Summary
---
This application takes the length and width of a house in feet and returns the number of studs needed to be purchased.
<br>
<br>

### How to use this Application

To run a calculation, pass in two paramaters
* The width of one house (preceded by the `-w` flag)
* The length of one house (preceded by the `-l` flag)

Example:
```
node dist/index.js -w 8 -l 8
```


<br>
<br>

### Scenario
Gerald owns a construction company and builds single room homes. He can quickly create a rectangular house, usually within one day. He has found, however, that he spends a good amount of time calculating how much lumber he needs to buy for the walls.

Each corner of the house has a single 4x4 beam that walls can be nailed into and the trusses for the roof come pre-assembled. The only materials that Gerald needs to bring with him are the 2x4’s.

Gerald has decided to commission you to build him a simple application to calculate the number of 2x4’s he needs to buy so that he doesn’t have to make two trips to the store, but doesn’t buy too much. He’s given us the following information to help us calculate:
<br>
<br>

### Requirements
---
1. Each wall has 2x4's flat against the floor for the edge of a wall
2. Each wall has vertical 2x4’s spaced 16 inches apart (measured from outside edge of a board to the next outside edge; the board is included in the 16 inches)
3. Each wall has 2x4’s flat against the ceiling for the length of the edge of a wall.
4. Gerald buys 10% MORE than a perfect calculation to account for waste.
5. Gerald notes that you can’t purchase a partial piece of lumber, so round up a decimal in the final calculation
6. 2x4’s are actually 1.5" x 3.5”
7. 4x4’s are actually 3.5” x 3.5”
8. Gerald only buys 8’ 2x4’s
<br>
<br>

### Example using an 8' by 8' house
---

1. Each wall is the same size in this case
2. Each wall has two beams, totaling 7”, so the space in between is 7’ 5”.
3. Each wall required one 2x4 on the top, bottom, and sides
4. The remaining space across, broken into 16” sections, is 5.56, rounded up to 6
8. Total: 10 boards per wall, 40 boards for this house.
<br>
<br>
--- 
## Test Log
| House Measurement | Studs Required | Application Returns |  Last Test Run By|
|------------------ | -------------- |------------------|------------------- |
| 8 x 8             |      40        |        40       | Doug Waffle      |
| 18 x 8            |      66        |          84     |   Doug Waffle      |
--- 
<br>
<br>

~~Strikethrough Test~~

### Paramaters
---
* l: The length of the house, in feet.
* w:  The width of the house, in feet.