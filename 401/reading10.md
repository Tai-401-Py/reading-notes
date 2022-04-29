
# Stacks and queues

---

### Stacks

A stack is a data structure of nodes, much like a single linked list, each node references the next node, but doesn't reference the previous. 

|Terminology|Definition|
:---:|:---|
|Push | Nodes or items that are put into the stack are pushed|
|Pop | Nodes or items that are removed from the stack are popped.| 
|Top | This is the top of the stack.|
|Peek | When you peek you will view the value of the top Node in the stack.|
|IsEmpty| Returns `True` when stack is empty otherwise returns `False`|
|FILO| First In Last Out|
|LIFO| Last In First Out|

Notes:

- You can't `pop` an empty stack, an exception will be raised.
- you can't `peek` an empty stack, an exception will be raised.

Pushing a Node onto the stack will always be O(1) since you are alwaysonly adding one item to teh stack, the same goes for popping, you will on ly ever be removing one at a time. 

When Pushing the reference to the next node will always be to the last item added to the stack. 

When Popping you will always start at the head/top of the stack. If you try and get rid of something i nthe middle of a stack, you need to either set references first to get the item and realign the references, or lose the whole stack.

When you peek you only look at the top of the stack, though always be sure to check `isEmpty` before peeking, you don't want to raise an exception. We don't assign next property when we peek, else we may lose reference to the node in the satck. 

### Queues

A queue is like a line that you stand in, the first person there will be the first to be serviced and leave. As you add things queues get longer, and they are typically added to the end (NO CUTTING IN LINE)

|Terminology|Definition|
:---:|:---|
|Enqueue| Nodes or items that are added to the queue.|
|Dequeue| Nodes or items that are removed from the queue.|
|Front|This is the front/first Node of the queue.
|Rear| This is the rear/last Node of the queue.
|Peek| When you peek you will view the value of the front Node.|
|IsEmpty| Returns `True` when queue is empty otherwise returns `False`.|
|FIFO| First In First Out|
|LILO| Last In First Out|

Note: 

Once again...

- Trying to peek an empty Queue will throw an exception.
- Trying to dequeue an empty Queue will raise an exception.

When queueing things are added to the back of the list, with the reference to the next one being set as the previous one added.