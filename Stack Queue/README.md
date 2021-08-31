### ? �����̶� ?
������ ���Լ���(LIFO) �ڷᱸ���� �����͸� �߰��� �� �� ���� �߰��ϰ� �����͸� ������ �� ���� �ִ�
 �����͸� ������ ����̴�. �� ���� �ֱٿ� �� �ڷᰡ ���� ���� �������� �����̴�.     
 
<br>

### ������ ����   
![stack](https://user-images.githubusercontent.com/64240637/107119454-fea76d80-68ca-11eb-9430-743b88841a13.PNG)    

__push__ : �����͸� �����ϴ� �����̴�    
__pop__ : ������ �� ���� �ִ� �����͸� �����ϸ鼭 ��ȯ�ϴ� �����̴�    

<br>

### ������ ����   
push(data) - data�� ������ �� ���� �߰��Ѵ�   
pop() - ���ÿ��� ���� ���� �ִ� ������ �����Ѵ�    
peek() - ������ front �����͸� ��ȯ�Ѵ� 
empty() - ������ ����ִ��� Ȯ���Ѵ�    

<br>

### ? ť�� ?
ť�� ���Լ���(FIFO)�ڷᱸ���� ���� ���� ���� �����Ͱ� ���� ���� ������ ���� �ʰ� ���� �����Ͱ�
���� �ʰ� ������ �����̴�.    
<br>

### ť�� ����
![ť](https://user-images.githubusercontent.com/64240637/107120988-55b14080-68d3-11eb-8aff-24ea4e8c6e4a.png)      
   

��ť(enqueuer) : �����͸� �����ϴ� ��   
��ť(dequeuer) : �����͸� ������ ��    
<br>

### ť�� ����
����ó�� ����Ʈ�� �̿��Ͽ� ť�� �����Ѵ�. ��ť�� append() �̿�, ��ť�� pop()�� �̿��Ͽ���   
```python
class Queue:
    def __init__(self):
        self.lists = []
        
    def enqueue(self,data):
        self.lists.append(data)
        print('push : ',data,end=' ')
        
        
    def dequeue(self):
        return self.lists.pop(0)
        
    def empty(self):
        if not self.lists:
            return True
        else:
            return False
    
    def peek(self):
        return self.lists[0]
    
q = Queue()
q.enqueue(1)
q.enqueue(2)
q.enqueue(3)
q.enqueue(4)
q.enqueue(5)
print('\n')

while not q.empty():
    print('pop :  ',q.dequeue(),end=' ')

"""
���
push :  1 push :  2 push :  3 push :  4 push :  5 

pop :   1 pop :   2 pop :   3 pop :   4 pop :   5 
"""
```
�����Ͱ� 1,2,3,4,5 ������ ��ť�������� ��ť�Ҷ��� ���� ���� 1���� ���ʴ�� pop�Ǵ� ���� �� �� �ִ�

<br>

### ���� ����Ʈ
��ũ�� �̿��ؼ� ���� ������ �ڷḦ �����ϴ� ����̴�. ���� ����Ʈ�� ��ũ�� ���� ���� ���� �˾Ƴ��� ������ �߰� ���� �����Ǵ� ��� ��ũ�� �ٲ��ָ� �Ǵ� ������ �ִ�. (���̽㿡�� �迭�� ���� ����Ʈ�� �����Ǿ� �ִ�)   

- �ܼ� ���� ����Ʈ (singly linked list)   
�ܼ� ���� ����Ʈ�� ��� ��尡 �����ϰ� ��� ���� ���� ��带 �׸��� ���� ���� �� ���� ��带 ����Ų��. �� �� �������� ����Ǿ� �ֱ� ������ �ܼ� ���� ����Ʈ��� �θ���   

- ���� ���� ����Ʈ
- ���� ���� ����Ʈ 