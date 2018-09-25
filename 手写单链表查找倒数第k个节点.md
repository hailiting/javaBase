class Node{
    Node next = null;
    int data;
    public Node(int data){
      this.data = data;
    }
}
public class MyLinkedList{
  Node head=null;
  public Node findElem(Node head,int k){
    if(k<1||k>this.length()){
      return null;
    }
    Node p1=head;
    Node p2=head;
    for(int i=0;i<k;i++)
      p1=p1.next;
    while(p1!=null){
        p1=p1.next;
        p2=p2.next;
    }
    return p2;
}
public static void main(String[] args) {

    MyLinkedList list=new MyLinkedList();
    list.addNode(1);
    list.addNode(2);
    list.addNode(3);
    list.addNode(4);
    list.addNode(5);
    MyLinkedList p=new MyLinkedList();
    p.head=list.findElem(list.head, 3);
    p.printList();

}
}

