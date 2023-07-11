import java.util.*;
//step-1 add at last index
//step-2 fix heap
//if parent idx is i then lc is 2i+1 and rc is 2i+2
//if value of child is less than parent so we have to swap the values
public class Main{
  static class Heap{
    ArrayList<Integer> arr = new ArrayList<>();
    public void add(int data){
      //add at last index
      arr.add(data);
      int child = arr.size()-1;
      int par = (child-1)/2;

      while(arr.get(child) > 0 && arr.get(child)<arr.get(par)){   //to get value of an object we use get() function
        //swap
        int temp = arr.get(child);
        arr.set(child,arr.get(par));
        arr.set(par,temp);

        child = par;
        par = (child-1)/2;
      }
    }
    public int peek(){
      return arr.get(0);
    }
    private void heapify(int idx){
      int left = 2*idx + 1;
      int right = 2*idx + 2;
      int minIdx = idx;

      if(left<arr.size() && arr.get(minIdx) > arr.get(left)){
        minIdx = left;
      }
      if(right<arr.size() && arr.get(minIdx) > arr.get(right)){
        minIdx = right;
      }
      if(minIdx != idx){
        //swap
        int temp = arr.get(idx);
        arr.set(idx,arr.get(minIdx));
        arr.set(minIdx,temp);
        heapify(minIdx);
      }
    }
    public int remove(){
      int data = arr.get(0);
      int temp = arr.get(0);
      arr.set(0,arr.get(arr.size()-1));  //set function needs an idx and element as it's input
      arr.set(arr.size()-1,temp);
      arr.remove(arr.size()-1);
      heapify(0);
      return data;
    }
    public boolean isEmpty(){
      return arr.size()==0;
    }
  }
  public static void main(String args[]){
    Heap h = new Heap();
    h.add(3);
    h.add(4);
    h.add(1);
    h.add(5);
    while(!h.isEmpty()){
      System.out.println(h.peek());
      h.remove();
    }
  }
}
