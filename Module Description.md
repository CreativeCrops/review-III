# Module Description

* **Module 1**- Preprocessing 

* **Module 2**- Algorithm identification
	* Gradient descent
	* Newton's method
	* Conjugate gradient
	* Quasi-Newton method
	* Levenberg-Marquardt algorithm
	

* **Module 3**- Implementation of existing system
	* recommendation system graph based
```java
public class Tris_data {

    
    static Node head=null;
    public static void main(String[] args) throws FileNotFoundException, IOException {
        
        
        
        if(head==null){
            head=new Node();
        }
        
         String content = new String(Files.readAllBytes(Paths.get("D:\\data.txt")));
        //System.out.println(""+content);
        String[] data=content.split(" ");
        
        for (int i = 0; i < data.length; i++) {
            String string = data[i].trim();
            
            Node t=head;
            
            for (int j = 0; j < string.length(); j++) {
                String c = string.charAt(j)+"";
                if(!t.link.containsKey(c)){
                    Node tmp=new Node();
                    t.link.put(c, tmp);
                }
                t=t.link.get(c);
            }
        }
        
        Node t=head;
       
        display(t,"");
      
        System.out.println(""+worlds.size());
        
        
        try(PrintWriter out=new PrintWriter(new FileOutputStream("D:\\newdata.txt"))){
            
            for (int i = 0; i < worlds.size(); i++) {
                out.println(worlds.get(i));
                
            }
           // out.print(worlds.toString());
        }
        
        
    }
    
    
    static ArrayList<String> worlds=new ArrayList<>();
    
    
    
    static void display(Node t,String str){
        if(t.link.isEmpty()){
            worlds.add(str);
            System.out.println(str+"");
            return;
        }else{
             Set<String> keys=t.link.keySet();
            for (String d:keys) {
                display(t.link.get(d),str+d);
            }
        }
    }
    
    
    
    static class Node{
        int wig=0;
        Map<String, Node> link;
        Node(){
            link=new HashMap();
        }
    }
    
}
```

* **Module 4**- Implementation of proposed system
	* Artificial Intelligence And Machine Learning!
	* Artificial Neural Networks (ANNs)

* **Module 5**- Comparison between existing and proposed system
