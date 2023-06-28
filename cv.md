# Dmitry Samsonenko
![photo](./img/photo_cv.jpg)
## Contacts
- **Email**: samsondm97it@gmail.com
- **Discord**: friday5386
- **GitHub**: https://github.com/Friday-13

## About Me
Beginner Python developer. 
Looking for a job in the backend (Python, Django etc), but also try to master the basic frontend.
I like to master new IT things and techology. 
I used to work (and still work) as an embedded developer. 

...

## Skills
- Python3
    - Django
    - Numpy
    - Matplotlib
- SQL
- C
    - STM32-programming
- LaTeX

## Code Example
- [LeetCode: 21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
```python
class Solution:
    def mergeTwoLists(self, list1: Optional[ListNode], list2: Optional[ListNode]) -> Optional[ListNode]:
        
        if not list1:
            return list2
        
        if not list2:
            return list1
        
        head1 = list1
        head2 = list2
        new_head = ListNode()
        current_node = None
        if head1.val <= head2.val:
            new_head.val = head1.val
            head1 = head1.next
        else:
            new_head.val = head2.val
            head2 = head2.next
            
        current_node = new_head
        
        while head1 and head2:
            if head1.val <= head2.val:
                current_node.next = head1
                head1 = head1.next
            else:
                current_node.next = head2
                head2 = head2.next
            current_node = current_node.next
            
        if head1:
            current_node.next = head1
        if head2:
            current_node.next = head2
        
        return new_head
```
- Handler realisation for average filter with excluding extremums
```c
void ExclAverFilterHandler(ExclAverFilterStruct *Signal)
{
    Signal->SampleFreqCount++;
    if (Signal->SampleFreqCount >= Signal->SampleFreq)
    {
        Signal->SampleFreqCount = 0;
        Signal->SampleCount++;
        Signal->Sum += Signal->Value;
        /*Search extremums for exclude*/
        if (Signal->MaxValue < Signal->Value)
        {
            Signal->MaxValue = Signal->Value;
        }
        if (Signal->MinValue > Signal->Value)
        {
            Signal->MinValue = Signal->Value;
        }
        if (Signal->SampleCount >= Signal->SampleSize)
        {
            Signal->Out = (Signal->Sum - Signal->MaxValue - Signal->MinValue) / (Signal->SampleCount - 2);
            Signal->SampleCount = 0;
            Signal->Sum = 0;
            Signal->MinValue = UINT16_MAX;
            Signal->MaxValue = 0;
            Signal->Filtered = 1;
        }
    }
}
```

### Project Example
- [Project with base blog functionality based on Django](https://github.com/Friday-13/dartblog)
- [C-based filters lib](https://github.com/Friday-13/libfilters)

## Work History
- **Self-employed** \
    December 2020 - Present \
    pos. *Microcontroller software developer*
    
- **Research Institute of Automation of Production Processes** \
    August 2020 - December 2020 and July 2021 - December 2021 \
    pos. *Microcontroller software developer*

- **TB.Budget** \
    July 2014 - August 2014 \
    pos. *Technical writer*



## Education
- **Master's degree** (2019-2021):
    - Bauman Moscow State Technical Uiversity \
    dep. Robotics and сomplex automation \
    spec. Mechanical engineering
- **Bachelor's degree** (2015-2019):
    - Bauman Moscow State Technical Uiversity \
    dep. Radioelectronics and laser technologies \
    spec. Nanoengineering 


### Additional Education
- **English** \
    Yandex Practicum \
    November 2022 - Present
- [**Database design**](https://stepik.org/cert/1988834) \
    Stepik \
    March 2022 - July 2022
- [**Advanced SQL**](https://stepik.org/cert/1962732) \
    Stepik \
    March 2022 - July 2022
- [**Base SQL**](https://stepik.org/cert/1523830) \
    Stepik \
    March 2022 - July 2022

### Language
- **Russian** - native speaker
- **English** - B1
