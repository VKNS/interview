//// Binary search function using JavaScript

/// Defining function
function binSearch(arr, toFind)
{
    /// Checking our array for emptiness.
    if (!arr) return null;
    var first = 0;
    var last = arr.length - 1;
    /// Running binary search
    while (first < last)
    {
        var mid = first + Math.floor((last - first) / 2);
        if (arr[mid] >= toFind) last = mid;
        else first = mid + 1;
    }
    /// After the end of the loop, lastIndex can point to the search item. 
    /// Otherwise the element is missing in the array.
    if (arr[last] == toFind)
        return last;
    else return null;
}

/// Let's try out our function:
console.log(binSearch([1, 2, 4],  4 )); // Output is: 2
console.log(binSearch([1, 2, 4],  3 )); // Output is: null
console.log(binSearch([1, 2, 4],  2 )); // Output is: 1
console.log(binSearch([           ],  1 )); // Output is: null
console.log(binSearch("abcdef",'c')); // Output is: 2