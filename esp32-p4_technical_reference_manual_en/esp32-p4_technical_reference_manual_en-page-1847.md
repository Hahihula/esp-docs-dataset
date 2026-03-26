

```markdown
- mode: 2D, mode1.
- length/size: HA is the number of horizontal pixels of the picture. VA is the number of vertical pixels of the picture, HB is 16 x 4, and VB is 16.

2. Configure the channel of reading reference picture (TX channel 1):
    - mode: 2D, mode1.
    - length/size: HA is NUM_H_MB x 16 x 16, VA is 3, HB is 16 x 16, and VB is 3.

3. Configure the channel of reading DB intermediate data (TX channel 2):
    - mode: 1D.
    - length/size: The read space size is NUM_H_MB x (16 x 4 + 8 x 4 x 2).

4. Configure the channel of reading first 12 lines of DB data (TX channel 3):
    - mode: 1D.
    - length/size: The read space size is (NUM_H_MB x (number of vertical macro block lines in the picture - 1) x (16 x 12 + 8 x 4 x 2)) + (NUM_H_MB x 16 x 16 x 1.5).

5. Configure the channel of reading last 4 lines DB data (TX channel 4):
    - mode: 1D.
    - length/size: The read space size is (NUM_H_MB x (number of vertical MB lines in the picture - 1) x (16 x 4 + 8 x 4 x 2)).

6. Configure the channel of writing first 12 lines of DB data (RX channel 0):
    - mode: 1D.
    - length/size: The size of the writing space is the same as the size of TX channel 3.

7. Configure the channel of writing last 4 lines of DB data (RX channel 1):
    - mode: 1D.
    - length/size: The size of the writing space is the same as the size of TX channel 4.

8. Configure the channel of writing DB intermediate data (RX channel 2):
    - mode: 1D.
    - length/size: The size of the writing space is the same as the size of TX channel 2.

9. Configure the channel of writing MV merge data (RX channel 3):
    - mode: 1D.
    - length/size: The writing space size is NUM_H_MB x the number of vertical MB lines x 4.

10. Configure the channel of writing bit stream data (RX channel 4):
    - mode: 1D.
    - length/size: The size of the writing space is the number of horizontal pixels of the picture x the number of vertical pixel lines x 1.5.

Register configuration:
```