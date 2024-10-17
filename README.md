# links
Active Practice URLS : 
Basics : https://www.hackerrank.com/cmrit26-1-basics

Loops : https://www.hackerrank.com/cmrit26-2-lpb

MONTHLY GOAL : MAY
https://www.hackerrank.com/cmrit-may-2024
MONTLY GOAL : JUNE
https://www.hackerrank.com/cmrit-june-2024
MONTHLY GOAL : AUGUST
https://www.hackerrank.com/cmrit-august-2024
MONTHLY GOAL : SEPTEMBER
https://www.hackerrank.com/cmrit-september-2024

ALL TOPIC PRACTICE : 
https://www.hackerrank.com/cmrit-2y-2026

//////////////////////Dll///////////////////
import java.util.*;  

class DLL{ // Doubly Linked List in Java
    Node head, tail;
    class Node{ 
        int data; 
        Node next, prev; 
        Node(int v){ this.data = v; } // constructor
    } 
    void push(int v){
        // 1. create the node, insert value
        Node n = new Node(v);
        // 2. n next is head
        n.next = head;
        // 3. if linkedlist is empty, n is also tail
        if(head == null) tail = n;
        // 4. if linkedlist is not empty, head prev is n
        if(head != null) head.prev = n;
        // 3. n becomes the new head
        head = n;
    }
    void printDLL(){
        System.out.println("Forwards : ");
        for(Node tmp=head; tmp != null; tmp = tmp.next) 
            System.out.print(tmp.data + " ");
        System.out.println("\nBackwards : ");
        for(Node tmp=tail; tmp != null; tmp = tmp.prev) 
            System.out.print(tmp.data + " ");
        System.out.println();
    }
} 
public class Main  { 
    public static void main(String args[] ){ 
        DLL o = new DLL();
        o.push(45); o.push(89); o.push(99);
        o.printDLL(); 
        // forwards : 99(h) -> 89 -> 45 -> null
        // backwards : 45-> 89 -> 99 -> null
    }  
}  


//////////////////////////////////////////////////////////////

import java.io.*; // SINGLY LINKED LIST CREATE AND PUSH IN JAVA
import java.util.*; 
class SLL{
    Node head;
    class Node{
        int data; Node next; Node(int v) { this.data = v; }
    }
    void push(int v){
        Node n = new Node(v); n.next = head; head = n;
    }
    void printSLL() { 
        for(Node tmp=head;tmp!=null; tmp=tmp.next)
            System.out.print(tmp.data + " "); 
    }
}

public class Solution {
    public static void main(String args[] )  {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        SLL o = new SLL();
        while(n-- > 0){
            o.push(sc.nextInt());
        }
        o.printSLL();
    }
}

///////////////////////////////////////////////////////////////////
import java.util.*;  
class DLL{ // Doubly Linked List in Java
    Node head, tail;
    class Node{ 
        int data;
        Node next, prev;
        Node (int v) { this.data = v; }
    } 
    void push(int v){ 
        Node n = new Node(v); 
        n.next = head;
        if(head == null) tail = n;
        if(head != null) head.prev = n;
        head = n;
    }
    void append(int v){
        // 1. if list is empty, push
        if(head == null) { push(v); return; }
        // 2. create Node, insert value
        Node n = new Node(v);
        // 3. tail next is n, n prev is tail
        tail.next = n; n.prev = tail;
        // 4. n is new tail
        tail = n;
    }
    void printDLL(){
        System.out.print("Forwards: ");
        for(Node tmp=head; tmp != null; tmp = tmp.next) 
            System.out.print(tmp.data + " ");
        System.out.print("\nBackwards: ");
        for(Node tmp=tail; tmp != null; tmp = tmp.prev) 
            System.out.print(tmp.data + " ");
        System.out.println();
    }
} 
public class Solution  { 
    public static void main(String args[] ){ 
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        DLL o = new DLL();
        for(int i=0;i<n;i++) {
            if(i < 3) o.append(sc.nextInt());
            else o.push(sc.nextInt());
        }
        o.printDLL();
    }  
}  
Sensei — 10/15/2024 11:28 AM
Doubly LinkedList Push Operation: 
1. List is empty
NULL(head,tail)
2. Push(89)
null<-89(head,tail)->NULL
3. push(88)
null<-88(head)<->89(tail)->null
4. push(77)
null<-77(head)<->88<->89(tail)->null

Append operation with DLL:
1. append(20) : if LL is empty, push
null<-20(head,tail)->null
2. append(23) 
null<-20(head)<->23(tail)->null
3. append(66)
null<-20(head)<->23<->66(tail) ->null
4. append(77)
null<-20(head)<->23<->66<->77(tail) ->null

Algorithm : 
if list is empty: push
1. create Node(n) and insert value
2. tail next is n. n prev is tail. n is tail.
3.
4.
5. . https://www.hackerrank.com/cmrit-october-2024
