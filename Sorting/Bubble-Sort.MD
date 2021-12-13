# Bubble Sort Algorithm

Video example https://www.bbc.co.uk/bitesize/guides/z22wwmn/revision/3

Explanation https://www.studytonight.com/data-structures/bubble-sort

### Implementing Bubble Sort Algorithm

#### Operating principle:
- If the given array has to be sorted in ascending order, then bubble sort will start by comparing the first element of the array with the second element, if the first element is greater than the second element, it will swap both the elements, and then move on to compare the second and the third element, and so on.
- If we have total `n` elements, then we need to repeat this process for `n-1` times.




If we have total n elements, then we need to repeat this process for n-1 times.
 ```js
const bubbleSort = (list) => {
    for (let i = 0; i < list.length; i++) {
        for (let j = 0; j < list.length; j++) {
            if (list[j] > list[j + 1]) {
                // destructuring assignment
                [list[j], list[j + 1]] = [list[j + 1], list[j]];
            }
        }
    }
    return list
};

console.log(bubbleSort([5, 1, 6, 2, 4, 3]))
```
#### Limitations of this approach:

- the `outer for loop` will keep on executing for 6 iterations even if the array gets sorted after the second iteration.

