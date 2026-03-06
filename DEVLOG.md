# Developer Log (DEVLOG.md)
## Monopoly Board Simulator (Spring 2026)
Minimum **6 entries** required.
Each entry must document learning and reasoning. Fabricated bugs are not expected.
---
## Allowed Entry Types
Each entry may be one of the following:
1) **Bug Fix Entry**
- The issue encountered.
- Error messages or symptoms.
- Attempts made.
- Final resolution.
2) **Edge Case / Testing Entry**
- A failure discovered through testing.
- The specific input/state that caused it.
- The change you made to handle it correctly.
3) **Engineering Decision Entry (up to 2 allowed)**
- A design decision you made.
- An alternative approach you considered.
- Why you chose one approach over another (tradeoffs).
---
### Entry 1
**Date:** 2026-03-01
**Entry Type:** Edge Case
**Task worked on:** printBoardOnce()
**Issue or decision:** When wanting to print the board, it never prints that last node.
**Error message / symptom (if applicable):** board.printBoardOnce() would print the whole board but the last node.
**What I tried:** I wrote a while loop, where while(current != tailNode) it would keep printing the next node. But this way it would stop printing once current is equal to the tailNode. I also tried while(current != headNode) but then nothing gets printed out.
**Fix / resolution (or final decision):** I decided to use a for loop since I realized there is also a variable nodeCount to keep count of the number of nodes, so I can print them out. Resulting in for(i = 0; i < nodeCount; i++), printing every single node in the board.
**Commit(s):** I wrote core d printFromPlayer method and at first it took a while for me to figure out how I can print and keep track of each node being printed while also moving forward to print the others, since I wanna keep playerNode the same, and cannot move forward since we just wanna print the next nodes from player. Then I remembered I could make a new temporary node called player which is a pointer to playerNode and does not change it either, allowing us to start and move from the playerNode. I also added the printBoardOnce method and had the same problem with this one except the temp node is called current, and instead of using MAX_SPACES or counting the nodes in the list, I just remembered to use an already existing variable called nodeCount which is the number of nodes in the list.
---
### Entry 2
**Date:** 2026-03-04
**Entry Type:** Bug Fix
**Task worked on:** mirrorBoard()
**Issue or decision:** Everytime I run mirrorBoard(), it gives me the wrong reversed board.
**Error message / symptom (if applicable):** Let's say we have a list 1->2->3->..., the method should change it to 3->2->1->.... Instead, it turns it into 3->1->3->....
**What I tried:** I tried writing while(curr != nullptr), but that would be an infinite loop.  I also tried while(curr != headNode), but that wouldn't even change the list at all.
**Fix / resolution (or final decision):** After some time, I realized it doesn't have to be like the slides from canvas and I can use a for loop. I used a for loop with nodeCount in order to know how many times I should change the pointers.
**Commit(s):** I chose the Advanced Option B: Mirror the Board and wrote the mirrorBoard() method. I also ran into an error/bug and fixed that. I mentioned it in my DEVLOG. Added a few more board spaces for testing purposes.
---
### Entry 3
**Date:** 2026-03-05
**Entry Type:** Edge Case
**Task worked on:** countSpaces()
**Issue or decision:** When testing the method in main, the program ran an error. 
**Error message / symptom (if applicable):** "error: expected ';' at end of declaration" 
**What I tried:** I found the line and realized I had just forgotten a ; 
**Fix / resolution (or final decision):** Wow, such a stupid mistake. I just went in and added a ; 
**Commit(s):** I wrote and completed the countSpaces() method, but along the way I ran into a small error and struggle with decision-making. I wrote both the edge case and the engineering decision in my DEVLOG. 
---
### Entry 4
**Date:** 2026-03-05
**Entry Type:** Engineering Decision
**Task worked on:** countSpaces() 
**Issue or decision:** Since I cannot rely on nodeCount, so no for loop, I wanted to see if i can use a while loop. 
**Error message / symptom (if applicable):** N/A
**What I tried:** I tried using a while loop while(curr != tailNode) but it leaves out the last node, and if I try while(curr != headNode) it just never starts counting. 
**Fix / resolution (or final decision):** I found a loop hole though, I can have while(true) and in the for loop I can count and everything, then check if the curr == headNode, since we have already counted and moved on from the headNode. 
**Commit(s):** I wrote and completed the countSpaces() method, but along the way I ran into a small error and struggle with decision-making. I wrote both the edge case and the engineering decision in my DEVLOG.
---
### Entry 5
**Date:** 2026-03-06
**Entry Type:** Edge Case
**Task worked on:** clear() method
**Issue or decision:** When printing the board after clear(), since it's empty it should print "Board is empty", but it didn't.
**Error message / symptom (if applicable):** board.printBoardOnce() wouldn't print anything at all. 
**What I tried:** I saw the condition for printing "Board is empty" so I tried to set headNode, tailNode, and playerNode all to null.
**Fix / resolution (or final decision):** By setting headNode, tailNode, and playerNode to null, the printBoardOnce() method runs the if statement and prints "Board is empty". I also realized I should probably set the nodeCount and passGoCount back to 0, since the board is now empty.
**Commit(s):** I wrote and completed the clear() method. Using the hint made the code structure a lot easier, since we can set tailNode to point to null, making it a singly linked list instead of circular. Which makes the whole tracking and deletion process easier and takes less lines of code.
---
### Entry 6
**Date:** YYYY-MM-DD
**Entry Type:** Bug Fix / Edge Case / Engineering Decision
**Task worked on:**
**Issue or decision:**
**Error message / symptom (if applicable):**
**What I tried:**
**Fix / resolution (or final decision):**
**Commit(s):**
