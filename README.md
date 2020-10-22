# MyList
Class MyList

package mylist;  
public class MyList {
    class Node{
        private int value;
        private Node next; //ссылка на следующий элемент списка
        
        public Node(int value) {
            this.value = value;
            this.next = null;
        }
        
        public boolean hasNext(){ //выполняется проверка наличия следующего элемента
            if (this.next == null) {
                return true;
            }
            else {
                return false;
            }
        }
        
        public String toString(){
            return Long.toString(this.value);
        }
        
         public int getValue(){
            return value;
        }
         
         public void setValue(int value) {
             this.value = value;
         }
        
        public Node getNext() {
            return next;
        }
        
        public void setNext(Node next){
            this.next = next;
        }
        
    }
    
     private Node begin;
    private long counter;
    
    public MyList(){
        this.begin = null;
        this.counter = 0;
        }
        
    public Node end() {
        if (this.begin == null)
            return null;
        
    Node iter = this.begin;
        while (iter.hasNext()){
            iter = iter.getNext(); //возвращается ссылка
        }
        return iter;
     }

