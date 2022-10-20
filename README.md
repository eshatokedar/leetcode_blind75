# leetcode_blind75

/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *    
  */
  class Solution {
    public static ListNode reverseList(ListNode head) {
       if(head == null || head.next == null) {
       return head;
    }
   
     ListNode prevNode = head;
    ListNode currNode = head.next;
    while(currNode != null) {
       ListNode nextNode = currNode.next;
       currNode.next = prevNode;
       prevNode = currNode;
       currNode = nextNode;
    }
    head.next = null;
    head = prevNode;
       return head;
    }
 }
 
