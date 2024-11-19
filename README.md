# balls

การเคลื่อนที่ จะมองเป็นรูปแบบเวกเตอร์

```
public class Vector{
    public double x,y;
    public Vector add(Vector v){
    Vector result = new Vector();
    result.x = this.x+ v.x;
    result.y = this.y+ v.y;
    return result;

// Also implements methods for vectors subtraction and multiplication
// public Vector sub(Vector v) 
// public Vector mul(Vector v)
}
```

กำหนดรูปร่างและพฤติกรรมของลูกบอล
Each Ball is made up of RGB values, size, initial position (x and y coordinates), and velocity (x and y coordinates).
```
public class Ball {
    public int R,G,B,size;
    public Vector position, velocity;

    public Ball(){
    	  R = (int) (Math.random() * 255);
    	  G = (int) (Math.random() * 255);
    	  B = (int) (Math.random() * 255);
    	  size = (int) (Math.random()*100);
    	  pos = new Vector();
    	  pos.x = (int) (Math.random() * 500);
    	  pos.y = (int) (Math.random() * 500);
    	  vel = new Vector();
    	  vel.x = (int) (Math.random()*10 -5);
    	  vel.y = (int) (Math.random()*10 -5);
    }

    public void draw (Graphics graphics){
    	  graphics.setColor(new Color(R,G,B));
    	  graphics.fillOval((int)position.x, (int)position.y, size, size);
    }
}
```
