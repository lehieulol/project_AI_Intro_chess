    /=====  |    |  |=====  /====\  /====\         A    =====
    |       |    |  |       |       |             / \     |
    |       |====|  |=====  \====\  \====\       /===\    |
    |       |    |  |            |       |      |     |   |
    \=====  |    |  |=====  \====/  \====/      |     | =====
    
by  Le Quang Hieu 20210335 (Lichtut)  
    Zuy  
    Quoc  
    Thanh  
    
    
    
What inside:  
   * Chess simulator (A):  
      * Display current state
      * Return value of current board (w-l; material)
      * Return value of the current board after a sequence of moves 
      * Return the terminal states (1) - white win, (-1) - black win, (0) - draw
      * Return next moves of opponent
   * Real-life tester (B):
      * Play in online chess platfrom (chess.com, lichess.com)
	  * Get the color you play in
	  * Get the move opponent move
	  * Move the piece with the input you got from (A)
   * Chess model (C):
      * Standard alpha-beta pruning model with 10-14 depths
	  * Monte - Carlo algorithm with 10-14 depths
	  * Monte - Carlo with triming to reach better depths
   * Connector (D):
      * Send move from (B), (C) to (A) (i.e from a1 to a7 as a1a7)
	  * Send simulating query from (C) to (A) (i.e a1a7 c1c3 a7g7) 
