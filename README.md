<h1>Tetris Game</h1>

<h3> About </h3>
<p> Ini adalah Game Tetris untuk Final Project Pemograman Berorientasi Objek.</p>  

<h3>
• Nama : Muhammad Naufal Fawwaz Ramadhan<br>
• NRP : 5025211223<br>
</h3>
<br>
<p>  
Pada final project saya akan membuat game tetris. Tetris merupakan sebutan bagi permainan yang ada block puzzle runtuh dan pada game ini mempunyai beberapa bentuk yang berbeda, masing masing bentuk nanti akan berjatuhan pada papan game. Jadi kita mengatur agar mereka bisa masuk dengan pola yang benar, semakin besar score yang kita dapat makan semakin cepat block bergerak dan level yang semkain tinggi. Hasil permainan kita akan tersimpan di leaderboard saat gameover kita memasukan nama untuk ditampilkan di leaderboard.


Link Referensi : https://www.youtube.com/watch?v=dgVh6S8X25k<br>
Link Rekaman : https://youtu.be/b4sQ7hBiTTE<br>
  
<h3>Daftar implementasi OOP</h3>
</p>
✅ <b>Casting/Conversion</b><br>
    Line 267-277 <br>
    GameArea.java<br>
    
  ```
  public void moveBlockToBackground()
    {
        int[][] shape = block.getShape();
        double h = block.getHeight();
        double w = block.getWidth();
        
        int xPos = block.getX();
        int yPos = block.getY();
        
        Color color = block.getColor();
        
        for(int r = 0; r < (int)h; r++)
        {
            for(int c = 0; c < (int)w; c++)
            {
                if(shape[r][c] == 1)
                {
                    background[r + yPos][c + xPos] = color;
                }    
            }    
        }    
    }    
```

✅ <b>Constructor</b><br>
Line 119-124 <br> 
GameArea.java<br>

```
private boolean checkBottom()
    {
        if( block.getBottomEdge() == gridRows)
        {
            return false;
        }         
 ```
 
✅ <b>Overloading</b><br>
Line 6-21 <br>
TetrisBlock.java<br>

```
public class TetrisBlock 
{
  private int[][] shape;
  private Color color;
  private int x, y;
  private int[][][] shapes;
  private int currentRotation;
  
  private Color[] availableColors = {Color.green, Color.red, Color.blue};
  
  public TetrisBlock(int[][] shape)
  {
     this.shape = shape;
     
     initShapes();
  }  
```
  
✅ <b>Overriding</b><br>
Line 6-21<br> 
TetrisBlock.java<br>

```
public class TetrisBlock 
{
  private int[][] shape;
  private Color color;
  private int x, y;
  private int[][][] shapes;
  private int currentRotation;
  
  private Color[] availableColors = {Color.green, Color.red, Color.blue};
  
  public TetrisBlock(int[][] shape)
  {
     this.shape = shape;
     
     initShapes();
  }
```

✅ <b>Encapsulation</b><br>
Line 59, Line 61<br> 
TetrisBlock.java<br>

```
public int [][] getShape(){ return shape; }
```
```
public Color getColor(){ return color; }
```

✅ <b>Inheritance</b><br>
Line 6<br> 
GameThread.java<br>

```
public class GameThread extends Thread
```

✅<b>Polymorphism</b><br>
Line 6<br>
IShape.java<br>

```
public class IShape extends TetrisBlock
```

✅ <b>Exception Handling</b><br>
Line 35-40<br> 
GameThread.java<br>

```
{    
               try{
                  Thread.sleep(pause);
                }
                catch (InterruptedException ex) {
                    return;
                }
           }
```

✅ <b>GUI</b><br>
<br>
  
✅<b>Collection</b><br>
Line 9<br>
GameArea.java<br>

```
public class GameArea extends JPanel
{
    private int gridRows;
    private int gridColumns;
    private int gridCellSize;
    private Color[][] background;
    
    private TetrisBlock block;
    
    private TetrisBlock[] blocks;
```              

✅ <b>Input Output</b><br>
Line 37, Line 43<br>
GameForm.Form<br>

```
          @Override
            public void actionPerformed(ActionEvent e){
                ga.moveBlockRight();
            }         
```
```
 am.put("left", new AbstractAction(){
            @Override
            public void actionPerformed(ActionEvent e){
                ga.moveBlockLeft();
            }         
```

<p>
