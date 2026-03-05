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
**Commit(s):** I wrote the Core D, printFromPlayer method and the optional helper printBoardOnce method.
---
### Entry 2
**Date:** 2026-03-04
**Entry Type:** Bug Fix
**Task worked on:** mirrorBoard()
**Issue or decision:** Everytime I run mirrorBoard(), it gives me the wrong reversed board.
**Error message / symptom (if applicable):** Let's say we have a list 1->2->3->..., the method should change it to 3->2->1->.... Instead, it turns it into 3->1->3->....
**What I tried:** I tried writing while(curr != nullptr), but that would be an infinite loop.  I also tried while(curr != headNode), but that wouldn't even change the list at all.
**Fix / resolution (or final decision):** After some time, I realized it doesn't have to be like the slides from canvas and I can use a for loop. I used a for loop with nodeCount in order to know how many times I should change the pointers.
**Commit(s):** I chose the Advanced Option B: Mirror the Board, so I wrote the method mirrorBoard().
---
### Entry 3
**Date:** YYYY-MM-DD
**Entry Type:** Bug Fix / Edge Case / Engineering Decision
**Task worked on:**
**Issue or decision:**
**Error message / symptom (if applicable):**
**What I tried:**
**Fix / resolution (or final decision):**
**Commit(s):**
---
### Entry 4
**Date:** YYYY-MM-DD
**Entry Type:** Bug Fix / Edge Case / Engineering Decision
**Task worked on:**
**Issue or decision:**
**Error message / symptom (if applicable):**
**What I tried:**
**Fix / resolution (or final decision):**
**Commit(s):**
---
### Entry 5
**Date:** YYYY-MM-DD
**Entry Type:** Bug Fix / Edge Case / Engineering Decision
**Task worked on:**
**Issue or decision:**
**Error message / symptom (if applicable):**
**What I tried:**
**Fix / resolution (or final decision):**
**Commit(s):**
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
