    /=====  |    |  |=====  /====\  /====\         A    =====
    |       |    |  |       |       |             / \     |
    |       |====|  |=====  \====\  \====\       /===\    |
    |       |    |  |            |       |      |     |   |
    \=====  |    |  |=====  \====/  \====/      |     | =====
    
by  Le Quang Hieu 20210335 (Lichtut)  
    Zuy  
    Quoc  
    Thanh  
    
Using 'chess' package    

What inside:  
   * Chess UI + Grader (UI):  
      * Display current state
      * Return value of current board (w-l; material)
      * Return the terminal states (1) - white win, (-1) - black win, (0) - draw
      * Return next moves of opponent
      * Grader that play in online chess platfrom (chess.com, lichess.com)
	  * Get the color you play in
	  * Get the move opponent move
	  * Move the piece with the input you got from (A)
   * Chess model (Models):
      * Standard alpha-beta pruning model with 10-14 depths
      * Value Function:
          * Material difference.
	  * Deep learning (later)
   * Comunication (comunicate_file):
      * in-files standard:
          * first time '0 w' or '0 b' for color the model play with
	  * next time '(0/1)'+'(terminate?)'+if termanate: '(-1/0/1)' else '(start point) (end point)'
	    * (0/1) alternate to show the in-file is updated or not
	    * (terminate?) 0 for false, 1 for true
	    * (-1/0/1) black win/draw/white win
	    * (start point) (end point) opponent's move
      * out-files standard:
          * '(0/1)'+'(start point) (end point)'
	    * (0/1) alternate, start with 0
	    * (start point) (end point) your move
  
