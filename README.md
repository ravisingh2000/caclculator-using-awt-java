# caclculator-using-awt-java
//this is single digit calculator
//by using equal sign it give output:
import java.awt.*;
import java.awt.event.*;
class Notepad extends Frame implements ActionListener{
    TextField w;
    String a;
    Button u,u1,u2,u3,u4,u5,u6,u7,u8,u9,u10,u11,u12,u13,u14,u15;
    public void actionPerformed(ActionEvent ae){
          String i=ae.getActionCommand();
          if(i.equals("New")){
              w.setBackground(Color.pink);
              repaint();
          }
          else if(a==null || a.length()<3){
            // Notepad j=new Notepad();
                 if(a!=null)
                  a=a+i;
                 else {
                     a=i;
                 } 
                 System.out.println(a.length()+"a"+a);
                 //w.setBackground(Color.pink);
                 w.setText(a);

             }
          else if(a.length()==3){
            String [] ar=a.split("");
            if(ar[1].equals("+")){
                int d= Integer.parseInt(ar[0])+Integer.parseInt(ar[2]);
                
                w.setText(Integer.toString(d));
                a=Integer.toString(d);
          }
          else if (ar[1].equals("*")){
            int d= Integer.parseInt(ar[0])*Integer.parseInt(ar[2]);
            
            w.setText(Integer.toString(d));
            a=Integer.toString(d);
      }
      else if(ar[1].equals("-")){
        int d= Integer.parseInt(ar[0])-Integer.parseInt(ar[2]);
        
        w.setText(Integer.toString(d));
        a=Integer.toString(d);
  }

          
         
        }
          
    }
    public void paint(Graphics g){
          Font f=new Font ("arial",Font.BOLD,40);
          
         // w.setBackground(c);
    }
    

    Notepad(){
        Label r=new Label("Powered BY  Ravi Singh");
        this.setVisible(true);
        this.setSize(230,465);
        this.setTitle("Calculator");
        this.setLayout(null);
        r.setBounds(35,404,150,40);
        this.add(r);
        u=new Button("7");
        u1=new Button("8");
        u2=new Button("9");
        u3=new Button("4");u4=new Button("5");u5=new Button("6");u6=new Button("1");u7=new Button("2");u8=new Button("3"); u9=new Button(".");
        u10=new Button("0");
        u11=new Button("=");
        u12=new Button("+");
        u13=new Button("-");
        u14=new Button("*");
        u15=new Button("/");
         w=new TextField();
         this.add(w);
         this.add(u);
         this.add(u1);
         this.add(u2);
         this.add(u3);
         this.add(u4);
         this.add(u5);
         this.add(u6);
         this.add(u7);
         this.add(u8);
         this.add(u9);
         this.add(u10);
         this.add(u11);
         this.add(u12);
         this.add(u13);
         this.add(u14);
         this.add(u15);
         u.setBounds(8,117,55,70);
         u1.setBounds(60,117,55,70);
         u2.setBounds(110,117,55,70);
         u12.setBounds(165,117,55,70);
         u3.setBounds(8,190,55,70);
         u4.setBounds(60,190,55,70);
         u5.setBounds(110,190,55,70);
         u13.setBounds(165,190,55,70);
         u6.setBounds(8,263,55,70);
         u7.setBounds(60,263,55,70);
         u8.setBounds(110,263,55,70);
         u14.setBounds(165,263,55,70);

         
         u9.setBounds(8,333,55,70);
         u10.setBounds(60,333,55,70);
         u11.setBounds(110,333,55,70);
         u15.setBounds(165,333,55,70);
         u.addActionListener(this);
        u1 .addActionListener(this);
        u2.addActionListener(this);
        u3.addActionListener(this);
        u4.addActionListener(this);
        u5.addActionListener(this);
        u6.addActionListener(this);
        u7.addActionListener(this);
        u9.addActionListener(this);
        u10.addActionListener(this);
        u11.addActionListener(this);
        u12.addActionListener(this);
        u13.addActionListener(this);
        u14.addActionListener(this);
        u15.addActionListener(this);
        u8.addActionListener(this);
        MenuBar i=new MenuBar();
        Font f=new Font ("arial",Font.BOLD,40);
        w.setFont(f);

        this.addWindowListener(new WindowAdapter(){
             public void windowClosing(WindowEvent ae){
                 System.exit(0);
             }
        });
        this.setMenuBar(i);
      
        
        Menu j=new Menu("File");
        i.add(j);
        w.setBounds(7,47,350,65);
      //this.add(u);
     
        MenuItem j1=new MenuItem("New");
        MenuItem j2=new MenuItem("New Window");
        MenuItem j3=new MenuItem("Save");
        MenuItem j4=new MenuItem("Save As");   
        j1.addActionListener(this);
        j2.addActionListener(this);
        j3.addActionListener(this);
        j4.addActionListener(this);
        j.add(j1);
        j.add(j2);
        j.add(j3);
        j.add(j4);
        Menu k=new Menu("Edit");
        i.add(k);
        MenuItem k1=new MenuItem("New");
        MenuItem k2=new MenuItem("New Window");
        MenuItem k3=new MenuItem("Save");
        MenuItem k4=new MenuItem("Save As");   
        k1.addActionListener(this);
        k2.addActionListener(this);
        k3.addActionListener(this);
        k4.addActionListener(this);
        k.add(k1);
        k.add(k2);
        k.add(k3);
        k.add(k4);
        Menu m=new Menu("Format");
        i.add(m);
        MenuItem m1=new MenuItem("New");
        MenuItem m2=new MenuItem("New Window");
        MenuItem m3=new MenuItem("Save");
        MenuItem m4=new MenuItem("Save As");   
        m1.addActionListener(this);
        m2.addActionListener(this);
        m3.addActionListener(this);
        m4.addActionListener(this);
        m.add(m1);
        m.add(m2);
        m.add(m3);
        m.add(m4);
        Menu n=new Menu("View");
        i.add(n);
        MenuItem n1=new MenuItem("New");
        MenuItem n2=new MenuItem("New Window");
        MenuItem n3=new MenuItem("Save");
        MenuItem n4=new MenuItem("Save As");   
        n1.addActionListener(this);
        n2.addActionListener(this);
        m3.addActionListener(this);
        n4.addActionListener(this);
        n.add(n1);
        n.add(n2);
        n.add(n3);
        n.add(n4);

    }
}
class No{
    public static void main(String [] args){
        Notepad i=new Notepad();
    }
}
